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

<!-- more -->

Custom index page:
https://github.com/xing5/blog
https://github.com/timnew/timnew.github.com/tree/hexo https://github.com/timnew/landscape/tree/master

## Plugins

https://github.com/hexojs/hexo/wiki/Plugins
http://hexo.io/docs/plugins.html
[](about:blank)
hexo-console-optimize
hexo-console-rename
hexo-generator-alias
hexo-admin
hexo-tag-asset-res
hexo-tag-emojis
https://github.com/timnew/hexo-tag-codepen
https://github.com/timnew/hexo-helper-simple-tagcloud
https://github.com/akfish/hexo-math
https://github.com/akfish/hexo-diagram http://jumly.tmtk.net/
https://github.com/akfish/hexo-series
https://github.com/wzpan/hexo-tag-bootstrap
https://github.com/kywk/hexo-tag-eval

## Themes

I need: 
- archive page (list)
- categories page
- tags page
- tag cloud sorted by posts
- TOC

It's better to show tags and categories in archive and main index.

https://github.com/hexojs/hexo/wiki/Themes

https://github.com/wzpan/hexo-theme-freemind
https://github.com/xing5/hexo-theme-codeland
https://github.com/xiangming/landscape-plus
http://wuchong.me/jacman/
https://github.com/zhanglun/hexo-theme/tree/master/Tinny
http://www.hahack.com/codes/hexo-theme-wixo/

### Writing themes

http://hexo.io/docs/helpers.html
http://jr0cket.co.uk/hexo-themes-test/
http://jr0cket.co.uk/tags/hexo/
http://jr0cket.co.uk/hexo/customising-the-hexo-theme.html
http://jr0cket.co.uk/hexo/deconstructing-the-hexo-theme.html
http://kuangqi.me/tricks/hexo-optimizations-for-mainland-china/
http://kuangqi.me/tricks/enable-table-of-contents-on-hexo/

and study source code of Hexo and other themes

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
