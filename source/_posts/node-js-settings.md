---
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

NODE_VERSION=v0.12.7
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

## Using package manager

> This is the recommended way to install Node.js for daemons.

[Installing Node.js via package manager · nodejs/node-v0.x-archive Wiki](https://github.com/nodejs/node-v0.x-archive/wiki/Installing-Node.js-via-package-manager)

[nodesource/distributions](https://github.com/nodesource/distributions)

## Node REPL

```
$ node
> console.log('Node is running');
Node is running
> .help
.break Sometimes you get stuck, this gets you out
.clear Alias for .break
.exit  Exit the repl
.help  Show repl options
.load  Load JS from a file into the REPL session
.save  Save all evaluated commands in this REPL session to a file
> .exit
```

## npm

npm is included in node since v0.6.3
but npm update fails to update itself (isaacs/npm#4046, isaacs/npm#4099)

```sh
# install npm manually
curl -L https://npmjs.org/install.sh | sh
```

### Project homepage

Use `home` to visit the homepage of a project hosted on NPM.

```sh
npm home nomnom
npm home lodash
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
export PATH=${HOME}/.npm-packages/bin:$PATH
```

## jspm

[jspm.io - Frictionless Browser Package Management](http://jspm.io/)

## Node modules

### `node-gyp` and Python 3

`node-gyp` does not supports Python 3, use these on system with Python 3 as default:
- `PYTHON=$(which python2) npm intall`
- `npm config set -g python $(which python2)`

Global modules:
```sh
# dev tools
npm install -g bower gitignore nesh nodemon pageres-cli # coffee
npm install -g babel-cli babel-preset-es2015 babel-preset-react
# gulp
# npm install -g gulp gulp-watch gulp-shell
# linters
# eslint-plugin-react
npm install -g csslint eslint babel-eslint jsonlint htmlhint semistandard 
# debug
npm install -g bench-rest node-inspector
# generators
# ionic yuidocjs
npm install -g cordova documentation
# data utils
npm install -g json markdown-tools underscore-cli yamljs
# servers
npm install -g bedecked ecstatic fancy-server gfms hotel json-server
# bin
npm install -g gfm2html hexo-cli rfc 
# log tools
npm install -g bunyan logcat tap-spec tap-out faucet
```

`~/.script/` modules:
```sh
cd ~/.script
# lib modules
npm install chalk chance commander ip jsop nomnom lodash request
# automation
npm install cheerio revenant

# with package.json
npm install
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
babel-cli babel-eslint bedecked bench-rest bower browserify bunyan cordova csslint documentation ecstatic eslint-plugin-react fancy-server gfm2html gfms gitbook-cli gitignore hexo-cli hotel htmlhint jshint json jsonlint json-server logcat markdown-tools nesh node-inspector nodemon open-shortcut openslide-prop2json pageres-cli rfc semistandard tap-spec underscore-cli yamljs 
```

## npm fails

Try clearing npm cache with:

```sh
npm cache clean
```

Hope that helps.

[when all else fails, clear you cache](http://codebetter.com/glennblock/2012/02/27/my-tale-of-npm-woe-when-all-else-fails-clear-you-cache/)

## Running Node alongside web servers

[guides/run-node-server-alongside-apache.md at master · sindresorhus/guides](https://github.com/sindresorhus/guides/blob/master/run-node-server-alongside-apache.md)

