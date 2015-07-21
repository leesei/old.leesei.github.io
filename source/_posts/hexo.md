title: "Hexo"
date: 2014-12-09 17:18:32
categories:
- web
tags:
- hexo
- notes
toc: true
---

http://hexo.io/
http://jr0cket.co.uk/hexo/
[Hexo常见问题解决方案 | Xuanwo's Blog](http://xuanwo.org/2014/08/14/hexo-usual-problem/)
http://leesei.github.io/hexo-testground/2014/12/01/hello-world/#Customization

Validate YAML with [Online YAML Parser](http://yaml-online-parser.appspot.com/).

[Start From Hexo – Canvas](http://cinvro.com/post/start-from-hexo/)
[Hexo 源码略读（一）：init.js – Canvas](http://cinvro.com/post/hexo-source-1/)

[github pages - Repo Setup for Hexo? - Stack Overflow](http://stackoverflow.com/questions/27399219/repo-setup-for-hexo#27401742)

<!-- more -->

## Plugins

[Plugins | Hexo](https://hexo.io/plugins/)
[Plugins · hexojs/hexo Wiki](https://github.com/hexojs/hexo/wiki/Plugins)

[Writing Plugins | Hexo](https://hexo.io/docs/plugins.html)

hexo-console-rename
hexo-generator-alias
hexo-admin
hexo-tag-asset-res
hexo-tag-emojis
https://github.com/timnew/hexo-tag-codepen
https://github.com/wzpan/hexo-tag-bootstrap
https://github.com/kywk/hexo-tag-eval
https://github.com/oohcoder/hexo-tag-plantuml
https://github.com/akfish/hexo-math
https://github.com/akfish/hexo-diagram http://jumly.tmtk.net/
[JamesPan/hexo-ruby-character](https://github.com/JamesPan/hexo-ruby-character)

https://github.com/timnew/hexo-helper-simple-tagcloud
https://github.com/akfish/hexo-series

[celsomiranda/hexo-renderer-markdown-it](https://github.com/celsomiranda/hexo-renderer-markdown-it)

https://github.com/FlashSoft/hexo-console-optimize


## Themes

I need: 
- archive page (title only; link to months, see [jacman](http://wuchong.me/jacman/archives/))
- categories page
- tags page
- tags widget sorted by posts
- categories widget
- TOC

It's better to show tags and categories in archive and main index.

[Speed Up the Rendering Process of hexo 3 | HaHack](http://hahack.com/codes/hexo-3-speed-up/)

[Themes | Hexo](https://hexo.io/themes/)
[Themes · hexojs/hexo Wiki](https://github.com/hexojs/hexo/wiki/Themes)

https://github.com/wzpan/hexo-theme-freemind
https://github.com/xing5/hexo-theme-codeland
https://github.com/xiangming/landscape-plus
http://wuchong.me/jacman/
https://github.com/zhanglun/hexo-theme/tree/master/Tinny
http://www.hahack.com/codes/hexo-theme-wixo/ Wiki style theme
[LouisBarranqueiro/tranquilpeak-hexo-theme](https://github.com/LouisBarranqueiro/tranquilpeak-hexo-theme/)

[kywk/hexo-theme-spp](https://github.com/kywk/hexo-theme-spp) Good for CV

## Jade

[bubkoo/hexo-theme-formula](https://github.com/bubkoo/hexo-theme-formula)

Custom index page:
https://github.com/xing5/blog
http://jslite.io/tags/
https://github.com/timnew/timnew.github.com/tree/hexo 
https://github.com/timnew/landscape/tree/master

### Writing themes

Customization section of [hexo doc](https://hexo.io/docs/).
- [Themes | Hexo](https://hexo.io/docs/themes.html)
- [Helpers | Hexo](https://hexo.io/docs/helpers.html)

http://hexo.io/docs/helpers.html
http://jr0cket.co.uk/hexo-themes-test/
http://jr0cket.co.uk/tags/hexo/
http://jr0cket.co.uk/hexo/customising-the-hexo-theme.html
http://jr0cket.co.uk/hexo/deconstructing-the-hexo-theme.html

http://kuangqi.me/tricks/hexo-optimizations-for-mainland-china/
http://kuangqi.me/tricks/enable-table-of-contents-on-hexo/

and study source code of Hexo and other themes

### Favicon

Some themes support custom favicon.
You can also put `favicon.ico` in `source/favicon.ico` so it will be picked up by browsers.

[node.js - Add Favicon to Hexo Blog - Stack Overflow](http://stackoverflow.com/questions/30291588/add-favicon-to-hexo-blog/)

## Add doc

[hexojs/site](https://github.com/hexojs/site)

```
# Display 'Tech' in web pages, but 'Hack' in url.
category_map:
  Tech: Hack
  name2: slug2
  name3: slug3
  ...
```

```
{% for post in page.posts.toArray() %}
    title: {{ post.title }}
    content: {{ post.content }}
{% endfor %}
```
