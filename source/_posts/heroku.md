---
title: "Heroku"
date: 2014-12-11 17:39:03
categories:
- web
tags:
- shell-tool
- heroku
toc: true
---

[Heroku CLI | Heroku Dev Center](https://devcenter.heroku.com/articles/heroku-cli)
[heroku/cli: Heroku CLI](https://github.com/heroku/cli)

```sh
curl https://cli-assets.heroku.com/branches/stable/heroku-linux-amd64.tar.gz | tar xvz
./heroku/install
```

[Buildpack API | Heroku Dev Center](https://devcenter.heroku.com/articles/buildpack-api)
[Building Docker Images with heroku.yml | Heroku Dev Center](https://devcenter.heroku.com/articles/build-docker-images-heroku-yml)

[Process Types and the Procfile | Heroku Dev Center](https://devcenter.heroku.com/articles/procfile)

[Heroku Node.js Support | Heroku Dev Center](https://devcenter.heroku.com/articles/nodejs-support)

[Heroku Basics: Dynos and Costs - NaNLABS](https://www.nan-labs.com/blog/heroku-basics-dynos-and-costs/)
[How to host lightweight apps for free – freeCodeCamp](https://medium.freecodecamp.com/how-to-host-lightweight-apps-for-free-a29773e5f39e)

##  Heroku Button

[Creating a 'Deploy to Heroku' Button | Heroku Dev Center](https://devcenter.heroku.com/articles/heroku-button)
[Setting Up Apps Using the Platform API | Heroku Dev Center](https://devcenter.heroku.com/articles/setting-up-apps-using-the-heroku-platform-api)
[app.json Schema | Heroku Dev Center](https://devcenter.heroku.com/articles/app-json-schema)

## Pipeline

[Heroku Labs: New Pipelines | Heroku Dev Center](https://devcenter.heroku.com/articles/heroku-labs-new-pipelines)

Workflow that groups the codebase of an application in different stages of development ("review", "development", "staging", and "production") into a single dashboard.

## Docker

[Local Development with Docker | Heroku Dev Center](https://devcenter.heroku.com/articles/introduction-local-development-with-docker)
[Getting Started with Node.js and Heroku Local Docker Development | Heroku Dev Center](https://devcenter.heroku.com/articles/getting-started-with-node-js-and-heroku-local-docker-dev)

[gliderlabs/herokuish: Utility for emulating Heroku build and runtime tasks in containers](https://github.com/gliderlabs/herokuish)
[progrium/cedarish: Heroku Cedar-ish Base Image for Docker](https://github.com/progrium/cedarish)

## Passenger

[Heroku and Passenger: focus on the app-performance](https://blog.phusion.nl/2015/11/10/heroku-and-passenger-focus-on-the-app-performance/)

## commands

[Command Line | Heroku Dev Center](https://devcenter.heroku.com/categories/command-line)

- create a new heroku app

  `heroku apps:create <NAME>`  
  if current directory is a git repo, this should have added remote `heroku`  
  `git remote -v`

- with existing git repo

  `heroku git:remote -a <NAME>`  
  `git remote add heroku git@heroku.com:<NAME>.git`

- deploy

  `git push heroku master`  

  To force an compile on Heroku,  
  `git commit --allow-empty -m "Message"`

  Also see `heroku-repo` below

- restart server

  `heroku restart`

- terminal

  `heroku run bash`  
  > All changes are lost when server is restarted

- multiple buildpack

[Heroku’s support for running multiple buildpacks against a single application now has first-class support in the Heroku Toolbelt. | Heroku Dev Center](https://devcenter.heroku.com/changelog-items/653)

## Plugins

- [heroku-vim](https://github.com/naaman/heroku-vim)

  `heroku plugins:install https://github.com/naaman/heroku-vim`
  `heroku vim`

  Or use [`vim-on-heroku.sh`](https://gist.github.com/naaman/2847793)

```sh
#!/usr/bin/env bash
mkdir vim
curl https://s3.amazonaws.com/heroku-vim/vim-7.3.tar.gz --location --silent | tar xz -C vim
export PATH=$PATH:/app/vim/bin
```

- [heroku-config](https://github.com/xavdid/heroku-config)

  `heroku plugins:install heroku-config`

```sh
# pull Heroku config as .env
heroku config:pull --overwrite --interactive
```

- [heroku-repo](https://github.com/heroku/heroku-repo)

```sh
heroku plugins:install https://github.com/heroku/heroku-repo.git
heroku repo:rebuild
```

## Heroku Help extract (2015-07-28)

heroku-toolbelt/3.40.6 (x86_64-linux) ruby/2.0.0
heroku-cli/4.20.11-62a7bb8 (amd64-linux) go1.4.2

Installed Plugins:
- heroku-git@2.4.0
- heroku-vim

### `heroku help`

```
Usage: heroku COMMAND [--app APP] [command-specific-options]

Primary help topics, type "heroku help TOPIC" for more details:

  addons    #  manage addon resources
  apps      #  manage apps (create, destroy)
  auth      #  authentication (login, logout)
  config    #  manage app config vars
  domains   #  manage domains
  logs      #  display logs for an app
  ps        #  manage dynos (dynos, workers)
  releases  #  manage app releases
  run       #  run one-off commands (console, rake)
  sharing   #  manage collaborators on an app

Additional topics:

  buildpacks   #  manage the buildpack for an app
  certs        #  manage ssl endpoints for an app
  drains       #  display drains for an app
  features     #  manage optional features
  fork         #  clone an existing app
  git          #  manage git for apps
  help         #  list commands and display help
  keys         #  manage authentication keys
  labs         #  manage optional features
  local        #  run heroku app locally
  maintenance  #  manage maintenance mode for an app
  members      #  manage membership in organization accounts
  orgs         #  manage organization accounts
  pg           # 
  pgbackups    #  manage backups of heroku postgresql databases
  plugins      #  manage plugins to the heroku gem
  redis        #  list redis databases for an app
  regions      #  list available regions
  stack        #  manage the stack for an app
  status       #  check status of heroku platform
  twofactor    #  manage two-factor authentication settings
  update       #  update the heroku client
  version      #  display version
  vim          # 

```

### `heroku help addons`

```
Usage: heroku addons [{--all,--app APP_NAME,--resource ADDON_NAME}]

 list installed add-ons

 NOTE: --all is the default unless in an application repository directory, in
 which case --all is inferred.

 --all                  # list add-ons across all apps in account
 --app APP_NAME         # list add-ons associated with a given app
 --resource ADDON_NAME  # view details about add-on and all of its attachments

Examples:

 $ heroku addons --all
 $ heroku addons --app acme-inc-website
 $ heroku addons --resource @acme-inc-database

Additional commands, type "heroku help COMMAND" for more details:

  addons:attach ADDON_NAME                        #  attach add-on resource to an app
  addons:create SERVICE:PLAN                      #  create an add-on resource
  addons:destroy ADDON_NAME [ADDON_NAME ...]      #  destroy add-on resources
  addons:detach ATTACHMENT_NAME                   #  detach add-on resource from an app
  addons:docs ADDON_NAME                          #  open an add-on's documentation in your browser
  addons:downgrade ADDON_NAME ADDON_SERVICE:PLAN  #  downgrade an existing add-on resource to PLAN
  addons:open ADDON_NAME                          #  open an add-on's dashboard in your browser
  addons:plans SERVICE                            #  list all available plans for an add-on service
  addons:services                                 #  list all available add-on services
  addons:upgrade ADDON_NAME ADDON_SERVICE:PLAN    #  upgrade an existing add-on resource to PLAN

```

### `heroku help apps`

```
Usage: heroku apps

 list your apps

 -o, --org ORG     # the org to list the apps for
 -A, --all         # list all apps in the org. Not just joined apps
 -p, --personal    # list apps in personal account when a default org is set

Example:

 $ heroku apps
 === My Apps
 example
 example2

 === Collaborated Apps
 theirapp   other@owner.name

Additional commands, type "heroku help COMMAND" for more details:

  apps:create [NAME]             #  create a new app
  apps:destroy --app APP         #  permanently destroy an app
  apps:info                      #  show detailed app information
  apps:join --app APP            #  add yourself to an organization app
  apps:leave --app APP           #  remove yourself from an organization app
  apps:lock --app APP            #  lock an organization app to restrict access
  apps:open --app APP            #  open the app in a web browser
  apps:rename NEWNAME --app APP  #  rename the app
  apps:unlock --app APP          #  unlock an organization app so that any org member can join it

```

### `heroku help config`

```
Usage: heroku config

 display the config vars for an app

 -s, --shell  # output config vars in shell format

Examples:

 $ heroku config
 A: one
 B: two

 $ heroku config --shell
 A=one
 B=two

Additional commands, type "heroku help COMMAND" for more details:

  config:get KEY                            #  display a config value for an app
  config:set KEY1=VALUE1 [KEY2=VALUE2 ...]  #  set one or more config vars
  config:unset KEY1 [KEY2 ...]              #  unset one or more config vars

```

### `heroku help logs`

```
Usage: heroku logs

 display recent log output

 -n, --num NUM        # the number of lines to display
 -p, --ps PS          # only display logs from the given process
 -s, --source SOURCE  # only display logs from the given source
 -t, --tail           # continually stream logs
 --force-colors       # Force use of ANSI color characters (even on non-tty outputs)

Example:

 $ heroku logs
 2012-01-01T12:00:00+00:00 heroku[api]: Config add EXAMPLE by email@example.com
 2012-01-01T12:00:01+00:00 heroku[api]: Release v1 created by email@example.com

```

### `heroku help buildpacks`

```
Usage: heroku buildpacks

 display the buildpack_url(s) for an app

Examples:

 $ heroku buildpacks
 https://github.com/heroku/heroku-buildpack-ruby

Additional commands, type "heroku help COMMAND" for more details:

  buildpacks:add BUILDPACK_URL       #  add new app buildpack, inserting into list of buildpacks if neccessary
  buildpacks:clear                   #  clear all buildpacks set on the app
  buildpacks:remove [BUILDPACK_URL]  #  remove a buildpack set on the app
  buildpacks:set BUILDPACK_URL       #  set new app buildpack, overwriting into list of buildpacks if neccessary

```

### `heroku help plugins`

```
Usage: heroku plugins

 list installed plugins

Example:

 $ heroku plugins
 === Installed Plugins
 heroku-production-check@0.2.0

Additional commands, type "heroku help COMMAND" for more details:

  plugins:install URL       #  install a plugin
  plugins:link [PATH]       #  This is useful when developing plugins locally.
  plugins:uninstall PLUGIN  #  uninstall a plugin
  plugins:update [PLUGIN]   #  updates all plugins or a single plugin by name

```

## References

https://devcenter.heroku.com/categories/command-line
https://devcenter.heroku.com/articles/quickstart
https://devcenter.heroku.com/articles/git
https://blog.heroku.com/archives/2014/12/5/http_git_now_generally_available
