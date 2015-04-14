title: "Node.js settings"
date: 2014-12-11 17:31:11
categories:
- comp.lang
tags:
- node-js
- settings
- nvm
- npm
- package-manager
toc: true
---

# Node.js Settings

## Using `nvm`

```sh
git clone git://github.com/creationix/nvm.git ~/.nvm
# echo ". ~/.nvm/nvm.sh" >> ~/.bashrc
. ~/.nvm/nvm.sh
```

### Installing/updating Node.js

```sh
nvm ls-remote

NODE_VERSION=v0.12.1
nvm install ${NODE_VERSION}
nvm use ${NODE_VERSION}
nvm alias default ${NODE_VERSION}

# copy global modules
# backup global module list and install]
# nvm copy-packages <previous-version>
# npm update

# add global module to NODE_PATH for require() to pick them up
NODE_PATH=$(npm root -g)
```

## Using PPA

> This is the recommended way to install Node.js for deamons.

[nodesource/distributions](https://github.com/nodesource/distributions)

## npm

npm is included in node since v0.6.3
but npm update fails to update itself (isaacs/npm#4046, isaacs/npm#4099)

```sh
# install npm manually
curl -L https://npmjs.org/install.sh | sh
```

### npmrc without sudo

> for system installs, not needed for `nvm`  
> https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md

Add this to `~/.npmrc`:
```
prefix = ${HOME}/.npm-packages
```

Then add this to `~/.profile` or `~/.bashrc`:
```
export PATH=~/.npm-packages/bin:$PATH
```

## Node modules

```sh
# dev tools
npm install -g bower browserify coffee nodemon wiredep
# linters
npm install -g csslint jshint jsonlint
# debug
npm install -g bench-rest node-inspector
# generators
npm install -g cordova ionic # yo
# bin
npm install -g bedecked chance ecstatic gfms gfm2html hexo-cli
# log tools
npm install -g bunyan logcat
# global modules
npm install -g ip nomnom lodash
# automation
npm install -g cheerio nightmare phantasma
# workshops, http://nodeschool.io/#workshoppers
npm install -g makemehapi how-to-npm browserify-adventure
```

## List globally installed modules

```sh
npm ls -g --depth 0
# OR
\ls $(npm root -g)
```

To get a list for installing in another machine (or backup the list)
> npm must be updated alone or it will cause error
> remove npm before `npm install -g`

```sh
npm ls -g --depth 0 | grep -P '(?<= ).*(?=@)' -o | grep -v npm | tr '\n' ' ' && echo
# OR
\ls $(npm root -g) | grep -v npm | tr -s ' \t\n' ' ' && echo
```

```
bedecked bench-rest bower browserify bunyan chance cheerio coffee cordova csslint ecstatic gfm2html gfms hexo-cli ionic ip jshint jsonlint lodash logcat nightmare node-inspector nodemon nomnom phantasma wiredep 
```

## Running Node alongside web servers

https://github.com/sindresorhus/guides/blob/master/run-node-server-alongside-apache.md

https://gist.github.com/leesei/7112870#nodenginx
