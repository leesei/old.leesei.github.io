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

[creationix/nvm: Node Version Manager - Simple bash script to manage multiple active node.js versions](https://github.com/creationix/nvm)
[How to install and manage Node.js, sudo free, with NVM](http://www.nearform.com/nodecrunch/nodejs-sudo-free/)

```sh
curl -o- https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
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

NODE_CURRENT=$(nvm current)
NODE_VERSION=v6  # new desired version
nvm install stable
nvm alias default stable
nvm reinstall-packages ${NODE_CURRENT}

# add global module to NODE_PATH for require() to pick them up
NODE_PATH=$(npm root -g)
```

You have to reinstall all your global modules after update.
See [Node modules](#node-modules) or use `nvm reinstall-packages <prev-version>`.

## Using package manager

> This is the recommended way to install Node.js for daemons.

[Installing Node.js via package manager · nodejs/node-v0.x-archive Wiki](https://github.com/nodejs/node-v0.x-archive/wiki/Installing-Node.js-via-package-manager)

[nodesource/distributions](https://github.com/nodesource/distributions)

## yarn

[Yarn](https://yarnpkg.com/)

[Installing Node Packages with Yarn - How To - Cloud9 Community](https://community.c9.io/t/installing-node-packages-with-yarn/10393)
[Yarn: A new package manager for JavaScript | Engineering Blog | Facebook Code](https://code.facebook.com/posts/1840075619545360)
[Yarn vs npm - The State of Node.js Package Managers | @RisingStack](https://blog.risingstack.com/yarn-vs-npm-node-js-package-managers/)

[To Yarn and Back (to npm) Again | Mixmax Engineering Blog](https://mixmax.com/blog/to-yarn-and-back-again-npm)

[Yarn Plug’n’Play – Thomas Reggi – Medium](https://medium.com/@thomasreggi/yarn-plugn-play-1c398bf3e417)
[Yarn Plug'n'Play vs node_modules | gap intelligence](https://gapintelligence.com/blog/2018/yarn-plug-n-play-vs-node_modules)

## pnpm

[pnpm · Fast, disk space efficient package manager](https://pnpm.js.org/)

[Why should we use pnpm? by @ZoltanKochan](https://www.kochan.io/nodejs/why-should-we-use-pnpm.html)
[Flat node_modules is not the only way – pnpm – Medium](https://medium.com/pnpm/flat-node-modules-is-not-the-only-way-d2e40f7296a3)

## npm

npm is included in node since v0.6.3
but npm update fails to update itself (isaacs/npm#4046, isaacs/npm#4099)

```sh
# install npm manually
curl -L https://npmjs.org/install.sh | sh
```

[The Ultimate Guide to Configuring NPM](http://stackabuse.com/the-ultimate-guide-to-configuring-npm/)
[npm Documentation](https://docs.npmjs.com/)
`npm help 7 config`
`npm help npmrc`

[The npm Blog — Next Generation Package Management](https://blog.npmjs.org/post/178027064160/next-generation-package-management)
[npm/tink: a dependency unwinder for javascript](https://github.com/npm/tink)

[sindresorhus/awesome-npm: Awesome npm resources and tips](https://github.com/sindresorhus/awesome-npm)

### Behind GFW

```sh
npm config set registry https://registry.npm.taobao.org
```

### Disabling progress

Disabling progress with `npm set progress=false` yields faster `npm install`.
[Faster npm](https://davidwalsh.name/faster-npm)

### Project homepage

Use `home` to visit the homepage of a project hosted on NPM.

```sh
npm home nomnom
npm home lodash
```

### npmrc without sudo

> for system installs, not needed for `nvm`
> https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md

[03 - Fixing npm permissions | npm Documentation](https://docs.npmjs.com/getting-started/fixing-npm-permissions)

Add this to `~/.npmrc`:

```
prefix = ${HOME}/.npm-packages
```

Then add this to `~/.profile` or `~/.bashrc`:

```
export PATH=${HOME}/.npm-packages/bin:$PATH
```

## `npx`

[zkat/npx: execute npm package binaries](https://github.com/zkat/npx)  
included in `npm@5.2+`

[Introducing npx: an npm package runner – Kat Marchán – Medium](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b)
[How to use npx: the npm package runner](https://blog.scottlogic.com/2018/04/05/npx-the-npm-package-runner.html)
[suarasaur/awesome-npx: 🌟 packages and resources that work really well with zkat/npx 🕶](https://github.com/suarasaur/awesome-npx)

## Node modules

[How to Solve the Global npm Module Dependency Problem](http://www.sitepoint.com/solve-global-npm-module-dependency-problem/)

### `node-gyp` and Python 3

`node-gyp` does not supports Python 3, use these on system with Python 3 as default:
- `PYTHON=$(which python2) npm intall`
- `npm config set -g python $(which python2)`

> latest `nvm` supports command `nvm reinstall-packages <old-version>` to assist upgrade

Global modules:

```sh
# dev tools
npm install -g nesh nodemon
# project tools
npm install -g gitignore npm-check npm-remote-ls yarn
npx create-react-app fixpack
# browserify coffee
# npm install -g babel-cli babel-preset-es2015 babel-preset-react
# gulp
# npm install -g gulp gulp-watch gulp-shell
# linters
#  eslint-plugin-react
npm install -g babel-eslint csslint eslint jsonlint htmlhint prettier semistandard
# debug
npm install -g bench-rest node-inspector
# generators
# ionic yuidocjs
npm install -g cordova
# doc tools
npm install -g tldr bootprint bootprint-openapi dredd gitbook-cli raml1-doc ramlo
npm install -g doctoc markdown-tools
# data utils
npm install -g get-hrefs jq.node json pipeable-js yamljs
# servers
npm install -g ecstatic fancy-server hotel json-server live-server
# bin
npm install -g gfm2html hexo-cli rfc
# log tools
npm install -g bunyan logcat tap-spec faucet
# license tools
npm install -g license-generator license-sniffer license-spelunker
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
\ls $(npm root -g) | grep -v npm | paste -s -d' ' && echo
```

```
# home
babel-eslint bunyan csslint ecstatic eslint eslint-plugin-prettier eslint-config-prettier fancy-server faucet gfm2html github-commits-since-tag-cli gitignore htmlhint json jsonlint json-server license-generator live-server markdown-tools nodemon pipeable-js prettier refine-manhuaren rfc semistandard tldr yarn

# work
babel-eslint bootprint bootprint-openapi bunyan csslint dredd ecstatic eslint eslint-plugin-prettier fancy-server faucet gfm2html gitbook-cli gitignore htmlhint httpbin.js json jsonlint json-server license-generator live-server logcat markdown-tools nodemon prettier raml1-doc ramlo rfc semistandard tap-spec tldr yaml-lint yarn
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

---

# Packages

[Bookshelf.js](http://bookshelfjs.org/)
[Mongoose ODM](http://mongoosejs.com/)
[Chance](https://chancejs.com/)
[bitinn/node-fetch: A light-weight module that brings window.fetch to Node.js](https://github.com/bitinn/node-fetch)
[Schniz/cuery: A composable SQL query builder using template literals](https://github.com/Schniz/cuery)
[Knex.js - A SQL Query Builder for Javascript](http://knexjs.org/)
[math.js | an extensive math library for JavaScript and Node.js](http://mathjs.org/docs/datatypes/units.html)
[Numeral.js](http://numeraljs.com/) formatting and manipulating numbers
[Papa Parse - Powerful CSV Parser for JavaScript](https://www.papaparse.com/)
[natergj/excel4node: Node module to allow for easy Excel file creation](https://github.com/natergj/excel4node)
[oussamahamdaoui/forgJs: ForgJs is a javascript lightweight object validator. Go check the Quick start section and start coding with love](https://github.com/oussamahamdaoui/forgJs)

[10 Node Frameworks to Use in 2019 ― Scotch](https://scotch.io/bar-talk/10-node-frameworks-to-use-in-2019/amp)
[Fastify, Fast and low overhead web framework, for Node.js](https://www.fastify.io/)
[NestJS - A progressive Node.js web framework](https://nestjs.com/)

[alexreardon/memoize-one: A memoization library which only remembers the latest invocation](https://github.com/alexreardon/memoize-one)

Unambiguous characters for token
[chilts/node-coupon-code: Implementation of Perl's Algorithm::CouponCode for NodeJS](https://github.com/chilts/node-coupon-code)
[hirespace/token-gen: Generate unique human readable codes (e.g. vouchers, referrals, passwords, keys)](https://github.com/hirespace/token-gen)

## Backend

> see `hapi.md`

[Deployd](http://deployd.com/)
[deployd docs](http://docs.deployd.com/docs/)
[deployd/deployd: a toolkit for building realtime APIs](https://github.com/deployd/deployd)

LoopBack is based on Express
[LoopBack 3.x | LoopBack Documentation](https://loopback.io/doc/en/lb3/index.html)
[LoopBack 4 | LoopBack Documentation](https://loopback.io/doc/en/lb4/index.html) OpenAPI, ES2017, TypeScript

## Database/ORM

[Why you should avoid ORMs (with examples in Node.js)](https://blog.logrocket.com/why-you-should-avoid-orms-with-examples-in-node-js-e0baab73fa5)
Low level: Database Driver
Middle Level: Query Builder
High Level: ORM

[Which JavaScript ORM should you be using in 2018? – freeCodeCamp.org](https://medium.freecodecamp.org/a-comparison-of-the-top-orms-for-2018-19c4feeaa5f)
[From TypeORM to LoopBack: A Retrospective – Hacker Noon](https://hackernoon.com/from-typeorm-to-loopback-a-retrospective-188ea18527a2)

[Knex.js - A SQL Query Builder for Javascript](https://knexjs.org/)
[Sequelize | The Node.js / io.js ORM for PostgreSQL, MySQL, SQLite and MSSQL](https://sequelize.readthedocs.io/)
[Bookshelf.js | Home](https://bookshelfjs.org/)
[typeorm/typeorm: ORM for TypeScript and JavaScript (ES7, ES6, ES5). Supports MySQL, PostgreSQL, MariaDB, SQLite, MS SQL Server, Oracle, WebSQL databases. Works in NodeJS, Browser, Ionic, Cordova and Electron platforms.](https://github.com/typeorm/typeorm)
