---
title: Unicode
categories:
  - comp.lang
toc: true
date: 2015-06-05 10:17:15
tags:
- unicode
---

[Unicode - Wikiwand](https://www.wikiwand.com/en/Unicode)
[Universal Character Set characters - Wikiwand](http://www.wikiwand.com/en/Universal_Character_Set_characters)
[Code point - Wikiwand](http://www.wikiwand.com/en/Code_point)
[BMP](http://www.wikiwand.com/en/Plane_%28Unicode%29#/Basic_Multilingual_Plane)
[SMP](http://www.wikiwand.com/en/Plane_%28Unicode%29#/Supplementary_Multilingual_Plane)

[Legacy Character Models and an Introduction to Unicode - Slide list](http://www.cip.ifi.lmu.de/~bolzer/unicode_intro/slides/Overview-5.html)

From Python PEP-261:

```
**Character**

Used by itself, means the addressable units of a Python Unicode string.

**Code point**

A code point is an integer between 0 and TOPCHAR. If you imagine Unicode as a mapping from integers to characters, each integer is a code point. But the integers between 0 and TOPCHAR that do not map to characters are also code points. Some will someday be used for characters. Some are guaranteed never to be used for characters.

**Codec**

A set of functions for translating between physical encodings (e.g. on disk or coming in from a network) into logical Python objects.

**Encoding**

Mechanism for representing abstract characters in terms of physical bits and bytes. Encodings allow us to store Unicode characters on disk and transmit them over networks in a manner that is compatible with other Unicode software.

**Surrogate pair**

Two physical characters that represent a single logical character. Part of a convention for representing 32-bit code points in terms of two 16-bit code points.

**Unicode string**

A Python type representing a sequence of code points with "string semantics" (e.g. case conversions, regular expression compatibility, etc.) Constructed with the unicode() function.
```

[UTS #10: Unicode Collation Algorithm](http://www.unicode.org/reports/tr10/) sorting
[&what: Discover Unicode & HTML Character Entities](http://www.amp-what.com/)
[Math Unicode Entities](http://symbolcodes.tlt.psu.edu/bylanguage/mathchart.html)

[Programming with Unicode — Programming with Unicode](http://unicodebook.readthedocs.io/index.html)
[The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets (No Excuses!) - Joel on Software](http://www.joelonsoftware.com/articles/Unicode.html) !important
[What every JavaScript developer should know about Unicode](https://rainsoft.io/what-every-javascript-developer-should-know-about-unicode/)

[Unify – Unicode support on browsers and devices](http://unicode.johnholtripley.co.uk/)

## Normalization

[FAQ - Normalization](http://www.unicode.org/faq/normalization.html)
[Unicode equivalence - Wikiwand](https://www.wikiwand.com/en/Unicode_equivalence)
[String.prototype.normalize() - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/normalize)

[UAX #15: Unicode Normalization Forms](http://unicode.org/reports/tr15/)

Normal Form Decomposed (NFD): “é” (U+00E9) = “e” + “ ́” (U+0065 U+0301).

NFC — Normalization Form Canonical Composition.
NFD — Normalization Form Canonical Decomposition.
NFKC — Normalization Form Compatibility Composition.
NFKD — Normalization Form Compatibility Decomposition.

## Encoding

[UTF-8 - Wikiwand](http://www.wikiwand.com/en/UTF-8)
[UTF-16 - Wikiwand](http://www.wikiwand.com/en/UTF-16)
[Surrogates](http://www.wikiwand.com/en/Universal_Character_Set_characters#/Surrogates)
[Punycode - Wikiwand](https://www.wikiwand.com/en/Punycode)

[RFC 3492 - Punycode: A Bootstring encoding of Unicode for Internationalized Domain Names in Applications (IDNA)](https://tools.ietf.org/html/rfc3492)
[RFC 3629 - UTF-8, a transformation format of ISO 10646](http://tools.ietf.org/html/rfc3629)

[Byte order mark - Wikiwand](https://www.wikiwand.com/en/Byte_order_mark)
[FAQ - UTF-8, UTF-16, UTF-32 & BOM](http://www.unicode.org/faq/utf_bom.html#BOM)
[UTR#17: Unicode Character Encoding Model](https://www.unicode.org/reports/tr17/)

## Emoji

[Emoji - Wikiwand](https://www.wikiwand.com/en/Emoji)
[How emoji conquered the world | The Verge](http://www.theverge.com/2013/3/4/3966140/how-emoji-conquered-the-world)
[The Oral History Of The Poop Emoji (Or, How Google Brought Poop To America) | Fast Company | Business + Innovation](http://www.fastcompany.com/3037803/the-oral-history-of-the-poop-emoji-or-how-google-brought-poop-to-america)
[Emoji and the Levitating Businessman - Computerphile - YouTube](https://www.youtube.com/watch?v=tITwM5GDIAI)

[iEmoji.com](http://www.iemoji.com/)
[Emoji searcher](http://emoji.muan.co/)
[emojidex - custom emoji service and apps](https://www.emojidex.com/)
[muan/mojibar: Emoji searcher but as a menubar app.](https://github.com/muan/mojibar)
[📙 Emojipedia — 😃 Home of Emoji Meanings 💁👌🎍😍](http://emojipedia.org/)
[😋 Get Emoji — List of all Emojis to ✂ Copy and 📋 Paste 👌](http://getemoji.com/)
[Full Emoji List, v5.0](http://www.unicode.org/emoji/charts/full-emoji-list.html)
[emot.es - All your favorite emoticons in one place ( ͡° ͜ʖ ͡°)](http://emot.es/)
[EmojiOne | The Authentic Digital Emoji Brand](https://www.emojione.com/)

[Emoji cheat sheet for GitHub, Basecamp and other services](http://www.emoji-cheat-sheet.com/)

[Twitter Emoji (Twemoji)](http://twitter.github.io/twemoji/)

### Font

[android - CSS reference to phone's Emoji font? - Stack Overflow](https://stackoverflow.com/questions/27688046/css-reference-to-phones-emoji-font)

[jslegers/emoji-icon-font: An experimental icon font](https://github.com/jslegers/emoji-icon-font)
[Twemoji Awesome | Like Font Awesome, but for Twitter Emoji.](http://ellekasai.github.io/twemoji-awesome/)
[EmojiSymbols Font](https://emojisymbols.com/)
[MorbZ/OpenSansEmoji: OpenSans based font which includes the full iOS Emoji set](https://github.com/MorbZ/OpenSansEmoji)
[EmojiSymbols Font](https://emojisymbols.com/)
[Google Noto Fonts - Noto Emoji](https://www.google.com/get/noto/#emoji-zsye)
[Google Noto Fonts - Noto Color Emoji](https://www.google.com/get/noto/#emoji-zsye-color)

[Emoji on the Web – Making Faces (and Other Emoji) – Medium](https://medium.com/making-faces-and-other-emoji/emoji-on-the-web-537c5769dffa)

## Character Table

[Unicode character table](http://unicode-table.com/en/)
[Unicodinator](http://unicodinator.com/)
[Find all Unicode characters from Hieroglyphs to Dingbats – Codepoints](https://codepoints.net/)
[Unicode codepoint lookup/search tool](http://unicode.scarfboy.com/)
[&what: Discover Unicode & HTML Character Entities](http://www.amp-what.com/)
[Unicode Characters ☯ ⚡ ∑ ♥ 😄](http://xahlee.info/comp/unicode_index.html)
[&what: Discover Unicode & HTML Character Entities](http://www.amp-what.com/)
[Graphemica - For people who ♥ letters, numbers, punctuation, &c](http://graphemica.com/)
[Code Charts](http://www.unicode.org/charts/) (Unicode official one, PDFs)
[List of Unicode characters - Wikiwand](https://www.wikiwand.com/en/List_of_Unicode_characters)
[Unicode Table](http://www.tamasoft.co.jp/en/general-info/unicode.html)
[Unicode/UTF-8-character table](http://www.utf8-chartable.de/unicode-utf8-table.pl?number=1024&unicodeinhtml=hex)

[Typography Cheatsheet → A Comprehensive Guide to Smart Quotes, Dashes & Other Typographic Characters → Typewolf](http://www.typewolf.com/cheatsheet)
[Keycodes - Javascript Keyboard Codes, Character Codes, Unicode, HTML Entities](http://keycodes.atjayjo.com/)

[Shapecatcher: Draw the Unicode character you want!](http://shapecatcher.com/)

### Guobiao

[國家標準代碼 - Wikiwand](https://www.wikiwand.com/zh-hk/国家标准代码)
[国标码查询；汉字国家标准编码：GB2312、GBK、GB18030](https://www.qqxiuzi.cn/bianma/guobiaoma.php)

2 bytes per character, with leading bit 1
