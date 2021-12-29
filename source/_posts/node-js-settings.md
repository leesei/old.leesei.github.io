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
[jorgebucaran/nvm.fish: Node.js version manager lovingly made for Fish.](https://github.com/jorgebucaran/nvm.fish)
[nvm-sh/nvm: Node Version Manager - POSIX-compliant bash script to manage multiple active node.js versions](https://github.com/nvm-sh/nvm)
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
NODE_VERSION=v15  # new desired version
nvm install latest
# proper nvm
nvm alias default latest
# nvm.fish
set --universal nvm_default_version latest
nvm reinstall-packages ${NODE_CURRENT}

# add global module to NODE_PATH for require() to pick them up
NODE_PATH=$(npm root -g)
```

You have to reinstall all your global modules after update.
See [Node modules](#node-modules) or use `nvm reinstall-packages <prev-version>`.

## Using Volta

[Volta - The Hassle-Free JavaScript Tool Manager](https://volta.sh/)
[Introducing Volta - it manages your Node.js versions so you don't have to -- newline](https://www.newline.co/@paigen11/introducing-volta-it-manages-your-nodejs-versions-so-you-dont-have-to--eef49522)

## Using distro's package manager

> This is the recommended way to install Node.js for daemons.

[nodesource/distributions](https://github.com/nodesource/distributions)

---

[An abbreviated history of JavaScript package managers](https://medium.com/javascript-in-plain-english/an-abbreviated-history-of-javascript-package-managers-f9797be7cf0e)
[Understanding differences between npm, yarn and pnpm](https://www.alexkras.com/understanding-differences-between-npm-yarn-and-pnpm/#twitter-widget-0)
[Yarn determinism | Yarn Blog](https://legacy.yarnpkg.com/blog/2017/05/31/determinism/)

## Yarn

[Yarn](https://yarnpkg.com/)
[Compare Yarn Performance | Yarn](https://yarnpkg.com/en/compare)

[Installing Node Packages with Yarn - How To - Cloud9 Community](https://community.c9.io/t/installing-node-packages-with-yarn/10393)
[Yarn: A new package manager for JavaScript | Engineering Blog | Facebook Code](https://code.facebook.com/posts/1840075619545360)
[Yarn vs npm - The State of Node.js Package Managers | @RisingStack](https://blog.risingstack.com/yarn-vs-npm-node-js-package-managers/)

[To Yarn and Back (to npm) Again | Mixmax Engineering Blog](https://mixmax.com/blog/to-yarn-and-back-again-npm)

[Plug'n'Play | Yarn - Package Manager](https://next.yarnpkg.com/features/pnp)
[PnP Overview | Yarn](https://yarnpkg.com/lang/en/docs/pnp/)
[Getting rid of node_modules with Yarn Plug’n’Play](https://www.freecodecamp.org/news/getting-rid-of-node-modules-with-yarn-plugn-play-a490e5e747d7/)
[Yarn Plug’n’Play – Thomas Reggi – Medium](https://medium.com/@thomasreggi/yarn-plugn-play-1c398bf3e417)

## Entropic

[Entropic - we federate packages](https://discourse.entropic.dev/)
[entropic-dev/entropic: 🦝 a package registry for anything, but mostly javascript 🦝 🦝 🦝](https://github.com/entropic-dev/entropic)

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
[npm Commands and Features You Should Know ← Alligator.io](https://alligator.io/nodejs/npm-commands-you-should-know/)
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

> for system installs, not needed for `nvm` > https://github.com/sindresorhus/guides/blob/master/npm-global-without-sudo.md

[03 - Fixing npm permissions | npm Documentation](https://docs.npmjs.com/getting-started/fixing-npm-permissions)

Add this to `~/.npmrc`:

```
prefix = ${HOME}/.npm-packages
```

Then add this to `~/.profile` or `~/.bashrc`:

```
export PATH=${HOME}/.npm-packages/bin:$PATH
```

## GuPM

[azukaar/GuPM: 🐶📦 Global Universal Project Manager -- Package manager, cli tool, scripts for all your projects and your system](https://github.com/azukaar/GuPM)
[GuPM to manage your Node/JS project - ITNEXT](https://itnext.io/gupm-to-manage-your-node-js-project-b7664503f3de)

## `npx`

[npm/npx: npm package executor](https://github.com/npm/npx) included in `npm@5.2+`
[suarasaur/awesome-npx: 🌟 packages and resources that work really well with zkat/npx 🕶](https://github.com/suarasaur/awesome-npx)

[Introducing npx: an npm package runner – Kat Marchán – Medium](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b)
[How to use npx: the npm package runner](https://blog.scottlogic.com/2018/04/05/npx-the-npm-package-runner.html)
[What is NPX?](https://www.educative.io/edpresso/what-is-npx)

## Node modules

[How to Solve the Global npm Module Dependency Problem](http://www.sitepoint.com/solve-global-npm-module-dependency-problem/)

[module-alias - npm](https://www.npmjs.com/package/module-alias)

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
npm install -g npm-check npm-remote-ls yarn
npx create-react-app fixpack
# linters
#  eslint-plugin-react
npm install -g jsonlint htmlhint prettier
# debug
npm install -g bench-rest node-inspector
# generators
# ionic yuidocjs
# npm install -g cordova
# doc tools
npm install -g bootprint bootprint-openapi dredd gitbook-cli raml1-doc ramlo
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
# shell independent
npm ls -g --depth 0 | grep -P '(?<= ).*(?=@)' -o | grep -v npm | tr '\n' ' ' && echo
```

```
# home
bunyan create-react-app csslint fancy-server faucet fixpack gfm2html github-commits-since-tag-cli hexo-cli htmlhint json jsonlint json-server licenseify live-server markdown-tools nodemon npm-check pipeable-js prettier pxt refine-manhuaren yarn @google/clasp

@google/clasp fixpack json-server licenseif nodemon prettier yarn

# work
csslint depcheck dredd ecstatic faucet fixpack gfm2html htmlhint httpbin.js imgmini json jsonlint json-server lerna licenseify live-server lodash logcat markdown-tools netlify-cli nodemon prettier remarkable rfc tap-spec tldr typescript yamljs yaml-lint yarn
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

[Mongoose ODM](http://mongoosejs.com/)
[Chance](https://chancejs.com/)
[bitinn/node-fetch: A light-weight module that brings window.fetch to Node.js](https://github.com/bitinn/node-fetch)
[Papa Parse - Powerful CSV Parser for JavaScript](https://www.papaparse.com/)
[natergj/excel4node: Node module to allow for easy Excel file creation](https://github.com/natergj/excel4node)

[Voca: The JavaScript string library](https://vocajs.com/)
[panzerdp/voca: The ultimate JavaScript string library](https://github.com/panzerdp/voca)

[alexreardon/memoize-one: A memoization library which only remembers the latest invocation](https://github.com/alexreardon/memoize-one)

## Tokens

Unambiguous characters for token, good for OTP
Charset (base 30): "13456789ACDEFGHJKLMNPQRTUVWXYZ"

[nanoid: Docs, Tutorials, Reviews | Openbase](https://openbase.com/js/nanoid)
[Nano ID CC](https://zelark.github.io/nano-id-cc/)
[ai/nanoid: A tiny (108 bytes), secure, URL-friendly, unique string ID generator for JavaScript](https://github.com/ai/nanoid)
[CyberAP/nanoid-dictionary: Predefined character sets to use with nanoid](https://github.com/CyberAP/nanoid-dictionary)

[chilts/node-coupon-code: Implementation of Perl's Algorithm::CouponCode for NodeJS](https://github.com/chilts/node-coupon-code)

[hirespace/token-gen: Generate unique human readable codes (e.g. vouchers, referrals, passwords, keys)](https://github.com/hirespace/token-gen)

[nwoltman/node-uid-generator: Generates cryptographically strong pseudo-random UIDs with custom size and base-encoding](https://github.com/nwoltman/node-uid-generator)

[lukeed/hexoid: A tiny (190B) and extremely fast utility to generate random IDs of fixed length](https://github.com/lukeed/hexoid)
[lukeed/uuid: A tiny (~230B)and fast UUID (V4) generator for Node and the browser](https://github.com/lukeed/uuid)

[short-uuid: Docs, Tutorials, Reviews | Openbase](https://openbase.com/js/short-uuid)

## Backend

> see `hapi.md`

[Deployd](http://deployd.com/)
[deployd docs](http://docs.deployd.com/docs/)
[deployd/deployd: a toolkit for building realtime APIs](https://github.com/deployd/deployd)

LoopBack is based on Express
[LoopBack 4 | LoopBack Documentation](https://loopback.io/doc/en/lb4/index.html) OpenAPI, ES2017, TypeScript

[Using three of the top NodeJS Web REST API Frameworks](https://medium.com/swlh/using-three-of-the-top-nodejs-web-rest-api-frameworks-d1d6dac021ee)

### NestJS

[NestJS - A progressive Node.js web framework](https://nestjs.com/) Wrapper of Express/Fastify
[Documentation | NestJS - A progressive Node.js framework](https://docs.nestjs.com/)

[Nestjs🐺⚡ | The framework of Nodejs Series' Articles - DEV Community](https://dev.to/krtirtho/series/14048)

### Fastify

> fast API server, JSON schema for validation

[Fastify, Fast and low overhead web framework, for Node.js](https://www.fastify.io/)

[fastify/Getting-Started.md · fastify/fastify](https://github.com/fastify/fastify/blob/HEAD/docs/Getting-Started.md)
[fastify/fastify-sensible: Defaults for Fastify that everyone can agree on](https://github.com/fastify/fastify-sensible)

[fastify/fastify-cli: Run a Fastify application with one command!](https://github.com/fastify/fastify-cli)
[fastify/create-fastify: Rapidly generate a Fastify project](https://github.com/fastify/create-fastify)
[fastify/fastify-env: Fastify plugin to check environment variables](https://github.com/fastify/fastify-env)
[fastify/fastify-helmet: Important security headers for Fastify](https://github.com/fastify/fastify-helmet)
[fastify/fastify-error](https://github.com/fastify/fastify-error)
[fastify/fastify-routes: Decorates fastify instance with a map of routes](https://github.com/fastify/fastify-routes)

[fastify/fastify-websocket: basic websocket support for fastify](https://github.com/fastify/fastify-websocket)
[fastify/fastify-multipart: Multipart support for Fastify](https://github.com/fastify/fastify-multipart)
[fastify/fastify-formbody: A Fastify plugin to parse x-www-form-urlencoded bodies](https://github.com/fastify/fastify-formbody)
[fastify/fastify-rate-limit: A low overhead rate limiter for your routes](https://github.com/fastify/fastify-rate-limit)
[fastify/fastify-cors: Fastify CORS](https://github.com/fastify/fastify-cors)

[fastify/fastify-static: Plugin for serving static file as fast as possible](https://github.com/fastify/fastify-static)
[fastify/fastify-etag: Automatically generate etags for HTTP responses, for Fastify](https://github.com/fastify/fastify-etag)
[fastify/point-of-view: Template rendering plugin for Fastify](https://github.com/fastify/point-of-view)
[fastify/fastify-response-validation: A simple plugin that enables response validation for Fastify.](https://github.com/fastify/fastify-response-validation)
[fastify/fastify-compress: Fastify compression utils](https://github.com/fastify/fastify-compress)

[fastify/fastify-auth: Run multiple auth functions in Fastify](https://github.com/fastify/fastify-auth)
[fastify/fastify-jwt: JWT utils for Fastify](https://github.com/fastify/fastify-jwt)
[fastify/fastify-bearer-auth: A Fastify plugin to require bearer Authorization headers](https://github.com/fastify/fastify-bearer-auth)

[fastify/fastify-plugin: Plugin helper for Fastify](https://github.com/fastify/fastify-plugin)
[fastify/skeleton: Template repository to create standardized Fastify plugins.](https://github.com/fastify/skeleton)

### AdonisJs

[AdonisJs - Node.js web framework](https://adonisjs.com/)

[AdonisJS Framework](https://github.com/adonisjs)

### FeathersJS

> worth looking

[Feathers | A framework for real-time applications and REST APIs | FeathersJS](https://docs.feathersjs.com/)
[The Feathers Flightpath](https://blog.feathersjs.com/)
[Why we built the best web framework you’ve probably never heard of (until now).](https://blog.feathersjs.com/why-we-built-the-best-web-framework-you-ve-probably-never-heard-of-until-now-176afc5c6aac)
[Introducing Feathers 4: A framework for real-time apps and REST APIs](https://blog.feathersjs.com/introducing-feathers-4-a-framework-for-real-time-apps-and-rest-apis-afff3819055b)
[Building lightning-fast APIs with FeatherJS - LogRocket Blog](https://blog.logrocket.com/building-lightning-fast-apis-with-featherjs/)

[FeathersJS Channel Subscriptions - The Feathers Flightpath](https://blog.feathersjs.com/feathersjs-channel-subscriptions-647c771ca6c8) multiple chatroom

[feathersjs/awesome-feathersjs: A list of awesome things related to FeathersJS](https://github.com/feathersjs/awesome-feathersjs)
[FeathersJS - YouTube](https://www.youtube.com/playlist?list=PLwSdIiqnDlf_lb5y1liQK2OW5daXYgKOe)

## Fullstack frameworks

### RedwoodJS

[RedwoodJS - Bringing Full-stack to the JAMstack](https://redwoodjs.com/) GraphQL + React
[redwoodjs/redwood: Bringing full-stack to the JAMstack.](https://github.com/redwoodjs/redwood)

### Hasura

[Build fullstack applications quickly | Hasura](https://hasura.io/)
[Tutorials – Hasura](https://blog.hasura.io/tutorials/home)
[How Hasura works (in doodles) – Hasura](https://blog.hasura.io/how-hasura-works-in-doodles-ba03d6ce6044)

[Tutorial: Leveraging Hasura, GraphQL and Apollo to build and deploy a fullstack react app](https://blog.hasura.io/tutorial-leveraging-hasura-graphql-and-apollo-to-build-and-deploy-a-fullstack-react-app-bafa32724010)

### Blitz.js

> build on to of Next.js, with Prisma powered backend

[Blitz.js - The Fullstack React Framework](https://blitzjs.com/)
[blitz-js/blitz: ⚡️The Fullstack React Framework — built on Next.js](https://github.com/blitz-js/blitz)

[Get Started with Blitz](https://blitzjs.com/docs/get-started)
[Why use Blitz instead of Next.js?](https://blitzjs.com/docs/why-blitz)
[Complete Intro to Blitz.js (Beta Preview, Jan 31, 2021) - YouTube](https://www.youtube.com/watch?v=UHyx8MtCVVk)

[Introduction to Blitz.js. Yet another framework on the block. It… | by Chidume Nnamdi 🔥💻🎵🎮 | Bits and Pieces](https://blog.bitsrc.io/introduction-to-blitz-js-ff1e48ea5714)
[Getting Started with Blitz.js | egghead.io](https://egghead.io/courses/getting-started-with-blitz-js-0585)

### Appwrite

[Appwrite - Open-Source End-to-End Backend Server](https://appwrite.io/)
[Authentication - Exploring Appwrite.io with React Series - DEV Community](https://dev.to/daryllukas/authentication-exploring-appwrite-io-with-react-series-1iec)

## Database/ORM

[Why you should avoid ORMs (with examples in Node.js)](https://blog.logrocket.com/why-you-should-avoid-orms-with-examples-in-node-js-e0baab73fa5)
Low level: Database Driver
Middle Level: Query Builder
High Level: ORM

[Top 11 Node.js ORMs, Query Builders & Database Libraries in 2021](https://www.prisma.io/dataguide/database-tools/top-nodejs-orms-query-builders-and-database-libraries)
[Which JavaScript ORM should you be using in 2018? – freeCodeCamp.org](https://medium.freecodecamp.org/a-comparison-of-the-top-orms-for-2018-19c4feeaa5f)
[From TypeORM to LoopBack: A Retrospective – Hacker Noon](https://hackernoon.com/from-typeorm-to-loopback-a-retrospective-188ea18527a2)

[Schniz/cuery: A composable SQL query builder using template literals](https://github.com/Schniz/cuery)
[Sequelize | The Node.js / io.js ORM for PostgreSQL, MySQL, SQLite and MSSQL](https://sequelize.readthedocs.io/)

[Knex.js - A SQL Query Builder for Javascript](http://knexjs.org/)
[Bookshelf.js](http://bookshelfjs.org/)
[Objection.js](https://vincit.github.io/objection.js/)

[typeorm/typeorm: ORM for TypeScript and JavaScript (ES7, ES6, ES5). Supports MySQL, PostgreSQL, MariaDB, SQLite, MS SQL Server, Oracle, WebSQL databases. Works in NodeJS, Browser, Ionic, Cordova and Electron platforms.](https://github.com/typeorm/typeorm)

### Prisma

> v2 is a query builder instead of a GraphQL wrapper

[Prisma - Database tools for modern application development](https://www.prisma.io/)
[Prisma Documentation | Concepts, Guides, and Reference](https://www.prisma.io/docs/)
[Getting started | Prisma Docs](https://www.prisma.io/docs/getting-started)
[Prisma](https://github.com/prisma?type=source) GitHub org
[Relation queries (Concepts) | Prisma Docs](https://www.prisma.io/docs/concepts/components/prisma-client/relation-queries)

[How Prisma and GraphQL fit together | Prisma](https://www.prisma.io/blog/prisma-and-graphql-mfl5y2r7t49c/) role changes of Prisma
[Prisma – The Complete ORM for Node.js & TypeScript](https://www.prisma.io/blog/prisma-the-complete-orm-inw24qjeawmb)
[Prisma 2 (Node JS ORM) Crash Course - 2021 - YouTube](https://www.youtube.com/watch?v=mU8-nKwfw4Y)

[prisma/prisma-examples: 🚀 Ready-to-run Prisma example projects](https://github.com/prisma/prisma-examples) many GraphQL examples

[Building a Habit Tracker with Prisma 2, Chakra UI, and React — SitePoint](https://www.sitepoint.com/habit-tracker-prisma-2-chakra-ui-react/)
[Filtering with GraphQL and Prisma: What NOT to do - DEV Community 👩‍💻👨‍💻](https://dev.to/yaariii3/filtering-with-graphql-and-prisma-what-not-to-do-38fk)

[TypeScript, PostgreSQL, Prisma | Data Modeling, CRUD, Aggregates](https://www.prisma.io/blog/backend-prisma-typescript-orm-with-postgresql-data-modeling-tsjs1ps7kip1)
[TypeScript, PostgreSQL, Prisma Backend | REST API, Validation, Testing](https://www.prisma.io/blog/backend-prisma-typescript-orm-with-postgresql-rest-api-validation-dcba1ps7kip3)
[TypeScript, PostgreSQL, Prisma Backend | Authentication, Authorization](https://www.prisma.io/blog/backend-prisma-typescript-orm-with-postgresql-auth-mngp1ps7kip4)
[TypeScript, PostgreSQL, Prisma | Continuous Integration & Deployment](https://www.prisma.io/blog/backend-prisma-typescript-orm-with-postgresql-deployment-bbba1ps7kip5)

[The Changelog #297: Prisma and the GraphQL data layer with Johannes Schickling | News and podcasts for developers | Changelog](https://changelog.com/podcast/297)
[Prisma: Modern Database Tooling with Johannes Schickling - Software Engineering Daily](https://softwareengineeringdaily.com/2020/06/04/prisma-modern-database-tooling-with-johannes-schickling/)

#### Schema

[Prisma schema (Reference) | Prisma Docs](https://www.prisma.io/docs/concepts/components/prisma-schema)
[Prisma schema API (Reference) | Prisma Docs](https://www.prisma.io/docs/reference/api-reference/prisma-schema-reference)

[Schema design // How to handle polymorphism? · Discussion #3668 · prisma/prisma](https://github.com/prisma/prisma/discussions/3668)
[Support for a Union type · Issue #2505 · prisma/prisma](https://github.com/prisma/prisma/issues/2505)
