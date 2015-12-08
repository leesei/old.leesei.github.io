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
[The Docker user guide](http://docs.docker.com/engine/userguide/)
[Get started with images](https://docs.docker.com/userguide/dockerimages/)
[Get Started with Docker for Linux](http://docs.docker.com/linux/started/)
[Get Started with Docker for Windows](http://docs.docker.com/windows/started/)
[Get Started with Docker for Mac OS X](http://docs.docker.com/mac/started/)
[Dockerfile reference](http://docs.docker.com/reference/builder/)
[Best practices for writing Dockerfiles](https://docs.docker.com/articles/dockerfile_best-practices/)

[Docker: Up & Running](https://www.safaribooksonline.com/library/view/docker-up/9781491917565/)
[Free eBook - Docker Security - Using Containers Safely in Production](https://www.openshift.com/promotions/docker-security.html)

[The Hitchhiker's Guide to Docker and Modulus - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/the-hitchhikers-guide-to-docker-and-modulus--cms-24770)
[Docker Basic Command | Fast Deploying Systems With Docker](http://chunchio.gitbooks.io/docker/content/DockerBasicCommand.html)
[The Docker Ecosystem | DigitalOcean](https://www.digitalocean.com/community/tutorial_series/the-docker-ecosystem)
[Getting Started with Docker | Scotch](https://scotch.io/tutorials/getting-started-with-docker)
[Docker Basics - Amazon EC2 Container Service](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html)
[Creating a Cross-platform Docker Development Environment | via @codeship](https://blog.codeship.com/cross-platform-docker-development-environment/)
[Running a MEAN web application in Docker containers on AWS | via @codeship](http://blog.codeship.com/running-mean-web-application-docker-containers-aws/)

[Docker —— 从入门到实践](http://yeasy.gitbooks.io/docker_practice/content/)
[Docker中文教程](http://letong.gitbooks.io/docker/content/)
[全面易懂的Docker指令大全](http://joshhu.gitbooks.io/dockercommands/content/index.html)

[Create a Node.js Container image for Windows](https://stefanscherer.github.io/create-an-io-js-container-image-for-windows/)
[danawoodman/docker-node-hello-world](https://github.com/danawoodman/docker-node-hello-world?utm_source=nodeweekly&utm_medium=email)

[Bitnami Stacksmith](https://stacksmith.bitnami.com/?vero_conv=1304303901)

## InfoQ

[深入浅出Docker - InfoQ](http://www.infoq.com/cn/dockerdeep/)
[Docker - InfoQ cn](http://www.infoq.com/cn/dockers)

[Easier, Better, Faster, Safer Deployment with Docker and Immutable Containers](http://www.infoq.com/presentations/immutable-servers-docker)

[Docker - InfoQ](http://www.infoq.com/docker-2)
[Executable Images - How to Dockerize Your Development Machine](http://www.infoq.com/articles/docker-executable-images)

* coolshell

[Docker基础技术：Linux CGroup | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17049.html)
[Docker基础技术：Linux Namespace（上） | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17010.html)
[Docker基础技术：Linux Namespace（下） | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17029.html)
[Docker基础技术：AUFS | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/17061.html)

[StrongLoop | Containerizing Node.js Apps with Docker and StrongLoop](https://strongloop.com/strongblog/containerizing-node-js-apps-with-docker-and-strongloop/)
[使用docker-compose进行python开发 | YL Notes](http://yunlzheng.github.io/2015/06/06/dev-python-with-docker-compose/)

[Should I use Vagrant or Docker.io for creating an isolated environment? - Stack Overflow](http://stackoverflow.com/questions/16647069/should-i-use-vagrant-or-docker-io-for-creating-an-isolated-environment)

## Docker Hub

[Docker Hub](https://hub.docker.com/explore/)
[Introducing Docker Hub](https://docs.docker.com/docker-hub/)
[docker-dev](https://hub.docker.com/_/docker-dev/)
[ubuntu](https://hub.docker.com/_/ubuntu/)
[wordpress](https://hub.docker.com/_/wordpress/)
[node](https://hub.docker.com/_/node/)

[aptible/docker-nodejs](https://github.com/aptible/docker-nodejs)

## Fig

[Fig | Fast, isolated development environments using Docker](http://www.fig.sh/index.html)

[Getting started with Fig and Express.js | GuoLin's blog](http://guolinn.com/2015/Getting-started-with-Fig-and-Express-js/)
[Getting started with Fig and MEAN.JS | GuoLin's blog](http://guolinn.com/2015/fig-meanjs/)

## Dokku

[progrium/dokku](https://github.com/progrium/dokku)
[Dokku Tutorials | DigitalOcean](https://www.digitalocean.com/community/tags/dokku)
[Setting up Dokku with DigitalOcean and Namecheap](https://gist.github.com/ngoldman/7287753)

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

## clean Dockers

```sh
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```

## LXC

[Linux Containers: Part 1, The Intro | Linux.org](http://www.linux.org/threads/linux-containers-part-1-the-intro.4379/)
[Linux Containers: Part 2, Creating Stopping and Connecting | Linux.org](http://www.linux.org/threads/linux-containers-part-2-creating-stopping-and-connecting.4399/)
