---
title: "Regular expression"
date: 2015-02-26 17:55:43
categories:
- comp.lang
tags:
- formal-language
- regex
- javascript
- python
- ruby
- perl
- notes
toc: true
---

[Regular expression](http://www.wikiwand.com/en/Regular_expression) is a [formal language](http://www.wikiwand.com/en/Formal_language) for pattern matching. Different languages supports different feature sets and have different syntaxes, see summary [here](http://www.greenend.org.uk/rjk/tech/regexp.html).

[The true power of regular expressions](https://nikic.github.io/2012/06/15/The-true-power-of-regular-expressions.html)

<!-- more -->

## Learning

[Learn regular expressions in about 55 minutes](http://qntm.org/files/re/re.html)
[Regex Tutorial—From Regex 101 to Advanced Regex](http://www.rexegg.com/)
[RegexOne - Learn Regular Expressions](http://regexone.com/)
[Regular-Expressions.info - Regex Tutorial, Examples and Reference - Regexp Patterns](http://www.regular-expressions.info/)
[Tech Stuff - Regular Expressions - A Gentle User Guide and Tutorial](http://zytrax.com/tech/web/regex.htm)
[zeeshanu/learn-regex: Learn regex the easy way](https://github.com/zeeshanu/learn-regex)
[Learn Regular Expressions in 20 Minutes | Tutorialzine](http://tutorialzine.com/2014/12/learn-regular-expressions-in-20-minutes/)

[Best of Fluent 2012: /Reg(exp){2}lained/: Demystifying Regular Expressions - YouTube](https://www.youtube.com/watch?v=EkluES9Rvak)

[VerbalExpressions ♥ Open Source](http://verbalexpressions.github.io/)

## Visualizer

Use these visualizers to help you understand the regexes.

[Debuggex](https://www.debuggex.com/) (JavaScript, Python, PCRE)

[Regulex：JavaScript Regular Expression Visualizer.](http://jex.im/regulex/)
[Regexper](http://www.regexper.com/) (JavaScript)

[txt2re: headache relief for programmers :: regular expression generator](http://txt2re.com/)

## Tester

These highlight matches in input test string.

[Online regex tester and debugger: JavaScript, Python, PHP, and PCRE](https://regex101.com/) (with explanation)
[RegExr: Learn, Build, & Test RegEx](http://www.regexr.com/) (JavaScript)
[Regex Builder](http://ysmood.github.io/regex-builder/) (JavaScript)
[Regex Tester - Javascript, PCRE, PHP](http://www.regexpal.com/)
[RegExp playground](http://leaverou.github.io/regexplained/) (JavaScript)
[ReFiddle](http://refiddle.com/) (JavaScript, Ruby, .Net)
[Python Regex Tool](http://www.pythonregex.com/)
[Rubular: a Ruby regular expression editor and tester](http://rubular.com/)

## #perfmatters

[Five Invaluable Techniques to Improve Regex Performance](https://www.loggly.com/blog/five-invaluable-techniques-to-improve-regex-performance/)
[Runaway Regular Expressions: Catastrophic Backtracking](http://www.regular-expressions.info/catastrophic.html)
[Regular expression (regex) performance: The fundamental guide — / org.site-reliability — Medium](https://site-reliability.org/regular-expression-regex-performance-the-fundamental-guide-3d39e6af33af#.bd4qad54r)
[Optimizing regular expressions in Java | JavaWorld](http://www.javaworld.com/article/2077757/core-java/optimizing-regular-expressions-in-java.html)
[What you should know about JavaScript regular expressions](http://bjorn.tipling.com/state-and-regular-expressions-in-javascript)

[Flagrant Badassery » Performance of Greedy vs. Lazy Regex Quantifiers](http://blog.stevenlevithan.com/archives/greedy-lazy-performance)
[Flagrant Badassery » Capturing vs. Non-Capturing Groups](http://blog.stevenlevithan.com/archives/capturing-vs-non-capturing-groups)
[Flagrant Badassery » Regexes in Depth: Advanced Quoted String Matching](http://blog.stevenlevithan.com/archives/match-quoted-string)
[Flagrant Badassery » Matching Nested Constructs in JavaScript](http://blog.stevenlevithan.com/archives/javascript-match-nested)
[Flagrant Badassery » Matching Nested Constructs in JavaScript, Part 2](http://blog.stevenlevithan.com/archives/javascript-match-recursive-regexp)
[Flagrant Badassery » Regex Recursion (Matching Nested Constructs)](http://blog.stevenlevithan.com/archives/regex-recursion)

## POSIX ERE

[Tech Stuff - Regular Expressions - A Gentle User Guide and Tutorial](http://zytrax.com/tech/web/regex.htm)
[Regular expression - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Regular_expression#Standards)
[The conditional expression [Bash Hackers Wiki]](http://wiki.bash-hackers.org/syntax/ccmd/conditional_expression)
[Patterns and pattern matching [Bash Hackers Wiki]](http://wiki.bash-hackers.org/syntax/pattern)

[Bash double bracket regex comparison using negative lookahead error return 2 - Stack Overflow](http://stackoverflow.com/questions/30905017/bash-double-bracket-regex-comparison-using-negative-lookahead-error-return-2)

## Perl (PCRE)

I think Perl's regex is the most expressive and portable (via wide support of Perl Compatible Regular Expressions).

[PCRE - Perl Compatible Regular Expressions](https://pcre.org/)
[PCRE Regular Expression Cheatsheet - Debuggex](https://www.debuggex.com/cheatsheet/regex/pcre)

`grep` support PCRE with `-P` option.

```sh
man 3 pcrepattern
man 3 pcresyntax
man 1 perlre
```

[perlre - perldoc.perl.org](http://perldoc.perl.org/perlre.html)
[perlretut - perldoc.perl.org](http://perldoc.perl.org/perlretut.html)
[Perl Regular Expression Syntax - 1.44.0](http://www.boost.org/doc/libs/1_44_0/libs/regex/doc/html/boost_regex/syntax/perl_syntax.html)

[rust-lang/regex: An implementation of regular expressions for Rust. This implementation uses finite automata and guarantees linear time matching on all inputs.](https://github.com/rust-lang/regex)

```sh
echo "123\n456" | perl -n -e '/[15](\d+)/ && print "$1\n"'
```

## JavaScript

JavaScript's Regex does not have look behind and named captures. Use [XRegExp](http://xregexp.com/) if you need them.
> [Upcoming Regular Expression Features  |  Web  |  Google Developers](https://developers.google.com/web/updates/2017/07/upcoming-regexp-features) Chrome begin to support these features in 2018

[JavaScript Regular Expression Cheatsheet - Debuggex](https://www.debuggex.com/cheatsheet/regex/javascript)

[JavaScript: an overview of the regular expression API](http://www.2ality.com/2011/04/javascript-overview-of-regular.html)
[The flag /g of JavaScript’s regular expressions](http://www.2ality.com/2013/08/regexp-g.html)

[RegExps — Centralized place for community-driven collections of RegExp patterns and tools that can make our life easier.](http://regexps.github.io/)

[hokein/Automata.js](https://github.com/hokein/Automata.js) converts Regex to FSM
[jwerle/sregex](https://github.com/jwerle/sregex)
[dtao/simplex](https://github.com/dtao/simplex)

[VerbalExpressions/JSVerbalExpressions](https://github.com/VerbalExpressions/JSVerbalExpressions)

## Python

[Python Regular Expression Cheatsheet - Debuggex](https://www.debuggex.com/cheatsheet/regex/python)

[Regular Expression HOWTO — Python documentation](https://docs.python.org/3/howto/regex.html)
[6.2. re — Regular expression operations — Python documentation](https://docs.python.org/3/library/re.html)
[Python Regular Expressions - Google for Education — Google Developers](https://developers.google.com/edu/python/regular-expressions)

[python - Named regular expression group "(?P<group_name>regexp)": what does "P" stand for? - Stack Overflow](http://stackoverflow.com/questions/10059673/named-regular-expression-group-pgroup-nameregexp-what-does-p-stand-for)

[Kodos - The Python Regex Debugger](http://kodos.sourceforge.net/)
[Google Code Archive - kiki-re](https://code.google.com/archive/p/kiki-re/)

## Ruby


## Other resources

[Implementing Regular Expressions](http://swtch.com/~rsc/regexp/)
