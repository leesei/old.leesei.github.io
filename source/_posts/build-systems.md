---
title: "Build Systems"
categories:
  - comp.lang
toc: true
date: 2015-06-11 15:54:07
tags:
  - make
  - buck
  - meson
  - lake
  - gradle
  - bazel
  - gyn
  - gn
---

[Build Tools: Make, Rake, Ant, Sbt - Hyperpolyglot](http://hyperpolyglot.org/build)
[The 13 Things That Make a Good Build System | SignalFx](https://www.signalfx.com/blog/the-13-things-that-make-a-good-build-system/)

<!-- more -->

## GNU Make

[Make - GNU Project - Free Software Foundation](http://www.gnu.org/software/make/)
[GNU make](https://www.gnu.org/software/make/manual/make.html)
[跟我一起写 Makefile](https://seisman.github.io/how-to-write-makefile/) [source](https://github.com/seisman/how-to-write-makefile)
[Makefile Tutorial by Example](http://makefiletutorial.com/)
[Linux Fu: The Great Power Of Make | Hackaday](https://hackaday.com/2018/06/22/linux-fu-the-great-power-of-make/)

[The joy of make at jsconfeu](http://codeofrob.com/entries/the-joy-of-make-at-jsconfeu.html)
[Practical Makefiles, by example](http://nuclear.mutantstargoat.com/articles/make/)
[Building Web Applications With Make – Smashing Magazine](http://www.smashingmagazine.com/2015/10/building-web-applications-with-make/)
[Building JavaScript projects with Make – The If Works](https://blog.jcoglan.com/2014/02/05/building-javascript-projects-with-make/)
[Makefiles – Mrbook's Stuff](http://mrbook.org/blog/tutorials/make/)
[The Lost Art of the Makefile](https://www.olioapps.com/blog/the-lost-art-of-the-makefile/)
[Makefile instead of hoop jumping](https://remysharp.com/2014/12/02/makefile) [gist](https://gist.github.com/remy/274232f8b47dfa163324)

[Creating configuration scripts and Makefiles using autoconf & automake](http://www.ifnamemain.com/posts/2014/Mar/13/autoconf_automake/)

[Jobserver Implementation | GNU make](http://make.mad-scientist.net/papers/jobserver-implementation/)

[GNU make: Automatic Variables](https://www.gnu.org/software/make/manual/html_node/Automatic-Variables.html)

```sh
# show rules
make -pn

# shows how make works
make --debug=v
```

### mmake

[Modernizing Make - TJ Holowaychuk - Medium](https://medium.com/@tjholowaychuk/modern-make-b55d53cf80d9)
[tj/mmake: Modern Make](https://github.com/tj/mmake)

### non-recursive make

[Recursive Make Considered Harmful](http://c2.com/cgi/wiki?RecursiveMakeConsideredHarmful)
[Recursive make Reloaded | Linux Magazine](http://www.linux-mag.com/id/2101/)
[Implementing non-recursive make](http://evbergen.home.xs4all.nl/nonrecursive-make.html)

I evaluated two implementations: [aostruszka/nonrec-make](https://github.com/aostruszka/nonrec-make/) and [dmoulding-boilermake · GitHub](https://github.com/dmoulding/boilermake) on these grounds:

- simple to modify and maintain
- fast to compile
- auto .h dependencies checking
  allows for external dependencies (support libraries built out of the build - system)
- separate storage for object code generated

`boilermake` is quite restrictive in that each .mk only supports one target, so a module could contain multiple `.mk` to build multiple libs and test app. To add a dependency, we need:

```make
TGT_PREREQS += lib/libfoo.a
TGT_LDLIBS  += -lfoo
```

`nonrec-make` is easier in including multiple sub-makefiles and supports expanding rule for source files (akin to \*.c). It also added support for [external build system](https://github.com/aostruszka/nonrec-make/commit/0aaae67b1c67aeef28e6ca3a692fc4619878ba23).

Examples:

- [GHC](https://ghc.haskell.org/trac/ghc/wiki/Building/Architecture/Idiom/NonRecursiveMake) (Haskell compiler)
- Android [1](http://www.netmite.com/android/mydroid/development/pdk/docs/build_system.html) [2](http://elinux.org/Android_Build_System) [3](http://www.programering.com/a/MDN5EDNwATM.html) [4](https://docs.google.com/document/d/1jDmWgVgorTY_njX68juH5vt0KY_FXWgxkxmi2v_W_a4/edit)

### CMake

[CMake](http://www.cmake.org/)
[CMake Tutorial — CMake Documentation](https://cmake.org/cmake/help/latest/guide/tutorial/index.html)
[CMake Reference Documentation — CMake Documentation](https://cmake.org/cmake/help/latest/)
[FAQ · Wiki · CMake / Community · GitLab](https://gitlab.kitware.com/cmake/community/-/wikis/FAQ)
[Home · Wiki · CMake / Community · GitLab](https://gitlab.kitware.com/cmake/community/-/wikis/home)

[Webinars | CMake](https://cmake.org/webinars/)
[Introduction to CMake on Vimeo](https://vimeo.com/32212195)
[How to CMake Good - Recommended Order - YouTube](https://www.youtube.com/playlist?list=PLK6MXr8gasrGmIiSuVQXpfFuE1uPT615s)
[Akagi201/learning-cmake: learning cmake](https://github.com/Akagi201/learning-cmake)

`ccmake` and the Windows CMake GUI will prompt for config

```sh
make VERBOSE=1
```

[Cross-Platform Software Development Using CMake | Linux Journal](https://www.linuxjournal.com/article/6700)
[unbornchikken-cmake-js · GitHub](https://github.com/unbornchikken/cmake-js)
[Learning CMake: A beginner's guide · GitBook](https://www.gitbook.com/book/tuannguyen68/learning-cmake-a-beginner-s-guide/details)
[The Architecture of Open Source Applications: CMake](http://aosabook.org/en/cmake.html)
[An Introduction to CMake](https://www.slideshare.net/ICSinc/an-introduction-to-cmake)
[CMake and FIND PACKAGE - Wiki for iCub and Friends](http://wiki.icub.org/wiki/CMake_and_FIND_PACKAGE)

[c++ - Debug vs Release in CMake - Stack Overflow](https://stackoverflow.com/questions/7724569/debug-vs-release-in-cmake)

```sh
mkdir Release
cd Release
cmake -DCMAKE_BUILD_TYPE=Release ..
make

mkdir Debug
cd Debug
cmake -DCMAKE_BUILD_TYPE=Debug ..
make
```

### `CMakeLists.txt`

[Examples | CMake](https://cmake.org/examples)
[VariablesListsStrings · Wiki · CMake / Community · GitLab](https://gitlab.kitware.com/cmake/community/-/wikis/doc/cmake/VariablesListsStrings)

[cmake-variables(7) — CMake Documentation](https://cmake.org/cmake/help/latest/manual/cmake-variables.7.html)
[cmake-properties(7) — CMake Documentation](https://cmake.org/cmake/help/latest/manual/cmake-properties.7.html)

`project(HELLO)` => `${HELLO_SOURCE_DIR}` and `${HELLO_BINARY_DIR}` available

## Buck

[Buck: A fast build tool](https://buckbuild.com/) by Facebook

[7 Reasons to Use Buck Build – Hacker Noon](https://hackernoon.com/7-reasons-to-use-buck-build-5b44d7413585)
[(Even) More Reasons to Use Buck Build – Hacker Noon](https://hackernoon.com/even-more-reasons-to-use-buck-build-9e2f6bf451d4)
[How to Create a Buck-based C/C++ Project – Hacker Noon](https://hackernoon.com/how-to-create-a-buck-based-c-c-project-38b85273d6a6)
[Generating a Single-Include C++ Header File Using Buck](https://hackernoon.com/generating-a-single-include-c-header-file-using-buck-827f20be3f9d)
[Lessons Learned from Porting 300 C/C++ Projects to Buck Build](https://hackernoon.com/lessons-learned-from-porting-300-projects-to-buck-build-ff6463b65142)

## BuildInfer

[BuildInfer — Next Generation C/C++ Build Acceleration](https://buildinfer.loopperfect.com/)
[Why Not Make? – Hacker Noon](https://hackernoon.com/why-not-make-db142ccb2081)

## Meson

[The Meson Build system](https://mesonbuild.com/)

## Lake

[Lake – a Lua-based Build Engine](http://stevedonovan.github.io/lake/topics/index.md.html)
[stevedonovan/Lake: A Lua-based Build Tool](https://github.com/stevedonovan/Lake)

## Gradle

> see `gradle.md`

## Node.js ecosystem

> see `build-systems-node-js.md`

## Bazel

[Bazel](http://bazel.build/), supported [languages](http://bazel.build/docs/build-encyclopedia.html#rules)

## gyp

gyp was the build system used by Chromium and Node.
But Chromium has since moved to GN.

[gyp-UserDocumentation.md](https://chromium.googlesource.com/external/gyp/+/HEAD/docs/UserDocumentation.md)
[Converting a C library to gyp — n8.io](https://n8.io/converting-a-c-library-to-gyp/)

## Ninja

[Ninja, a small build system with a focus on speed](https://ninja-build.org/)
[Using GN build - Google Slides](https://docs.google.com/presentation/d/15Zwb53JcncHfEwHpnG_PoIbbzQ3GQi_cpujYwbpcbZo/edit#slide=id.g119d702868_0_12)
[The Performance of Open Source Software | Ninja](https://aosabook.org/en/posa/ninja.html)
[Building Like (a) Ninja [Pt1]](https://vector-of-bool.github.io/2018/12/20/build-like-ninja-1.html)

[docs - gn - Git at Google](https://gn.googlesource.com/gn/+/master/docs/) GN is a meta-build system that generates build files for Ninja.

[saghul/gyn](https://github.com/saghul/gyn)

## Pants

[Pants Build](https://pantsbuild.github.io/)
Pants is a build system written by Twitter to build Python and Java codes.

[Getting Started with the Pants Build System - YouTube](https://www.youtube.com/playlist?list=PLDVc2EaAVPg8ACDeLfN2KWkPZi0Th5d04)

## Mule

[algorand/mule: General automation framework](https://github.com/algorand/mule/tree/develop)
[Automating with the Mule framework | by Brice Rising | Algorand | Medium](https://medium.com/algorand/automating-with-the-mule-framework-f9b34789920a)

## tup

[tup | Home](http://gittup.org/tup/)

## Buildout

[Buildout, an automation tool written in and extended with Python — Buildout documentation](http://docs.buildout.org/en/latest/)

## Waf

[Waf: the meta build system](https://waf.io/)
[The Waf Book](https://waf.io/book/)
[waf-project/waf: The Waf build system](https://github.com/waf-project/waf)

## Make-It-Quick (MIQ)

[c3d/make-it-quick: A simple auto-configuring make-only build system](https://github.com/c3d/make-it-quick)
