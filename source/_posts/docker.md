title: "Docker"
date: 2014-12-11 17:37:50
categories:
- linux
tags:
- shell-tool
- docker
- devops
---

[Docker - Build, Ship, and Run Any App, Anywhere](https://www.docker.com/)
[Supported installation](https://docs.docker.com/installation/)
[Using the command line](https://docs.docker.com/reference/commandline/cli/)
[Understand the architecture](http://docs.docker.com/introduction/understanding-docker/)
[Get started with images](https://docs.docker.com/userguide/dockerimages/)
[Dockerfile reference](http://docs.docker.com/reference/builder/)
[Best practices for writing Dockerfiles](https://docs.docker.com/articles/dockerfile_best-practices/)
[Docker Hub Registry - Repositories of Docker Images](https://registry.hub.docker.com/)

[Docker Basic Command | Fast Deploying Systems With Docker](http://chunchio.gitbooks.io/docker/content/DockerBasicCommand.html)

[Docker —— 从入门到实践](http://yeasy.gitbooks.io/docker_practice/content/)
[Docker中文教程](http://letong.gitbooks.io/docker/content/)
[全面易懂的Docker指令大全](http://joshhu.gitbooks.io/dockercommands/content/index.html)

* InfoQ

[深入浅出Docker - InfoQ](http://www.infoq.com/cn/dockerdeep/)
[Docker - InfoQ](http://www.infoq.com/cn/dockers)

* coolshell

[Docker基础技术：Linux CGroup | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17049.html)
[Docker基础技术：Linux Namespace（上） | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17010.html)
[Docker基础技术：Linux Namespace（下） | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17029.html)

[StrongLoop | Containerizing Node.js Apps with Docker and StrongLoop](https://strongloop.com/strongblog/containerizing-node-js-apps-with-docker-and-strongloop/)
[使用docker-compose进行python开发 | YL Notes](http://yunlzheng.github.io/2015/06/06/dev-python-with-docker-compose/)

[Should I use Vagrant or Docker.io for creating an isolated environment? - Stack Overflow](http://stackoverflow.com/questions/16647069/should-i-use-vagrant-or-docker-io-for-creating-an-isolated-environment)

## Fig

[Fig | Fast, isolated development environments using Docker](http://www.fig.sh/index.html)

[Getting started with Fig and Express.js | GuoLin's blog](http://guolinn.com/2015/Getting-started-with-Fig-and-Express-js/)
[Getting started with Fig and MEAN.JS | GuoLin's blog](http://guolinn.com/2015/fig-meanjs/)

## solving `sudo`

Docker binds Unix sockets requiring su rights, add user to `docker` group to release the tight escalation.

```sh
sudo usermod -aG docker $(whoami)
```

## running GUI app in container

1. install `xvfb`
2. in host, `xvfb :88 -screen 0 1366x768x24 -ac`
3. in container, `DISPLAY:88 firefox`

[如何在Vagrant/Docker中运行Firefox | YL Notes](http://yunlzheng.github.io/2014/10/19/intro-xvfn-ubuntu/)

## Dokku

[progrium/dokku](https://github.com/progrium/dokku)
[Dokku Tutorials | DigitalOcean](https://www.digitalocean.com/community/tags/dokku)
[Setting up Dokku with DigitalOcean and Namecheap](https://gist.github.com/ngoldman/7287753)

## clean Dockers

```sh
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

## LXC

[Linux Containers: Part 1, The Intro | Linux.org](http://www.linux.org/threads/linux-containers-part-1-the-intro.4379/)
[Linux Containers: Part 2, Creating Stopping and Connecting | Linux.org](http://www.linux.org/threads/linux-containers-part-2-creating-stopping-and-connecting.4399/)
