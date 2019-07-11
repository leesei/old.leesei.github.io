---
title: Lua
categories:
  - comp.lang
tags:
  - lua
toc: true
date: 2016-03-22 10:48:31
---

# Lua

[Lua (programming language) - Wikiwand](https://www.wikiwand.com/en/Lua_(programming_language%29)

[The Programming Language Lua](http://www.lua.org/)
[Lua: demo](http://www.lua.org/demo.html)
[Lua: documentation](http://www.lua.org/docs.html)
[Lua 5.1 Reference Manual](http://www.lua.org/manual/5.1/manual.html)

[Lua (programming language) - Wikiwand](https://www.wikiwand.com/en/Lua_%28programming_language%29)
[lua-users wiki: Home Page](http://lua-users.org/wiki/)
[Lua - Wikiversity](https://en.wikiversity.org/wiki/Lua)
[Lua Unofficial FAQ (uFAQ)](http://www.luafaq.org/)

[Lua Short Reference](http://lua-users.org/files/wiki_insecure/users/thomasl/luarefv51single.pdf) (PDF)

[Lua简明教程 | | 酷 壳 - CoolShell](https://coolshell.cn/articles/10739.html)

[Metalua](http://metalua.luaforge.net/)

[Lua: Good, bad, and ugly parts - ZeroBrane](http://notebook.kulchenko.com/programming/lua-good-different-bad-and-ugly-parts)

## Tutorials

[Fun with Lua](http://www.fredshack.com/docs/lua.html)
[Lua: the world's most infuriating language](http://www.slideshare.net/jgrahamc/lua-the-worlds-most-infuriating-language)
[Learn Lua in 15 Minutes](http://tylerneylon.com/a/learn-lua/)
[Learn Lua in 15 minutes | Corona Labs](https://coronalabs.com/learn-lua/)
[Programming in Lua (1st Edition)](http://www.lua.org/pil/contents.html) for Lua 5.0; 2nd Edition for 5.1; 3rd Edition for 5.2

[LewisJEllis/awesome-lua: A curated list of quality Lua packages and resources.](https://github.com/LewisJEllis/awesome-lua)
[mysandbox/lua at master · arch-jslin/mysandbox](https://github.com/arch-jslin/mysandbox/tree/master/lua)

[Intro to Programming in Lua - YouTube](https://www.youtube.com/playlist?list=PLz-rYTT-2nIvtosMFa-OVURa5J9fAgtNU)
[Learning Lua - YouTube](https://www.youtube.com/playlist?list=PLxgtJR7f0RBKGid7F2dfv7qc-xWwSee2O)

### Leafo

He's the one behind LuaRocks, MoonScript, Lapis.

[leafo's Guides](http://leafo.net/guides.html)
[Using PostgreSQL with OpenResty](http://leafo.net/guides/using-postgres-with-openresty.html) [leafo/pgmoon: A pure Lua Postgres driver for use in OpenResty & more](https://github.com/leafo/pgmoon)
[An introduction to Parsing Expression Grammars with LPeg](http://leafo.net/guides/parsing-expression-grammars.html) lpeg

## LuaJIT

LuaJIT is faster then v8. However it conforms only to [Lua 5.1](http://www.lua.org/versions.html#5.1) spec (not the latest) and its [standard library](http://www.lua.org/manual/5.1/manual.html#5), supports some Lua 5.2 features as [extensions](http://luajit.org/extensions.html#lua52). Support for Lua 5.2 and 5.3 is a huge task.

> For those that think that LuaJIT's 5.1 compatibility isn't too far behind 5.3, be aware that Lua changes a lot in its minor versions.
> To give you an idea, 5.2 introduced changed how scope works (both some stuff with lexical/global scope, and by redoing environments), introduced the `goto` statement, finalisers, and changed how `break` works.
> 5.3 introduced integers (Lua was previously like Javascript with only one Number type which was backed by a `double`), and utf8 support.
> This means that upgrading a Lua version can be a big deal and break all of the programs written in it. For instance, redis and WoW both still embed 5.1.

[The LuaJIT Project](http://luajit.org/)
[mkottman/AndroLua](https://github.com/mkottman/AndroLua)
[luapower - The LuaJIT distribution for Windows, Linux and OS X](https://luapower.com/)
[malkia/ufo: Portable distribution of LuaJIT with precompiled binaries, libraries and FFI bindings](https://github.com/malkia/ufo)

[bobsayshilol/luajit-decomp: LuaJIT decompiler](https://github.com/bobsayshilol/luajit-decomp)

[Embedding LuaJIT in 30 minutes (or so) | The CZ.NIC Staff Blog](https://en.blog.nic.cz/2015/08/12/embedding-luajit-in-30-minutes-or-so/)

## MoonScript

[MoonScript, a language that compiles to Lua](http://moonscript.org/)
[MoonScript Online Compiler](http://moonscript.org/compiler/)
[Language Guide - MoonScript 0.4.0](http://moonscript.org/reference/)

### Overview of Differences & Highlights

* Whitespace sensitive blocks defined by indenting
* All variable declarations are local by default
* `export` keyword to declare global variables, `import` keyword to make local
copies of values from a table
* Parentheses are optional for function calls, similar to Ruby
* Fat arrow, `=>`, can be used to create a function with a self argument
* `@` can be prefixed in front of a name to refer to that name in `self`
* `!` operator can be used to call a function with no arguments
* Implicit return on functions based on the type of last statement
* `:` is used to separate key and value in table literals instead of `=`
* Newlines can be used as table literal entry delimiters in addition to `,`
* \\ is used to call a method on an object instead of `:`
* `+=`, `-=`, `/=`, `*=`, `%=`, `..=` operators
* `!=` is an alias for `~=`
* Table comprehensions, with convenient slicing and iterator syntax
* Lines can be decorated with for loops and if statements at the end of the line
* If statements can be used as expressions
* Class system with inheritance based on metatable's `__index` property
* Constructor arguments can begin with `@` to cause them to automatically be
assigned to the object
* Magic `super` function which maps to super class method of same name in a
class method
* `with` statement lets you access anonymous object with short syntax

[An in-depth look into the MoonScript class implementation](http://leafo.net/guides/moonscript-classes.html)

## eLua

[eLua - eluaproject](http://www.eluaproject.net/) for micro-controllers
[eLua Project](https://github.com/elua) on GitHub

## Tools

> how to create executables (without lua dependency)? 
> Luarock's build system (rockspec)?

[amalg.lua](http://siffiejoe.github.io/lua-amalg/) dependency bundler
[Squish [Matthew Wild]](http://matthewwild.co.uk/projects/squish/home) dependency bundler, minifier and compiler
[lua-users wiki: Bin To Cee](http://lua-users.org/wiki/BinToCee)
[L-Bia Home](http://l-bia.sourceforge.net/) but it says it doesn't do that
[stevedonovan/luabuild: A highly customizable Lua 5.2 build system, allowing for common external modules to be linked in statically, and built-in modules to be excluded](https://github.com/stevedonovan/luabuild) http://lua-users.org/lists/lua-l/2012-04/msg00639.html

[Luiz Henrique de Figueiredo: Libraries and tools for Lua](http://webserver2.tecgraf.puc-rio.br/~lhf/ftp/lua/) !important
example of distributed Lua tools, srlua
[Lua Toolbox](https://lua-toolbox.com/)
[leafo/moonscrape: web scraper](https://github.com/leafo/moonscrape)

## Embedding Lua

Lua itself is designed to be an "embedded language". Embedding the Lua Runtime to a C program is one of it's use case.

It is used in VLC, Adode Photoshop Lightroom, World of Warcraft, AwesomeWM
[A stripped console-only Lua CLI for use with shell scripts - The VideoLAN Forums](https://forum.videolan.org/viewtopic.php?t=124590)

### Nginx

> see [nginx.md#openresty]

Lua + Nginx = magic

## Bindings

LuaJIT provides an easy(-er) to use Foreign Function Interface.
[FFI Tutorial](http://luajit.org/ext_ffi_tutorial.html)
[Introduction to LuaJIT & How to bind CPP code base using LuaJIT FFI // Speaker Deck](https://speakerdeck.com/igdshare/introduction-to-luajit-how-to-bind-cpp-code-base-using-luajit-ffi)

FFI is also backported to Lua.
[jmckaskill/luaffi: Standalone FFI library for calling C functions from lua. Compatible with the luajit FFI interface.](https://github.com/jmckaskill/luaffi)

[kyren/rlua: High level Lua bindings to Rust](https://github.com/kyren/rlua)

## IDE

[ZeroBrane Studio - Lua IDE/editor/debugger for Windows, Mac OSX, and Linux](https://studio.zerobrane.com/)

## LuaRocks

[LuaRocks - The Lua package manager](https://luarocks.org/)
[luarocks documentation](http://stevedonovan.github.io/luarocks/) (API)
[Documentation · keplerproject/luarocks Wiki](https://github.com/keplerproject/luarocks/wiki/Documentation)
[Using LuaRocks · keplerproject/luarocks Wiki](https://github.com/keplerproject/luarocks/wiki/Using-LuaRocks)
`~/.luarocks/config.<version>`

LuaRocks is implemented upon Lua's [package](https://www.lua.org/manual/5.3/manual.html#6.3) and [require](https://www.lua.org/pil/8.1.html) mechanism.

### paths

[Using LuaRocks to install packages in the current directory](http://leafo.net/guides/customizing-the-luarocks-tree.html)
Rocks are installed to:
- `/usr/share/lua/<version>/` (system rock tree)
- `~/.luarocks` with `--local`
  Adding LuaRocks' `LUA_PATH` and `LUA_CPATH` to your environment:
```sh
eval $(luarocks path --bin)
lua -e 'print(package.path)'
lua -e 'print(package.cpath)'
```
  Add this to `~/.luarocks/config.lua` to make this the default:
  `local_by_default=true`
- custom rock tree with `--tree ./lua_modules` to install to local folder
```lua
-- modules_path.lua
local version = _VERSION:match("%d+%.%d+")
package.path = 'lua_modules/share/lua/' .. version .. '/?.lua;lua_modules/share/lua/' .. version .. '/?/init.lua' .. package.path
package.cpath = 'lua_modules/lib/lua/' .. version .. '/?.so' .. package.path
```
  the question mark is used to interpolate the package name
  mimic `$(luarocks path)`

### Rocks

A rock is a zip file containing the rockspec and all files needed to install the module.
Each version of a rock get its own `.rockspec`.
A `.rockspec` may build multiple rocks.

[About - LuaRocks](https://luarocks.org/about)

## Packages

[Penlight](http://stevedonovan.github.io/Penlight/api/manual/01-introduction.md.html) Lua's battery
[torch/paths](https://github.com/torch/paths)
[leafo/etlua: Embedded Lua templates](https://github.com/leafo/etlua)
[leafo/loadkit: Loadkit allows you to load arbitrary files within the Lua package path](https://github.com/leafo/loadkit)
[hishamhm/f-strings: String interpolation for Lua](https://github.com/hishamhm/f-strings)
[dkjson - dkjson](http://dkolf.de/src/dkjson-lua.fsl/home)
[pkulchenko/serpent: Lua serializer and pretty printer](https://github.com/pkulchenko/serpent)
[LDoc documentation](http://stevedonovan.github.io/ldoc/)

[mpeterv/luacheck: A tool for linting and static analysis of Lua code.](https://github.com/mpeterv/luacheck)

### Concurrency

[Re: Question about multi-threading in Lua](http://lua-users.org/lists/lua-l/2008-05/msg00490.html)
[What multithreading package for Lua "just works" as shipped? - Stack Overflow](http://stackoverflow.com/questions/5689548/what-multithreading-package-for-lua-just-works-as-shipped)
[Lua Coroutine Roundup | William A Adams](https://williamaadams.wordpress.com/2014/01/03/lua-coroutine-roundup/)

### CLI

[Argparse: Feature-rich command line parser for Lua](http://argparse.readthedocs.io/en/stable/) [source](https://github.com/mpeterv/argparse)
[luaposix/luaposix: Lua bindings for POSIX APIs](https://github.com/luaposix/luaposix/)

### Testing

[busted : Elegant Lua unit testing, by Olivine-Labs](http://olivinelabs.com/busted/) [source](https://github.com/Olivine-Labs/busted)
[LuaCov - Coverage analysis for Lua scripts](http://keplerproject.github.io/luacov/)
