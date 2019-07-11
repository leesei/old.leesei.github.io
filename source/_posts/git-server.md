---
title: Git server
categories:
  - app
tags:
  - git
toc: true
date: 2016-03-04 17:05:28
---

Git server:

- serves the bare repo for remote clone/pull/push
- enforce access control
- include web interface for better access

<!-- more -->

[GitPrep](http://gitprep.yukikimoto.com/) GitHub clone in Perl
[gitbucket/gitbucket](https://github.com/gitbucket/gitbucket) GitHub clone
[Gerrit Code Review](https://www.gerritcodereview.com/) by Google

[git-daemon(1)](https://www.kernel.org/pub/software/scm/git/docs/git-daemon.html)
[Git - git-daemon Documentation](https://git-scm.com/docs/git-daemon)

[vanilla git/ssh](http://stackoverflow.com/questions/10888300/gitosis-vs-gitolite)

[Run your own GitHub-like service with the help of Docker · Docker Pirates ARMed with explosive stuff](http://blog.hypriot.com/post/run-your-own-github-like-service-with-docker/)

## Sharing port 22

Sharing port 22 with containerized git server

[Share port 22 between Gogs inside Docker & the local system](http://www.ateijelo.com/blog/2016/07/09/share-port-22-between-docker-gogs-ssh-and-local-system)
[How to config SSH settings - Tips, Tricks, and How-To's - Gogs Discussion](https://discuss.gogs.io/t/how-to-config-ssh-settings/34)

> `git` user need login shell?

```sh
# test from client
ssh git@<host> /bin/true
ssh git@<host> git-receive-pack <path-to-git-repository>

# on host
ssh -v git@127.0.0.1:10022 git-receive-pack <path-to-git-repository>
```

## gitosis

[tv42/gitosis](https://github.com/tv42/gitosis) no update since 2007
[Gitbook](https://git-scm.com/book/en/v1/Git-on-the-Server-Gitosis)
[Mivok.net - Gitosis - manage git repositories sanely](http://mivok.net/2010/03/05/gitosis.html)

The `git` user will check `/home/git/.gitosis.conf` (which symlinks to `/home/git/repositories/gitosis-admin.git/gitosis.conf`) for repo access
It will be updated upon push to `gitosis-admin`.

To debug gitosis, edit `/home/git/.gitosis.conf` and add:

```ini
[gitosis]
loglevel=DEBUG

...
```

You can even edit it to override the access control.

## Gitolite

[gitolite](http://gitolite.com/gitolite/index.html) replace gitosis, written in Perl
[ssh - How do programs like gitolite work? - Stack Overflow](http://stackoverflow.com/questions/13318715/how-do-programs-like-gitolite-work/)
[Internal Git server with Gitolite](https://sysadmincasts.com/episodes/11-internal-git-server-with-gitolite)

## GitLab

[GitLab](https://about.gitlab.com/) GitHub clone, bought [gitorious](https://gitorious.org/)

[GitLab Documentation](http://doc.gitlab.com/ce/)
[GitLab CI](http://doc.gitlab.com/ce/ci/quick_start/README.html) integrated to GitLab

The Omnibus package simplifies the setup of GitLab ALOT
[Download GitLab Community Edition (CE) | GitLab](https://about.gitlab.com/downloads/)

[GitLab 11.0 released with Auto DevOps and License Management | GitLab](https://about.gitlab.com/2018/06/22/gitlab-11-0-released/)
[Easy & simple guide to Backup & Restore GITLAB - LinuxTechLab](https://linuxtechlab.com/simple-guide-backup-restore-gitlab/)

Upgrading GitLab is as simple as:

```sh
sudo gitlab-ctl stop unicorn
sudo gitlab-ctl stop sidekiq
sudo gitlab-rake gitlab:backup:create
sudo dpkg -i gitlab_x.x.x-omnibus.xxx.deb
sudo gitlab-ctl reconfigure
```

[Gitlab - ArchWiki](https://wiki.archlinux.org/index.php/gitlab)
[README.md · master · GitLab.org / omnibus-gitlab · GitLab](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/README.md)
[How To Set Up GitLab As Your Very Own Private GitHub Clone | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-set-up-gitlab-as-your-very-own-private-github-clone) from scratch

## Gogs

[Gogs](http://gogs.io/) GitHub clone in Go
[Gogs Discussion](https://discuss.gogs.io/)

[Introduction - Gogs - Go Git Service](https://gogs.io/docs)
[Troubleshooting - Gogs - Go Git Service](https://gogs.io/docs/intro/troubleshooting.html)
[Config Cheat Sheet - Gogs](https://gogs.io/docs/advanced/configuration_cheat_sheet)

[Gogs, an alternative to Gitlab](http://jbrodriguez.io/gogs-an-alternative-to-gitlab/)

### API

[gogs/docs-api: A repository for Gogs API v1 documentation.](https://github.com/gogs/docs-api)

[mattddowney/gogs-bash: Bash Script for Interacting with the GOGS API](https://github.com/mattddowney/gogs-bash)
[unfoldingWord-dev/node-gogs-client: A client library for interacting with the gogs REST api](https://github.com/unfoldingWord-dev/node-gogs-client)
[gogs_client — gogs_client documentation](https://pythonhosted.org/gogs-client/index.html) Python
[gogs/go-gogs-client: Gogs API client in Go.](https://github.com/gogs/go-gogs-client) official Go one

## Gitea

[Gitea](https://gitea.io/en-us/)

Gitea is a [fork of Gogs](https://blog.gitea.io/2016/12/welcome-to-gitea/) at 2016-11 that is more community based.

[Gitea compared to other Git hosting options - Docs](https://docs.gitea.io/en-us/comparison/)

## sr.ht

[sr.ht - software hosting for hackers](https://meta.sr.ht/)

## gitweb

```sh
# start server
git instaweb -d webrick --start

# visit http://localhost:1234

# stop server
git instaweb -d webrick --stop
```
