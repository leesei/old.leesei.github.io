---
title: Kotlin
categories:
  - comp.lang
tags:
  - kotlin
toc: true
date: 2019-04-04 10:02:53
---

[Kotlin Programming Language](https://kotlinlang.org/)
[Kotlin (programming language) - Wikiwand](https://www.wikiwand.com/en/Kotlin_%28programming_language%29)
Statically typed programming language for the JVM, Android, the browser and native

[Kotlin 1.3.50 released | Kotlin Blog](https://blog.jetbrains.com/kotlin/2019/08/kotlin-1-3-50-released/)

[Kotlin Clean Architecture – ProAndroidDev](https://proandroiddev.com/kotlin-clean-architecture-1ad42fcd97fa)
[Kotlin, Android's new programming language - Things you need to know about it](https://www.readinbrief.com/kotlin/)
[Kt. Academy](https://blog.kotlin-academy.com/)

[Will everyone use Kotlin programming language instead of Java? - Quora](https://www.quora.com/Will-everyone-use-Kotlin-programming-language-instead-of-Java)
[Toppling the Giant: Kotlin vs. Java](https://blog.scottlogic.com/2019/04/29/kotlin-vs-java.html)
[Kotlin on the server at Khan Academy | Khan Academy Engineering](http://engineering.khanacademy.org/posts/kotlin-adoption.htm)
[What is Kotlin? The Java alternative explained | InfoWorld](https://www.infoworld.com/article/3224868/java/what-is-kotlin-the-java-alternative-explained.html)
[Kotlin tutorial: Get started with Kotlin | InfoWorld](https://www.infoworld.com/article/3281125/application-development/kotlin-tutorial-get-started-with-kotlin.html)
[Beyond Java: Programming languages on the JVM | InfoWorld](https://www.infoworld.com/article/3268484/java/beyond-java-programming-languages-on-the-jvm.html)
[8-Minute Crash Course on Kotlin Programming Language.](https://blog.kotlin-academy.com/8-minute-crash-course-on-kotlin-programming-language-e8a804ed3d8a)

[Kotlin vs Java The Whole Story | TechYourChanceTechYourChance](https://www.techyourchance.com/kotlin-vs-java-whole-story/)
[Kotlin - The Good, the Bad and the Ugly - DEV Community 👩‍💻👨‍💻](https://dev.to/martinhaeusler/kotlin---the-good-the-bad-and-the-ugly-3jfo)

## The Whys

[Why Learn Kotlin? [Infographic] - DZone Java](https://dzone.com/articles/why-learn-kotlin-infographic)
[Rise of Kotlin: The Programming Language for the Next Generation](https://hackernoon.com/rise-of-kotlin-the-programming-language-for-the-next-generation-27beeb529204)
[Why you should totally switch to Kotlin – Magnus Vinther – Medium](https://medium.com/@magnus.chatt/why-you-should-totally-switch-to-kotlin-c7bbde9e10d5)
[Why Kotlin is my next programming language – Mike Hearn – Medium](https://medium.com/@octskyward/why-kotlin-is-my-next-programming-language-c25c001e26e3)
[Why Kotlin? Eight features that could convince Java developers to switch | JavaWorld](https://www.javaworld.com/article/3396141/why-kotlin-eight-features-that-could-convince-java-developers-to-switch.html)

[Kotlin: A massive leap forward – ProAndroidDev](https://proandroiddev.com/kotlin-a-massive-leap-forward-78251531f616)
[Kotlin avoids entire categories of Java defects – ProAndroidDev](https://proandroiddev.com/kotlin-avoids-entire-categories-of-java-defects-89f160ba4671)
[Kotlin is not Android - Kt. Academy](https://blog.kotlin-academy.com/kotlin-is-not-android-c96984730c35)

## SDK

[Working with the Command Line Compiler - Kotlin Programming Language](https://kotlinlang.org/docs/tutorials/command-line.html)
`kotlinc` is also the REPL

```kotlin
fun main(args: Array<String>) {
    println("Hello, World!")
}
```

```sh
kotlinc hello.kt -include-runtime -d hello.jar

# invoke by class
java -jar hello.jar
# invoke by class, Kotlin source file name is used to generate CamelCase Java class name
java -classpath hello.jar HelloKt
```

Inspecting compiled code:

```sh
kotlinc hello.kt
javap -c HelloKt.class
```

### Kotlin Script

Kotlin can also be used to write script with `.kts` extension

[KEEP/scripting-support.md at master · Kotlin/KEEP](https://github.com/Kotlin/KEEP/blob/master/proposals/scripting-support.md)
[Kotlin for scripting - Programming Kotlin](https://subscription.packtpub.com/book/application_development/9781787126367/1/ch01lvl1sec10/kotlin-for-scripting)

```sh
# script
kotlinc -script script.kts arg1 arg2
```

```kotlin
// script.main.kts:
@file:Import("common.main.kts")
val bar = "bar with $foo"
```

[holgerbrandl/kscript: Scripting enhancements for Kotlin](https://github.com/holgerbrandl/kscript)

Scratches can be created in IntelliJ IDEA to show result of each statement (and in near-realtime in Interactive mode)
[Running Code Snippets - Kotlin Programming Language](https://kotlinlang.org/docs/tutorials/quick-run.html#scratches)

[Gradle Script Kotlin with Rodrigo Oliveira – Talking Kotlin](http://talkingkotlin.com/gradle-script-kotlin-with-rodrigo-oliveira/)

## Playground

[Kotlin Playground: Edit, Run, Share Kotlin Code Online](https://play.kotlinlang.org/)
[Kotlin Examples: Learn Kotlin Programming By Example](https://play.kotlinlang.org/byExample/01_introduction/01_Hello%20world)

[Try Kotlin](https://try.kotlinlang.org) old playground?

## Learning

[Reference - Kotlin Programming Language](https://kotlinlang.org/docs/reference/)
[Learning Kotlin: Introduction | Robert MacLean](https://www.sadev.co.za/learning-kotlin-introduction)
[Kotlin Bootcamp for Programmers | Udacity](https://www.udacity.com/course/developing-android-apps-with-kotlin--ud9011)
[Google Codelabs](https://codelabs.developers.google.com/?cat=Kotlin)
[Kotlin Bootcamp Course](https://codelabs.developers.google.com/kotlin-bootcamp/)

[Blog - SuperKotlin](https://superkotlin.com/blog/)
[Kotlin is Awesome!](https://kotlin.link/)
[mcxiaoke/awesome-kotlin: A curated list of awesome Kotlin frameworks, libraries, documents and other resources](https://github.com/mcxiaoke/awesome-kotlin)
[DZone: Programming & DevOps news, tutorials & tools](https://dzone.com/search?page=1) Learning Kotlin series by Robert Maclean
[Learn Kotlin - Best Kotlin Tutorials (2019) | gitconnected](https://gitconnected.com/learn/kotlin)

[On Kotlin | Baeldung](https://www.baeldung.com/kotlin-overview)
[Kotlin Mega Tutorial - SuperKotlin](https://superkotlin.com/kotlin-mega-tutorial/)
[Idioms - Kotlin Programming Language](https://kotlinlang.org/docs/reference/idioms.html)
[Kotlin Tutorial - grokonez](https://grokonez.com/kotlin-tutorial)
[Learning Kotlin: Introduction | Robert MacLean](https://www.sadev.co.za/learning-kotlin-introduction)

[Uberto Barbini – ProAndroidDev](https://proandroiddev.com/@ramtop)
[uberto/kotlin-pearls](https://github.com/uberto/kotlin-pearls)

[The problem with extension functions - Kt. Academy](https://blog.kotlin-academy.com/the-problem-with-extension-functions-dffd22eb5df9)
[Learn Kotlin Through Unit Tests - Android Developers - Medium](https://medium.com/androiddevelopers/learn-kotlin-through-unit-tests-914106d2d8c5)

### Conversion Program

Good for veteran programmers

[Kotlin for Java Developers | Coursera](https://www.coursera.org/learn/kotlin-for-java-developers/) !important, audit for free, with exercises in IntelliJ IDEA Educational Edition

[The Kotlin Guide for the Busy Java Developer – ProAndroidDev](https://proandroiddev.com/the-kotlin-guide-for-the-busy-java-developer-93dde84a77b7)
[Kotlin for Python developers | kotlin-for-python-developers](https://khan.github.io/kotlin-for-python-developers/)

Then do the Koans
[Kotlin Koans: The Best Way To Learn Kotlin for Java Developers](https://play.kotlinlang.org/koans/overview)
[Kotlin/kotlin-koans: Kotlin workshop](https://github.com/Kotlin/kotlin-koans) offline

[Hello, world! | Try Kotlin](https://try.kotlinlang.org/#/Kotlin%20Koans/) old playground?

## Lambda

The parameter list of a lambda expression must be inside the curly brace and must not be enclosed in parentheses.

Lambda of zero or one parameter can omit the parameter list and arrow. The single parameter can be referred by `it` in lambda.
If the last parameter to a function is a function type and you use lambda, you can 1) put the lambda out of the omit parentheses; 2) omit the parentheses for invocation altogether if there is only one parameter.
This is very useful for enabling Kotlin a DSL.

[Higher-Order Functions and Lambdas - Kotlin Programming Language](https://kotlinlang.org/docs/reference/lambdas.html)
[Lambda Expressions in Kotlin | Baeldung](https://www.baeldung.com/kotlin-lambda-expressions)
[Best Practices using Java 8 Lambdas | Baeldung](https://www.baeldung.com/java-8-lambda-expressions-tips)
[How Kotlin helps you avoid memory leaks – ProAndroidDev](https://proandroiddev.com/how-kotlin-helps-you-avoid-memory-leaks-e2680cf6e71e) non-instance-capturing lambdas are translated to private, static methods
[Diving into Higher order functions and lambdas in Kotlin](https://sourcediving.com/diving-into-higher-order-functions-and-lambdas-in-kotlin-e07656cdffe1)
[Lambda, Filter, and Map Function In Kotlin - AhsenSaeed](https://ahsensaeed.com/lambda-filter-map-function-kotlin/)
[Function literals with receiver in Kotlin](https://blog.mindorks.com/function-literals-with-receiver-in-kotlin)

[Funtion reference - Kotlin Programming Language](https://kotlinlang.org/docs/reference/reflection.html#function-references) passing named function as reference

### SAM

[Calling Java from Kotlin - Kotlin Programming Language](https://kotlinlang.org/docs/reference/java-interop.html#sam-conversions) Like Java 8, lambda functions can be used directly to implement Single Abstract Method (SAM), no need for anonymous object

google: kotlin comparator sam
[Learning Kotlin: Object Expressions and SAM Conversions - DZone Java](https://dzone.com/articles/learning-kotlin-object-expressions-and-sam-convers)

## Reflection

[Reflection - Kotlin Programming Language](https://kotlinlang.org/docs/reference/reflection.html)
[KProperty - Kotlin Programming Language](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-property/index.html)

## Smartcast

Kotlin 1.3 `stdlib` used contract for smartcasting in functions
[What's New in Kotlin 1.3 - Kotlin Programming Language](https://kotlinlang.org/docs/reference/whatsnew13.html#contracts)
[Kotlin Contracts | Baeldung](https://www.baeldung.com/kotlin-contracts)
[Kotlin Contracts: Make Great Deals With The Compiler! 🤜🤛](https://proandroiddev.com/kotlin-contracts-make-great-deals-with-the-compiler-f524e57f11c)
[Discovering Kotlin Contracts – ProAndroidDev](https://proandroiddev.com/discovering-kotlin-contracts-3e7ed1360602)

## Kotlin DSL

[Writing DSLs in Kotlin (part 1) – ProAndroidDev](https://proandroiddev.com/writing-dsls-in-kotlin-part-1-7f5d2193f277)
[Writing DSLs in Kotlin (part 2) – ProAndroidDev](https://proandroiddev.com/writing-dsls-in-kotlin-part-2-cd9dcd0c4715)
[Migrating Android build scripts from Groovy to Kotlin DSL](https://proandroiddev.com/migrating-android-build-scripts-from-groovy-to-kotlin-dsl-f8db79dd6737)

[Mastering Kotlin DSL In Android - Step By Step Guide](https://blog.mindorks.com/mastering-kotlin-dsl-in-android-step-by-step-guide)

[A Kotlin Time DSL for Java 8 Time - Jworks.io](https://www.jworks.io/kotlin-time-dsl-for-java-8-time/)

## Java Interop

[Java-Friendly Kotlin](https://codelabs.developers.google.com/codelabs/java-friendly-kotlin/#0)
[How to write Java-Friendly Kotlin Code - Android Developers - Medium](https://medium.com/androiddevelopers/how-to-write-java-friendly-kotlin-code-333f32ad0df3)

[Calling Java from Kotlin - Kotlin Programming Language](https://kotlinlang.org/docs/reference/java-interop.html)

[Calling Kotlin from Java - Kotlin Programming Language](https://kotlinlang.org/docs/reference/java-to-kotlin-interop.html)
[Java Calling — Kotlin – ProAndroidDev](https://proandroiddev.com/java-calling-kotlin-3cb3a84bde63)

[Run Kotlin Scripts from Kotlin Programs - Kotlin Expertise Blog](https://kotlinexpertise.com/run-kotlin-scripts-from-kotlin-programs/)
[How can I run Kotlin-Script (.kts) files from within Kotlin/Java? - Stack Overflow](https://stackoverflow.com/questions/34974039/how-can-i-run-kotlin-script-kts-files-from-within-kotlin-java)

## Module and Package

https://khan.github.io/kotlin-for-python-developers/#packages-and-imports

Module is defined by built tool and can consist of multiple packages. `internal` symbol is visible in the file and throughout all packages in the module.

## Tips and Tricks

[afollestad/library-template: A Kotlin + Android library template (with a sample project).](https://github.com/afollestad/library-template)

[Abstract class vs interface in Kotlin – Kt. Academy](https://blog.kotlin-academy.com/abstract-class-vs-interface-in-kotlin-5ab8697c3a14)
[Kotlin: Sealed Classes - ITNEXT](https://itnext.io/kotlin-sealed-classes-70f83d6ab567)
[Kotlin Generics Tutorial: Getting Started | raywenderlich.com](https://www.raywenderlich.com/3634394-kotlin-generics-tutorial-getting-started)

[Increasing readability using operator conventions in Kotlin](https://proandroiddev.com/increasing-readability-using-operator-conventions-in-kotlin-d518541f4c0a)

## Kotlin Native

[Kotlin/Native - Kotlin Programming Language](https://kotlinlang.org/docs/reference/native-overview.html)
[A Basic Kotlin/Native Application - Kotlin Programming Language](https://kotlinlang.org/docs/tutorials/native/basic-kotlin-native-app.html)

[Why we need Kotlin Native – Android Things – Medium](https://medium.com/android-things/why-we-need-kotlin-native-adacc03e988c)
improvements in 1.3, but not for prime time yet  
[Is Kotlin/Native production ready? Why we are not using it (yet) - QuickBird Studios Blog](https://quickbirdstudios.com/blog/is-kotlin-native-production-ready/)
[Why is Kotlin Native much slower than JVM? - Native - Kotlin Discussions](https://discuss.kotlinlang.org/t/why-is-kotlin-native-much-slower-than-jvm/10226/2)
[Debugging Kotlin Native’s Compiler – Kevin Galligan – Medium](https://medium.com/@kpgalligan/debugging-kotlin-natives-compiler-3cba9daec076)

[kotlin-native/performance at master · JetBrains/kotlin-native · GitHub](https://github.com/JetBrains/kotlin-native/tree/master/performance)
[frol/completely-unscientific-benchmarks: Naive performance comparison of a few programming languages (JavaScript, Kotlin, Rust, Swift, Nim, Python, Go, Haskell, D, C++, Java, C#, Object Pascal, Ada, Lua, Ruby)](https://github.com/frol/completely-unscientific-benchmarks)

[The magic of Kotlin/Native: Part 1 – AndroIDIOTS – Medium](https://medium.com/androidiots/the-magic-of-kotlin-native-part-1-fad2795632b1)
[The magic of Kotlin/Native: Part 2 – AndroIDIOTS – Medium](https://medium.com/androidiots/the-magic-of-kotlin-native-part-2-49097c2dea1a)
[The Magic of Kotlin/Native: Part 3 – AndroIDIOTS – Medium](https://medium.com/androidiots/the-magic-of-kotlin-native-part-3-9c647bb1c368)

## Server

[Introducing Kotlin support in Spring Framework 5.0](https://spring.io/blog/2017/01/04/introducing-kotlin-support-in-spring-framework-5-0)
[Tutorial · Building web applications with Spring Boot and Kotlin](https://spring.io/guides/tutorials/spring-boot-kotlin/)
[Creating a RESTful Web Service with Spring Boot - Kotlin Programming Language](https://kotlinlang.org/docs/tutorials/spring-boot-restful.html)
[Going Reactive with Spring, Coroutines and Kotlin Flow](https://spring.io/blog/2019/04/12/going-reactive-with-spring-coroutines-and-kotlin-flow)

[Ktor - asynchronous Web framework for Kotlin](https://ktor.io/)
[Ktor for fast server prototyping. Ktor is framework for creating server… | by Jarosław Michalik | Kt. Academy](https://blog.kotlin-academy.com/ktor-for-fast-server-prototyping-6e7c6d2ec296?gi=5b6b1ced336e)

[Javalin - A lightweight Java and Kotlin web framework](https://javalin.io/)
[Introducing Javalin: a Lightweight Web Framework for Java and Kotlin](https://www.infoq.com/news/2019/07/javalin/)

## #perfmatters

[Faster command line tools with Kotlin - Renato Athaydes](https://sites.google.com/a/athaydes.com/renato-athaydes/posts/fastercommandlinetoolswithkotlin)

## Stdlib

[kotlin-stdlib - Kotlin Programming Language](https://kotlinlang.org/api/latest/jvm/stdlib/index.html)
[kotlin/libraries/stdlib/src/kotlin at master · JetBrains/kotlin](https://github.com/JetBrains/kotlin/tree/master/libraries/stdlib/src/kotlin) source

[Subtle differences between Kotlin's with(), apply(), let(), also(), and run()](https://ask.ericlin.info/post/2017/06/subtle-differences-between-kotlins-with-apply-let-also-and-run/)

### Collections

`c.size` for collections
`s.length` for strings

[Pair and Triple in Kotlin](https://blog.mindorks.com/pair-and-triple-in-kotlin)

[Kotlin Collection Extensions Cheat Sheet by Xantier - Download free from Cheatography - Cheatography.com: Cheat Sheets For Every Occasion](https://www.cheatography.com/xantier/cheat-sheets/kotlin-collection-extensions/)

[Exploring Kotlin: useful standard library functions](https://medium.freecodecamp.org/exploring-kotlin-useful-standard-library-functions-6de19342f35a)
[Kotlin Sequences: An Illustrated Guide - Dave Leeds on Kotlin](https://typealias.com/guides/kotlin-sequences-illustrated-guide/)

[Kotlin Array sort(), sortBy(), sortWith() - grokonez](https://grokonez.com/kotlin/kotlin-array-sort-sortby-sortwith)
[Functional Android (II): Collection operations in Kotlin](https://antonioleiva.com/collection-operations-kotlin/)

Conversion between collections:
`toList()`, `toMutableList()`, `toSet()`, `toMutableSet()`

[Collections vs Sequences: War of use-cases! - ProAndroidDev](https://proandroiddev.com/collections-vs-sequences-war-of-use-cases-1f2ca06a8ac4)
`Sequence<T>` is a lazily evaluated list, like Python's generator. Use `Collection.asSequence()` to get a Sequence.

`people.associateBy({it.ssn}, {it.name})` to generate a `ssn` to `name` Map. Omit the second lambda to generate a `ssn` to `people` Map ("key by" operation). Call `toMutableMap()` at the end to make the result mutable.

### Concurrency

[Coroutines Guide - Kotlin Programming Language](https://kotlinlang.org/docs/reference/coroutines/coroutines-guide.html)
[Kotlin Coroutines Tutorial for Android : Advanced | raywenderlich.com](https://www.raywenderlich.com/2117501-kotlin-coroutines-tutorial-for-android-advanced)
[A Bottom-Up View of Kotlin Coroutines](https://www.infoq.com/articles/kotlin-coroutines-bottom-up/)
[Understanding Kotlin coroutines - LogRocket Blog](https://blog.logrocket.com/understanding-kotlin-coroutines/)

[Migrating your Network calls to Coroutines and Moshi in Kotlin](https://itnext.io/migrating-your-network-calls-to-coroutines-and-moshi-in-kotlin-e92f1f311ef)
[Caching with Kotlin Coroutines – ProAndroidDev](https://proandroiddev.com/caching-with-kotlin-coroutines-7d819276c820)
[Async tasks with Kotlin Coroutines - NaNLABS](https://www.nan-labs.com/blog/async-tasks-with-kotlin-coroutines/)
[A simple way to work with Kotlin Coroutines in Android](https://proandroiddev.com/a-simple-way-to-work-with-kotlin-coroutines-in-android-62f5338386e1)

[Flow - kotlinx-coroutines-core](https://kotlin.github.io/kotlinx.coroutines/kotlinx-coroutines-core/kotlinx.coroutines.flow/-flow/)
[Simple design of Kotlin Flow – Roman Elizarov – Medium](https://medium.com/@elizarov/simple-design-of-kotlin-flow-4725e7398c4c)
[Reactive Streams and Kotlin Flows - Roman Elizarov - Medium](https://medium.com/@elizarov/reactive-streams-and-kotlin-flows-bfd12772cda4)
[Kotlin Flows and Coroutines – Roman Elizarov – Medium](https://medium.com/@elizarov/kotlin-flows-and-coroutines-256260fb3bdb)
[Execution context of Kotlin Flows – Roman Elizarov – Medium](https://medium.com/@elizarov/execution-context-of-kotlin-flows-b8c151c9309b)
[Blocking threads, suspending coroutines – Roman Elizarov – Medium](https://medium.com/@elizarov/blocking-threads-suspending-coroutines-d33e11bf4761)
[Explicit concurrency – Roman Elizarov – Medium](https://medium.com/@elizarov/explicit-concurrency-67a8e8fd9b25)

## Style Guide

[Coding Conventions - Kotlin Programming Language](https://kotlinlang.org/docs/reference/coding-conventions.html)
[Kotlin style guide | Android Developers](https://developer.android.com/kotlin/style-guide)

[Coding Conventions - Kotlin Programming Language](https://kotlinlang.org/docs/reference/code-style-migration-guide.html) "Kotlin Coding Conventions" vs "IntelliJ IDEA default code style"

[pinterest/ktlint: An anti-bikeshedding Kotlin linter with built-in formatter](https://github.com/pinterest/ktlint)
[Code Formatting in Kotlin using ktlint](https://blog.mindorks.com/code-formatting-in-kotlin-using-ktlint)

## Libraries

[Awesome Kotlin Resources - Kotlin Resources](https://www.kotlinresources.com/)

[Vert.x](http://vertx.io/) building reactive applications

[Compose Multiplatform Framework | JetBrains: Developer Tools for Professionals and Teams](https://www.jetbrains.com/lp/compose-mpp/) reactive Desktop and Web UI framework for Kotlin

### CLI

[Kotlin/kotlinx.cli: Pure Kotlin implementation of a generic CLI parser.](https://github.com/Kotlin/kotlinx.cli)
[xenomachina/kotlin-argparser: Easy to use and concise yet powerful and robust command line argument parsing for Kotlin](https://github.com/xenomachina/kotlin-argparser) built on `kotlin.cli`
[leprosus/kotlin-cli: Kotlin-CLI - command line interface options parser for Kotlin](https://github.com/leprosus/kotlin-cli)
[Clikt: Simple, powerful command line parser for Kotlin](https://ajalt.github.io/clikt/)
[picocli - a mighty tiny command line interface](https://picocli.info/)
[jimschubert/kopper: A simple Kotlin option parser](https://github.com/jimschubert/kopper)

[parameter passing - Functional style main function argument parsing for Kotlin - Stack Overflow](https://stackoverflow.com/questions/53946908/functional-style-main-function-argument-parsing-for-kotlin)
