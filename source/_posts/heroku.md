title: Heroku
toc: true
date: 2014-12-11 17:39:03
tags:
- heroku
---

# Heroku Toolbelt

https://toolbelt.heroku.com/

https://blog.heroku.com/archives/2014/12/5/http_git_now_generally_available

* [hk](https://github.com/heroku/hk) - Fast Heroku Client

```bash
$ su
# L=/usr/local/bin/hk && curl -sL -A "`uname -sp`" https://hk.heroku.com/hk.gz | zcat >$L && chmod +x $L
```

## commands

- create new heroku app

  `heroku apps:create <NAME>`  
  this should have added remote repo `heroku`  
  `git remote -v`

- with existing app

  `heroku git:remote -a <NAME>`  
  `git remote add heroku git@heroku.com:<NAME>.git`

- deploy

  `git push heroku master`  

  To force an compile on Heroku:  
  `git commit -am "empty" --allow-empty # force a git commit`

- restart server

  `heroku restart`

- ssh

  `heroku run bash`  
  > All changes are lost when server is restarted

## Plugins

> https://outlet.herokuapp.com/

- [heroku-vim](https://github.com/naaman/heroku-vim)

  `heroku plugins:install https://github.com/naaman/heroku-vim`
  `heroku vim`

  Or use [`vim-on-heroku.sh`](https://gist.github.com/naaman/2847793)

```bash
#!/usr/bin/env bash
mkdir vim
curl https://s3.amazonaws.com/heroku-vim/vim-7.3.tar.gz --location --silent | tar xz -C vim
export PATH=$PATH:/app/vim/bin
```

- [heroku-push](https://github.com/ddollar/heroku-push)
  
 `heroku plugins:install https://github.com/ddollar/heroku-push`

- [heroku-config](https://github.com/ddollar/heroku-config)
  
 `heroku plugins:install git://github.com/ddollar/heroku-config.git`

```
# pull Heroku config as .env
heroku config:pull --overwrite --interactive
```

## Help extract (20141211)

### `heroku help`

```
Usage: heroku COMMAND [--app APP] [command-specific-options]

Primary help topics, type "heroku help TOPIC" for more details:

  addons    #  manage addon resources
  apps      #  manage apps (create, destroy)
  auth      #  authentication (login, logout)
  config    #  manage app config vars
  domains   #  manage custom domains
  logs      #  display logs for an app
  ps        #  manage dynos (dynos, workers)
  releases  #  manage app releases
  run       #  run one-off commands (console, rake)
  sharing   #  manage collaborators on an app

Additional topics:

  certs        #  manage ssl endpoints for an app
  drains       #  display syslog drains for an app
  features     #  manage optional features
  fork         #  clone an existing app
  git          #  manage git for apps
  help         #  list commands and display help
  keys         #  manage authentication keys
  labs         #  manage optional features
  maintenance  #  manage maintenance mode for an app
  members      #  manage membership in organization accounts
  orgs         #  manage organization accounts
  pg           #  manage heroku-postgresql databases
  pgbackups    #  manage backups of heroku postgresql databases
  plugins      #  manage plugins to the heroku gem
  regions      #  list available regions
  stack        #  manage the stack for an app
  status       #  check status of heroku platform
  twofactor    # 
  update       #  update the heroku client
  version      #  display version
  vim          # 
```

### `heroku help addons`

```
Usage: heroku addons

 list installed addons

Additional commands, type "heroku help COMMAND" for more details:

  addons:add ADDON                   #  install an addon
  addons:docs ADDON                  #  open an addon's documentation in your browser
  addons:downgrade ADDON             #  downgrade an existing addon
  addons:list                        #  list all available addons
  addons:open ADDON                  #  open an addon's dashboard in your browser
  addons:remove ADDON1 [ADDON2 ...]  #  uninstall one or more addons
  addons:upgrade ADDON               #  upgrade an existing addon
```

### `heroku help apps`

```
Usage: heroku apps

 list your apps

 -o, --org ORG  # the org to list the apps for
 -A, --all      # list all apps in the org. Not just joined apps
 -p, --personal # list apps in personal account when a default org is set

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

Example:

 $ heroku logs
 2012-01-01T12:00:00+00:00 heroku[api]: Config add EXAMPLE by email@example.com
 2012-01-01T12:00:01+00:00 heroku[api]: Release v1 created by email@example.com
```

### `heroku help plugins`

```
Usage: heroku plugins

 list installed plugins

Example:

 $ heroku plugins
 === Installed Plugins
 heroku-accounts

Additional commands, type "heroku help COMMAND" for more details:

  plugins:install URL       #  install a plugin
  plugins:uninstall PLUGIN  #  uninstall a plugin
  plugins:update [PLUGIN]   #  updates all plugins or a single plugin by name
```

## References

https://devcenter.heroku.com/categories/command-line
https://devcenter.heroku.com/articles/quickstart
https://devcenter.heroku.com/articles/git
https://blog.heroku.com/archives/2014/12/5/http_git_now_generally_available
