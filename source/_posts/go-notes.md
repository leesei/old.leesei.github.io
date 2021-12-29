---
title: Go notes
date: 2015-02-16 17:58:42
categories:
  - comp.lang
tags:
  - golang
  - package-manager
  - notes
toc: true
---

> materials before 2019 should probably be removed

[The Go Programming Language](https://golang.org/)
[Go (programming language) - Wikiwand](<https://www.wikiwand.com/en/Go_(programming_language)>)
[Go 1.17 Release Notes - go.dev](https://go.dev/doc/go1.17)
[What reasons are there to not use Go (programming language)? - Quora](https://www.quora.com/What-reasons-are-there-to-not-use-Go-programming-language)

[Go 1 and the Future of Go Programs - go.dev](https://go.dev/doc/go1compat)
[How to Write Go Code - go.dev](https://go.dev/doc/code)
[Learn Go Programming - Golang Tutorial for Beginners - YouTube](https://www.youtube.com/watch?v=YS4e4q9oBaU)
[Getting started with VS Code Go - YouTube](https://www.youtube.com/watch?v=1MXIGYrMk80) 2021-01

[Awesome Go](https://awesome-go.com/)
[avelino/awesome-go: A curated list of awesome Go frameworks, libraries and software](https://github.com/avelino/awesome-go)
[tenntenn/gopher-stickers: gopher stickers](https://github.com/tenntenn/gopher-stickers)
[travis-ci/gimme: Install go, yay!](https://github.com/travis-ci/gimme) `nvm` for Go

[Tap the power of Google's Go language | InfoWorld](http://www.infoworld.com/article/3190210/application-development/tap-the-power-of-googles-go-language.html)
[Understand Go in 5 minutes - Je suis un dev](https://www.jesuisundev.com/en/understand-go-in-5-minutes/)
[Practical Go – The acme of foolishness](https://dave.cheney.net/practical-go)

[go command - cmd/go - pkg.go.dev](https://pkg.go.dev/cmd/go)

[Building A Queue - Part 1](https://www.openmymind.net/Building-A-Queue-Part-1/)
[Building A Queue - Part 2](https://www.openmymind.net/Building-A-Queue-Part-2/)
[Building A Queue - Part 3](https://www.openmymind.net/Building-A-Queue-Part-3/)
[Building A Queue - Part 4](https://www.openmymind.net/Building-A-Queue-Part-4/)

```sh
go run a.go
go build a.go
go run -x -v a.go
go build -x -v a.go

go build -v PACKAGE
env GOOS=linux GOARCH=arm go build -v PACKAGE

go run folder
go build folder
```

## Version Manager

[Go Version manager — gobrew. Install and manage Go versions on Mac… | by pulkit kathuria | web-developer | Medium](https://medium.com/web-developer/go-version-manager-gobrew-c8750157dfe6)

[kevincobain2000/gobrew: Go version manager. Super simple tool to install and manage Go versions. Install go without root. Gobrew doesn't require shell rehash.](https://github.com/kevincobain2000/gobrew)

[stefanmaric/g: Simple go version manager, gluten-free](https://github.com/stefanmaric/g)

[syndbg/goenv: Like pyenv and rbenv, but for Go.](https://github.com/syndbg/goenv)

[moovweb/gvm: Go Version Manager](https://github.com/moovweb/gvm) requires several host tools

## Go 2

[Toward Go 2 - go.dev](https://go.dev/blog/toward-go2)
[Go2 · golang/go Wiki](https://github.com/golang/go/wiki/Go2)
[Go 2 Draft Designs - go.dev](https://go.dev/blog/go2draft)
[Go 2 Draft Designs](https://go.googlesource.com/proposal/+/master/design/go2draft.md)

[Go team proposes parametric polymorphism • DEVCLASS](https://devclass.com/2019/07/30/go-team-proposes-parametric-polymorphism/)

## godoc

```sh
godoc -http=":6060"
# docs for all installed packages at http://localhost:6060/pkg

godoc pkg Label  # look up function/type
```

[Godoc: documenting Go code - go.dev](https://go.dev/blog/godoc)
[Static analysis features of godoc - go.dev](https://go.dev/lib/godoc/analysis/help)

[Golds -Go 101](https://go101.org/apps-and-libs/golds.html)
[go101/golds: An experimental Go local docs server/generator and code reader implemented with some fresh ideas.](https://github.com/go101/golds)

## Editor/IDE

[The best Go language IDEs and editors | InfoWorld](http://www.infoworld.com/article/3171158/application-development/the-best-go-language-ides-and-editors.html)

[Gopls on by default in the VS Code Go extension - go.dev](https://blog.golang.org/gopls-vscode-go)
[golang/vscode-go: Go extension for VS Code](https://github.com/golang/vscode-go/)
[vscode-go/features.md at master · golang/vscode-go](https://github.com/golang/vscode-go/blob/master/docs/features.md)
[GopherCon 2019: Rebecca Stambler - Go, pls stop breaking my editor - YouTube](https://www.youtube.com/watch?v=EFJfdWzBHwE) old way -> `gopls`

[LiteIDE X](http://liteide.org/en/)
[visualfc/liteide: LiteIDE is a simple, open source, cross-platform Go IDE.](https://github.com/visualfc/liteide)

## Commentary

[Comparing Elixir and Go - via @codeship | via @codeship](https://blog.codeship.com/comparing-elixir-go/)
[The success of Go heralds that of Rust – George Hosu – Medium](https://medium.com/@george3d6/the-success-of-go-heralds-that-of-rust-73cb2e4c0500)
[Go: the Good, the Bad and the Ugly](https://bluxte.net/musings/2018/04/10/go-good-bad-ugly/)
[What Go Programming Language does and does not have](https://medium.com/@amritpandey/what-go-programming-language-does-and-does-not-have-ed6a9f83ab2d)
[Why Go gets exceptions right | Dave Cheney](https://dave.cheney.net/2012/01/18/why-go-gets-exceptions-right)
[My reflections on Golang - DEV Community 👩‍💻👨‍💻](https://dev.to/deepu105/my-reflections-on-golang-38jk)
[Rust vs. Go: How to choose | InfoWorld](https://www.infoworld.com/article/3436960/rust-vs-go-how-to-choose.html)
[Why Go Is Not Good :: Will Yager](http://yager.io/programming/go.html)

## Compile

[containous/yaegi: Yaegi is Another Elegant Go Interpreter](https://github.com/containous/yaegi)

[How a Go Program Compiles down to Machine Code – Hacker Noon](https://hackernoon.com/how-a-go-program-compiles-down-to-machine-code-e4532dc8b8ca)

Use `-ldflags=-w` flag to disable DWARF to reduce binary size

[vladimirvivien/go-cshared-examples: Calling Go Functions from Other Languages using C Shared Libraries](https://github.com/vladimirvivien/go-cshared-examples) build `.so`

[gopherjs/gopherjs: A compiler from Go to JavaScript for running Go code in a browser](https://github.com/gopherjs/gopherjs)

[Introducing Joy](https://mat.tm/joy/)
[matthewmueller/joy: A delightful Go to Javascript compiler](https://github.com/matthewmueller/joy)
on hold in light of WASM target

[GoReleaser - GoReleaser](https://goreleaser.com/)

[Golang 跨平台交叉编译 | Tony Bai](https://tonybai.com/2014/10/20/cross-compilation-with-golang/)

```sh
# OSX
cd $GOROOT/src
sudo GOOS=darwin GOARCH=amd64 ./make.bash
GOOS=darwin GOARCH=amd64 go build
```

### Cgo

[C? Go? Cgo! - go.dev](https://go.dev/blog/cgo)
[cgo command - cmd/cgo - pkg.go.dev](https://pkg.go.dev/cmd/cgo)

[Go 与 C 语言的互操作 | Tony Bai](https://tonybai.com/2012/09/26/interoperability-between-go-and-c/)
[探讨 docker 容器对共享内存的支持情况 | Tony Bai](https://tonybai.com/2014/10/12/discussion-on-shared-mem-support-in-docker/)
[Python and Go : Part IV - Using Python in Memory](https://www.ardanlabs.com/blog/2020/09/using-python-memory.html)

## Packages

`go get` can retrieve packages given the URL
std package are located at `$GOROOT/pkg/<platform>/`
no std package are located at `$GOROOT/src/`

[Home · pkg.go.dev](https://pkg.go.dev/) package repository
[godocs.io](https://godocs.io/)
[Go Report Card | Go project code quality report cards](https://goreportcard.com/)

[Projects · golang/go Wiki](https://github.com/golang/go/wiki/Projects)
[golang-standards/project-layout: Standard Go Project Layout](https://github.com/golang-standards/project-layout)
[Package names - go.dev](https://go.dev/blog/package-names)

[The Go Programming Language Specification - go.dev](https://go.dev/ref/spec#Package_initialization) Package initialization
[The Go init Function | TutorialEdge.net](https://tutorialedge.net/golang/the-go-init-function/)

[Standard library - pkg.go.dev](https://pkg.go.dev/std)
[fs package - io/fs - pkg.go.dev](https://pkg.go.dev/io/fs)
[fmt package - fmt - pkg.go.dev](https://pkg.go.dev/fmt)
[log package - log - pkg.go.dev](https://pkg.go.dev/log)
[strings package - strings - pkg.go.dev](https://pkg.go.dev/strings)
[strconv package - strconv - pkg.go.dev](https://pkg.go.dev/strconv)
[reflect package - reflect - pkg.go.dev](https://pkg.go.dev/reflect)
[json package - encoding/json - pkg.go.dev](https://pkg.go.dev/encoding/json)

```go
fmt.Printf("%T\n", variable)  // print type of variable

// The next line prints: coco
fmt.Printf("%[2]v%[1]v%[2]v%[1]v", "o", "c")
```

[mobile module - golang.org/x/mobile - pkg.go.dev](https://pkg.go.dev/golang.org/x/mobile)
[golang/mobile: [mirror] Go on Mobile](https://github.com/golang/mobile/)

[mitchellh/protostructure: Encode and decode Go (golang) struct types via protocol buffers.](https://github.com/mitchellh/protostructure)
[ulikunitz/xz: Pure golang package for reading and writing xz-compressed files](https://github.com/ulikunitz/xz)
[mholt/archiver: Easily create & extract archives, and compress & decompress files of various formats](https://github.com/mholt/archiver)

[afero package - github.com/spf13/afero - pkg.go.dev](https://pkg.go.dev/github.com/spf13/afero)
[spf13/afero: A FileSystem Abstraction System for Go](https://github.com/spf13/afero)

### import

[goimports command - golang.org/x/tools/cmd/goimports - pkg.go.dev](https://pkg.go.dev/golang.org/x/tools/cmd/goimports)

[理解 Go import |虞双齐的博客](https://www.yushuangqi.com/blog/2016/understanding-golang-import-package.html)
[理解 Golang 包导入 | Tony Bai](https://tonybai.com/2015/03/09/understanding-import-packages/)

```go
// Import declaration       Local name of Sin
import   "lib/math"         math.Sin
import m "lib/math"         m.Sin
import . "lib/math"         Sin  // include symbols to local namespace
import _ "lib/math"         // subpress unused warning, run init, no load symbol
```

### Dependency Management

[Managing dependencies - The Go Programming Language](https://golang.org/doc/modules/managing-dependencies)
[PackageManagementTools · golang/go Wiki](https://github.com/golang/go/wiki/PackageManagementTools)
[The Saga of Go Dependency Management GopherAcademy](https://blog.gopheracademy.com/advent-2016/saga-go-dependency-management/)
[go 打包机制 | 李乾坤的博客](https://qiankunli.github.io/2020/03/15/go_package.html)

#### Modules

> alternative to GOPATH, added in Go 1.11 (2018-08), default in Go 1.14 (2020-02)

[Go Modules in 2019 - go.dev](https://go.dev/blog/modules2019) plan for 2019
[Using Go Modules - go.dev](https://go.dev/blog/using-go-modules) 2019-03, 5 part series
[Modules · golang/go Wiki](https://github.com/golang/go/wiki/Modules)
[Go Modules Reference - The Go Programming Language](https://golang.org/ref/mod)

[Introduction to Go Modules – Roberto Selbach](https://roberto.selbach.dev/intro-to-go-modules/)
[跳出 Go module 的泥潭 | 鸟窝](https://colobu.com/2018/08/27/learn-go-module/) 1.11
[Go module 再回顾 | 鸟窝](https://colobu.com/2019/09/23/review-go-module-again/) 1.13

[Modules Part 01: Why And What](https://www.ardanlabs.com/blog/2019/10/modules-01-why-and-what.html)
[Modules Part 02: Projects, Dependencies and Gopls](https://www.ardanlabs.com/blog/2019/12/modules-02-projects-dependencies-gopls.html)
[Modules Part 03: Minimal Version Selection](https://www.ardanlabs.com/blog/2019/12/modules-03-minimal-version-selection.html)
[Modules Part 04: Mirrors, Checksums and Athens](https://www.ardanlabs.com/blog/2020/02/modules-04-mirros-checksums-athens.html)
[Modules Part 05: Gopls Improvements](https://www.ardanlabs.com/blog/2020/04/modules-05-gopls-improvements.html)
[Modules Part 06: Vendoring](https://www.ardanlabs.com/blog/2020/04/modules-06-vendoring.html)

[Packages and Modules in Go (Golang) - Part 1 - Welcome To Golang By Example](https://golangbyexample.com/packages-modules-go-first/)
[Packages and Modules in Go (Golang) - Part 2 - Welcome To Golang By Example](https://golangbyexample.com/packages-modules-go-second/)

```sh
go mod init  # init project
go mod tidy  # sync `go.mod` with project
```

#### dep

> obsolete

[Dependency Management Tool - Google Docs](https://docs.google.com/document/d/1qnmjwfMmvSCDaY4jxPmLAccaaUI5FfySNE90gB0pTKQ/edit#)

[golang/dep: Go dependency management tool experiment (deprecated)](https://github.com/golang/dep)
[Go 1.11 Modules (vgo) vs dep · Issue #1959 · golang/dep](https://github.com/golang/dep/issues/1959)

### Vendoring

> obsolete, `go mod` can use `vendor/` though

[Go Modules Reference - The Go Programming Language](https://golang.org/ref/mod#vendoring)
[Go 1.5 Vendor Experiment](https://go.googlesource.com/proposal/+/master/design/25719-go15vendor.md)
[Go Modules Reference - go.dev](https://go.dev/ref/mod#vendoring) `vendor/modules.txt` in `go.mod`

Go's `vendor/` = Node's `node_modules/`
import from project local instead of `GOPATH`
default in Go 1.7

### web

[RESTful routing in Go](https://www.openmymind.net/RESTful-routing-in-Go/)
[Go actions responses](https://www.openmymind.net/Go-action-responses/)

[speedwheel/awesome-go-web-frameworks: You may not need a web framework if you design a small application for yourself, but if you're going production then you definitely will need one, a good one.](https://github.com/speedwheel/awesome-go-web-frameworks)

[Golang: 6 must-have web frameworks for the Google Go language | InfoWorld](https://www.infoworld.com/article/3274464/web-development/6-must-have-web-frameworks-for-the-google-go-language.html)
[go-bootstrap: Generates a lean and mean Go web project](http://go-bootstrap.io/)

[Gin Web Framework](https://gin-gonic.com/)
[gin-gonic/gin: Gin is a HTTP web framework written in Go (Golang). It features a Martini-like API with much better performance -- up to 40 times faster. If you need smashing performance, get yourself some Gin.](https://github.com/gin-gonic/gin)
[go-martini/martini: Classy web framework for Go](https://github.com/go-martini/martini) no longer maintained
[gorilla/mux: A powerful URL router and dispatcher for golang.](https://github.com/gorilla/mux)

[Welcome - Fiber](https://docs.gofiber.io/)
[Create a Restful API with Golang from scratch - DEV Community](https://dev.to/pacheco/create-a-restful-api-with-golang-from-scratch-42g2)

[Introduction · go-zero document](https://go-zero.dev/en/)
[GitHub - zeromicro/go-zero: go-zero is a web and rpc framework written in Go. It's born to ensure the stability of the busy sites with resilient design. Builtin goctl greatly improves the development productivity.](https://github.com/zeromicro/go-zero)
[熔断原理与实现 Golang 版 - InfoQ 写作平台](https://xie.infoq.cn/article/3b8bd23dd808e28b8e230d527)

#### Iris

[Iris Web Framework](https://iris-go.com/)
[kataras/iris: 感谢中国开发者 - https://bit.ly/謝謝 | The fastest community-driven web framework for Go. Webassembly, Automatic HTTPS with Public Domain, MVC, Sessions, Caching, Versioning API, Problem API, Websocket, Dependency Injection and more. Fully compatible with the standard library and 3rd-party middleware packages. | https://bit.ly/iriscandothat1 | https://bit.ly/iriscandothat3 |](https://github.com/kataras/iris)
[kataras/iris-cli: [WIP] Iris Command Line Interface](https://github.com/kataras/iris-cli)

### CLI

[Writing Friendly Command Line Applications | Gopher Academy Blog](https://blog.gopheracademy.com/advent-2019/cmdline/)
[Fun With Flags | Gopher Academy Blog](https://blog.gopheracademy.com/advent-2019/flags/)
[Building an Awesome CLI App in Go – OSCON 2017 - spf13.com](https://spf13.com/presentation/building-an-awesome-cli-app-in-go-oscon/)
[flag package - flag - pkg.go.dev](https://pkg.go.dev/flag) CLI args parser

[Cobra. Dev](https://cobra.dev/)
[spf13/cobra: A Commander for modern Go CLI interactions](https://github.com/spf13/cobra)
[spf13/viper: Go configuration with fangs](https://github.com/spf13/viper)
[Building an Awesome CLI App in Go – OSCON 2017 - spf13.com](https://spf13.com/presentation/building-an-awesome-cli-app-in-go-oscon/) From slide 134

[gdamore/tcell: Tcell is an alternate terminal package, similar in some ways to termbox, but better in others.](https://github.com/gdamore/tcell)
[marcusolsson/tui-go: A UI library for terminal applications.](https://github.com/marcusolsson/tui-go)
[rivo/tview: Rich interactive widgets for terminal-based UIs written in Go](https://github.com/rivo/tview)

[AlecAivazis/survey: A golang library for building interactive prompts with full support for windows and posix terminals.](https://github.com/AlecAivazis/survey)

[urfave/cli: A simple, fast, and fun package for building command line apps in Go](https://github.com/urfave/cli)

[bitfield/script: Making it easy to write shell-like scripts in Go](https://github.com/bitfield/script)

### Resource embedding

[embed package - embed - pkg.go.dev](https://pkg.go.dev/embed)

[v0x.nl - Portable apps with Go and Next.js](https://v0x.nl/articles/portable-apps-go-nextjs)

### Database/ORM

[sql - The Go Programming Language](https://golang.org/pkg/database/sql/)
[Go database/sql tutorial](http://go-database-sql.org/index.html)
[go-pg/pg: Golang ORM with focus on PostgreSQL features and performance](https://github.com/go-pg/pg)

[GORM - The fantastic ORM library for Golang, aims to be developer friendly.](https://gorm.io/)

[Working with SQLite using Go and Python](https://www.ardanlabs.com/blog/2020/11/working-with-sqlite-using-go-python.html)

[rocketlaunchr/dbq: Zero boilerplate database operations for Go](https://github.com/rocketlaunchr/dbq)

## Installed Packages

```sh
go get -u github.com/golang/lint/golint
```

With Docker:
[Go + Docker = ♥](https://jpetazzo.github.io/2016/09/09/go-docker/)

# Learn

## Official

[Documentation - The Go Programming Language](https://golang.org/doc/)
[The Go Programming Language Specification - The Go Programming Language](https://golang.org/ref/spec)
[DevDocs/Go](https://devdocs.io/go/) standard library

[Talks - The Go Programming Language](https://talks.golang.org/)

[Get Started - go.dev](https://go.dev/learn/)
[A Tour of Go](https://tour.golang.org/), [solutions](https://github.com/golang/tour/tree/master/solutions)
[How to Write Go Code - The Go Programming Language](https://golang.org/doc/code)
[Effective Go - The Go Programming Language](https://golang.org/doc/effective_go.html)
[Frequently Asked Questions (FAQ) - The Go Programming Language](https://golang.org/doc/faq)
[Home · golang/go Wiki](https://github.com/golang/go/wiki)
[pityonline/learn-go-with-tests](https://github.com/pityonline/learn-go-with-tests)

[Neither self nor this: Receivers in Go | Heroku](https://blog.heroku.com/neither-self-nor-this-receivers-in-go)

[Go Dynamic Tools](https://talks.golang.org/2015/dynamic-tools.slide)

[Golang UK Conference 2015 - Andrew Gerrand - Stupid Gopher Tricks - YouTube](https://www.youtube.com/watch?v=UECh7X07m6E) [slides](https://talks.golang.org/2015/tricks.slide)

## Design

Golang `map[string]struct{}` can be used as a Set type where every element is unique.

[Go at Google: Language Design in the Service of Software Engineering - go.dev](https://go.dev/talks/2012/splash.article)
[Analysis of the Go runtime scheduler](http://www1.cs.columbia.edu/~aho/cs6998/reports/12-12-11_DeshpandeSponslerWeiss_GO.pdf)
[Scalable Go Scheduler Design Doc - Google Docs](https://docs.google.com/document/d/1TTj4T2JO42uD5ID9e89oa0sLKhJYD0Y_kqxDv3I3XMw/edit)

[The Why of Go - YouTube](https://www.youtube.com/watch?v=bmZNaUcwBt4)

[Keeping up with the Gophers](https://talks.golang.org/2015/keeping-up.slide#1)

[Principles of designing Go APIs with channels - inconshreveable](https://inconshreveable.com/07-08-2014/principles-of-designing-go-apis-with-channels/)

[GopherCon 2015: Andrew Gerrand - Closing Keynote - YouTube](https://www.youtube.com/watch?v=0ht89TxZZnk) [How Go was made](https://talks.golang.org/2015/how-go-was-made.slide#2)

## Data Structures

[research!rsc: Go Data Structures](https://research.swtch.com/godata)
[research!rsc: Data Structures Go Programs](https://research.swtch.com/godata2)

[Arrays, Slices and Maps in Go -Go 101](https://go101.org/article/container.html)

[The results of `reflect.DeepEqual(x, y)` and `x == y` may be different. -Go 101](https://go101.org/article/details.html#reflect-deep-equal)

Function values are equal only if both are nil and their types are identical.

### Array/Slices

[Arrays, slices (and strings): The mechanics of 'append' - go.dev](https://go.dev/blog/slices)
[Go Slices: usage and internals - go.dev](https://go.dev/blog/slices-intro)

### Maps

[Go maps in action - go.dev](https://go.dev/blog/maps)

[Maps -Go 101](https://go101.org/optimizations/6-map.html)

- using pointers (`string` included) in key/value adds pressure to GC
- `delete(m. key)` will not free up the backing array

[dictionary - Computing the memory footprint (or byte length) of a map - Stack Overflow](https://stackoverflow.com/questions/31847549/computing-the-memory-footprint-or-byte-length-of-a-map) 2015

### Struct

[Structs in Go -Go 101](https://go101.org/article/struct.html)

```go
type S = struct {
	X byte
	_ [7]byte  // blank field for padding
	Y int32
}
```

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

[Article index - go.dev](https://go.dev/blog/all)
[Inside the Go Playground - go.dev](https://go.dev/blog/playground)
[Text normalization in Go - go.dev](https://go.dev/blog/normalization)
[Strings, bytes, runes and characters in Go - go.dev](https://go.dev/blog/strings)
[The App Engine SDK and workspaces (GOPATH) - go.dev](https://go.dev/blog/appengine-gopath)
[Gobs of data - go.dev](https://go.dev/blog/gob)
[JSON and Go - go.dev](https://go.dev/blog/json)
[Go's Declaration Syntax - go.dev](https://go.dev/blog/declaration-syntax)

## Book

[Books · golang/go Wiki · GitHub](https://github.com/golang/go/wiki/Books)

[dariubs/GoBooks: List of Golang books](https://github.com/dariubs/GoBooks)
[stormtrooper96/books](https://github.com/stormtrooper96/books)

[Go Bootcamp | Softcover.io](http://www.golangbootcamp.com/book/_single-page) !important, concise, reference to official doc
[Go 101 - Go 101: an online Go programming book + knowledge base](https://go101.org/article/101.html) !important
[An Introduction to Programming in Go | Go Resources](http://www.golang-book.com/books/intro)
[Introducing Go -O'Reilly Media](http://shop.oreilly.com/product/0636920046516.do)
[The Little Go Book](https://www.openmymind.net/The-Little-Go-Book/)

[开源图书在线阅读 - Go 语言中文网 - Golang 中文社区](https://books.studygolang.com/)

## Third party

[10 Free Resources To Learn Go Programming Language](https://analyticsindiamag.com/10-free-resources-to-learn-go-programming-language/amp/)
[The Top 10 Places to Learn Go - DEV Community 👩‍💻👨‍💻](https://dev.to/pluralsight/the-top-10-places-to-learn-go-3lhp)
[Golang Tutorial Guide – A List of Free Courses to Learn the Go Programming Language](https://www.freecodecamp.org/news/golang-tutorial-list-free-courses-learn-go-programming-language/amp/)
[cdarwin/go-koans: koans for go](https://github.com/cdarwin/go-koans)
[Golang-challenge – We offers the best mobile tutorials for android and ios devices.](https://golang-challenge.com/)
[Gophercises - Coding exercises for budding gophers](https://gophercises.com/)
[Golang examples and solutions from different packages of the standard library. - golangprograms.com](https://www.golangprograms.com/golang-package-examples.html)

[Go by Example](https://gobyexample.com/)
[Golang Advanced Tutorial - Welcome To Golang By Example](https://golangbyexample.com/golang-comprehensive-tutorial/)
[Learn Go in Y Minutes](http://learnxinyminutes.com/docs/go/)
[GoLang Tutorials](http://golangtutorials.blogspot.hk/2011/05/table-of-contents.html)
[Go on Exercism](https://exercism.org/tracks/go)
[GopherCasts](https://gophercasts.io/)
[Home - Practical Go Lessons Book](https://www.practical-go-lessons.com/)
[Gopher Academy Blog](https://blog.gopheracademy.com/)
[Go (Golang) Programming Blog - Ardan Labs](https://www.ardanlabs.com/blog/)
[Learn Go Programming: A Tutorial with Code Examples | Toptal](https://www.toptal.com/go/go-programming-a-step-by-step-introductory-tutorial)
[Go Language Patterns](http://www.golangpatterns.info/)
[Go go-to guide · YourBasic](https://yourbasic.org/golang/)
[Golang tutorial: Table Of Contents](https://golangbot.com/learn-golang-series/)
[Go Code Tutorials by Envato Tuts+](https://code.tutsplus.com/categories/go)
[Getting started with Go for frontend developers - LogRocket Blog](https://blog.logrocket.com/getting-started-with-go-for-frontend-developers/)
[Let's Eat GO ! 實務開發雜談 by Golang :: 第 11 屆 iThome 鐵人賽](https://ithelp.ithome.com.tw/users/20080192/ironman/2194)

[Applied Go · Applied Go](https://appliedgo.net/)
[Programming with Google Go | Coursera](https://www.coursera.org/specializations/google-golang)

[aodin/golang-for-pythonistas: Advanced topics for Python programmers looking to use Go](https://github.com/aodin/golang-for-pythonistas)

[Golang for JavaScript developers - Part 1 - DEV Community 👩‍💻👨‍💻](https://dev.to/deepu105/golang-for-javascript-developers-part-1-38je)
[Golang for JavaScript developers - Part 2 - DEV Community 👩‍💻👨‍💻](https://dev.to/deepu105/golang-for-javascript-developers-part-2-p3p)

[mholt/meetupchat: Simple chat using TCP, as a quick workshop for beginner (Go) programmers](https://github.com/mholt/meetupchat)

[The Go Blog - go.dev](https://go.dev/blog/)
[Go – The acme of foolishness](https://dave.cheney.net/category/golang)
[Go (Golang) Programming Blog - Ardan Labs](https://www.ardanlabs.com/categories/go-programing/)
[Golang Development | TutorialEdge.net](https://tutorialedge.net/golang/)

## Internals

[src/ - go.dev](https://go.dev/src/)

[research!rsc: Broken abstractions in Go](https://research.swtch.com/goabstract) `go` and `defer` implementation

[Scheduling In Go : Part I - OS Scheduler](https://www.ardanlabs.com/blog/2018/08/scheduling-in-go-part1.html)
[Scheduling In Go : Part II - Go Scheduler](https://www.ardanlabs.com/blog/2018/08/scheduling-in-go-part2.html)
[Scheduling In Go : Part III - Concurrency](https://www.ardanlabs.com/blog/2018/12/scheduling-in-go-part3.html)

## `==`

> How `==` works?

```go
var a, b interface{} = []int{1, 2}, []int{1, 2}
fmt.Println(reflect.DeepEqual(a, b)) // true
fmt.Println(a == b)                  // panic
```

`x == y` will panic if the two operands are both interface values and their dynamic types are _identical_ and _incomparable_.

```go
var s2 = "abc"[0:0]
fmt.Println(s2 == "") // true
fmt.Println(*(*uintptr)(unsafe.Pointer(&s2))) // 4869856
fmt.Println(s1 == s2) // true
```

```go
func returnsError() error {
	var p *MyError = nil
	if bad() {
		p = ErrBad
	}
	return p // Will always return a non-nil error.
}
```

Following types don't support comparisons:

- map
- slice
- function
- struct types containing incomparable fields
- array types with incomparable element types

Types which don't support comparisons can't be used as the key type of map types.

Please note,

- although map, slice and function types don't support comparisons, their values can be compared to the bare `nil` identifier.
- [comparing two interface values](https://go101.org/article/interface.html#comparison) with `==` will panic at run time if the two dynamic types of the two interface values are identical and incomparable.

On why slice, map and function types don't support comparison, please read [this answer](https://golang.org/doc/faq#map_keys) in the official Go FAQ.

### Memory

[The Go Memory Model - go.dev](https://go.dev/ref/mem)
[research!rsc: Memory Models](https://research.swtch.com/mm)
[go 内存管理 | 李乾坤的博客](https://qiankunli.github.io/2020/11/22/go_mm.html)
[Memory Layouts -Go 101](https://go101.org/article/memory-layout.html)
[Memory Blocks -Go 101](https://go101.org/article/memory-block.html)
[A visual guide to Go Memory Allocator from scratch (Golang) | by Ankur Anand | Medium](https://medium.com/@ankur_anand/a-visual-guide-to-golang-memory-allocator-from-ground-up-e132258453ed)
[🚀 Visualizing memory management in Golang | Technorage](https://deepu.tech/memory-management-in-golang/)

[Getting to Go: The Journey of Go's Garbage Collector - go.dev](https://go.dev/blog/ismmkeynote)
[Go GC: Prioritizing low latency and simplicity - go.dev](https://go.dev/blog/go15gc)
[Go’s march to low-latency GC — Twitch Blog](https://blog.twitch.tv/gos-march-to-low-latency-gc-a6fa96f06eb7)

[Garbage Collection In Go : Part I - Semantics](https://www.ardanlabs.com/blog/2018/12/garbage-collection-in-go-part1-semantics.html)
[Garbage Collection In Go : Part II - GC Traces](https://www.ardanlabs.com/blog/2019/05/garbage-collection-in-go-part2-gctraces.html)
[Garbage Collection In Go : Part III - GC Pacing](https://www.ardanlabs.com/blog/2019/07/garbage-collection-in-go-part3-gcpacing.html)

## Concurrency

[Concurrency is not parallelism - go.dev](https://go.dev/blog/waza-talk)
[Advanced Go Concurrency Patterns - go.dev](https://go.dev/blog/io2013-talk-concurrency)
[Go Concurrency Patterns: Pipelines and cancellation - go.dev](https://go.dev/blog/pipelines)
[Go Concurrency Patterns: Timing out, moving on - go.dev](https://go.dev/blog/go-concurrency-patterns-timing-out-and)

[Rob Pike - 'Concurrency Is Not Parallelism' - YouTube](https://www.youtube.com/watch?v=cN_DpYBzKso) [slides](https://talks.golang.org/2012/waza.slide)
[Go: code that grows with grace on Vimeo](https://vimeo.com/53221560) [slides](https://talks.golang.org/2012/chat.slide) using channels for chat, copy interface, matcher
[Google I/O 2012 - Go Concurrency Patterns - YouTube](https://www.youtube.com/watch?v=f6kdp27TYZs) [slides](https://talks.golang.org/2012/concurrency.slide)
[Google I/O 2013 - Advanced Go Concurrency Patterns - YouTube](https://www.youtube.com/watch?v=QDDwwePbDtw) [slide](https://talks.golang.org/2013/advconc.slide)
[Concurrency Patterns In Go - YouTube](https://www.youtube.com/watch?v=YEKjSzIwAdA)
[dotgo applied concurrency in go](https://matt.aimonetti.net/posts/2015-12-dotgo-applied-concurrency-in-go/)

use `chan struct{}` to signify that this is a channel for event/signal

[Go Concurrency from the Ground Up | doxsey.net](https://www.doxsey.net/blog/go-concurrency-from-the-ground-up/)
[Visualizing Concurrency in Go · divan's blog](http://divan.github.io/posts/go_concurrency_visualize/)
[Goroutine IDs · Scott Mansfield](http://blog.sgmansfield.com/2015/12/goroutine-ids/)
[Share Memory By Communicating - go.dev](https://go.dev/blog/codelab-share)
[Codewalk: Share Memory By Communicating - go.dev](https://go.dev/doc/codewalk/sharemem/)

[Goroutine Leaks - The Forgotten Sender](https://www.ardanlabs.com/blog/2018/11/goroutine-leaks-the-forgotten-sender.html)
[Goroutine Leaks - The Abandoned Receivers](https://www.ardanlabs.com/blog/2018/12/goroutine-leaks-the-abandoned-receivers.html)
[Concurrency Trap #2: Incomplete Work](https://www.ardanlabs.com/blog/2019/04/concurrency-trap-2-incomplete-work.html)

[An Intro to Concurrency Patterns in Go - via @codeship | via @codeship](http://blog.codeship.com/an-intro-to-concurrency-patterns-in-go/)
[Concurrency in Go Part II - via @codeship | via @codeship](https://blog.codeship.com/concurrency-in-go-part-ii/)
[Patterns for scalable web services in Go](https://rcrowley.org/talks/strange-loop-2013.html)

[Go Microservices blog series, part 1. | Callista Enterprise](http://callistaenterprise.se/blogg/teknik/2017/02/17/go-blog-series-part1/)

[go - Multiple goroutines listening on one channel - Stack Overflow](https://stackoverflow.com/questions/15715605/multiple-goroutines-listening-on-one-channel)

[Introduction to Go - let's build a network application! | Go User Group Berlin](http://synflood.at/tmp/golang-slides/mrmcd2012.html)
[Directional Channels in Go | Gopher Academy Blog](https://blog.gopheracademy.com/advent-2019/directional-channels/)

### Context

[context package - context - pkg.go.dev](https://pkg.go.dev/context)

[Go Concurrency Patterns: Context - go.dev](https://go.dev/blog/context)
[Context Package Semantics In Go](https://www.ardanlabs.com/blog/2019/09/context-package-semantics-in-go.html)

### Data Race

[Introducing the Go Race Detector - go.dev](https://go.dev/blog/race-detector)
[Data races explained · YourBasic Go](https://yourbasic.org/golang/data-races-explained/)
[Data races in Go(Golang) and how to fix them](https://www.sohamkamani.com/golang/data-races/)
[谈谈 Golang 中的 Data Race - poslua | ms2008 Blog](https://ms2008.github.io/2019/05/12/golang-data-race/)

## Date time

[time package - time - pkg.go.dev](https://pkg.go.dev/time)
[time package - Duration - pkg.go.dev](https://pkg.go.dev/time?utm_source=godoc#Duration)

Use reference time (`2006-01-02T15:04:05Z07:00`) to define layout
[src/time/format.go - The Go Programming Language](https://golang.org/src/time/format.go)

[Time Conversion in Go (Golang) - Welcome To Golang By Example](https://golangbyexample.com/time-conversion-in-golang/)

## regex

> see `regex.md#go`

## Typing/Reflection

[Go Type System Overview -Go 101](https://go101.org/article/type-system-overview.html)
[Value Conversion, Assignment and Comparison Rules in Go -Go 101](https://go101.org/article/value-conversions-assignments-and-comparisons.html)

[reflect package - reflect - pkg.go.dev](https://pkg.go.dev/reflect)
[Effective Go - go.dev](https://go.dev/doc/effective_go#type_switch) Type switch/guard with type `T.(type)`
[The Laws of Reflection - go.dev](https://go.dev/blog/laws-of-reflection)
[A GIF decoder: an exercise in Go interfaces - go.dev](https://go.dev/blog/gif-decoder-exercise-in-go-interfaces)

[research!rsc: Go Data Structures: Interfaces](https://research.swtch.com/interfaces)
[How to use interfaces in Go - jordan orelli](https://jordanorelli.com/post/32665860244/how-to-use-interfaces-in-go)
[Reflection in Go: Use cases and tutorial - LogRocket Blog](https://blog.logrocket.com/reflection-go-use-cases-tutorial/)
[reflection - How get pointer of struct's member from interface{} - Stack Overflow](https://stackoverflow.com/questions/27992821/how-get-pointer-of-structs-member-from-interface)

Under the covers, interfaces are implemented as two elements, a type T and a value V.  
An interface value is `nil` only if the `V` and `T` are both unset, (`T=nil`, `V` is not set), In particular, a `nil` interface will always hold a `nil` type. If we store a `nil` pointer of type `*int` inside an interface value, the inner type will be `*int` regardless of the value of the pointer: (`T=*int`, `V=nil`). Such an interface value will therefore be non-`nil` _even when the pointer value `V` inside is_ `nil`.

```go
var r io.Reader
tty, err := os.OpenFile("/dev/tty", os.O_RDWR, 0)
r = tty

var w io.Writer
w = r.(io.Writer)  // type assertion
```

Type assertion is applicable to interface when you know the concrete type.
Type assertion is performed at runtime.
[Effective Go - go.dev](https://go.dev/doc/effective_go#interface_conversions)
[go - What is the difference between type conversion and type assertion? - Stack Overflow](https://stackoverflow.com/questions/20494229/what-is-the-difference-between-type-conversion-and-type-assertion)
[Type Assertions vs Type Conversions in Golang](https://www.sohamkamani.com/golang/type-assertions-vs-type-conversions/)

## Generics

[spec: add generic programming using type parameters · Issue #43651 · golang/go](https://github.com/golang/go/issues/43651)

[Who needs generics? Use ... instead! · Applied Go](https://appliedgo.net/generics/)

[Summary of Go Generics Discussions](https://docs.google.com/document/d/1vrAy9gMpMoS3uaVphB32uVXX4pi-HnNjkMEgyAHX4N4/mobilebasic)
[[ generics] Moving forward with the generics design draft](https://groups.google.com/g/golang-nuts/c/iAD0NBz3DYw/m/VcXSK55XAwAJ)

[Generics Part 01: Basic Syntax](https://www.ardanlabs.com/blog/2020/07/generics-01-basic-syntax.html)
[Generics Part 02: Underlying Types](https://www.ardanlabs.com/blog/2020/08/generics-02-underlying-types.html)
[Generics Part 03: Struct Types and Data Semantics](https://www.ardanlabs.com/blog/2020/09/generics-03-struct-types-and-data-semantics.html)

## Decorators

[Go 语言的修饰器编程 | | 酷 壳 - CoolShell](https://coolshell.cn/articles/17929.html)

## Testing

```sh
# skip test cache
go test -count=1
```

[Testing and Test-Driven-Development in Snap — Intel SDI — Medium](https://medium.com/intel-sdi/testing-and-test-driven-development-in-snap-d66359485561#.oc123kqcq)
[Testing and Test Driven Development in Snap (Part 2) — Intel SDI — Medium](https://medium.com/intel-sdi/testing-and-test-driven-development-in-snap-part-2-6304effa6b22#.ufy3wul7t)

[Getting Started In Testing Your Go Application | Toptal](https://www.toptal.com/go/your-introductory-course-to-testing-with-go)

[Writing table driven tests in Go – The acme of foolishness](https://dave.cheney.net/2013/06/09/writing-table-driven-tests-in-go)

[An Introduction to Testing in Go | TutorialEdge.net](https://tutorialedge.net/golang/intro-testing-in-go/)
[Advanced Go Testing Tutorial | TutorialEdge.net](https://tutorialedge.net/golang/advanced-go-testing-tutorial/)
[Improving Your Go Tests and Mocks With Testify | TutorialEdge.net](https://tutorialedge.net/golang/improving-your-tests-with-testify-go/)

[Integration Testing in Go: Part I - Executing Tests with Docker](https://www.ardanlabs.com/blog/2019/03/integration-testing-in-go-executing-tests-with-docker.html)
[Integration Testing in Go: Part II - Set-up and Writing Tests](https://www.ardanlabs.com/blog/2019/10/integration-testing-in-go-set-up-and-writing-tests.html)
[george-e-shaw-iv/integration-tests-example: An example project showcasing how Ardan Labs writes integration tests](https://github.com/george-e-shaw-iv/integration-tests-example)

## Cross Compile

[Cross compilation with Go 1.5 – The acme of foolishness](https://dave.cheney.net/2015/08/22/cross-compilation-with-go-1-5)

[mitchellh/gox: A dead simple, no frills Go cross compile tool](https://github.com/mitchellh/gox)

## Tips and Tricks

[Organizing Go code - go.dev](https://go.dev/blog/organizing-go-code)
[Go best practices, six years in](http://peter.bourgon.org/go-best-practices-2016/)
[Golang 新手开发需要注意的七个细节 |虞双齐的博客](https://www.yushuangqi.com/blog/2015/7_things-you-may-not-pay-attation-to-in-go.html)
[when nil is not nil - spf13.com](http://spf13.com/post/when-nil-is-not-nil/)
[7 common mistakes in Go (2015) - spf13.com](http://spf13.com/presentation/7-common-mistakes-in-go-2015/)
[★ Ultimate Visual Guide to Go Enums ★ – Learn Go Programming](https://blog.learngoprogramming.com/golang-const-type-enums-iota-bc4befd096d3)
[Trying Clean Architecture on Golang – Hacker Noon](https://hackernoon.com/golang-clean-archithecture-efd6d7c43047)
[The ultimate guide to writing a Go tool · Fatih Arslan](https://arslan.io/2017/09/14/the-ultimate-guide-to-writing-a-go-tool/)

[Go FAQ 101 - Go 101: an online Go programming book + knowledge base](https://go101.org/article/unofficial-faq.html)
[Go Tips 101 -Go 101](https://go101.org/article/tips.html)
[Go Details 101 -Go 101](https://go101.org/article/details.html)
[Go Details & Tips 101 -Go 101](https://go101.org/details-and-tips/101.html)
[Go Optimizations 101 -Go 101](https://go101.org/optimizations/101.html)

[The Top 10 Most Common Mistakes I’ve Seen in Go Projects](https://itnext.io/the-top-10-most-common-mistakes-ive-seen-in-go-projects-4b79d4f6cd65)
The part that passing 0.3KB data by value is faster than by reference is surprising

### Versioning

[gopkg.in - Stable APIs for the Go language](https://labix.org/gopkg.in)

### Docker

[Docker Images : Part I - Reducing Image Size](https://www.ardanlabs.com/blog/2020/02/docker-images-part1-reducing-image-size.html)

### Handling Errors

[Errors are values - go.dev](https://go.dev/blog/errors-are-values) Error handling does not obscure the flow of control.
[Error handling and Go - go.dev](https://go.dev/blog/error-handling-and-go)
[Defer, Panic, and Recover - go.dev](https://go.dev/blog/defer-panic-and-recover)
[Working with Errors in Go 1.13 - go.dev](https://go.dev/blog/go1.13-errors)
[How to compare Go errors - Stack Overflow](https://stackoverflow.com/a/57613539/665507)
[Go: Creating Custom Error Wrapper and Do Proper Error Equality Check - DEV Community](https://dev.to/tigorlazuardi/go-creating-custom-error-wrapper-and-do-proper-error-equality-check-11k7)
[Comparing error or error equality in Go (Golang) - Welcome To Golang By Example](https://golangbyexample.com/comparing-error-go/) error wrapping
[How to get stacktraces from errors in Golang with go-errors/errors | Bugsnag Blog](https://www.bugsnag.com/blog/go-errors)

Use `error.Is()` since Go 1.13 (2019-09)

```go
_, err := os.Stat("a-nonexistent-file.abcxyz")
fmt.Println(errors.Is(err, os.ErrNotExist)) // true
fmt.Println(err == os.ErrNotExist) // false
```

```go
// akin to catch for the function context
defer func() {
	if err := recover(); err != nil {
		fmt.Println("Error:", err)
		log.Println("stacktrace from panic: \n" + string(debug.Stack()))
	}
}()
```

## Visualization

[hirokidaichi/goviz: a visualization tool for golang project dependency](https://github.com/hirokidaichi/goviz)
[TrueFurby/go-callvis: Visualize call graph of your Go program using dot format.](https://github.com/TrueFurby/go-callvis)

## #perfmatters

[Profiling Go Programs - go.dev](https://go.dev/blog/pprof)
[GopherCon 2019: Dave Cheney - Two Go Programs, Three Different Profiling Techniques - YouTube](https://www.youtube.com/watch?v=nok0aYiGiYA)
[Profiling and Optimizing Go - YouTube](https://www.youtube.com/watch?v=N3PWzBeLX2M)

[Nitro : A quick and simple profiler for golang - spf13.com](http://spf13.com/project/nitro)
[profefe/profefe: Continuously collect profiling data for long-term postmortem analysis](https://github.com/profefe/profefe)
