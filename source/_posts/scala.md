---
title: Scala
categories:
  - comp.lang
tags:
  - java
  - scala
toc: true
date: 2016-03-04 12:07:53
---

[The Scala Programming Language](http://www.scala-lang.org/)
[Documentation | Scala Documentation](https://docs.scala-lang.org/)
[Scaladoc - Scaladoc for Library Authors - Scala Documentation](http://docs.scala-lang.org/overviews/scaladoc/for-library-authors.html)
[Scala Standard Library](http://www.scala-lang.org/api/current/index.html)

[Tutorials - Scala Documentation](http://docs.scala-lang.org/tutorials/)
[Guides and Overviews - Scala Documentation](http://docs.scala-lang.org/overviews/)
[Scala School](https://twitter.github.io/scala_school/) !important
[Effective Scala](http://twitter.github.io/effectivescala/)
[Scala Tutorial Through Katas | Technology Conversations](http://technologyconversations.com/2014/03/10/scala-tutorial-through-katas/)
[Functional Programming Principles in Scala - École Polytechnique Fédérale de Lausanne | Coursera](https://www.coursera.org/learn/progfun1)
[Scala Tutorial](https://www.tutorialspoint.com/scala/)
[First Steps to Scala](http://www.artima.com/scalazine/articles/steps.html)

[A 10-Minute Introduction to Scala – Hacker Noon](https://hackernoon.com/a-10-minute-introduction-to-scala-d1fed19eb74c)
[10 Reasons to Learn Scala and Functional Programming](https://hackernoon.com/10-reasons-to-learn-scala-and-functional-programming-2fce385e6ec7)

[Ammonite](http://ammonite.io/) Scala Scripting
[Scalafmt - code formatter for Scala](http://scalameta.org/scalafmt/)

[ScalaTest](http://www.scalatest.org/)
[Play Framework - Build Modern & Scalable Web Apps with Java and Scala](https://www.playframework.com/)

## Akka

[Akka](http://akka.io/) Akka replaces Sacla's Actor since 2.10
[52-technologies-in-2016/38-akka](https://github.com/shekhargulati/52-technologies-in-2016/blob/master/38-akka/README.md)
[52-technologies-in-2016/41-akka-dispatcher](https://github.com/shekhargulati/52-technologies-in-2016/blob/master/41-akka-dispatcher/README.md)
[General Concepts • Akka Documentation](https://doc.akka.io/docs/akka/current/general/index.html)
[Scala - Akka Documentation](https://doc.akka.io/docs/akka/current/?language=scala)

[spray | REST-HTTP for your Akka-Scala Actors](http://spray.io/)
[naaman-spray-bootstrap · GitHub](https://github.com/naaman/spray-bootstrap)

[Programming Throwdown Podcast: Jonas Bonér On Why Akka, the Actor Model, and Reactive Systems | @lightbend](https://www.lightbend.com/blog/programming-throwdown-podcast-jonas-boner-on-why-akka-the-actor-model-and-reactive-systems)
[How To Build Stateful, Cloud-Native Services With Akka and Kubernetes | White Paper | @lightbend](https://www.lightbend.com/stateful-cloud-native-services-with-akka-and-kubernetes)
[How Akka Works: "Akka A To Z", An Illustrated White Paper | @lightbend](https://www.lightbend.com/blog/how-akka-works-akka-a-to-z-illustrated-white-paper)

## `sbt`

[sbt - The interactive build tool](http://www.scala-sbt.org/)
[sbt Reference Manual — sbt Reference Manual](http://www.scala-sbt.org/1.x/docs/index.html)
[Building projects with sbt — Scala Native documentation](http://www.scala-native.org/en/latest/user/sbt.html)

[Simple Command Line Tools with Scala Native](https://spantree.net/blog/2017/06/26/scala-native-for-cli-tools.html?platform=hootsuite)

```sh
sbt new scala-native/scala-native.g8
sbt nativeLink
./target/scala-2.11/randomizer-out
```

[sbt Reference Manual — Library dependencies](http://www.scala-sbt.org/1.x/docs/Library-Dependencies.html)
When adding Library dependencies

```
libraryDependencies += groupID % artifactID % revision
# auto resolves scala version
libraryDependencies += groupID %% artifactID % revision
# auto resolves scala version and target, use this for Scala Native or Scala.js
libraryDependencies += groupID %%% artifactID % revision
```

## Scala Native

[Scala Native](https://github.com/scala-native)
[Scala Native documentation](http://www.scala-native.org/en/latest/)

[Scaled-down Scala variant cuts ties to the JVM | InfoWorld](http://www.infoworld.com/article/3180823/application-development/scaled-down-scala-variant-cuts-ties-to-the-jvm.html)
[Scala Native with Denys Shabalin | Software Engineering Daily](https://softwareengineeringdaily.com/2017/10/16/scala-native-with-denys-shabalin/)

[Scala Goes Native - by Denys Shabalin - YouTube](https://www.youtube.com/watch?v=ArWWlwQl37A)

[Bootstrapping the Web with Scala Native (Part 1)](https://www.spantree.net/blog/2017/08/29/bootstrapping-web-scala-native.html)

## Scala.js

[Scala.js](https://www.scala-js.org/)
[Tutorials - Scala.js](http://www.scala-js.org/tutorial/)
[Hands-on Scala.js](http://www.lihaoyi.com/hands-on-scala-js/)

[ScalaJS with Haoyi Li | Software Engineering Daily](https://softwareengineeringdaily.com/2016/10/06/scalajs-with-haoyi-li/)

[PNWS 2014 - Hands-on Scala.js - YouTube](https://www.youtube.com/watch?v=9SalPdAEI28)
[Why Scala.js - YouTube](https://www.youtube.com/watch?v=LxK04X7py9M)

## Libraries

[scalaz/scalaz @ GitHub](http://scalaz.github.io/scalaz/#scaladoc)
[scopt/scopt: simple scala command line options parsing](https://github.com/scopt/scopt)
