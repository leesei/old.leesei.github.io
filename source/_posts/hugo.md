---
title: Hugo
categories:
- app
tags:
- hugo
- notes
- static-site
toc: true
date: 2017-05-09 13:16:30
---

[Hugo :: A fast and modern static website engine](https://gohugo.io/)
[Comparing Static Site Engines with Brian Rinaldi - YouTube](https://www.youtube.com/watch?v=R-fJWOO1bjE)

[Hacking Management](http://spf13.com/) Author's blog

[Hugo - Shortcodes](https://gohugo.io/extras/shortcodes/) = tags
[Hugo - Go Template Primer](https://gohugo.io/templates/go-templates/)
[Hugo - Taxonomy Overview](https://gohugo.io/taxonomies/overview/)
[Hugo - Syntax Highlighting](https://gohugo.io/extras/highlighting/)

<!--more-->

## CLI

[Hugo - Using Hugo](https://gohugo.io/overview/usage/)
[Hugo - Commands](https://gohugo.io/commands/)

```sh
yaourt -S hugo-bin pygmentize # for Arch

hugo help
hugo config
hugo new site <name>
hugo new post/<file.md>
hugo -v

# install themes, Hugo does not comes with default theme
git clone https://github.com/dim0627/hugo_theme_robust.git themes/hugo_theme_robust
# cd themes/hugo_theme_robust; git checkout b8ce466; cd ../../
git clone https://github.com/spf13/herring-cove.git themes/herring-cove

hugo server
hugo server --theme=<theme> --buildDrafts
```

## Config

[Hugo | Configure Hugo](https://gohugo.io/getting-started/configuration/)
[Hugo | Archetypes](https://gohugo.io/content-management/archetypes/)


```yaml
draft: false
isCJKLanguage: true
```

## Template

[Hugo | Templates](https://gohugo.io/templates/)
[Hugo | Front Matter](https://gohugo.io/content-management/front-matter/)
[text/template - The Go Programming Language](https://golang.org/pkg/text/template/)
[html/template - The Go Programming Language](https://golang.org/pkg/html/template/)

## Themes

[Hugo Themes Site](http://themes.gohugo.io/)
[spf13/hugoThemes: All Themes Hugo](https://github.com/spf13/hugoThemes/)

[spf13/HugoBasicExample: Example site to use with Hugo & Hugo Themes](https://github.com/spf13/HugoBasicExample)

I need: 
- archive page (title only; link to months, see [jacman](http://wuchong.me/jacman/archives/))
- categories index page
- tags index page
- tags widget sorted by posts
- categories widget
- TOC

It's better to show tags and categories in archive and main index.

[Hugo Theme: Minos](http://themes.gohugo.io/hugo-theme-minos/) side TOC, responsive, tags/categories index
[first - Hugo PacMan Theme Demo](http://themes.gohugo.io/theme/hugo-pacman-theme/post/first/) side TOC
[Hugo Theme: Hugo Dusk](http://themes.gohugo.io/hugo-dusk/) tags/categories index
[Hugo Theme: Simple A](http://themes.gohugo.io/simple-a/) tags/categories index
[Hugo Theme: Hugo Bootstrap V4 Blog](http://themes.gohugo.io/hugo-theme-bootstrap4-blog/) project and about
[Hugo Theme: Wave](http://themes.gohugo.io/hugo-theme-wave/) tags/categories index
[Kube for Hugo](http://themes.gohugo.io/theme/kube/) top TOC
[Hugo Theme: Hello Programmer](http://themes.gohugo.io/hugo-hello-programmer-theme/) TOC
[Hugo Theme: Aglaus](http://themes.gohugo.io/aglaus/) AMP, responsive
[Hugo Theme: Gohugo Amp](http://themes.gohugo.io/gohugo-amp/) AMP showcase
[Hugo Theme: Mainroad](http://themes.gohugo.io/mainroad/)

Portfolio themes:
[Hugo Theme: Academic](http://themes.gohugo.io/academic/)
[Hugo Theme: Hugo Scroll](http://themes.gohugo.io/hugoscroll/)
[Hugo Theme: Freelancer](http://themes.gohugo.io/freelancer/)
[Hugo Theme: Creative](http://themes.gohugo.io/creative/)

Docs themes:
[Hugo Theme: DocDock](http://themes.gohugo.io/docdock/)
[Hugo Theme: Learn](http://themes.gohugo.io/hugo-theme-learn/)
[Hugo Theme: DocuAPI](http://themes.gohugo.io/docuapi/)
[Hugo Theme: Alabaster](http://themes.gohugo.io/hugo-alabaster-theme/)
[Hugo Theme: Material Docs](http://themes.gohugo.io/material-docs/) side TOC, tags/categories?
[Hugo Theme: Paper Now](http://themes.gohugo.io/hugo-paper-now/)

## Deployment

[Aerobatic - NPM scripts for building and deploying Hugo sites](https://www.aerobatic.com/blog/hugo-npm-buildtool-setup/)
[Hugo - Hosting on GitHub Pages](https://gohugo.io/tutorials/github-pages-blog/)

## Tutorial

[Hugo Website Tutorial with a Live Static E-Commerce Example - Snipcart](https://snipcart.com/blog/hugo-tutorial-static-site-ecommerce)

## Tips and Tricks

[Live Hugo Site search with Lunr.js - tips & tricks - Hugo Discussion](https://discuss.gohugo.io/t/live-hugo-site-search-with-lunr-js/2857/13)

### Dump context

Add `layouts/index.html`

```
{{ range $k, $v := .Site.Params }}
    {{ $k }} : {{ $v }}
{{ end }}

{{ range $k, $v := .Site.taxonomy }}
    {{ $k }} : {{ $v }}
{{ end }}
```
