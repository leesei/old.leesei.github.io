---
title: Testing
categories:
  - comp.lang
toc: true
date: 2015-06-17 11:08:48
tags:
  - testing
  - unit-test
---

[Unit testing - Wikiwand](http://www.wikiwand.com/en/Unit_testing)
[Test automation - Wikiwand](http://www.wikiwand.com/en/Test_automation)
[List of unit testing frameworks - Wikiwand](http://www.wikiwand.com/en/List_of_unit_testing_frameworks)
[Unit Testing Succinctly - Envato Tuts+ Code Tutorials](http://code.tutsplus.com/series/unit-testing-succinctly--cms-675)

Unit test (a single function)
Integration tests (multiple classes/units)
Functional tests (user-oriented, high level, full stack)
Smoke tests (quickly determine if the system is "working")

Integration/Functional Test: do the pieces work together as I expected?
Unit Test: given input _x_, is the output _y_?
[JavaScript Testing: Unit vs Functional vs Integration Tests](http://www.sitepoint.com/javascript-testing-unit-functional-integration/) !important
[What are Unit Testing, Integration Testing and Functional Testing? | CodeUtopia](https://codeutopia.net/blog/2015/04/11/what-are-unit-testing-integration-testing-and-functional-testing/)
[testing - What is Unit test, Integration Test, Smoke test, Regression Test? - Stack Overflow](http://stackoverflow.com/questions/520064/what-is-unit-test-integration-test-smoke-test-regression-test)
[Better software testing through automation | InfoWorld](http://www.infoworld.com/article/3068598/application-development/better-software-testing-through-automation.html)

[bbc/notes-on-perf-testing: An open-source book on system performance testing](https://github.com/bbc/notes-on-perf-testing)

## Theory

### Developer's aspect

[TDD, RDD and DDD](http://eigenhombre.com/tdd-rdd-and-ddd.html) Test-driven development, REPL-driven development, Documentation-driven development
[Tests as documentation | Technology Conversations](http://technologyconversations.com/2014/04/08/tests-as-documentation/)
[Giving Up on TDD - Clean Coder Blog](http://blog.cleancoder.com/uncle-bob/2016/03/19/GivingUpOnTDD.html)

[Test-driven development - Wikiwand](https://www.wikiwand.com/en/Test-driven_development)
[Test-Driven Development (TDD) | Technology Conversations](http://technologyconversations.com/2014/09/30/test-driven-development-tdd/)

[Behavior-driven development - Wikiwand](https://www.wikiwand.com/en/Behavior-driven_development)
[Introducing BDD | Dan North & Associates](http://dannorth.net/introducing-bdd/)
[What’s in a Story? | Dan North & Associates](http://dannorth.net/whats-in-a-story/)
[BDD Assistant: It’s alive and cries for help | Technology Conversations](http://technologyconversations.com/2014/09/02/bdd-assistant-its-alive-and-cries-for-help/)
[BDD (Behavior-Driven Development): Missing Piece in the Continuous Integration Puzzle | Technology Conversations](http://technologyconversations.com/2014/07/23/bdd-behavior-driven-development-missing-piece-in-the-continuous-integration-puzzle/)

[What’s the difference between Unit Testing, TDD and BDD? | CodeUtopia](http://codeutopia.net/blog/2015/03/01/unit-testing-tdd-and-bdd/)
[What is the difference between writing test cases for BDD and TDD? - Programmers Stack Exchange](http://programmers.stackexchange.com/questions/135218/what-is-the-difference-between-writing-test-cases-for-bdd-and-tdd)
[Relation between BDD and TDD - Programmers Stack Exchange](http://programmers.stackexchange.com/questions/111837/relation-between-bdd-and-tdd)
[From BDD to TDD, the pros and cons of various agile techniques | InfoWorld](https://www.infoworld.com/article/3269039/agile-development/from-bdd-to-tdd-the-pros-and-cons-of-various-agile-techniques.html)
[The Truth about BDD - Clean Coder](https://sites.google.com/site/unclebobconsultingllc/the-truth-about-bdd)

[Common Myths and Misconceptions of Test Driven Development - DEV Community 👩‍💻👨‍💻](https://dev.to/mrlarson2007/common-myths-and-misconceptions-of-test-driven-development-jcn)
[Six Ways of Improving Behaviour-Driven Development](http://www.infoq.com/news/2015/07/six-bdd-improvements)
[The WHY behind TDD/BDD and the HOW with RSpec](http://www.slideshare.net/bmabey/the-why-behind-tddbdd-and-the-how-with-rspec)
[5 Questions Every Unit Test Must Answer — JavaScript Scene — Medium](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)
[5 Common Misconceptions About TDD & Unit Tests — JavaScript Scene — Medium](https://medium.com/javascript-scene/5-common-misconceptions-about-tdd-unit-tests-863d5beb3ce9)
[One weird trick that will change the way you code forever: JavaScript TDD](http://jrsinclair.com/articles/2016/one-weird-trick-that-will-change-the-way-you-code-forever-javascript-tdd/)

#### Unit Test Fetish/Lean Testing

Unit test cons:

- increase maintenance
- too focus on edge case
- too isolated
- heavily relies on mocking
- code coverage != quality

[Lean Testing or Why Unit Tests are Worse than You Think](https://blog.usejournal.com/lean-testing-or-why-unit-tests-are-worse-than-you-think-b6500139a009)
[Write tests. Not too many. Mostly integration. – kentcdodds](https://blog.kentcdodds.com/write-tests-not-too-many-mostly-integration-5e8c7fff591c)
[Kent C. Dodds – Write tests. Not too many. Mostly integration. - YouTube](https://www.youtube.com/watch?v=Fha2bVoC8SE)
[Unit Test Fetish - 250bpm](http://250bpm.com/blog:40)
[Exploding Software-Engineering Myths - Microsoft Research](https://www.microsoft.com/en-us/research/blog/exploding-software-engineering-myths/)
[Why-Most-Unit-Testing-is-Waste.pdf](https://rbcs-us.com/documents/Why-Most-Unit-Testing-is-Waste.pdf)

[TestPyramid](https://martinfowler.com/bliki/TestPyramid.html)
[Unit Testing: The Good, Bad, and Ugly - DZone Performance](https://dzone.com/articles/unit-testing-the-good-bad-amp-ugly)

### QA's aspect

[Open Lecture by James Bach on Software Testing - YouTube](https://www.youtube.com/watch?v=ILkT_HV9DVU)

[如何测试洗牌程序 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/8593.html)

### Klarna Engineering

[How removing caching improved mobile performance by 25%](https://engineering.klarna.com/how-removing-caching-improved-mobile-performance-by-25-52a17cc339a2#.lxdf2jmr5)
[Four reasons developers should write their own load tests](https://engineering.klarna.com/four-reasons-developers-should-write-their-own-load-tests-fac74c1be9f1#.blg2y1q68)
[Four load testing mistakes developers love to make](https://engineering.klarna.com/four-load-testing-mistakes-developers-love-to-make-68b443f7e8a2#.n00gc1s2b)

## User story

[How to write Well-Formed User Stories | Pivotal P.O.V.](https://blog.pivotal.io/labs/labs/well-formed-stories)

```
Scenario: title
Given [some context]
And [additional context]
When [event]
Then [outcome]
```

### Gherkin/Cucumber

Gherkin is a human and machine friendly spec for specifying behavior:
[Cucumber](https://docs.cucumber.io/)
[Gherkin Syntax : Cucumber](https://docs.cucumber.io/gherkin/)
[Feature Introduction · cucumber/cucumber Wiki](https://github.com/cucumber/cucumber/wiki/Feature-Introduction)

[Behavior-driven development - Wikiwand](https://www.wikiwand.com/en/Behavior-driven_development#/Behavioral_specifications)

[Behat documentation](http://docs.behat.org/en/latest/user_guide/writing_scenarios.html)
[Writing better user stories with Gherkin and Cucumber](https://medium.com/@mvwi/story-writing-with-gherkin-and-cucumber-1878124c284c)
[BDD 101: Gherkin By Example | Automation Panda](https://automationpanda.com/2017/01/27/bdd-101-gherkin-by-example/)
[behave/features at master · behave/behave](https://github.com/behave/behave/tree/master/features) examples

[Behavior-Driven Development in Python](https://code.tutsplus.com/tutorials/behavior-driven-development-in-python--net-26547)
[Python Testing 101: behave | Automation Panda](https://automationpanda.com/2018/05/11/python-testing-101-behave/)
[What is behavior-driven Python? | Opensource.com](https://opensource.com/article/18/5/behavior-driven-python)

[cucumber/gherkin at master · cucumber/cucumber](https://github.com/cucumber/cucumber/tree/master/gherkin) Cross platform parser for the Gherkin language
[Related tools : Cucumber](https://docs.cucumber.io/tools/related-tools/)
[Cucumber Selenium tutorials - YouTube](https://www.youtube.com/playlist?list=PLmjcJNp9bQu-rWVEdLotVdYoWsmX2nWvL&disable_polymer=true)

[Custom Formatters · cucumber/cucumber Wiki](https://github.com/cucumber/cucumber/wiki/Custom-Formatters)
[cucumber/cucumber-html: Cross platform HTML formatter for all implementations of Cucumber](https://github.com/cucumber/cucumber-html)
[wswebcreation/multiple-cucumber-html-reporter: Generate beautiful Cucumber HTML reports](https://github.com/wswebcreation/multiple-cucumber-html-reporter)
[brynary/features2cards: Create PDFs from Cucumber features and scenarios for printing](https://github.com/brynary/features2cards)

### Test Runners

[高效开发运维](https://mp.weixin.qq.com/s?__biz=MzIzNjUxMzk2NQ==&mid=2247489346&idx=1&sn=7cb439ab65ccc8680f408ba5390d965f&chksm=e8d7e880dfa06196aed7860e5fadbf07ac8ac73e45be0c10011fe41de6e4fbfbd7d8f15caccc&scene=27#wechat_redirect)

Some test runners take the features and generate test scripts in various languages.

[Robot Framework](http://robotframework.org/) Python
[RedwoodHQ | Open Source Test Automation Framework](http://redwoodhq.com/) polyglot
[Cucumber project](https://cucumber.io/) polyglot
[Cucumber, BDD and 21st Century Hackable Atom Editor - SHASHIKANT JAGTAP](http://shashikantjagtap.net/cucumber-bdd-githubs-atom-editor/)
[behave](http://pythonhosted.org/behave/index.html) Python
[Behat](http://docs.behat.org/en/latest) PHP

## Automated Testing

[Automated Testing: Your End-to-End Ecosystem - DZone - Research Guides](https://dzone.com/guides/automated-testing-your-end-to-end-ecosystem)

[From 0 to 100: How to Get Into Automated Testing as a Manual Tester - DZone Agile](https://dzone.com/articles/from-0-to-100-how-to-get-into-automated-testing-as)
[What's the Difference Between Automated Testing and Manual Testing? - DZone Performance](https://dzone.com/articles/automated-testing-vs-manual-testing)

## Ad-hoc standard

[xUnit - Wikiwand](http://www.wikiwand.com/en/XUnit)
[Test Anything Protocol - Wikiwand](http://www.wikiwand.com/en/Test_Anything_Protocol) [TAP](https://testanything.org/) is a simple text-based interface between testing modules in a test harness. Many test frameworks can output TAP results.
[Main Page - Test Anything Protocol](http://testanything.org/)

<!-- more -->

---

## Shell Script

[jimeh/test-runner.sh](https://github.com/jimeh/test-runner.sh)
[jimeh/stub.sh](https://github.com/jimeh/stub.sh)
[sstephenson/bats](https://github.com/sstephenson/bats)

[shunit2 - Google Search](https://www.google.com.hk/search?q=shunit2&oq=shunit2&aqs=chrome..69i57j69i60l2&sourceid=chrome&es_sm=93&ie=UTF-8)
[Chaos Engineering 101 — Production Ready — Medium](https://medium.com/production-ready/chaos-engineering-101-1103059fae44)
[Chaos Monkey for Fun and Profit — Production Ready — Medium](https://medium.com/production-ready/chaos-monkey-for-fun-and-profit-87e2f343db31)

## Chaos Engineering

[Principles of Chaos Engineering](http://principlesofchaos.org/)
[chaos.community](http://chaos.community/)
[Chaos Engineering 101 — Production Ready — Medium](https://medium.com/production-ready/chaos-engineering-101-1103059fae44)
[Chaos Monkey for Fun and Profit — Production Ready — Medium](https://medium.com/production-ready/chaos-monkey-for-fun-and-profit-87e2f343db31)
[The Netflix Simian Army – Netflix TechBlog – Medium](https://medium.com/netflix-techblog/the-netflix-simian-army-16e57fbab116)
[How To Establish a High Severity Incident Management Program](https://www.gremlin.com/community/tutorials/how-to-establish-a-high-severity-incident-management-program/)
[Chaos Engineering: Chaos Testing Your HTTP Micro-Services](https://hackernoon.com/chaos-engineering-chaos-testing-your-http-micro-services-acc99d145515)

[Netflix 混沌工程手册](https://www.infoq.cn/theme/13)
[微服务架构下的质量迷思——混沌工程](https://www.infoq.cn/article/GQYkuMBWOF00CR_VxgDg)

[SE-Radio-Episode-325: Tammy Butow on Chaos Engineering : Software Engineering Radio](http://www.se-radio.net/2018/05/se-radio-episode-325-tammy-butow-on-chaos-engineering/)

[marmelab/gremlins.js: Monkey testing library for web apps and Node.js](https://github.com/marmelab/gremlins.js)

[Gremlin: Chaos Engineering Tools to Break Things on Purpose](https://www.gremlin.com/)
[Overview - Gremlin Help](https://help.gremlin.com/)
[How Gremlin is making chaos engineering accessible [Interview] | Packt Hub](https://hub.packtpub.com/how-gremlin-is-making-chaos-engineering-accessible-interview/)

## Android

[Automating User Interface Testing on Android - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/automating-user-interface-testing-on-android--cms-23969)

[LAVA](https://validation.linaro.org/)
[LAVA Manual — LAVA Server 2015.07 documentation](https://validation.linaro.org/static/docs/#)

## C

[Write Async Test Case by gtest & gmock for C++ | Thinking beyond Source Code](http://www.thinksrc.com/2016/03/18/write-async-test-case-by-gtest-gmock-for-c.html)

## UI automation

[Sikuli Script - Home](http://www.sikuli.org/)
[AutoIt](https://www.autoitscript.com/)

### PyAutoGUI

[Welcome to PyAutoGUI’s documentation!](https://pyautogui.readthedocs.io/en/latest/)
[Cheat Sheet — PyAutoGUI documentation](https://pyautogui.readthedocs.io/en/latest/cheatsheet.html)
[Automating keyboard and mouse with Python – Ankush Chatterjee – Medium](https://medium.com/@ankushc/automating-keyboard-and-mouse-with-python-985432e4b3bf)

## HTTP endpoint

[SoapUI | Functional Testing for SOAP and REST APIs](https://www.soapui.org/)
[mapbox/assert-http: Test helpers for testing a HTTP interface](https://github.com/mapbox/assert-http)
[Gor - test your system with real data](https://gortool.com/)

[Polly.JS](https://netflix.github.io/pollyjs/#/)

[apiaryio/dredd: Language-agnostic HTTP API Testing Framework](https://github.com/apiaryio/dredd#readme)
[Command-line Interface - Dredd](https://dredd.readthedocs.io/en/latest/usage-cli/)

### JavaScript

[visionmedia/supertest](https://github.com/visionmedia/supertest) testing server API with extended [superagent](https://github.com/visionmedia/superagent)
[Testable API's with Node.js](http://beletsky.net/2014/03/testable-apis-with-node-dot-js.html)

## Python

[pytest: helps you write better programs — pytest documentation](https://docs.pytest.org/en/latest/)
[Testing Your Code with Python's pytest | Linux Journal](https://www.linuxjournal.com/content/testing-your-code-pythons-pytest)
[hackebrot/pytest-emoji: pytest + emoji ==](https://github.com/hackebrot/pytest-emoji)
[hackebrot/pytest-tricks: Tips and Tricks for the Python Testing Tool](https://github.com/hackebrot/pytest-tricks)

[Note to Users — nose documentation](https://nose.readthedocs.io/en/latest/) nose extends unittest to make testing easier.
[unittest — Unit testing framework — Python documentation](https://docs.python.org/3/library/unittest.html#module-unittest)

[26.3. doctest — Test interactive Python examples — Python 3 documentation](https://docs.python.org/3/library/doctest.html)
[doctest - Wikiwand](https://www.wikiwand.com/en/Doctest)
[doctest — Testing Through Documentation — PyMOTW 3](https://pymotw.com/3/doctest/)

[Getting Started With Testing in Python – Real Python](https://realpython.com/python-testing/)

[Welcome to the tox automation project — tox documentation](https://tox.readthedocs.io/en/latest/)

## JavaScript

> TODO: Define "Test runner", "Assertion", "Framework"

[An Overview of JavaScript Testing in 2017 – powtoon-engineering – Medium](https://medium.com/powtoon-engineering/a-complete-guide-to-testing-javascript-in-2017-a217b4cd5a2a) !important
[Testing Node.js in 2018 – Hacker Noon](https://hackernoon.com/testing-node-js-in-2018-10a04dd77391)
[Incredibly convenient testing of front-end Javascript with Node.js - Staal Forge](http://staal.io/blog/2013/08/17/incredibly-convenient-testing-of-frontend-javascript-with-node-dot-js/)
[5 Questions Every Unit Test Must Answer — JavaScript Scene — Medium](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)
[6. Writing Testable JavaScript - YouTube](https://www.youtube.com/watch?v=OzjogCFO4Zo)
[Codeship's Philosophical Approach to Frontend Testing - via @codeship | via @codeship](https://blog.codeship.com/codeships-philosophical-approach-to-frontend-testing)

[Promises in JavaScript Unit Tests: the Definitive Guide](http://www.sitepoint.com/promises-in-javascript-unit-tests-the-definitive-guide/)
[Testing Node.js with Mocha and Chai - Michael Herman](http://mherman.org/blog/2015/09/10/testing-node-js-with-mocha-and-chai/)

[A Gentle Introduction to Javascript Test Driven Development: Part 1](http://jrsinclair.com/articles/2016/gentle-introduction-to-javascript-tdd-intro/)
[A Gentle Introduction to Javascript Test Driven Development: Part 2](http://jrsinclair.com/articles/2016/gentle-introduction-to-javascript-tdd-ajax/)
[A Gentle Introduction to Javascript Test Driven Development: Part 3](http://jrsinclair.com/articles/2016/gentle-introduction-to-javascript-tdd-html-dom/)

### Frameworks

[SpeckJS - Comment Driven Development](http://speckjs.github.io/)

[Intern: Software testing for humans](https://theintern.github.io/) [video](https://www.youtube.com/watch?v=_KFjuEKLqDA)

[avajs/ava: Futuristic JavaScript test runner](https://github.com/avajs/ava)
[AVA, low-config testing for JavaScript](https://dev.to/hugo__df/ava-low-config-testing-for-javascript)

[mochajs/mocha: ☕️ simple, flexible, fun javascript test framework for node.js & the browser](https://github.com/mochajs/mocha) pollutes global namespace, need assertion library, say [chai](http://chaijs.com/)

[bevry/joe: Joe is an accurate and powerful testing framework that can run on node and in the browser](https://github.com/bevry/joe)
[Welcome! Buster.JS is...](http://docs.busterjs.org/en/latest/)
[Vows « Asynchronous BDD for Node](http://vowsjs.org/)

#### Comparison

[Essential JavaScript: the top five testing libraries | JavaScript | Creative Bloq](http://www.creativebloq.com/javascript/essential-javascript-top-five-testing-libraries-10126048)

[List of unit testing frameworks (JavaScript) - Wikiwand](http://www.wikiwand.com/en/List_of_unit_testing_frameworks#/JavaScript)
[thegrtman/javascript-test-framework-comparison](https://github.com/thegrtman/javascript-test-framework-comparison)
[coderwall.com : establishing geek cred since 1305712800](https://coderwall.com/p/ntbixw/javascript-test-framework-comparison)
[JavaScript unit test tools for TDD - Stack Overflow](http://stackoverflow.com/questions/300855/javascript-unit-test-tools-for-tdd)

#### lab

[hapijs/lab: Node.js test framework](https://github.com/hapijs/lab) (need assertion library, say [code](https://github.com/hapijs/code/), includes coverage)
[hapijs/shot: Injects a fake HTTP request/response into your node server logic](https://github.com/hapijs/shot)
[hapi — Getting Started With Testing Using Lab and Code](https://futurestud.io/tutorials/hapi-getting-started-with-testing-using-lab-and-code)
[Chapter 7: Testing using lab | Hapi With Typescript | Softcover.io](https://hapibook.jjude.com/book/lab)

[nlf/lab-babel: A transform to allow testing babel.js transpiled code in lab more effectively](https://github.com/nlf/lab-babel)

```js
const Lab = require("lab");

// Test files must require the lab module, and export a test script
const lab = (exports.lab = Lab.script());

// shortcuts to functions from lab
const experiment = lab.experiment;
const test = lab.test;

experiment("getting started with hapi testing,", () => {
  test("lab considers this test as TOOD and skips it");

  test("always succeeding :)", () => {});
});
```

#### Mock/Stub

[Sinon.JS](http://sinonjs.org/) provides AJAX mock and spy that work in all test frameworks.
[Sinon Tutorial: JavaScript Testing with Mocks, Spies & Stubs](http://www.sitepoint.com/sinon-tutorial-javascript-testing-mocks-spies-stubs/)
[marmelab/FakeRest: Patch fetch/XMLHttpRequest to fake a REST API server in the browser, based on JSON data.](https://github.com/marmelab/FakeRest)

[pgte/nock](https://github.com/pgte/nock)
[Intercept HTTP Requests with Node.js nock](http://davidwalsh.name/nock)
[REM - REST API](http://rem-rest-api.herokuapp.com/)

[typicode/json-server: Get a full fake REST API with zero coding in less than 30 seconds (seriously)](https://github.com/typicode/json-server)
[WireMock - WireMock](http://wiremock.org/)

[Marak/faker.js](https://github.com/marak/Faker.js/)
[Chance.js: Utility library to generate anything random for JavaScript](http://chancejs.com/)
[drewbrokke/chance-token-replacer](https://github.com/drewbrokke/chance-token-replacer)
[adleroliveira/dreamjs: A lightweight json data generator.](https://github.com/adleroliveira/dreamjs)
[json-schema-faker/json-schema-faker: JSON-Schema + Faker](https://github.com/json-schema-faker/json-schema-faker)
[danibram/mocker-data-generator](https://github.com/danibram/mocker-data-generator/)
[aharris88/awesome-ipsum](https://github.com/aharris88/awesome-ipsum)

[mfncooper/mockery: Simplifying the use of mocks with Node.js](https://github.com/mfncooper/mockery)
[thlorenz/proxyquire: Proxies nodejs require in order to allow overriding dependencies during testing.](https://github.com/thlorenz/proxyquire)
[rvagg/node-mkfiletree](https://github.com/rvagg/node-mkfiletree)

[Introducing frock: Easy fake services for a microservices environment](https://www.urbanairship.com/blog/introducing-frock-easy-fake-services-for-a-microservices-environment)
[urbanairship/frock: A plugin-based tool for running fake HTTP and socket services](https://github.com/urbanairship/frock)

[LINKIWI/endpoint: Super simple mock API endpoints for static JSON data](https://github.com/LINKIWI/endpoint/)

[Raathigesh/Atmo: Server side powertool for prototyping](https://github.com/Raathigesh/Atmo)

#### React

[Jest | Painless JavaScript Unit Testing](https://facebook.github.io/jest/) by Facebook on top of [Jasmine](http://jasmine.github.io/edge/introduction.html)
[Testing your apps like a boss with React.js and Jest - DEV Community 👩‍💻👨‍💻](https://dev.to/softchris/testing-your-apps-like-a-boss-with-react-js-and-jest-1hkh) !important
[Rogelio Guzman - Jest Snapshots and Beyond - React Conf 2017 - YouTube](https://www.youtube.com/watch?v=HAuXJVI_bUs) comparing snapshots of rendered UI

[airbnb/enzyme: JavaScript Testing utilities for React](https://github.com/airbnb/enzyme)
[jquense/teaspoon: A jQuery like API for testing React elements and rendered components.](https://github.com/jquense/teaspoon)

#### TAP

```sh
mocha -R
lab -r tap
```

[Home - Test Anything Protocol](https://testanything.org/)
[Understand the Test Anything Protocol | The Effective Perler](http://www.effectiveperlprogramming.com/2011/05/understand-the-test-anything-protocol/)
[sindresorhus/awesome-tap](https://github.com/sindresorhus/awesome-tap)

[Writing javascript tests with tape - good coders code, great reuse](http://www.catonmat.net/blog/writing-javascript-tests-with-tape/)
[Testing JavaScript Modules with Tape](http://ponyfoo.com/articles/testing-javascript-modules-with-tape)
[Why I use Tape Instead of Mocha & So Should You — JavaScript Scene — Medium](https://medium.com/javascript-scene/why-i-use-tape-instead-of-mocha-so-should-you-6aa105d8eaf4)
[My node test strategy](https://remysharp.com/2015/12/14/my-node-test-strategy)
[tape (testling)](https://ci.testling.com/guide/tape)
[how I write tests for node and the browser](http://substack.net/how_I_write_tests_for_node_and_the_browser)

[TAP in JavaScript](https://github.com/tapjs) `node-tap` evolved
[substack/tape](https://github.com/substack/tape)
[scottcorgan/tapes](https://github.com/scottcorgan/tapes), `tape` with `beforeEach()`, `afterEach()`
[spion/blue-tape](https://github.com/spion/blue-tape) `tape` with promise
[wavded/babel-tape-runner](https://github.com/wavded/babel-tape-runner)
[Jam3/tap-dev-tool: prettifies TAP in the browser's console](https://github.com/Jam3/tap-dev-tool)

[rvagg/bustermove](https://github.com/rvagg/bustermove) use Buster syntax in `tape`

Reporters:
[scottcorgan/tap-spec](https://github.com/scottcorgan/tap-spec)
[substack/faucet](https://github.com/substack/faucet)
[namuol/tap-difflet](https://github.com/namuol/tap-difflet)

### Browser

task runner for browser tests:
[testem/testem: Test'em 'Scripts! A test runner that makes Javascript unit testing fun.](https://github.com/testem/testem)
[substack/testling: unit tests in all the browsers](https://github.com/substack/testling)

[assaf/zombie: Insanely fast, full-stack, headless browser testing using node.js](https://github.com/assaf/zombie)

[defunctzombie/zuul: multi-framework javascript browser testing](https://github.com/defunctzombie/zuul)
[prometheusresearch/zuul-builder-webpack: Webpack builder for zuul test runner](https://github.com/prometheusresearch/zuul-builder-webpack)

[Jasmine](http://jasmine.github.io/edge/introduction.html)
[uxebu/kommando: A functional / acceptance test runner (using Webdriver)](https://github.com/uxebu/kommando)

[CodeceptJS](http://codecept.io/) CucumberJS + Web driver

[Selenium - Web Browser Automation](http://www.seleniumhq.org/)
[Selenium, Travis-CI and WebRTC == <&](https://blog.andyet.com/2015/07/28/selenium-travis-webrtc/)
[Google Open Source Blog: Introducing WebDriver](http://google-opensource.blogspot.hk/2009/05/introducing-webdriver.html)
[Learn How to Automate Browser Testing With Selenium WebDriver — Part 1 - DZone DevOps](https://dzone.com/articles/learn-how-to-automate-browser-with-selenium-webdri)

[5 Best Python Frameworks for WebView Testing | Codementor](https://www.codementor.io/saifsadiq1995/5-best-python-frameworks-for-webview-testing-rp182gqxa)

### Assertion

[hapijs-code · GitHub](https://github.com/hapijs/code)
[Home - Chai](http://chaijs.com/)
[Chai HTTP - Chai](http://chaijs.com/plugins/chai-http)
[Automattic/expect.js](https://github.com/Automattic/expect.js)
[shouldjs/should.js](https://github.com/shouldjs/should.js)

### Runner

[airportyh/testem](https://github.com/airportyh/testem)
[cybertk/abao: REST API automated testing tool based on RAML](https://github.com/cybertk/abao)

### End-to-end

[JavaScript End to End Testing Framework | Cypress.io](https://www.cypress.io/)
[Testing Angular with Cypress and Docker - TestDriven.io](https://testdriven.io/testing-angular-with-cypress-and-docker)

[Late to the Party; End-to-End Testing: Part 1 – codeburst](https://codeburst.io/late-to-the-party-end-to-end-testing-part-1-ea15ff8e4f7a)
[Late to the Party; End-to-End Testing: Part 2 – codeburst](https://codeburst.io/late-to-the-party-end-to-end-testing-part-2-3246c69248ca)
[Late to the Party; End-to-End Testing: Part 3 – codeburst](https://codeburst.io/late-to-the-party-end-to-end-testing-part-3-be8bd5d66ada)
[Late to the Party; End-to-End Testing: Part 5 – codeburst](https://codeburst.io/late-to-the-party-end-to-end-testing-part-5-d8dd9159fee7)

[Karma - Spectacular Test Runner for Javascript](http://karma-runner.github.io/latest/index.html)
[ksunair-introtokarma](https://github.com/ksunair/introtokarma)
[douglasduteil/isparta: A code coverage tool for ES6 (babel/6to5)](https://github.com/douglasduteil/isparta)

[CodeceptJS](http://codecept.io/)

[Getting started with Mocha and Chai - Rob Dodson talks internets](http://robdodson.me/blog/2012/05/27/testing-backbone-boilerplate-with-mocha-and-chai/)
[ludovicofischer-mocha-chai-browser-demo · GitHub](https://github.com/ludovicofischer/mocha-chai-browser-demo)

### Coverage

[Rethinking JavaScript Test Coverage – Node.js Collection – Medium](https://medium.com/the-node-js-collection/rethinking-javascript-test-coverage-5726fb272949) TL;DR, c8
[bcoe/c8: output coverage reports using Node.js' built in coverage](https://github.com/bcoe/c8)

[gotwarlost/istanbul](https://github.com/gotwarlost/istanbul)
[Hard Thresholds on JavaScript Code Coverage](http://ariya.ofilabs.com/2013/05/hard-thresholds-on-javascript-code-coverage.html)
[The Hidden Trap of Code Coverage](http://ariya.ofilabs.com/2012/09/the-hidden-trap-of-code-coverage.html)
[bcoe/nyc: a code coverage tool that works well with subprocesses.](https://github.com/bcoe/nyc)

[alex-seville/blanket](https://github.com/alex-seville/blanket)

### Benchmark

[substack/node-ben](https://github.com/substack/node-ben)
[jeffbski/bench-rest](https://github.com/jeffbski/bench-rest)

### Browser as a Service

[Sauce Labs: Selenium Testing, Mobile Testing, JS Unit Testing](https://saucelabs.com/)
[Open Sauce](https://saucelabs.com/opensauce/)

[Cross Browser Testing Tool. 300+ Browsers, Mobile, Real IE.](https://www.browserstack.com/)

[Virtual Machine (VM), Windows Virtual PC & BrowserStack](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/)

## Continuous Integration

> TODO: move to `ci-cd.md`

[Continuous integration - Wikiwand](https://www.wikiwand.com/en/Continuous_integration)
[Continuous Integration Essentials | Codeship](https://codeship.com/continuous-integration-essentials)
[What is CI/CD? Continuous integration and continuous delivery explained | InfoWorld](https://www.infoworld.com/article/3271126/application-development/what-is-cicd-continuous-integration-and-continuous-delivery-explained.html)
[What is continuous testing? How to align test automation with agile and devops | InfoWorld](https://www.infoworld.com/article/3289104/application-testing/how-to-align-test-automation-with-agile-and-devops.html)

[cytopia/awesome-ci: Awesome Continuous Integration - Lot's of tools for git, file and static source code analysis.](https://github.com/cytopia/awesome-ci)
[ligurio/awesome-ci: List of Continuous Integration services](https://github.com/ligurio/awesome-ci)

[How to set up an efficient development workflow with Git and CI/CD](https://proandroiddev.com/how-to-set-up-an-efficient-development-workflow-with-git-and-ci-cd-5e8916f6bece)
[GitHub Flow](https://githubflow.github.io/)
[GitLab Flow | GitLab](https://about.gitlab.com/2014/09/29/gitlab-flow/)

[Continuous Delivery Software | Continuous Integration | Go CD](https://www.go.cd/)
[A beginner's guide to building DevOps pipelines with open source tools | Opensource.com](https://opensource.com/article/19/4/devops-pipeline)
[How secure is your CICD pipeline?](https://www.weave.works/blog/how-secure-is-your-cicd-pipeline)

[Danger JS](https://danger.systems/js/) code review

[Continuous Integration, Delivery and Deployment | Technology Conversations](http://technologyconversations.com/category/continuous-integration-delivery-and-deployment/) the series
[The Short History of CI/CD Tools | Technology Conversations](http://technologyconversations.com/2016/01/14/the-short-history-of-cicd-tools/) !important
[Build Automation Panel | Technology Conversations](http://technologyconversations.com/2015/05/17/build-automation-panel/#more-2294)
[Continuous Delivery: Unit Tests | Technology Conversations](http://technologyconversations.com/2014/06/10/continuous-delivery-unit-tests/) compares services

[screwdriver.cd](http://screwdriver.cd/)
[Open Source Continuous Delivery and Release Automation Server | GoCD](https://www.gocd.org/)
[Concourse CI](https://concourse-ci.org/)

[Scripts to Rule Them All - GitHub Engineering](http://githubengineering.com/scripts-to-rule-them-all/) project structure that is CI friendly
[github/scripts-to-rule-them-all: Scripts to Rule Them All](https://github.com/github/scripts-to-rule-them-all)

[Photon](http://photon.ci/)
[Photon-CI/Photon: An open-source .NET task platform designed for pipeline-as-code automation.](https://github.com/Photon-CI/Photon)

[Kubernetes Pipelines: Hello, New World - Container Journal](https://containerjournal.com/2019/03/12/kubernetes-pipelines-hello-new-world/amp/)
[CI/CD with Less Fluff & More Awesome – Donna Legal – Medium](https://medium.com/donna-legal/ci-cd-with-less-fluff-more-awesome-28af61288a03)

### CI with Docker

[Strider-CD/strider: Strider: Open Source Continuous Integration & Deployment Server.](https://github.com/Strider-CD/strider)
[rvagg/dnt: Docker Node Tester](https://github.com/rvagg/dnt)
[retrohacker/dante: Build tests against Docker images by harnessing the power of layers](https://github.com/retrohacker/dante)

[Docker and Travis-CI](http://www.gizra.com/content/docker-travis-ci/) Docker inside Travis

[Continuous Blog Delivery Part 1](https://niels.nu/blog/2017/continuous-blog-delivery-p1.html)
[Continuous Blog Delivery Part 2](https://niels.nu/blog/2017/continuous-blog-delivery-p2.html)

[Efficient development with Docker and docker-compose](https://medium.com/@Empanado/efficient-development-with-docker-and-docker-compose-e354b4d24831) GitLab CI example

[Dockerize your integration tests - DEV Community 👩‍💻👨‍💻](https://dev.to/vga/dockerize-your-integration-tests--4edm)
[Introduction · Testcontainers](https://www.testcontainers.org/)

[Follow these steps to build production-grade workflow with Docker and React](https://medium.freecodecamp.org/follow-these-steps-to-build-production-grade-workflow-with-docker-and-react-a860f695cf14) Travis CI and AWS Elastic BeanStalk

[fabric8: open source Integrated Development Platform for Kubernetes](http://fabric8.io/)

#### Drone

[drone/drone: Drone is a Continuous Delivery platform built on Docker, written in Go](https://github.com/drone/drone)
[drone/drone: Drone is a Continuous Delivery platform built on Docker, written in Go](https://github.com/drone/drone)
[Drone CI/CD Goes Kubernetes-Native](https://blog.drone.io/drone-goes-kubernetes-native/)

[How to set up a Private Continuous Deployment Server with Drone](http://paislee.io/how-to-run-a-private-continuous-integration-server-with-drone/)
[How to Build and Deploy Docker Images with Drone](http://paislee.io/how-to-build-and-deploy-docker-images-with-drone/)
[How to Automate Docker Deployments](http://paislee.io/how-to-automate-docker-deployments/)

#### Codeship

[How Docker Makes Testing More Efficient - via @codeship](http://blog.codeship.com/testing-with-docker/)
[Running Tests with Docker - Codeship Webinar on Vimeo](https://vimeo.com/160775195)
[Codeship Webinar Video: An Introduction to CI/CD With Docker Best Practices - Request Webinar Video](https://resources.codeship.com/webinars/intro-to-ci-cd-with-docker-best-practices)

[Codeship Webinar Video: Running Your Tests with Docker](http://resources.codeship.com/webinars/thank-you-video-running-your-tests-with-docker)
[Codeship Webinar Video: Continuous Delivery with Containers](http://resources.codeship.com/webinars/thank-you-video-getting-started-with-continuous-delivery-using-docker)
[Codeship Webinar Video: An Introduction to CI/CD With Docker Best Practices - Request Webinar Video](https://resources.codeship.com/webinars/intro-to-ci-cd-with-docker-best-practices)

#### Jenkins

[Jenkins X is a CI / CD platform for Kubernetes | Jenkins X](https://jenkins-x.io/)

[Testing Strategies for Docker Containers · Terra Nullius](http://blog.terranillius.com/post/docker_testing/)
[Building With Jenkins Inside an Ephemeral Docker Container | Riot Games Engineering](https://engineering.riotgames.com/news/building-jenkins-inside-ephemeral-docker-container)
[Get started with brand new Jenkins 2.0 with Docker - SHASHIKANT JAGTAP](http://shashikantjagtap.net/get-started-with-brand-new-jenkins-2-0-with-docker/)
[What is Jenkins? The CI server explained | InfoWorld](https://www.infoworld.com/article/3239666/devops/what-is-jenkins-the-ci-server-explained.html)
[Jenkins tutorial | Jenkins tutorial for beginners | Jenkins - YouTube](https://www.youtube.com/watch?v=-wZeZSMlvhM)

[Continuous Integration, Delivery or Deployment with Jenkins, Docker and Ansible | Technology Conversations](http://technologyconversations.com/2015/02/11/continuous-integration-delivery-or-deployment-with-jenkins-docker-and-ansible/) [code](https://github.com/vfarcic/jenkins-docker-ansible)
[Continuous Deployment: Implementation with Ansible and Docker | Technology Conversations](http://technologyconversations.com/2014/12/29/continuous-deployment-implementation-with-ansible-and-docker/) [code](https://github.com/vfarcic/provisioning/tree/master/ansible)

[Overview of Jenkins - YouTube](https://www.youtube.com/playlist?list=PLfXWzKEc7gHxnW_IF46mrXm51uv81eN6H)

#### Docker Flow

[Docker Flow – Walkthrough | Technology Conversations](https://technologyconversations.com/2016/04/18/docker-flow/)
[vfarcic/docker-flow: Docker Flow: Walkthrough](https://github.com/vfarcic/docker-flow)

#### Kubernetes

[CI/CD for Kubernetes](https://www.weave.works/technologies/ci-cd-for-kubernetes/)
[Continuous Delivery to Kubernetes for Machine Learning with Michelle Casbon (Qordoba)](https://www.weave.works/blog/continuous-delivery-to-kubernetes-for-machine-learning)

[Tekton  |  Google Cloud](https://cloud.google.com/tekton/)
[New Google project offers Kubernetes building blocks for CI/CD | InfoWorld](https://www.infoworld.com/article/3373650/new-google-project-offers-kubernetes-building-blocks-for-cicd.amp.html)

### Hygieia

[Tech - Hygieia | Capital One](https://www.capitalone.com/tech/solutions/hygieia)

### Hosted

> usually have self-hosted enterprise option

[Continuous Delivery with Codeship: Fast, secure and fully customizable.](https://codeship.com/)
[Continuous Integration and Deployment - CircleCI](https://circleci.com/)
[Semaphore - Continuous Integration & Deployment](https://semaphoreci.com/)
[Continuous Integration and Deployment service for Windows developers - Appveyor](https://www.appveyor.com/)

[Wercker - From code to containers](http://wercker.com/)

### Travis

> Travis is hosted service, with self-hosted enterprise option

[Travis CI - Wikiwand](https://www.wikiwand.com/en/Travis_CI)
[Travis CI - Test and Deploy Your Code with Confidence](https://travis-ci.org/)
[DamonOehlman/travis-multirunner: A simple configuration for running (limited) multibrowser tests on travis ci](https://github.com/damonoehlman/travis-multirunner)
[GUI and Headless Browser Testing - Travis CI](https://dosc.travis-ci.com/user/gui-and-headless-browsers/)

### Buildbot

[Buildbot](http://buildbot.net/)
[Buildbot in 5 minutes - a user-contributed tutorial — Buildbot 0.8.12 documentation](http://docs.buildbot.net/current/tutorial/fiveminutes.html)

### Jenkins

[Welcome to Jenkins CI! | Jenkins CI](https://jenkins-ci.org/)
[Introduction to Jenkins: An Open Source Continuous Integration Server - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/introduction-to-jenkins-an-open-source-continuous-integration-server--cms-23879)
[Production Ready Jenkins 2.0 in Two Steps with Docker | FlowLog-Stats.com](https://blog.flowlog-stats.com/2016/05/05/production-ready-jenkins-2-0-in-two-steps-with-docker/)
[Docker inside docker and overview about Jenkins 2](http://gianarb.it/blog/docker-inside-docker-and-jenkins-2)

[What is Jenkins? The CI server explained | InfoWorld](https://www.infoworld.com/article/3239666/what-is-jenkins-the-ci-server-explained.html)
[Jenkins CI/CD is in trouble, so its founder wants to split it up | InfoWorld](https://www.infoworld.com/article/3304282/jenkins-cicd-is-in-trouble-so-its-founder-wants-to-split-it-up.html)
[Jenkins tries to reinvent itself as cloud-native for Kubernetes | InfoWorld](https://www.infoworld.com/article/3366428/jenkins-tries-to-reinvent-itself-as-cloud-native-for-kubernetes.html)

### OVH CDS

[ovh/cds: Enterprise-Grade Continuous Delivery & DevOps Automation Open Source Platform](https://github.com/ovh/cds)
[Comparison Matrix](https://github.com/ovh/cds#comparison-matrix)

### Kitchen

[Welcome to Test Kitchen - KitchenCI](http://kitchen.ci/)
[Setting your environment in test-kitchen - The Doctor What](https://docwhat.org/setting-environment-test-kitchen/)

### Build your own

[Ansibot by hiddentao](http://hiddentao.github.io/ansijet/)
[Shippable + Ansible + Docker + Loggly for awesome deployments](http://www.hiddentao.com/archives/2014/06/03/shippable-ansible-docker-loggly-for-awesome-deployments/)
[Ansijet – Ansible playbook automation server](http://www.hiddentao.com/archives/2014/06/20/ansijet-ansible-playbook-automation-server/)

### Static Analysis/Coverage

[Codecov - Code Coverage](https://codecov.io/)
[Coveralls - Test Coverage History & Statistics](https://coveralls.io/)
[Code Climate. Hosted static analysis for Ruby, PHP and JavaScript source code.](https://codeclimate.com/)
[Dependency management + Code analytics for Node.js projects](https://www.bithound.io/)
