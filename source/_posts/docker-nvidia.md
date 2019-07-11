---
title: "Nvidia GPU in Docker"
date: 2017-11-03 16:49:32
categories:
  - container
tags:
  - docker
  - nvidia
  - web-deploy
---

[NVIDIA Container Runtime | NVIDIA Developer](https://developer.nvidia.com/nvidia-container-runtime)
[Enabling GPUs in the Container Runtime Ecosystem | NVIDIA Developer Blog](https://devblogs.nvidia.com/gpu-containers-runtime/)

[NVIDIA/nvidia-docker: Build and run Docker containers leveraging NVIDIA GPUs](https://github.com/NVIDIA/nvidia-docker)  
[Releases · NVIDIA/nvidia-docker](https://github.com/NVIDIA/nvidia-docker/releases) [Motivation · NVIDIA/nvidia-docker Wiki](https://github.com/NVIDIA/nvidia-docker/wiki/Motivation)  
2.0 uses `nvidia-container-runtime` instead of `runC`.

[Repository configuration | libnvidia-container](https://nvidia.github.io/libnvidia-container/)
[NVIDIA/nvidia-container-runtime: NVIDIA container runtime](https://github.com/nvidia/nvidia-container-runtime#installation) a modified runC that will invoke `nvidia-container-cli` from project `libnvidia-container` when container starts.  
[NVIDIA/libnvidia-container: NVIDIA container runtime library](https://github.com/NVIDIA/libnvidia-container)

# Installation

[Installation (version 2.0) · NVIDIA/nvidia-docker Wiki](https://github.com/NVIDIA/nvidia-docker/wiki/Installation-%28version-2.0%29)

## Docker

- Installation Ubuntu 16.04 Server (16.04 with upgrade)
- Install Docker CE (17.06+) with.deb  
  https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/#install-from-a-package

```sh
sudo apt install libltdl7
sudo dpkg -i docker-ce_17.06.2-ce-0-ubuntu_amd64.deb
sudo systemctl enable docker && sudo systemctl start docker
sudo usermod -a -G docker ${USER}
```

## NVIDIA driver

[How do I install the NVIDIA driver? · NVIDIA/nvidia-docker Wiki](https://github.com/NVIDIA/nvidia-docker/wiki/Frequently-Asked-Questions#how-do-i-install-the-nvidia-driver)
[Installation Guide Linux :: CUDA Toolkit Documentation](http://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#ubuntu-installation)
[Installing Nvidia CUDA 8.0 on Ubuntu 16.04 for Linux GPU Computing (New Troubleshooting Guide)](https://www.linkedin.com/pulse/installing-nvidia-cuda-80-ubuntu-1604-linux-gpu-new-victor)

install NVIDIA driver (384.90+) and CUDA

```sh
sudo apt-get install nvidia-384 nvidia-cuda-toolkit

# verify installation
lsmod | grep nvidia
ldconfig -p | grep -E 'nvidia|cuda'

nvidia-smi
nvidia-modprobe
nvcc --version
```

[解决 Driver/library version mismatch | Comzyh 的博客](https://comzyh.com/blog/archives/967/)  
Also fixed by a reboot
[Proprietary GPU Drivers : “Graphics Drivers” team](https://launchpad.net/~graphics-drivers/+archive/ubuntu/ppa)
https://blog.csdn.net/xianglao1935/article/details/80512345

## `nvidia-docker2`

> Note: installing this overwrites `/etc/docker/daemon.json`

Set default runtime of docker daemon with `--default-runtime=nvidia`.  
[Environment variables (OCI spec)](https://github.com/nvidia/nvidia-container-runtime#environment-variables-oci-spec)

> Use `nvidia-docker2` matching the Docker version installed

```sh
curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | \
  sudo apt-key add -
curl -s -L https://nvidia.github.io/nvidia-docker/ubuntu16.04/amd64/nvidia-docker.list | \
  sudo tee /etc/apt/sources.list.d/nvidia-docker.list
sudo apt-get update
sudo apt-get install nvidia-docker2  # latest

# MUST match the Docker version installed
apt show nvidia-docker2 -a | grep Version
apt show nvidia-container-runtime -a | grep Version
# for Docker 17.06.2
sudo apt-get install \
  nvidia-docker2=2.0.3+docker17.06.2-1 \
  nvidia-container-runtime=2.0.0+docker17.06.2-1
# for Docker 17.09
sudo apt-get install \
  nvidia-docker2=2.0.3+docker17.09.0-1 \
  nvidia-container-runtime=2.0.0+docker17.09.0-1
sudo pkill -SIGHUP dockerd
```

## Changing default runtime

Use `/usr/bin/nvidia-container-runtime` in `/etc/docker/daemon.json`:

```json
{
  "default-runtime": "nvidia",
  "runtimes": {
    "nvidia": {
      "path": "/usr/bin/nvidia-container-runtime",
      "runtimeArgs": []
    }
  }
}
```

```sh
# now use
docker run --rm nvidia/cuda:8.0-runtime-ubuntu16.04 nvidia-smi
# instead of
docker run --runtime=nvidia --rm nvidia/cuda:8.0-runtime-ubuntu16.04 nvidia-smi

# swarm service also work
docker swarm init
docker service create --name cuda-service --constraint node.labels.gpu==true nvidia/cuda:test-service
```

## cuda Base Image

[nvidia/cuda - Docker Hub](https://hub.docker.com/r/nvidia/cuda/)  
[8.0/runtime/Dockerfile · ubuntu16.04 · nvidia / cuda · GitLab](https://gitlab.com/nvidia/cuda/blob/ubuntu16.04/8.0/runtime/Dockerfile)  
[8.0/devel/Dockerfile · ubuntu16.04 · nvidia / cuda · GitLab](https://gitlab.com/nvidia/cuda/blob/ubuntu16.04/8.0/devel/Dockerfile)  
[8.0/runtime/cudnn8/Dockerfile · ubuntu16.04 · nvidia / cuda · GitLab](https://gitlab.com/nvidia/cuda/blob/ubuntu16.04/8.0/runtime/cudnn8/Dockerfile)

## Kubernetes

[NVIDIA Container Runtime and Orchestrators | NVIDIA Developer](https://developer.nvidia.com/kubernetes-gpu)
[Kubernetes on NVIDIA GPUs Installation Guide :: Data Center Documentation](https://docs.nvidia.com/datacenter/kubernetes/kubernetes-install-guide/index.html)

[Schedule GPUs - Kubernetes](https://kubernetes.io/docs/tasks/manage-gpus/scheduling-gpus/)
[Using GPGPUs with Kubernetes | Ubuntu](https://ubuntu.com/blog/using-gpgpus-with-kubernetes)
[基于 Kubernetes 的 GPU 类型调度实现](https://www.infoq.cn/article/ypP*1sbAuBAD1KL1qB4K)
