---
title: Java
categories:
  - comp.lang
tags:
  - java
  - groovy
  - clojure
  - guava
toc: true
date: 2016-03-04 12:07:53
---

[Heroku | The Next Twenty Years of Java: Where We've Been and Where We're Going](https://blog.heroku.com/archives/2015/6/4/the_next_twenty_years_of_java_where_we_ve_been_and_where_we_re_going)

[Java Tools and Technologies Landscape Report 2016 | zeroturnaround.com](https://zeroturnaround.com/rebellabs/java-tools-and-technologies-landscape-2016/)
[Java Tools and Technologies Landscape Report 2016: Pivoting data | zeroturnaround.com](https://zeroturnaround.com/rebellabs/java-tools-and-technologies-landscape-2016-pivoting-data/)
[Java Tools and Technologies Landscape Report 2016: Trends and Historical data | zeroturnaround.com](https://zeroturnaround.com/rebellabs/java-tools-and-technologies-landscape-2016-trends/)

[7 New Java Talks You Need to See | Takipi Blog](http://blog.takipi.com/7-new-java-talks-you-need-to-see/)

It's easier to extract the JDK tarball and use `JAVA_HOME` to use it.

```sh
JAVA_HOME=/usr/local/share/jdk1.8.0_91 java_app
```

[OpenJDK](https://openjdk.java.net/)
[Differences Between Oracle JDK and OpenJDK | Baeldung](https://www.baeldung.com/oracle-jdk-vs-openjdk)
[java - Differences between Oracle JDK and OpenJDK - Stack Overflow](https://stackoverflow.com/questions/22358071/differences-between-oracle-jdk-and-openjdk)
[Java Future Release Notices](https://java.com/en/download/release_notice.jsp) Oracle Java SE is not applicable to business since April 16, 2019
[Red Hat Breathes New Life Into Java | Enterprise | LinuxInsider](https://www.linuxinsider.com/story/85972.html)
[Oracle JDK Releases for Java 11 and Later | Oracle Java Platform Group, Product Management Blog](https://blogs.oracle.com/java-platform-group/oracle-jdk-releases-for-java-11-and-later) Oracle JDK and OpenJDK builds are essentially identical from Java 11 onward
[Migrating from Oracle JDK to OpenJDK on Red Hat Enterprise Linux: What you need to know - Red Hat Developer Blog](https://developers.redhat.com/blog/2018/11/05/migrating-from-oracle-jdk-to-openjdk-on-red-hat-enterprise-linux-what-you-need-to-know/)

[Not all OpenJDK 12 builds include Shenandoah: Here's why - Red Hat Developer Blog](https://developers.redhat.com/blog/2019/04/19/not-all-openjdk-12-builds-include-shenandoah-heres-why/)
[Main - Shenandoah - OpenJDK Wiki](https://wiki.openjdk.java.net/display/shenandoah/Main)
[When Will Java 11 Replace Java 8 as the Default Java? - DZone Java](https://dzone.com/articles/when-will-java-11-replace-java-8-as-the-default-ja)

[JavaPoly.js — Java(script) in the Browser](https://www.javapoly.com/)

## Learn

From Oracle:
[Java SE Specifications](http://docs.oracle.com/javase/specs/)
[The Java™ Tutorials](http://docs.oracle.com/javase/tutorial/) [offline/eBook](http://www.oracle.com/technetwork/java/javase/java-tutorial-downloads-2005894.html)

[Java "Back to Basics" Tutorial | Baeldung](https://www.baeldung.com/java-tutorial)
[Java Tutorial Through Katas | Technology Conversations](http://technologyconversations.com/2014/10/16/java-tutorial-through-katas/)
[Java Programming, Learn Java Online with the Java Code Geeks | Java developers resource center - Java, Scala, Groovy, Android](http://www.javacodegeeks.com/)

[Java "Back to Basics" Tutorial | Baeldung](https://www.baeldung.com/java-tutorial)
[Home - Thoughts on Java](https://thoughts-on-java.org/)
[Thoughts On Java - YouTube](https://www.youtube.com/c/thoughtsonjava)

[14 YouTube Channels You Should Follow in 2019 - Thoughts on Java](https://thoughts-on-java.org/youtube-channels-you-should-follow-in-2019/)

### Book

[Think Java – Green Tea Press](http://greenteapress.com/wp/think-java/)
[Free Online Version of Core Servlets and JavaServer Pages (Second Edition) in PDF](http://pdf.coreservlets.com/)
[Javanotes 7.0 -- Title Page](http://math.hws.edu/javanotes/)

[Quick Links - MindView Exceptional Learning Experiences](https://www.mindviewllc.com/quicklinks/#java) Thinking in Java
[Thinking in Java 4th Edition (R1) : Bruce Eckel : Free Download, Borrow, and Streaming : Internet Archive](https://archive.org/details/TIJ4CcR1/page/n3)

## Maven

[Maven – Welcome to Apache Maven](https://maven.apache.org/index.html)
[Maven – Introduction](http://maven.apache.org/what-is-maven.html)

[How to create a Java project with Maven](http://www.mkyong.com/maven/how-to-create-a-java-project-with-maven/)

```sh
mvn archetype:generate -DgroupId={project-packaging}
   -DartifactId={project-name}
   -DarchetypeArtifactId=maven-archetype-quickstart
   -DinteractiveMode=false
```

[Maven Multimodule Project: A Detailed View | by Anish Antony | Javarevisited | Medium](https://medium.com/javarevisited/maven-multimodule-project-a-detailed-view-e03a56e0d43d)

## Server

[15 Java frameworks that give developers a boost | InfoWorld](https://www.infoworld.com/article/3263767/java/15-java-frameworks-that-give-developers-a-boost.html)

[Project Grizzly](https://grizzly.java.net/)
[Java SE 8: Creating a Basic REST Web Service using Grizzly, Jersey, and Maven](https://www.oracle.com/webfolder/technetwork/tutorials/obe/java/griz_jersey_intro/Grizzly-Jersey-Intro.html)

[GlassFish Server](https://glassfish.java.net/)
[DUBBO](http://dubbo.io/)

[A Fast Introduction to Basic Servlet Programming | The Advantages of Servlets Over "Traditional" CGI | InformIT](http://www.informit.com/articles/article.aspx?p=29817)

[CRaSH the shell for the Java Platform](http://www.crashub.org/)

[Blade](https://lets-blade.com/)
[lets-blade/blade: Lightning fast and elegant mvc framework for Java8](https://github.com/lets-blade/blade)

### Jakarta EE

[Java Platform, Enterprise Edition - Wikiwand](https://www.wikiwand.com/en/Java_Platform,_Enterprise_Edition) Java EE is rebranded as Jarkarta EE

[Jakarta EE: Generation IV — A New Hope - DZone Java](https://dzone.com/articles/jakarta-ee-generation-iv-a-new-hope)
[Java roadmap: Eclipse’s Jakarta EE enterprise Java takes shape | InfoWorld](https://www.infoworld.com/article/3269210/java/java-roadmap-eclipses-jakarta-ee-enterprise-java-takes-shape.html)
[What's New With Jakarta NoSQL? (Part 1): Intro to Document With MongoDB - DZone Database](https://dzone.com/articles/whats-new-with-jakarta-nosql-part-i-introduction-t)

## Internals

[JVM Optimization 101](http://www.infoq.com/presentations/jvm-optimization)
[Honey, you have changed quite a bit lately, haven't you? | Elastic](https://www.elastic.co/blog/honey-you-have-changed-quite-a-bit)

[A Primer on JVM Memory Management and Troubleshooting - 1](https://dev.to/rrampage/a-primer-on-jvm-memory-management-and-troubleshooting---1-12b6)
[JVM Primer Part 2 - Debugging memory issues](https://dev.to/rrampage/jvm-primer-part-2---debugging-performance-issues-1od)
[How to Read a Thread Dump - DZone Java](https://dzone.com/articles/how-to-read-a-thread-dump)

## Libraries

[Comsat - Parallel Universe](http://www.paralleluniverse.co/comsat/) transparent concurrency for maximal
http service scalability
[Quasar - Parallel Universe](http://www.paralleluniverse.co/quasar/) lightweight threads and actors for the JVM, Kotlin compatible

### Guava

[google/guava: Google core libraries for Java](https://github.com/google/guava)
[Home · google/guava Wiki](https://github.com/google/guava/wiki)
[Overview (Guava: Google Core Libraries for Java HEAD-jre-SNAPSHOT API)](https://guava.dev/releases/snapshot-jre/api/docs/)

[Guava | Baeldung](https://www.baeldung.com/category/guava/)
[Thomas Ferris Nicolaisen - Google Guava](https://www.tfnico.com/presentations/google-guava)

---

# JVM as a Platform

[JVM Minimal Survival Guide – Hadi Hariri](https://hadihariri.com/2013/12/29/jvm-minimal-survival-guide-for-the-dotnet-developer/)

[SE-Radio Episode 266: Charles Nutter on the JVM as a Language Platform : Software Engineering Radio](http://www.se-radio.net/2016/08/se-radio-episode-266-charles-nutter-on-the-jvm-as-a-language-platform/)
JRuby history and compile to JVM in general. The project leads to the introduction of `invokedynamic` to JVM instructions which Java 8's lambdas depends on.

[Java Virtual Machine Support for Non-Java Languages](http://docs.oracle.com/javase/7/docs/technotes/guides/vm/multiple-language-support.html)

[Invokedynamic 101 | JavaWorld](http://www.javaworld.com/article/2860079/learn-java/invokedynamic-101.html)
[Invokedynamic - Java’s Secret Weapon](https://www.infoq.com/articles/Invokedynamic-Javas-secret-weapon)
[Why are Java 8 lambdas invoked using invokedynamic? - Stack Overflow](http://stackoverflow.com/questions/30002380/why-are-java-8-lambdas-invoked-using-invokedynamic)
[The Apache Groovy programming language - Invoke dynamic support](http://groovy-lang.org/indy.html)

## GraalVM

[GraalVM](https://www.graalvm.org/) ahead-of-time VM for compiled _polyglot_ binaries
[Oracle's Graal project empowers language creation on the JVM | InfoWorld](https://www.infoworld.com/article/2688340/application-development/oracles-graal-project-empowers-language-creation-on-the-jvm.html)
[GraalVM with Thomas Wuerthinger - Software Engineering Daily](https://softwareengineeringdaily.com/2018/08/03/graalvm-with-thomas-wuerthinger/)

[Thomas Wuerthinger on GraalVM and Optimizing Java with Ahead-of-Time Compilation](https://www.infoq.com/podcasts/graalvm-optimizing-java/)
[Maximizing Performance with GraalVM](https://www.infoq.com/presentations/graalvm-performance/)

[Quarkus - Supersonic Subatomic Java](https://quarkus.io/)
[Introducing Quarkus: a next-generation Kubernetes native Java framework - Red Hat Developer Blog](https://developers.redhat.com/blog/2019/03/07/quarkus-next-generation-kubernetes-native-java-framework/)
[Quarkus beginners guide! - JAX London](https://jaxlondon.com/quarkus-beginners-guide-cheat-sheet/)
[GraalVM Quarkus: Java Acceleration with Guillaume Smet and Emmanuel Bernard - Software Engineering Daily](https://softwareengineeringdaily.com/2019/11/14/graalvm-quarkus-java-acceleration-with-guillaume-smet-and-emmanuel-bernard/)
[Microservices: Quarkus vs. Spring Boot - DZone Microservices](https://dzone.com/articles/microservices-quarkus-vs-spring-boot)

## RoboVM

[The Death of RoboVM | Linux Journal](https://www.linuxjournal.com/content/death-robovm) RoboVM was dead after Xamarin has been acquired by Microsoft

[MobiDevelop's RoboVM Fork](http://robovm.mobidevelop.com/)
[MobiVM/robovm: Ahead of time compiler for JVM bytecode targetting iOS, Mac OSX and Linux](https://github.com/MobiVM/robovm)

# Derivatives

There a many compile-to-bytecode language. They have the advantage of:

- provide different programming paradigms
- Java interoperability (varies)
- utilize highly optimized JVM

[List of JVM languages - Wikiwand](https://www.wikiwand.com/en/List_of_JVM_languages)
[Pirates of the JVM — The infographic: Are you ready for an adventure? - JAXenter](https://jaxenter.com/pirates-of-the-jvm-the-infographic-132524.html)
[Beyond Java: Programming languages on the JVM | InfoWorld](https://www.infoworld.com/article/3268484/java/beyond-java-programming-languages-on-the-jvm.htm)

[SDKMAN! the Software Development Kit Manager](http://sdkman.io/) install Java related toolchains
[Why is Scala more popular than Clojure despite the simplicity of the latter? - Quora](https://www.quora.com/Why-is-Scala-more-popular-than-Clojure-despite-the-simplicity-of-the-latter)
[Scala VS Groovy: A Response | Kevin Wright | LinkedIn](https://www.linkedin.com/pulse/someone-wrong-internet-kevin-wright)
[Scala vs. Groovy vs. Clojure - Stack Overflow](http://stackoverflow.com/questions/1314732/scala-vs-groovy-vs-clojure)
[What are the key differences between Scala and Groovy? - Stack Overflow](http://stackoverflow.com/questions/711913/what-are-the-key-differences-between-scala-and-groovy)

[Why I abandoned Java in favour of Kotlin - Hashnode](https://hashnode.com/post/why-i-abandoned-java-in-favour-of-kotlin-ciuzhmecf09khdc530m1ghu6d)
[Groovy vs Kotlin - Which One Is Best ( With Infographics)](https://www.educba.com/groovy-vs-kotlin/)
[Scala vs Kotlin – Agilewombat](https://agilewombat.com/2016/02/01/scala-vs-kotlin/)

[Who's More Functional: Kotlin, Groovy, Scala, or Java? - YouTube](https://www.youtube.com/watch?v=s4zasprvfVE)

## Kotlin

> see `kotlin.md`

## Scala

> see `scala.md`

## Groovy

> It's probably wiser to go for Kotlin or Scala instead

Groovy is a dynamic and scripting language running on JVM. It is adopted as an Apache project in April 2015.
Groovy script is interpreted to Java Bytecode. It also has a compiled mode to archive Java performance.
It utilizes invoke dynamic runtime on JVM 7+, Groovy 3 is expected to drop legacy mode which uses reflection and hacks.

[The Groovy programming language](http://groovy-lang.org/)
[Apache Groovy - Wikiwand](https://www.wikiwand.com/en/Apache_Groovy)

[Groovy web console](http://groovyconsole.appspot.com/) playground

[The Groovy programming language - Learn](http://groovy-lang.org/learn.html)
[The Groovy programming language - Documentation](http://groovy-lang.org/documentation.html)

[Cédric Champeau's blog](http://melix.github.io/blog/) Blog of ex-Groovy contributor

[The Grails Framework](https://grails.org/) A powerful Groovy-based web application framework for the JVM

[Groovy 3.0 Adds New Java-Like Features](https://www.infoq.com/articles/groovy-3-new-features-java/)
[5 reasons why Groovy programming language is still a valid choice in late 2018 | Codementor](https://www.codementor.io/szymonstpniak/5-reasons-groovy-programming-language-is-still-a-valid-choice-in-late-2018-npogilod3)

### Compiling Groovy

```sh
groovy ./file.groovy

# compile to ./file.class
groovyc ./file.groovy
java -cp ".;${GROOVY_HOME}/LIB/*" <classname>
```

```sh
groovyc -d classes myclasses.groovy
jar cvf myclasses.jar -C classes .
```

[dmitart/scriptjar](https://github.com/dmitart/scriptjar) in Groovy
[Bernhard's Weblog](http://www.jroller.com/berni/entry/wrapping_groovy_scripts_as_executable)
[bond-/gradle-groovy-jar-example: Example for a groovy executable using gradle-1.0](https://github.com/bond-/gradle-groovy-jar-example)

## Clojure

[Clojure - home](http://clojure.org/)
[Learning colojure — Medium](https://medium.com/@mshanu/learning-colojure-f99e5c80921e#.zdkexduwf)
[Clojure Newbie Guide](http://www.clojurenewbieguide.com/)

[Clojure - ClojureScript](http://clojure.org/about/clojurescript) compile to JavaScript
[Google Closure · clojure/clojurescript Wiki](https://github.com/clojure/clojurescript/wiki/Google-Closure)
[What Holds Me Back From Clojurescript | Jared Forsyth.com](https://jaredforsyth.com/2015/11/26/What-holds-me-back-from-Clojurescript/)
[Courses with Free Content | PurelyFunctional.tv](https://purelyfunctional.tv/free-content/)

[Pedestal](http://pedestal.io/)

## Eta

[The Eta Programming Language](http://eta-lang.org/)
[typelead/eta: The Eta Programming Language, a dialect of Haskell on the JVM](https://github.com/typelead/eta)

## Purple JS

[PurpleJS](http://purplejs.io/) run JS in JVM
[purplejs/purplejs: PurpleJS framework - A javascript application framework on the JVM.](https://github.com/purplejs/purplejs)
[Home · purplejs/purplejs Wiki](https://github.com/purplejs/purplejs/wiki)
