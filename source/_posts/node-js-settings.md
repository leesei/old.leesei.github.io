title: "Node.js settings"
date: 2014-12-11 17:31:11
categories:
- comp.lang
tags:
- node-js
- settings
- nvm
- npm
- jspm
- package-manager
toc: true
---

# Node.js Settings

## Using `nvm`

```sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.25.4/install.sh | bash
# nvm installer will load nvm in your shell profile

# use git repo
git clone git://github.com/creationix/nvm.git ~/.nvm
# you have to source nvm in your shell proflie
# echo ". ~/.nvm/nvm.sh" >> ~/.bashrc
. ~/.nvm/nvm.sh
```

### Installing/updating Node.js

```sh
nvm ls-remote

NODE_VERSION=v0.12.3
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

## jspm

[jspm.io - Frictionless Browser Package Management](http://jspm.io/)


## Node modules

### `node-gyp` and Python 3

`node-gyp` does not supports Python 3, use these on system with Python 3 as default:
- `PYTHON=$(which python2) npm intall`
- `npm config set -g python $(which python2)`

```sh
# dev tools
npm install -g bower browserify coffee nodemon
# gulp
npm install -g gulp gulp-watch gulp-shell
# linters
npm install -g csslint jshint jsonlint htmlhint
# debug
npm install -g bench-rest node-inspector
# generators
npm install -g cordova ionic
# bin
npm install -g bedecked chance ecstatic fancy-server gfms gfm2html hexo-cli markdown-tools rfc
# log tools
npm install -g bunyan logcat
# workshops, http://nodeschool.io/#workshoppers
npm install -g makemehapi how-to-npm browserify-adventure
```

```sh
cd ~/.script
# lib modules
npm install -g chalk ip nomnom lodash request
# automation
npm install -g cheerio nightmare phantasma

npm uninstall -g chalk ip nomnom lodash cheerio nightmare phantasma
npm uninstall -g gulp gulp-shell gulp-watch wiredep
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
bedecked bench-rest bower browserify bunyan chance coffee cordova csslint ecstatic fancy-server gfm2html gfms gitbook-cli hexo-cli htmlhint ionic jsdoc jshint json jsonlint logcat markdown-tools node-inspector nodemon rfc 
```

## npm fails

Try clearing npm cache with:

```sh
npm cache clean
```

Hope that helps.

[when all else fails, clear you cache](http://codebetter.com/glennblock/2012/02/27/my-tale-of-npm-woe-when-all-else-fails-clear-you-cache/)

## Running Node alongside web servers

https://github.com/sindresorhus/guides/blob/master/run-node-server-alongside-apache.md

https://gist.github.com/leesei/7112870#nodenginx
