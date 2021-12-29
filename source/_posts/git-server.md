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

[Run your own GitHub-like service with the help of Docker · Docker Pirates ARMed with explosive stuff](http://blog.hypriot.com/post/run-your-own-github-like-service-with-docker/)

## Sharing port 22

Sharing port 22 with containerized git server

[Share port 22 between Gogs inside Docker & the local system](http://www.ateijelo.com/blog/2016/07/09/share-port-22-between-docker-gogs-ssh-and-local-system)
[How to config SSH settings - Tips, Tricks, and How-To's - Gogs Discussion](https://discuss.gogs.io/t/how-to-config-ssh-settings/34)

[ssh forward git user - Google Search](https://www.google.com/search?newwindow=1&sxsrf=ALeKk02aCapVMBcZwftsFRJFrYPUh5Y4Kg%3A1592008090725&ei=mh3kXv7mK9vXhwOLh5rwBQ&q=ssh+forward+git+user&oq=forward+git+ssh+&gs_lcp=CgZwc3ktYWIQAxgDMgYIABAWEB4yBggAEBYQHjIGCAAQFhAeMgYIABAWEB46BAgjECc6BAgAEEM6BQgAEJECOgcIABCDARBDOgcIABCxAxBDOgUIABCxAzoCCAA6BwgjEOoCECc6BQgAEMsBUPmLCVivtQlgotUJaAFwAHgAgAFwiAHCCpIBBDE4LjGYAQCgAQGqAQdnd3Mtd2l6sAEK&sclient=psy-ab)

`Match User` block with `ForceCommand` in `/etc/ssh/sshd_config`
[How to SSH gate forwarding git user to gitserver? - Server Fault](https://serverfault.com/questions/437952/how-to-ssh-gate-forwarding-git-user-to-gitserver)
[ssh - Have sshd forward logins of git user to a (GitLab) Docker container - Stack Overflow](https://stackoverflow.com/questions/33042817/have-sshd-forward-logins-of-git-user-to-a-gitlab-docker-container)
[ssh - Forward git user's login name to (gitlab) docker container with sshd](https://try2explore.com/questions/12062988)
[Forward ssh for Git user to Git server - Unix & Linux Stack Exchange](https://unix.stackexchange.com/a/260570/7691)
[networking - How can I redirect SSH users to another SSH login? - Ask Ubuntu](https://askubuntu.com/questions/649729/how-can-i-redirect-ssh-users-to-another-ssh-login)

[Git - Setting Up the Server](https://git-scm.com/book/en/v2/Git-on-the-Server-Setting-Up-the-Server)
`git` user should use `git-shell`

```sh
# test from client
ssh git@<host> /bin/true
ssh git@<host> git-receive-pack <path-to-git-repository>

# on host
ssh -v git@127.0.0.1:10022 git-receive-pack <path-to-git-repository>
```

## git/ssh

[vanilla git/ssh](http://stackoverflow.com/questions/10888300/gitosis-vs-gitolite)
[Howto: Git Server over SSH - SysTutorials](https://www.systutorials.com/set-up-git-server-through-ssh-connection/)

## git-daemon

read-only unauthenticated (public) access

[git-daemon(1)](https://www.kernel.org/pub/software/scm/git/docs/git-daemon.html)
[Git - git-daemon Documentation](https://git-scm.com/docs/git-daemon)
[Git - Git Daemon](https://git-scm.com/book/en/v2/Git-on-the-Server-Git-Daemon)

## gitosis

[tv42/gitosis](https://github.com/tv42/gitosis) no update since 2007
[Mivok.net - Gitosis - manage git repositories sanely](http://mivok.net/2010/03/05/gitosis.html)
[Setting Up a Git Server Using Gitosis - SysTutorials](https://www.systutorials.com/setting-up-git-server-using-gitosis/)

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
[How to Set Up A Gitolite Git Server - A Ten-Minute Tutorial - SysTutorials](https://www.systutorials.com/how-to-set-up-gitolite-git-server-a-ten-minute-tutorial/)

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
