---
title: "Gradle"
categories:
  - comp.lang
toc: true
date: 2019-04-04 12:18:07
tags:
  - gradle
---

[Gradle: Build Automation for the JVM, Android, and C/C++](https://gradle.org/)
[Gradle | Gradle Features](https://gradle.org/features/)

[Command-Line Interface](https://docs.gradle.org/current/userguide/command_line_interface.html)

```sh
# info and debug log
gradle -i task
gradle -d task

# show project properties
gradle properties
```

[Gradle Release Notes](https://docs.gradle.org/current/release-notes)
[Gradle User Guide](https://docs.gradle.org/current/userguide/userguide.html)
[Gradle | Gradle Tutorials and Guides](https://gradle.org/guides/)
[Gradle User Guide 中文版](http://dongchuan.gitbooks.io/gradle-user-guide-/content/) of older version

[An introduction to Gradle for complete beginners - Android Authority](https://www.androidauthority.com/introduction-to-gradle-991743/)
[Building C++ applications and libraries](https://docs.gradle.org/current/userguide/cpp_plugins.html)
[Building Java & JVM projects](https://docs.gradle.org/current/userguide/building_java_projects.html)

[Gradle in 60 Seconds](https://code.tutsplus.com/tutorials/gradle-in-60-seconds--cms-25296)
[Using Gradle Build Variants - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/using-gradle-build-variants--cms-25005)
[The Ins and Outs of Gradle](https://code.tutsplus.com/tutorials/the-ins-and-outs-of-gradle--cms-22978)

[Trainings | Gradle Enterprise](https://gradle.com/training/)
[Blog | Gradle Enterprise](https://gradle.com/blog/)
[Dependency Management with Gradle Part 1 - Fundamentals | Gradle Enterprise](https://gradle.com/blog/dependency-management-with-gradle-fundamentals/)
[Build Best Practicess | Gradle Enterprise](https://gradle.com/blog/category/build-best-practices/)
[Build performances | Gradle Enterprise](https://gradle.com/blog/category/build-performance/)

[CircleCI cache key over many files – Chris Banes – Medium](https://medium.com/@chrisbanes/circleci-cache-key-over-many-files-c9e07f4d471a)

## DSL

[Gradle DSL Version](https://docs.gradle.org/current/dsl/index.html)

[The Power of Gradle Kotlin DSL - Kotlin Expertise Blog](https://kotlinexpertise.com/gradlekotlindsl/)
[Gradle Kotlin DSL Primer](https://docs.gradle.org/current/userguide/kotlin_dsl.html)
[A Groovy Build Script Primer](https://docs.gradle.org/current/userguide/groovy_build_script_primer.html)

[Gradle Kotlin DSL 1.0](https://blog.gradle.org/kotlin-dsl-1.0)
[The Road to Gradle Script Kotlin 1.0](https://blog.gradle.org/kotlin-scripting-update)
[Kotlin Meets Gradle](https://blog.gradle.org/kotlin-meets-gradle)
[gradle/kotlin-dsl: Kotlin language support for Gradle build scripts](https://github.com/gradle/kotlin-dsl)

[The Power of Gradle Kotlin DSL - Kotlin Expertise Blog](https://kotlinexpertise.com/gradlekotlindsl/)
[Migrating build logic from Groovy to Kotlin](https://guides.gradle.org/migrating-build-logic-from-groovy-to-kotlin/)
[Migrating Android build scripts from Groovy to Kotlin DSL](https://proandroiddev.com/migrating-android-build-scripts-from-groovy-to-kotlin-dsl-f8db79dd6737)

### Anti-pattern

```kts
// don't use this
apply plugin: 'kotlin'

// use this
plugins {
    kotlin("jvm") version "1.3.21"
}
```

### Examples

[gradle/subprojects/docs/src/samples at master · gradle/gradle](https://github.com/gradle/gradle/tree/master/subprojects/docs/src/samples)
[kotlin-dsl/samples at master · gradle/kotlin-dsl](https://github.com/gradle/kotlin-dsl/tree/master/samples)

[JetBrains/kotlin: The Kotlin Programming Language](https://github.com/JetBrains/kotlin) Kotlin project uses Kotlin DSL

### Groovy vs Kotlin

I prefer Kotlin over Groovy:

- Kotlin is more modern, has more potential and more worthy to learn than Groovy
- Parentheses for function invocation is optional in Groovy, making it even harder to distingush between setting field or calling function

```groovy
repositories {
    jcenter()
}

configurations {
    ktlint
}

dependencies {
    ktlint "com.github.shyiko:ktlint:0.29.0"
}

task ktlint(type: JavaExec, group: "verification") {
    description = "Check Kotlin code style."
    classpath = configurations.ktlint
    main = "com.github.shyiko.ktlint.Main"
    args "src/**/*.kt"
}

task ktlintFormat(type: JavaExec, group: "formatting") {
    description = "Fix Kotlin code style deviations."
    classpath = configurations.ktlint
    main = "com.github.shyiko.ktlint.Main"
    args "-F", "src/**/*.kt"
}
```

```groovy
allprojects {
    apply from: "$rootDir/ktlint.gradle"
}
```

## Plugins

[Gradle - Plugins](https://plugins.gradle.org/)

## Wrapper

[The Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html)

A local copy of Gradle can be downloaded in `./gradle/`, a wrapper `gradlew` will be created. This allows for version controlling Gradle tool and self-contained build environment.

```sh
# with gradle installed on host
gradle init --dsl kotlin
gradle wraper --gradle-version=5.3.1
```

```sh
# even better using gradle Docker image
docker run --rm -u $(id -u):$(id -g) \
   -v "$PWD":/home/gradle/project -w /home/gradle/project \
   gradle gradle init --dsl kotlin
docker run --rm -u $(id -u):$(id -g) \
   -v "$PWD":/home/gradle/project -w /home/gradle/project \
   gradle gradle wrapper --gradle-version=5.3.1
```

[gradle - Docker Hub](https://hub.docker.com/_/gradle)

## Lifecycle

[Build Lifecycle](https://docs.gradle.org/current/userguide/build_lifecycle.html)
[Understanding Gradle: the Build Lifecycle – ProAndroidDev](https://proandroiddev.com/understanding-gradle-the-build-lifecycle-5118c1da613f)
[Cédric Champeau's blog: Gradle myth busting: lifecycle](http://melix.github.io/blog/2018/09/gradle-lifecycle.html)

## Tasks

```sh
# show tasks
gradle tasks
# also show tasks not in task group
gradle tasks --all

# filter by task group
gradle tasks --group="build setup"

# show details of task
gradle -q help --task <task>

# upload build scan to https://scans.gradle.com/
# https://gradle.com/build-scans/
gradle --scan <task>
```

## Milti project

```sh
# list sub-projects, displayed in a hierarchy
gradle projects
```

## Docker plugins

[palantir/gradle-docker: a Gradle plugin for orchestrating docker builds and pushes.](https://github.com/palantir/gradle-docker)
[Gradle Docker Plugin User Guide & Examples](https://bmuschko.github.io/gradle-docker-plugin/)
[bmuschko/gradle-docker-plugin: Gradle plugin for managing Docker images and containers.](https://github.com/bmuschko/gradle-docker-plugin)
[avast/gradle-docker-compose-plugin: Simplifies usage of Docker Compose for integration testing in Gradle environment.](https://github.com/avast/gradle-docker-compose-plugin)

## Comparison

[Gradle vs Maven Comparison](https://gradle.org/maven-vs-gradle/)
[Gradle vs. Maven - DZone Java](https://dzone.com/articles/gradle-vs-maven)
[Java Build Tools: Ant vs Maven vs Gradle | Technology Conversations](http://technologyconversations.com/2014/06/18/build-tools/)

## Android adoption

[New Build System - Android Tools Project Site](http://tools.android.com/tech-docs/new-build-system)
[Build System Overview | Android Developers](https://developer.android.com/sdk/installing/studio-build.html)
