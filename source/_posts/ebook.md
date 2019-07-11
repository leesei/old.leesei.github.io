---
title: eBook
categories:
  - ebook
tags:
  - null
toc: true
date: 2016-09-13 15:08:22
---

# Formats

[Comparison of e-book formats - Wikiwand](https://www.wikiwand.com/en/Comparison_of_e-book_formats)
[Difference Between EPUB, MOBI, AZW and PDF eBook Formats](http://www.guidingtech.com/9661/difference-between-epub-mobi-azw-pdf-ebook-formats/)
[EPUB and Kindle formats explained | Digital Publishing 101](http://digitalpublishing101.com/digital-publishing-101/digital-publishing-basics/epub-kindle-formats/)
[Difference Between EPUB, MOBI and AZW E-Book Formats](http://techwelkin.com/difference-between-epub-pdf-mobi-and-azw-ebook-formats)
[Why Amazon’s Proprietary eBook Format is Better than ePub](http://goodereader.com/blog/e-book-news/why-amazons-proprietary-ebook-format-is-better-than-epub)

# Readers

## Amazon Kindle

[Amazon.com Help - Which Kindle E-reader Do I Have?](https://www.amazon.com/gp/help/customer/display.html?nodeId=201263790)

[Kindle Paperwhite 3](https://www.wikiwand.com/en/Amazon_Kindle#/Kindle_Paperwhite_%283rd_generation%29):

- 7th Generation, 2015
- 6-inch, 1440×1080, 300 ppi E Ink Carta HD display
- 4 LED backlight
- 3GB user storage
- 6.7" x 4.6" x 0.36" (169 mm x 117 mm x 9.1 mm)
  \$770@201604

[Kindle Paperwhite 4](https://www.wikiwand.com/en/Amazon_Kindle#/Kindle_Paperwhite_%284rd_generation%29)

- 10th Generation, 2018
- 6-inch, 1440×1080, 300 ppi E Ink Carta HD display
- 5 LED backlight
- flat screen
- waterproof with an IPX8
- bluetooth audio

## 京東博閱

[随阅随心—新版 JDRead 1 入手快速体验\_\_什么值得买](https://post.smzdm.com/p/658503/)
[【達人首選】看書小法寶-博閱博閱 JDRead @ 閱讀的未來 :: 痞客邦 ::](http://hanbori6.pixnet.net/blog/post/82780876-%E3%80%90%E9%81%94%E4%BA%BA%E9%A6%96%E9%81%B8%E3%80%91%E7%9C%8B%E6%9B%B8%E5%B0%8F%E6%B3%95%E5%AF%B6-%E5%8D%9A%E9%96%B1%E5%8D%9A%E9%96%B1-jdread)

[Paper 博阅 电子书阅读器 使用评测\_\_什么值得买](https://post.smzdm.com/p/607643/)
Paper:
7.8"

# Tools

[Ebooks Stack Exchange](https://ebooks.stackexchange.com/)

Paper Sizes:
A4 210 x 297 mm 8.3 x 11.7 in
A5 148 x 210 mm 5.8 x 8.3 in
A6 105 x 148 mm 4.1 x 5.8 in

Printing to A5 or A6 PDF would be ok.

[KindleGen](http://www.amazon.com/gp/feature.html?docId=1000765211)

```sh
kindlegen [-c0|-c2] <input>
```

[Kindle Comic Creator](http://www.amazon.com/gp/feature.html?docId=1001103761)
[Kindle Textbook Creator](http://www.amazon.com/gp/feature.html?docId=1002998671)

[No.722](http://no722.cocolog-nifty.com/blog/) ChainLP Homepage
[ASSIOMA(アショーマ) » Kindle Paperwhite と ChainLP で自炊した書籍を読む方法](http://www.assioma.jp/?p=3623)
[Kindle 漫画制作软件 ChainLP 简明教程 – Kindle 伴侣](http://kindlefere.com/post/266.html)
[[超详细教程] MOBI 全屏漫画/图片书籍*kindle 吧*百度贴吧](http://tieba.baidu.com/p/2191868417)

[ciromattia/kcc: KCC (a.k.a. Kindle Comic Converter) is a comic and manga converter for ebook readers.](https://github.com/ciromattia/kcc)
[FooSoft Productions - Mangle](https://foosoft.net/projects/mangle/)

[kanasimi/work_crawler: 小说漫画下载工具](https://github.com/kanasimi/work_crawler)
[leesei/refine-manhuaren: Refine Manhuaren is an extractor to extract Manhuaren comics.](https://github.com/leesei/refine-manhuaren)
[gumblex/refine-buka: Extract images downloaded by Buka.](https://github.com/gumblex/refine-buka)
[extract buka manga archive (\*.buka)](https://gist.github.com/randphu/5277346)
[布卡漫畫 – 布卡 JPG 圖像提取器 3/3 – 使用方法 | DmpSuen 創作室](https://dmpsuen2.wordpress.com/2014/03/28/extract-jpg-from-buka-comic-33-buka-jpg-extractor/)

[10 Best Comic Book Viewers for Linux](https://www.fossmint.com/best-comic-book-viewers-readers-for-linux/)

[天火藏書排版系統 ( Kindle/NOOK/iPad 電子書 EPUB MOBI PDF 中文 直書 直排 轉檔 系統 )](http://ebook.cdict.info/)

## calibre

[calibre - About](https://calibre-ebook.com/about)
[calibre - Watch it in action](https://calibre-ebook.com/demo)
[calibre User Manual — calibre User Manual](https://manual.calibre-ebook.com/index.html) ebook version available

[Adding your favorite news website — calibre User Manual](https://manual.calibre-ebook.com/news.html) recipes for cloning and converting websites
[Command Line Interface — calibre User Manual](https://manual.calibre-ebook.com/generated/en/cli-index.html)
[ebook-convert — calibre User Manual](htstp://manual.calibre-ebook.com/cli/ebook-convert.html)

## pandoc conversion

[Pandoc - Pandoc User’s Guide](https://pandoc.org/MANUAL.html)
[Pandoc - Creating an ebook with pandoc](https://pandoc.org/epub.html)

```sh
pandoc -f FROM -t TO -o OUTPUT INPUT

FIN=<inputfile>
# convert md to HTML
pandoc -f markdown -t html -o ${FIN%.*}.html ${FIN}
# convert md to HTML
# markdown_github is available but the output is weird
pandoc -f markdown -t textile -o ${FIN%.*}.textile ${FIN}
# generate standalone HTML and save as PDF
pandoc -f gfm -t html5 -s ${FIN} -o ${FIN%.*}.pdf
```

## Converting Website

> see `http-agents.md#wget`

```sh
# use `ebook-convert` from Calibre to convert static site to ebook
cd website-dir-with-index-html
ebook-convert index.html book.mobi
ebook-convert index.html book.azw3
ebook-convert index.html book.fb2
ebook-convert index.html book.epub
```

## Converting Gitbook

> see `gitbook.md`

Download the source, use these commands:

```sh
# Generate a PDF file
# print to 'a5' or 'a6'
$ gitbook pdf ./ ./mybook.pdf

# Generate an ePub file
$ gitbook epub ./ ./mybook.epub

# Generate a Mobi file
$ gitbook mobi ./ ./mybook.mobi
```

[eBook and PDF · GitBook Toolchain Documentation](https://toolchain.gitbook.com/ebook.html)
[PDF Configuration · GitBook Toolchain Documentation](https://toolchain.gitbook.com/config.html#pdf-options)

## Converting Ansible docs

Ansible docs are generated with [Sphinx](http://www.sphinx-doc.org/en/stable/), which natively supports ePub as output.

[Make epub of documentation available · Issue #7205 · ansible/ansible](https://github.com/ansible/ansible/issues/7205#issuecomment-65662371)

```sh
git clone -b master --single-branch https://github.com/ansible/ansible.git
# optionally checkout a stable branch
cd ansible/docsite
sed -i s/\'html\'/\'epub\'/ build-site.py
make docs
# ePub available at `docsite/htmlout/AnsibleDocumentation.epub`
```

## Converting Docker docs

Docker docs are generated with [MkDocs](http://www.mkdocs.org/).

```sh
git clone -b master --single-branch https://github.com/docker/docker.git
make docs
```

## Converting Rust docs

killercup's [killercup/trpl-ebook](https://github.com/killercup/trpl-ebook) project converts Rust docs to HTML (hence eBook) with `pandoc`. OBSOLETE!
The upstream code have some issue in headings so [patch](https://github.com/rust-lang/rust/issues/20866) is needed when generating ebook.

> see `rust.md#books`

Save as HTML with some hacks:  
https://github.com/rust-lang/rust/issues/20866#issuecomment-495962961

```sh
git clone -b master --single-branch https://github.com/abcdev/trpl-ebook/tree/restructure
# https://github.com/killercup/trpl-ebook/pull/52
```

## Converting Redux docs

[paulkogel/redux-offline-docs: Redux documentation in PDF, ePub and MOBI formats for offline reading.](https://github.com/paulkogel/redux-offline-docs)

```sh
git clone -b master --single-branch https://github.com/reactjs/redux.git
gitbook install
gitbook mobi . docs/redux-documentation.mobi
```

## Converting ELK docs

[elastic/docs](https://github.com/elastic/docs)

[elastic/elasticsearch-definitive-guide: The Definitive Guide to Elasticsearch](https://github.com/elastic/elasticsearch-definitive-guide) uses [Asciidoctor](http://asciidoctor.org/)

```sh
docker run -it -v --rm ./elasticsearch-definitive-guide:/documents/ -w /documents asciidoctor/docker-asciidoctor
# in container
asciidoctor -v -r asciidoctor-pdf -d book -b pdf -a toc book.asciidoc
asciidoctor -v -r asciidoctor-epub3 -d book -b epub3 -a toc book.asciidoc

ebook-convert book.epub book.azw3
```

## Converting Hugo docs

```sh
git clone -b release-docs --single-branch git@github.com:spf13/hugo.git
cd hugo
hugo
```

## Converting ZSH docs

```sh
curl http://zsh.sourceforge.net/Doc/zsh_html.tar.gz | tar zx
cd zsh_html; ebook-convert index.html ../zshdoc.azw3
```

```sh
curl http://zsh.sourceforge.net/Guide/zshguide_html.tar.gz | tar zx
cd zshguide_html; ebook-convert zshguide.html ../zshguide.azw3
```

# Writing/Publishing

[Digital Publishing 101 for Ebooks | Course Home | Digital Publishing 101](http://digitalpublishing101.com/digital-publishing-101/)
[Notjohn's Self-Publishing Guide](https://notjohnkdp.blogspot.hk/)

# Portals

[MobileRead Forums](http://www.mobileread.com/)
[Good e-Reader - e-book and e-reader News](http://goodereader.com/blog/)
[Kindle 人社区-Kindle 人都爱的 Kindle 论坛](https://kindleren.com/forum.php)
[Kindle 高登悅讀專頁](http://hkgolden-kindle.blogspot.hk/)

[天火藏書排版系統 ( Kindle/NOOK/iPad 電子書 EPUB MOBI PDF 中文 直書 直排 轉檔 系統 )](http://ebook.cdict.info/)

[BookAuthority: The Best Business Books Recommended By Experts](https://bookauthority.org/)

# Resources

[O'Reilly Open Books Project](https://www.oreilly.com/openbook/)
[Free O'Reilly Books, Ebooks, Webcasts, Conference Sessions, Tutorials, Videos - O'Reilly Media](https://www.oreilly.com/free/)
[Open Book Project](http://openbookproject.net/index.php)
[Welcome to Open Library | Open Library](https://openlibrary.org/)

[广场 - 看云](http://www.kancloud.cn/explore) China's Gitbook
[SoKindle - 免费电子书分享交流下载](http://sokindle.com/)
[无忧书城 - 为您免费提供在线阅读服务](http://www.51shucheng.com/)
[中國哲學書電子化計劃](https://ctext.org/zh) 中國文獻, public domain
[明朝那些事儿-明朝那些事儿全集在线阅读](http://www.mingchaonaxieshier.com/)
[看看豆(原看 Kindle)-免费电子书分享下载](http://kankandou.com/) 1 download per day
[ScanLibs - Ebooks & Elearning For Programming](https://scanlibs.com/)
[Share And Download IT Ebook](http://www.it-ebooks.com/)
[Fox eBook - eBooks Free Download Site](http://www.foxebook.net/)
[Ebook-dl | Free Download Ebooks & Video Tutorials](http://ebook-dl.com/)
[Download free eBooks at ebooks10.com](http://www.ebooks10.com/)
[ScanLibs - Ebooks & Elearning For Programming](http://scanlibs.com/)
[Programming | Scoop.it](http://www.scoop.it/t/programming-by-martin-mifsud)
[Free eBooks - Archives](http://proxymator.com/category/free-ebooks/)
[Programmer's Heaven - Free Programming books](http://ebooks.programmersheaven.com/)
[Free IT ebooks ownload , Free programming ebooks download](http://onlinevideolecture.com/ebooks/)
[Online Textbooks for Free | bookboon](http://bookboon.com/en/textbooks-ebooks)
[The Linux Documentation Project](http://www.tldp.org/)
[Free Programming Books](http://www.eduhub.io/b/free-programming-books)
[Free Programming Books: leanpub.com](http://www.eduhub.io/b/free-programming-books/t/leanpub-com)
[allinurl:https://leanpub.com read - Google Search](https://www.google.com.hk/search?sclient=psy-ab&site=&source=hp&q=allinurl:https://leanpub.com+read&oq=allinurl:https://leanpub.com+read)

[Wikisource, the free library](https://en.wikisource.org/wiki/Main_Page)
[Wikibooks](https://en.wikibooks.org/wiki/Main_Page)
[Public Domain | Feedbooks](http://www.feedbooks.com/publicdomain)
[eBooks and Texts : Internet Archive](https://archive.org/details/texts)
[Sharing Knowledge and Building Communities - OpenStax CNX](http://cnx.org/)
[Welcome to Open Library (Open Library)](https://openlibrary.org/)
[Free ebooks by Project Gutenberg - Gutenberg](https://www.gutenberg.org/)
[GitBook · Writing made easy](https://www.gitbook.com/)
[Leanpub: Publish Early, Publish Often](https://leanpub.com/) try adding `/read` to url

[smusali/Leanpub-Hack: I used some web scraping and web automation techniques within Python to legally download free books from www.leanpub.com](https://github.com/smusali/Leanpub-Hack)

[Free eBooks For Your Kindle or Other eReader | ManyBooks](http://manybooks.net/)
[800 Free eBooks for iPad, Kindle & Other Devices | Open Culture](http://www.openculture.com/free_ebooks)
[Electronic library. Download books free. Finding books](http://bookzz.org/)
[Top Shelf Book | Download Free Ebooks And Audiobooks](http://topshelfbook.org/)
[Free eBooks Download - ebook3000.com](http://www.ebook3000.com/)

[ISBN.Directory - Book Search Engine - Price Comparison](http://isbn.directory/)

## Comics

[kindle 知道漫画补档专区](http://kindle.smgzd.com/)
[Kindle 漫画 mobi 漫画推送下载 - pixvol.com](https://www.pixvol.com/)
[Kindle 漫画 Kindle 人社区](https://kindleren.com/forum.php?mod=forumdisplay&fid=65)
[漫画\_在线漫画 - 动漫屋:你的我的在线漫画](http://www.dm5.com/)
[布卡漫画](http://buka.cn/)
[nn64 的漫畫列表 - nn64 Comic List](http://www.dijanet.net/)

## Corporates

[Ebooks | Resources | Syncfusion](https://www.syncfusion.com/resources/techportal/ebooks/)
[Resources / White Papers | InfoWorld](http://www.infoworld.com/resources)
[Codeship eBooks](http://resources.codeship.com/ebooks)
[eBooks Series: The Docker and Container Ecosystem - The New Stack](http://thenewstack.io/ebookseries/)

[Free Programming Ebooks - O'Reilly Media](http://www.oreilly.com/programming/free/)
[Free Web Development Ebooks - O'Reilly Media](http://www.oreilly.com/web-platform/free/)
[Free Web Performance & DevOps Ebooks - O'Reilly Media](http://www.oreilly.com/webops-perf/free/)
[Free Security Ebooks - O'Reilly Media](http://www.oreilly.com/security/free/)
[Free Data Science and Big Data Ebooks - O'Reilly Media](http://www.oreilly.com/data/free/)
[Practical design knowledge from experts in UX, Data, IoT - Free Ebooks - O'Reilly Media](http://www.oreilly.com/design/free/)
[Free IoT Ebooks and Compilations - O'Reilly Media](http://www.oreilly.com/iot/free/)

## Paid

[多看阅读(duokan.com) - 海量畅销电子书免费试读，数百万读者阅读首选](http://www.duokan.com/)
[首頁-銅板漫畫出版署-淘寶網](https://shop60225721.world.taobao.com/shop/view_shop.htm?shopId=60225721)
[A Book Apart, Brief books for people who make websites.](https://abookapart.com/)
