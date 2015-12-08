---
title: "Web Security"
date: 2015-05-18 09:52:27
categories:
- web
tags:
- security
toc: true
---

[Category:Web security exploits - Wikiwand](http://www.wikiwand.com/en/Category:Web_security_exploits)
[The Open Web Application Security Project (OWASP)](https://www.owasp.org/index.php/Main_Page)
[The ^lift Security Blog](https://blog.liftsecurity.io/)

[Node.js application (in)security - Ilja van Sprundel - OWASP AppSec California 2015 - YouTube](https://www.youtube.com/watch?v=4J6-IFqyBjY)

[Logjam, Part 1: Why the Internet is Broken Again (an Explainer) | Electronic Frontier Foundation](https://www.eff.org/deeplinks/2015/05/logjam-internet-breaks-again)

[Single Page Web App Security Cheat Sheet](https://github.com/eoftedal/writings/blob/master/published/javascript-security-cheat-sheet.md)

[Frontend Security - Frontend Conf 2013, Zürich - YouTube](https://www.youtube.com/watch?v=fYjO5pIY1mY)

[Web Security @ SFHTML5 - YouTube](https://www.youtube.com/playlist?list=PLOU2XLYxmsIIkEU3Z_xdVo9EADurbdxKa)

[Feisty Duck: Fine computer security and open source books](https://www.feistyduck.com/)

[Node Security Project](https://nodesecurity.io/)

> see also `ssl-tls.md`

## XSS

[Cross-site scripting - Wikiwand](http://www.wikiwand.com/en/Cross-site_scripting)
[SQL injection - Wikiwand](http://www.wikiwand.com/en/SQL_injection)

[Excess XSS: A comprehensive tutorial on cross-site scripting](http://excess-xss.com/)

These are vulnerabilities that **exploits trust on user inputs**, the app renders or executes them without sanity check and escaping.

## XSRF

[Cross-site request forgery - Wikipedia, the free encyclopedia](http://en.wikipedia.org/wiki/Cross-site_request_forgery)

These are vulnerbilities that **exploits trust on user's browser**. Malicious scripts initiates attack from user's browser to reuse the token it stores. The attack usually involves form submit or API call.

The counter-measure is to create unique tokens for each form or each login.

## CORS

[Using CORS - HTML5 Rocks](http://www.html5rocks.com/en/tutorials/cors/)
[enable cross-origin resource sharing](http://enable-cors.org/index.html)
[Getting CORS Working](https://remysharp.com/2011/04/21/getting-cors-working)

## Buffer Overflow

[Writing buffer overflow exploits - a tutorial for beginners](http://www.eecis.udel.edu/~bmiller/cis459/2007s/readings/buff-overflow.html)

