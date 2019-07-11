---
title: Go notes
date: 2015-02-16 17:58:42
categories:
  - comp.lang
tags:
  - golang
  - gopm
  - package-manager
  - notes
toc: true
---

[The Go Programming Language](https://golang.org/)
[Go (programming language) - Wikiwand](http://www.wikiwand.com/en/Go_%28programming_language%29)
[What reasons are there to not use Go (programming language)? - Quora](https://www.quora.com/What-reasons-are-there-to-not-use-Go-programming-language)

[avelino/awesome-go: A curated list of awesome Go frameworks, libraries and software](https://github.com/avelino/awesome-go)
[travis-ci/gimme: Install go, yay!](https://github.com/travis-ci/gimme) `nvm` for Go

[Tap the power of Google's Go language | InfoWorld](http://www.infoworld.com/article/3190210/application-development/tap-the-power-of-googles-go-language.html)

[Go Tooling in Action — Google Cloud Platform — Community — Medium](https://medium.com/google-cloud/go-tooling-in-action-eca6882ff3bc#.dlfizcmy1)

[Building A Queue - Part 1](https://www.openmymind.net/Building-A-Queue-Part-1/)
[Building A Queue - Part 2](https://www.openmymind.net/Building-A-Queue-Part-2/)
[Building A Queue - Part 3](https://www.openmymind.net/Building-A-Queue-Part-3/)
[Building A Queue - Part 4](https://www.openmymind.net/Building-A-Queue-Part-4/)

## Go 2

[Toward Go 2 - The Go Blog](https://blog.golang.org/toward-go2)
[Go 2 Draft Designs - The Go Blog](https://blog.golang.org/go2draft)
[Go 2 Draft Designs](https://go.googlesource.com/proposal/+/master/design/go2draft.md)

## Editor/IDE

[The best Go language IDEs and editors | InfoWorld](http://www.infoworld.com/article/3171158/application-development/the-best-go-language-ides-and-editors.html)

[LiteIDE X](http://liteide.org/en/)
[visualfc/liteide: LiteIDE is a simple, open source, cross-platform Go IDE.](https://github.com/visualfc/liteide)

## Commentary

[Comparing Elixir and Go - via @codeship | via @codeship](https://blog.codeship.com/comparing-elixir-go/)
[The success of Go heralds that of Rust – George Hosu – Medium](https://medium.com/@george3d6/the-success-of-go-heralds-that-of-rust-73cb2e4c0500)
[Go: the Good, the Bad and the Ugly](https://bluxte.net/musings/2018/04/10/go-good-bad-ugly/)
[What Go Programming Language does and does not have](https://medium.com/@amritpandey/what-go-programming-language-does-and-does-not-have-ed6a9f83ab2d)

## Compile

[How a Go Program Compiles down to Machine Code – Hacker Noon](https://hackernoon.com/how-a-go-program-compiles-down-to-machine-code-e4532dc8b8ca)

[vladimirvivien/go-cshared-examples: Calling Go Functions from Other Languages using C Shared Libraries](https://github.com/vladimirvivien/go-cshared-examples)

[gopherjs/gopherjs: A compiler from Go to JavaScript for running Go code in a browser](https://github.com/gopherjs/gopherjs)

[Introducing Joy](https://mat.tm/joy/)
[matthewmueller/joy: A delightful Go to Javascript compiler](https://github.com/matthewmueller/joy)
on hold in light of WASM target

## Packages

`go get` can retrieve packages given the URL

[GoDoc (package repository)](https://godoc.org/)
[Go Search - Find popular and relevant Go packages!](http://go-search.org/)
[Projects · golang/go Wiki](https://github.com/golang/go/wiki/Projects)

[Package Documentation (Go standard library)](http://golang.org/pkg/)
[fmt - The Go Programming Language](http://golang.org/pkg/fmt/)
[strings - The Go Programming Language](http://golang.org/pkg/strings/)
[strconv - The Go Programming Language](http://golang.org/pkg/strconv/)
[reflect - The Go Programming Language](http://golang.org/pkg/reflect/)
[json - The Go Programming Language](http://golang.org/pkg/encoding/json/)
[flag - The Go Programming Language](http://golang.org/pkg/flag/)
[Projects - go-wiki - A list of Go projects. - Go Language Community Wiki - Google Project Hosting](https://code.google.com/p/go-wiki/wiki/Projects)

[golang/mobile](https://github.com/golang/mobile/)

### gopm

[gpmgo/gopm](https://github.com/gpmgo/gopm)
[Gopm Registry - Versioning caching and delivery for your Go packages](http://gopm.io/)

### Glide

[Glide | Package Management For Go](https://glide.sh/)
Glide is a tool for managing [vendor directories](http://glide.readthedocs.io/en/latest/vendor/).

### Dependency Management

[The Saga of Go Dependency Management GopherAcademy](https://blog.gopheracademy.com/advent-2016/saga-go-dependency-management/)
[PackageManagementTools · golang/go Wiki](https://github.com/golang/go/wiki/PackageManagementTools)
[Dependency Management Tool - Google Docs](https://docs.google.com/document/d/1qnmjwfMmvSCDaY4jxPmLAccaaUI5FfySNE90gB0pTKQ/edit#)

[Go Modules in 2019 - The Go Blog](https://blog.golang.org/modules2019)
[Using Go Modules - The Go Blog](https://blog.golang.org/using-go-modules) Finally in 2019-03

[Go 1.11 Modules (vgo) vs dep · Issue #1959 · golang/dep](https://github.com/golang/dep/issues/1959)

### import

[bradfitz/goimports: Tool to fix (add, remove) your Go imports automatically.](https://github.com/bradfitz/goimports)
[理解 Go import |虞双齐的博客](https://www.yushuangqi.com/blog/2016/understanding-golang-import-package.html)

### `vendor/`

[Go 1.5 Vendor Experiment - Google Docs](https://docs.google.com/document/d/1Bz5-UB7g2uPBdOx-rw5t9MxJwkfpx90cqG9AFL0JAYo/edit)

Go's `vendor/` = Node's `node_modules/`
import from project local instead of `GOPATH`
default in Go 1.7

### web

[RESTful routing in Go](https://www.openmymind.net/RESTful-routing-in-Go/)
[Go actions responses](https://www.openmymind.net/Go-action-responses/)

[Golang: 6 must-have web frameworks for the Google Go language | InfoWorld](https://www.infoworld.com/article/3274464/web-development/6-must-have-web-frameworks-for-the-google-go-language.html)

[gorilla/mux: A powerful URL router and dispatcher for golang.](https://github.com/gorilla/mux)
[go-martini/martini: Classy web framework for Go](https://github.com/go-martini/martini) no longer maintained

[gin-gonic/gin: Gin is a HTTP web framework written in Go (Golang). It features a Martini-like API with much better performance -- up to 40 times faster. If you need smashing performance, get yourself some Gin.](https://github.com/gin-gonic/gin)

[go-bootstrap: Generates a lean and mean Go web project](http://go-bootstrap.io/)

### CLI

[spf13/cobra: A Commander for modern Go CLI interactions](https://github.com/spf13/cobra)
[spf13/viper: Go configuration with fangs](https://github.com/spf13/viper)

[gdamore/tcell: Tcell is an alternate terminal package, similar in some ways to termbox, but better in others.](https://github.com/gdamore/tcell)
[marcusolsson/tui-go: A UI library for terminal applications.](https://github.com/marcusolsson/tui-go)
[rivo/tview: Rich interactive widgets for terminal-based UIs written in Go](https://github.com/rivo/tview)

[AlecAivazis/survey: A golang library for building interactive prompts with full support for windows and posix terminals.](https://github.com/AlecAivazis/survey)

### Database/ORM

[sql - The Go Programming Language](https://golang.org/pkg/database/sql/)
[Go database/sql tutorial](http://go-database-sql.org/index.html)
[go-pg/pg: Golang ORM with focus on PostgreSQL features and performance](https://github.com/go-pg/pg)

## Installed Packages

```sh
go get -u github.com/golang/lint/golint
```

With Docker:
[Go + Docker = ♥](http://jpetazzo.github.io/2016/09/09/go-docker/)

# Learn

## Official

[DevDocs/Go](http://devdocs.io/go/)
[Documentation - The Go Programming Language](http://golang.org/doc/)
[The Go Programming Language Specification - The Go Programming Language](http://golang.org/ref/spec)

[Talks - The Go Programming Language](https://talks.golang.org/)

[A Tour of Go](http://tour.golang.org/), [solutions](https://github.com/golang/tour/tree/master/solutions)
[How to Write Go Code - The Go Programming Language](http://golang.org/doc/code.html)
[Effective Go - The Go Programming Language](http://golang.org/doc/effective_go.html)
[Frequently Asked Questions (FAQ) - The Go Programming Language](http://golang.org/doc/faq)
[Wiki Pages - go-wiki - Go Language Community Wiki - Google Project Hosting](https://code.google.com/p/go-wiki/w/list)

[Neither self nor this: Receivers in Go | Heroku](https://blog.heroku.com/neither-self-nor-this-receivers-in-go)

[Go Dynamic Tools](https://talks.golang.org/2015/dynamic-tools.slide)

[Golang UK Conference 2015 - Andrew Gerrand - Stupid Gopher Tricks - YouTube](https://www.youtube.com/watch?v=UECh7X07m6E) [slides](https://talks.golang.org/2015/tricks.slide)

## Design

[Go at Google: Language Design in the Service of Software Engineering](http://talks.golang.org/2012/splash.article)
[Analysis of the Go runtime scheduler](http://www1.cs.columbia.edu/~aho/cs6998/reports/12-12-11_DeshpandeSponslerWeiss_GO.pdf)
[Scalable Go Scheduler Design Doc - Google Docs](https://docs.google.com/document/d/1TTj4T2JO42uD5ID9e89oa0sLKhJYD0Y_kqxDv3I3XMw/edit)

[Keeping up with the Gophers](https://talks.golang.org/2015/keeping-up.slide#1)

[GopherCon 2015: Andrew Gerrand - Closing Keynote - YouTube](https://www.youtube.com/watch?v=0ht89TxZZnk) [How Go was made](https://talks.golang.org/2015/how-go-was-made.slide#2)

## Videos

[The Go Programming Language - YouTube](https://www.youtube.com/watch?v=rKnDgT73v8s&feature=related) Rob Pike 2009
[Go Programming - YouTube](https://www.youtube.com/watch?v=CF9S4QZuV30)
[Go Language Programming Practical Basics Tutorial - YouTube](https://www.youtube.com/playlist?list=PLQVvvaa0QuDeF3hP0wQoSxpkqgRcgxMqX)
[Go Programming Language Tutorials - Todd McLeod - YouTube](https://www.youtube.com/playlist?list=PL6cactdCCnTI1RH7kGY7nGT13gj6yMzvX)
[Writing, building, installing, and testing Go code - YouTube](https://www.youtube.com/watch?v=XCsL89YtqCs)
[Google I/O 2011: Writing Web Apps in Go - YouTube](https://www.youtube.com/watch?v=-i0hat7pdpk&feature=relmfu)

Building a Trie data structure.
[Tries - YouTube](https://www.youtube.com/watch?v=9HqbKLcxQmo)

## Go Blog

> collection of whitepaper-ish articles in Go Blog

[Article index - The Go Blog](http://blog.golang.org/index)
[Go Concurrency Patterns: Context - The Go Blog](http://blog.golang.org/context)
[Go Concurrency Patterns: Pipelines and cancellation - The Go Blog](http://blog.golang.org/pipelines)
[Inside the Go Playground - The Go Blog](http://blog.golang.org/playground)
[Text normalization in Go - The Go Blog](http://blog.golang.org/normalization)
[Strings, bytes, runes and characters in Go - The Go Blog](http://blog.golang.org/strings)
[Arrays, slices (and strings): The mechanics of 'append' - The Go Blog](http://blog.golang.org/slices)
[Introducing the Go Race Detector - The Go Blog](http://blog.golang.org/race-detector)
[Advanced Go Concurrency Patterns - The Go Blog](http://blog.golang.org/advanced-go-concurrency-patterns)
[Go maps in action - The Go Blog](http://blog.golang.org/go-maps-in-action)
[Concurrency is not parallelism - The Go Blog](http://blog.golang.org/concurrency-is-not-parallelism)
[The App Engine SDK and workspaces (GOPATH) - The Go Blog](http://blog.golang.org/the-app-engine-sdk-and-workspaces-gopath)
[Organizing Go code - The Go Blog](http://blog.golang.org/organizing-go-code)
[The Laws of Reflection - The Go Blog](http://blog.golang.org/laws-of-reflection)
[Error handling and Go - The Go Blog](http://blog.golang.org/error-handling-and-go)
[Profiling Go Programs - The Go Blog](http://blog.golang.org/profiling-go-programs)
[A GIF decoder: an exercise in Go interfaces - The Go Blog](http://blog.golang.org/gif-decoder-exercise-in-go-interfaces)
[Godoc: documenting Go code - The Go Blog](http://blog.golang.org/godoc-documenting-go-code)
[Gobs of data - The Go Blog](http://blog.golang.org/gobs-of-data)
[C? Go? Cgo! - The Go Blog](http://blog.golang.org/c-go-cgo)
[JSON and Go - The Go Blog](http://blog.golang.org/json-and-go)
[Go Slices: usage and internals - The Go Blog](http://blog.golang.org/go-slices-usage-and-internals)
[Go Concurrency Patterns: Timing out, moving on - The Go Blog](http://blog.golang.org/go-concurrency-patterns-timing-out-and)
[Defer, Panic, and Recover - The Go Blog](http://blog.golang.org/defer-panic-and-recover)
[Share Memory By Communicating - The Go Blog](http://blog.golang.org/share-memory-by-communicating)
[Go's Declaration Syntax - The Go Blog](http://blog.golang.org/gos-declaration-syntax)
[JSON-RPC: a tale of interfaces - The Go Blog](http://blog.golang.org/json-rpc-tale-of-interfaces)
[Go GC: Prioritizing low latency and simplicity - The Go Blog](http://blog.golang.org/go15gc)

## Book

[An Introduction to Programming in Go | Go Resources](http://www.golang-book.com/books/intro)
[Go Bootcamp | Softcover.io](http://www.golangbootcamp.com/book)
[Building Web Apps with Go - GitBook](https://www.gitbook.com/book/codegangsta/building-web-apps-with-go/details)
[The Little Go Book](https://www.openmymind.net/The-Little-Go-Book/)

## Third party

[Go by Example](https://gobyexample.com/)
[Learn Go in Y Minutes](http://learnxinyminutes.com/docs/go/)
[GoLang Tutorials](http://golangtutorials.blogspot.hk/2011/05/table-of-contents.html)
[GopherCasts](https://gophercasts.io/)
[Gopher Academy Blog](https://blog.gopheracademy.com/)
[Go (Golang) Programming Blog - Ardan Labs](https://www.ardanlabs.com/blog/)
[Learn Go Programming: A Tutorial with Code Examples | Toptal](https://www.toptal.com/go/go-programming-a-step-by-step-introductory-tutorial)
[Go Language Patterns](http://www.golangpatterns.info/)
[Go Code Tutorials by Envato Tuts+](https://code.tutsplus.com/categories/go)

[Applied Go · Applied Go](https://appliedgo.net/)
[Programming with Google Go | Coursera](https://www.coursera.org/specializations/google-golang)

## Concurrency

[Rob Pike - 'Concurrency Is Not Parallelism' - YouTube](https://www.youtube.com/watch?v=cN_DpYBzKso) [slides](https://talks.golang.org/2012/waza.slide)
[Go: code that grows with grace on Vimeo](https://vimeo.com/53221560) [slides](https://talks.golang.org/2012/chat.slide) using channels for chat, copy interface, matcher
[Google I/O 2012 - Go Concurrency Patterns - YouTube](https://www.youtube.com/watch?v=f6kdp27TYZs) [slides](https://talks.golang.org/2012/concurrency.slide)
[Google I/O 2013 - Advanced Go Concurrency Patterns - YouTube](https://www.youtube.com/watch?v=QDDwwePbDtw) [slide](https://talks.golang.org/2013/advconc.slide)
[Concurrency Patterns In Go - YouTube](https://www.youtube.com/watch?v=YEKjSzIwAdA)

[Visualizing Concurrency in Go · divan's blog](http://divan.github.io/posts/go_concurrency_visualize/)
[Goroutine IDs · Scott Mansfield](http://blog.sgmansfield.com/2015/12/goroutine-ids/)

[An Intro to Concurrency Patterns in Go - via @codeship | via @codeship](http://blog.codeship.com/an-intro-to-concurrency-patterns-in-go/)
[Concurrency in Go Part II - via @codeship | via @codeship](https://blog.codeship.com/concurrency-in-go-part-ii/)

[Patterns for scalable web services in Go](https://rcrowley.org/talks/strange-loop-2013.html)
[Go Microservices blog series, part 1. | Callista Enterprise](http://callistaenterprise.se/blogg/teknik/2017/02/17/go-blog-series-part1/)

[Introduction to Go - let's build a network application! | Go User Group Berlin](http://synflood.at/tmp/golang-slides/mrmcd2012.html)

## Generics

[Who needs generics? Use ... instead! · Applied Go](https://appliedgo.net/generics/)

[Summary of Go Generics Discussions](https://docs.google.com/document/d/1vrAy9gMpMoS3uaVphB32uVXX4pi-HnNjkMEgyAHX4N4/mobilebasic)

## Decorators

[Go 语言的修饰器编程 | | 酷 壳 - CoolShell](https://coolshell.cn/articles/17929.html)

## Testing

[Testing and Test-Driven-Development in Snap — Intel SDI — Medium](https://medium.com/intel-sdi/testing-and-test-driven-development-in-snap-d66359485561#.oc123kqcq)
[Testing and Test Driven Development in Snap (Part 2) — Intel SDI — Medium](https://medium.com/intel-sdi/testing-and-test-driven-development-in-snap-part-2-6304effa6b22#.ufy3wul7t)

[Getting Started In Testing Your Go Application | Toptal](https://www.toptal.com/go/your-introductory-course-to-testing-with-go)

## Tips and Tricks

[mitchellh/gox: A dead simple, no frills Go cross compile tool](https://github.com/mitchellh/gox)
[fatih/gomodifytags: Go tool to modify struct field tags](https://github.com/fatih/gomodifytags) for JSON serialization

[Go best practices, six years in](http://peter.bourgon.org/go-best-practices-2016/)
[Golang 新手开发需要注意的七个细节 |虞双齐的博客](https://www.yushuangqi.com/blog/2015/7_things-you-may-not-pay-attation-to-in-go.html)
[when nil is not nil - spf13.com](http://spf13.com/post/when-nil-is-not-nil/)
[7 common mistakes in Go (2015) - spf13.com](http://spf13.com/presentation/7-common-mistakes-in-go-2015/)
[★ Ultimate Visual Guide to Go Enums ★ – Learn Go Programming](https://blog.learngoprogramming.com/golang-const-type-enums-iota-bc4befd096d3)
[Trying Clean Architecture on Golang – Hacker Noon](https://hackernoon.com/golang-clean-archithecture-efd6d7c43047)
[The ultimate guide to writing a Go tool · Fatih Arslan](https://arslan.io/2017/09/14/the-ultimate-guide-to-writing-a-go-tool/)

## Visualization

[hirokidaichi/goviz: a visualization tool for golang project dependency](https://github.com/hirokidaichi/goviz)
[TrueFurby/go-callvis: Visualize call graph of your Go program using dot format.](https://github.com/TrueFurby/go-callvis)

## #perfmatters

[Go’s march to low-latency GC — Twitch Blog](https://blog.twitch.tv/gos-march-to-low-latency-gc-a6fa96f06eb7)
[Nitro : A quick and simple profiler for golang - spf13.com](http://spf13.com/project/nitro)
