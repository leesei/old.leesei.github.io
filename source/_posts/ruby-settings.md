title: Ruby settings
toc: true
date: 2015-01-13 13:14:43
tags:
- python
- settings
- rvm
- gem
- package-manager
---

## Install `rvm`

https://rvm.io/

```sh
\curl -L https://get.rvm.io | bash -s stable
source ~/.rvm/bin/rvm
```

## Installing/updating Rubies

```sh
rvm list known

# ruby-latest have to be compiled
RUBY_VERSION=ruby-2.0.0
rvm install ${RUBY_VERSION}
rvm alias create default ${RUBY_VERSION}
```

## `rvm` basics

```sh
rvm list 
rvm info    # general rvm info
rvm gemdir  # current gem directory 
```

# modules

gem or rvm install?

```sh
# app
gem install humongous # mongodb browser
# redhat openshift
gem install rhc
```

```sh
# heroku can alternately installed by
wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh
```
