title: Docker
date: 2014-12-11 17:37:50
categories:
- linux
tags:
- shell-tool
- docker
---

## clean Dockers

```sh
docker stop $(docker ps -a -q)
docker rm $(docker ps -a -q)
```
