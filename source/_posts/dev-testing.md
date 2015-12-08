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

## Theory

### Developer's aspect

[Test-driven development - Wikiwand](https://www.wikiwand.com/en/Test-driven_development)
[Behavior-driven development - Wikiwand](https://www.wikiwand.com/en/Behavior-driven_development)
[What’s the difference between Unit Testing, TDD and BDD? | CodeUtopia](http://codeutopia.net/blog/2015/03/01/unit-testing-tdd-and-bdd/)

Integration/Functional Test: do the pieces work together as I expected?
Unit Test: given input *x*, is the output *y*?

[Introducing BDD | Dan North & Associates](http://dannorth.net/introducing-bdd/)
[What’s in a Story? | Dan North & Associates](http://dannorth.net/whats-in-a-story/)

```
Scenario: title
Given [some context]
And [additional context]
When [event]
Then [outcome]
```

[Six Ways of Improving Behaviour-Driven Development](http://www.infoq.com/news/2015/07/six-bdd-improvements?utm_campaign=infoq_content&utm_source=infoq&utm_medium=feed&utm_term=global)
[The WHY behind TDD/BDD and the HOW with RSpec](http://www.slideshare.net/bmabey/the-why-behind-tddbdd-and-the-how-with-rspec)
[5 Questions Every Unit Test Must Answer — JavaScript Scene — Medium](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)

### QA's aspect

[Open Lecture by James Bach on Software Testing - YouTube](https://www.youtube.com/watch?v=ILkT_HV9DVU)

[如何测试洗牌程序 | 酷 壳 - CoolShell.cn](http://coolshell.cn/articles/8593.html)

## Ad-hoc standard

[xUnit - Wikiwand](http://www.wikiwand.com/en/XUnit)
[Test Anything Protocol - Wikiwand](http://www.wikiwand.com/en/Test_Anything_Protocol) [TAP](https://testanything.org/) is a simple text-based interface between testing modules in a test harness. Many test frameworks can output TAP results.
[Main Page - Test Anything Protocol](http://testanything.org/)

<!-- more -->

## Shell Script

[jimeh/test-runner.sh](https://github.com/jimeh/test-runner.sh)
[jimeh/stub.sh](https://github.com/jimeh/stub.sh)
[sstephenson/bats](https://github.com/sstephenson/bats)

[shunit2 - Google Search](https://www.google.com.hk/search?q=shunit2&oq=shunit2&aqs=chrome..69i57j69i60l2&sourceid=chrome&es_sm=93&ie=UTF-8)

## Android

[Automating User Interface Testing on Android - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/automating-user-interface-testing-on-android--cms-23969)

[LAVA](https://validation.linaro.org/)
[LAVA Manual — LAVA Server 2015.07 documentation](https://validation.linaro.org/static/docs/#)

## JavaScript

> TODO: Define "Test runner", "Assertion", "Framework"

[Incredibly convenient testing of front-end Javascript with Node.js - Staal Forge](http://staal.io/blog/2013/08/17/incredibly-convenient-testing-of-frontend-javascript-with-node-dot-js/)
[5 Questions Every Unit Test Must Answer — JavaScript Scene — Medium](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)

[6. Writing Testable JavaScript - YouTube](https://www.youtube.com/watch?v=OzjogCFO4Zo)

[Promises in JavaScript Unit Tests: the Definitive Guide](http://www.sitepoint.com/promises-in-javascript-unit-tests-the-definitive-guide/)
[Testing Node.js with Mocha and Chai - Michael Herman](http://mherman.org/blog/2015/09/10/testing-node-js-with-mocha-and-chai/)

### Frameworks

[SpeckJS - Comment Driven Development](http://speckjs.github.io/)

[Jest | Painless JavaScript Unit Testing](https://facebook.github.io/jest/) by Facebook on top of [Jasmine](http://jasmine.github.io/edge/introduction.html)
[Intern: A next-generation JavaScript testing stack](http://theintern.io/) [video](https://www.youtube.com/watch?v=_KFjuEKLqDA)
[hapijs-lab · GitHub](https://github.com/hapijs/lab) (need assertion library, say [code](https://github.com/hapijs/code/))
[mochajs-mocha · GitHub](https://github.com/mochajs/mocha) (need assertion library, say [chai](http://chaijs.com/))

[abe33-spectacular · GitHub](https://github.com/abe33/spectacular)
[bevry-joe · GitHub](https://github.com/bevry/joe)
[gotwarlost-istanbul · GitHub](https://github.com/gotwarlost/istanbul)
[Vows « Asynchronous BDD for Node](http://vowsjs.org/)
[Welcome! Buster.JS is...](http://docs.busterjs.org/en/latest/)

[visionmedia/supertest](https://github.com/visionmedia/supertest) testing server API with extended [superagent](https://github.com/visionmedia/superagent)

### Mock/Stub

[Sinon.JS](http://sinonjs.org/) provides AJAX mock and spy that work in all test frameworks.

[pgte/nock](https://github.com/pgte/nock)
[Intercept HTTP Requests with Node.js nock](http://davidwalsh.name/nock)

[Marak/faker.js](https://github.com/marak/Faker.js/)
[Chance.js: Utility library to generate anything random for JavaScript](http://chancejs.com/)

[rvagg/node-mkfiletree](https://github.com/rvagg/node-mkfiletree)

#### Comparison

[Essential JavaScript: the top five testing libraries | JavaScript | Creative Bloq](http://www.creativebloq.com/javascript/essential-javascript-top-five-testing-libraries-10126048)

[List of unit testing frameworks (JavaScript) - Wikiwand](http://www.wikiwand.com/en/List_of_unit_testing_frameworks#/JavaScript)
[thegrtman/javascript-test-framework-comparison](https://github.com/thegrtman/javascript-test-framework-comparison)
[coderwall.com : establishing geek cred since 1305712800](https://coderwall.com/p/ntbixw/javascript-test-framework-comparison)
[JavaScript unit test tools for TDD - Stack Overflow](http://stackoverflow.com/questions/300855/javascript-unit-test-tools-for-tdd)

#### TAP

```sh
mocha -R
lab -r tap
```

[Writing javascript tests with tape - good coders code, great reuse](http://www.catonmat.net/blog/writing-javascript-tests-with-tape/)
[Testing JavaScript Modules with Tape](http://ponyfoo.com/articles/testing-javascript-modules-with-tape)
[Why I use Tape Instead of Mocha & So Should You — JavaScript Scene — Medium](https://medium.com/javascript-scene/why-i-use-tape-instead-of-mocha-so-should-you-6aa105d8eaf4)
[tape (testling)](https://ci.testling.com/guide/tape)
[how I write tests for node and the browser](http://substack.net/how_I_write_tests_for_node_and_the_browser)

[isaacs-node-tap · GitHub](https://github.com/isaacs/node-tap)
[substack/tape](https://github.com/substack/tape)
[scottcorgan/tapes](https://github.com/scottcorgan/tapes), with `beforeEach()`, `afterEach()`
[spion/blue-tape](https://github.com/spion/blue-tape)
[wavded/babel-tape-runner](https://github.com/wavded/babel-tape-runner)

[rvagg/bustermove](https://github.com/rvagg/bustermove) use Buster syntax in tape

Reporters:
[scottcorgan/tap-spec](https://github.com/scottcorgan/tap-spec)
[substack/faucet](https://github.com/substack/faucet)
[namuol/tap-difflet](https://github.com/namuol/tap-difflet)

### Assertion

[hapijs-code · GitHub](https://github.com/hapijs/code)
[Home - Chai](http://chaijs.com/)
[Chai HTTP - Chai](http://chaijs.com/plugins/chai-http)
[Automattic/expect.js](https://github.com/Automattic/expect.js)
[shouldjs/should.js](https://github.com/shouldjs/should.js)

#### Runner

[airportyh/testem](https://github.com/airportyh/testem)

#### End-to-end

[Getting started with Mocha and Chai - Rob Dodson talks internets](http://robdodson.me/blog/2012/05/27/testing-backbone-boilerplate-with-mocha-and-chai/)
[ksunair-introtokarma](https://github.com/ksunair/introtokarma)
[ludovicofischer-mocha-chai-browser-demo · GitHub](https://github.com/ludovicofischer/mocha-chai-browser-demo)

#### Coverage

[gotwarlost/istanbul](https://github.com/gotwarlost/istanbul)
[alex-seville/blanket](https://github.com/alex-seville/blanket)

#### Benchmark

[substack/node-ben](https://github.com/substack/node-ben)
[jeffbski/bench-rest](https://github.com/jeffbski/bench-rest)

## Continuous Integration

[Continuous integration - Wikiwand](https://www.wikiwand.com/en/Continuous_integration)

[Travis CI - Wikiwand](https://www.wikiwand.com/en/Travis_CI)
[Travis CI - Test and Deploy Your Code with Confidence](https://travis-ci.org/)

[Welcome to Jenkins CI! | Jenkins CI](https://jenkins-ci.org/)
[Introduction to Jenkins: An Open Source Continuous Integration Server - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/introduction-to-jenkins-an-open-source-continuous-integration-server--cms-23879)

## Documentation

[Is Your Product's Documentation Good Enough?](http://www.sitepoint.com/products-documentation-good-enough/)

[Use JSDoc: Index](http://usejsdoc.org/)
