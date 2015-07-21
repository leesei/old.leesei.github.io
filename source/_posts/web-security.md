title: "Web Security"
date: 2015-05-18 09:52:27
categories:
- web
tags:
- security
toc: true
---

[Category:Web security exploits - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Category:Web_security_exploits)
[The Open Web Application Security Project (OWASP)](https://www.owasp.org/index.php/Main_Page)
[The ^lift Security Blog](https://blog.liftsecurity.io/)

[Node.js application (in)security - Ilja van Sprundel - OWASP AppSec California 2015 - YouTube](https://www.youtube.com/watch?v=4J6-IFqyBjY)

[Logjam, Part 1: Why the Internet is Broken Again (an Explainer) | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2015/05/logjam-internet-breaks-again)

[Single Page Web App Security Cheat Sheet](https://github.com/eoftedal/writings/blob/master/published/javascript-security-cheat-sheet.md)

[Frontend Security - Frontend Conf 2013, Zürich - YouTube](https://www.youtube.com/watch?v=fYjO5pIY1mY)

[Web Security @ SFHTML5 - YouTube](https://www.youtube.com/playlist?list=PLOU2XLYxmsIIkEU3Z_xdVo9EADurbdxKa)

> see also `ssl-tls.md`

## XSS

[Cross-site scripting - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Cross-site_scripting)
[SQL injection - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/SQL_injection)

These are vulnerbilities that **exploits trust on user inputs**, the app renders or executes them without sanity check and escaping.

## XSRF

[Cross-site request forgery - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Cross-site_request_forgery)

These are vulnerbilities that **exploits trust on user's browser**. Malicious scripts initiates attack from user's browser to reuse the token it stores. The attack usually involves form submit or API call.

The counter-measure is to create unique tokens for each form or each login.

## CORS

## Buffer Overflow

[Writing buffer overflow exploits - a tutorial for beginners](http://www.eecis.udel.edu/~bmiller/cis459/2007s/readings/buff-overflow.html)

