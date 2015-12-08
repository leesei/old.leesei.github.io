---
title: Build Systems
categories:
  - comp.lang
toc: true
date: 2015-06-11 15:54:07
tags:
- make
- gradle
- gulp
- bazel
- gyn
- gn
---

## GNU Make

[Make - GNU Project - Free Software Foundation](http://www.gnu.org/software/make/)
[GNU make](http://www.gnu.org/software/make/manual/make.html)
[The joy of make at jsconfeu](http://codeofrob.com/entries/the-joy-of-make-at-jsconfeu.html)
[Building Web Applications With Make – Smashing Magazine](http://www.smashingmagazine.com/2015/10/building-web-applications-with-make/)

### non-recursive make

[Recursive Make Considered Harmful](http://c2.com/cgi/wiki?RecursiveMakeConsideredHarmful)
[Recursive make Reloaded | Linux Magazine](http://www.linux-mag.com/id/2101/)
[Implementing non-recursive make](http://evbergen.home.xs4all.nl/nonrecursive-make.html)
[dmoulding-boilermake · GitHub](https://github.com/dmoulding/boilermake)
[aostruszka/nonrec-make](https://github.com/aostruszka/nonrec-make/)

Examples:
- [GHC](https://ghc.haskell.org/trac/ghc/wiki/Building/Architecture/Idiom/NonRecursiveMake) (Haskell compiler)
- Android [1](http://www.netmite.com/android/mydroid/development/pdk/docs/build_system.html) [2](http://elinux.org/Android_Build_System) [3](http://www.programering.com/a/MDN5EDNwATM.html) [4](https://docs.google.com/document/d/1jDmWgVgorTY_njX68juH5vt0KY_FXWgxkxmi2v_W_a4/edit)

[CMake](http://www.cmake.org/)
[unbornchikken-cmake-js · GitHub](https://github.com/unbornchikken/cmake-js)
[Learning CMake: A beginner's guide](http://tuannguyen68.gitbooks.io/learning-cmake-a-beginner-s-guide/content/)

## Gradle

[Gradle: Build Automation for the JVM, Android, and C/C++](https://gradle.org/)
[Gradle 2.4 Release Notes](https://docs.gradle.org/current/release-notes)
[Gradle User Guide](https://docs.gradle.org/current/userguide/userguide.html)
[Gradle User Guide 中文版](http://dongchuan.gitbooks.io/gradle-user-guide-/content/)

[Getting Started - Native (C/C++) - Gradle](https://gradle.org/getting-started-native/)
[Getting Started - Java / JVM - Gradle](https://gradle.org/getting-started-jvm/)
[Getting Started - Android - Gradle](https://gradle.org/getting-started-android/)

[Using Gradle Build Variants - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/using-gradle-build-variants--cms-25005)

### Android adoption

[The Ins and Outs of Gradle - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/the-ins-and-outs-of-gradle--cms-22978)
[New Build System - Android Tools Project Site](http://tools.android.com/tech-docs/new-build-system)
[Build System Overview | Android Developers](https://developer.android.com/sdk/installing/studio-build.html)

## JavaScript

### Gulp

[Automate Your Tasks Easily with Gulp.js | Scotch](https://scotch.io/tutorials/automate-your-tasks-easily-with-gulp-js)
[Gulp Basics Course](http://teamtreehouse.com/library/gulp-basics)

### Brunch

[Brunch - ultra-fast HTML5 build tool](http://brunch.io/)
[brunch/brunch-guide](https://github.com/brunch/brunch-guide)

## Bazel

[Bazel](http://bazel.io/), supported [languages](http://bazel.io/docs/build-encyclopedia.html#rules)

## gyp

gyp was the build system used by Chromium and Node.
But Chromium has since moved to GN.

[gyp-UserDocumentation.md](https://chromium.googlesource.com/external/gyp/+/HEAD/docs/UserDocumentation.md)
[saghul-gyn · GitHub](https://github.com/saghul/gyn)

## Ninja

[What is GN?](https://chromium.googlesource.com/chromium/src/+/master/tools/gn/README.md)
[The Performance of Open Source Software | Ninja](http://aosabook.org/en/posa/ninja.html)
