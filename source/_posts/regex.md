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
[Learn Regular Expressions in 20 Minutes | Tutorialzine](http://tutorialzine.com/2014/12/learn-regular-expressions-in-20-minutes/)

[Best of Fluent 2012: /Reg(exp){2}lained/: Demystifying Regular Expressions - YouTube](https://www.youtube.com/watch?v=EkluES9Rvak)

## Visualizer

Use these visualizers to help you understand the regexes.

[Debuggex: Online visual regex tester. JavaScript, Python, and PCRE.](https://www.debuggex.com/)

[Regulex：JavaScript Regular Expression Visualizer.](http://jex.im/regulex/)
[Regexper](http://www.regexper.com/) (JavaScript)

[txt2re: headache relief for programmers :: regular expression generator](http://txt2re.com/)

## Tester

These highlight matches in test string.

[Online regex tester and debugger: JavaScript, Python, PHP, and PCRE](https://regex101.com/) (with explanation)
[RegExr: Learn, Build, & Test RegEx](http://www.regexr.com/) (JavaScript)
[Regex Builder](http://ysmood.github.io/regex-builder/) (JavaScript)
[RegExp playground](http://leaverou.github.io/regexplained/) (JavaScript)
[ReFiddle](http://refiddle.com/) (JavaScript, Ruby, .Net)
[Python Regex Tool](http://www.pythonregex.com/)
[Rubular: a Ruby regular expression editor and tester](http://rubular.com/)

## POSIX ERE

[Tech Stuff - Regular Expressions - A Gentle User Guide and Tutorial](http://zytrax.com/tech/web/regex.htm)
[Regular expression - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Regular_expression#Standards)
[The conditional expression [Bash Hackers Wiki]](http://wiki.bash-hackers.org/syntax/ccmd/conditional_expression)
[Patterns and pattern matching [Bash Hackers Wiki]](http://wiki.bash-hackers.org/syntax/pattern)

[Bash double bracket regex comparison using negative lookahead error return 2 - Stack Overflow](http://stackoverflow.com/questions/30905017/bash-double-bracket-regex-comparison-using-negative-lookahead-error-return-2)

## Perl (PCRE)

I think Perl's regex is the most expressive and portable (via wide support of Perl Compatible Regular Expressions).
`grep` support PCRE with `-P` option.

```sh
man 3 pcrepattern
man 3 pcresyntax
man 1 perlre
```

[perlre - perldoc.perl.org](http://perldoc.perl.org/perlre.html)
[perlretut - perldoc.perl.org](http://perldoc.perl.org/perlretut.html)
[Perl Regular Expression Syntax - 1.44.0](http://www.boost.org/doc/libs/1_44_0/libs/regex/doc/html/boost_regex/syntax/perl_syntax.html)

```sh
echo "123\n456" | perl -n -e '/[15](\d+)/ && print "$1\n"'
```

## JavaScript

JavaScript's Regex does not have look behind and named captures.
Use [XRegExp](http://xregexp.com/) if you need them.

[JavaScript: an overview of the regular expression API](http://www.2ality.com/2011/04/javascript-overview-of-regular.html)
[The flag /g of JavaScript’s regular expressions](http://www.2ality.com/2013/08/regexp-g.html)

## Python

[Regular Expression HOWTO — Python 2.7.9 documentation](https://docs.python.org/2/howto/regex.html)
[7.2. re — Regular expression operations — Python 2.7.9 documentation](https://docs.python.org/2/library/re.html)
[Python Regular Expressions - Google for Education — Google Developers](https://developers.google.com/edu/python/regular-expressions)

## Ruby


## Other resources

[Implementing Regular Expressions](http://swtch.com/~rsc/regexp/)
