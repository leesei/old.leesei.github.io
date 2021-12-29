---
title: "Web Authentication"
categories:
  - web
tags:
  - security
  - authentication
  - web-token
toc: true
date: 2016-01-21 00:45:59
---

[Secure authentication means moving beyond passwords | CSO Online](https://www.csoonline.com/article/3237827/password-security/ready-for-more-secure-authentication-try-these-password-alternatives-and-enhancements.html)

[Enterprise APIs and OAuth: Have it All](http://news.sys-con.com/node/2275857/print)

[API Keys vs OAuth Tokens vs JSON Web Tokens - The Zapier Engineering Blog - Zapier](https://zapier.com/engineering/apikey-oauth-jwt/)

[Authentication on the Web (Sessions, Cookies, JWT, localStorage, and more) - YouTube](https://www.youtube.com/watch?v=2PPSXonhIck)

- sessions + cookies
- tokens + local/session storage

[Handling Authentication Secrets in the Browser - miguelgrinberg.com](https://blog.miguelgrinberg.com/post/handling-authentication-secrets-in-the-browser)
[Secure your users' passwords from the browser on](https://coolaj86.com/articles/secure-your-users-passwords-from-the-browser-on/)

[Facebook, GitHub team up to better secure password resets | InfoWorld](http://www.infoworld.com/article/3163198/security/facebook-github-teams-up-to-make-password-resets-more-secure.html)
[Delegated Account Recovery](https://rawgit.com/facebookincubator/DelegatedRecovery/master/draft-hill-delegated-recovery.html)

[The Identity Cookbook](http://www.theidentitycookbook.com/)

[Spring Security Registration Tutorial | Baeldung](https://www.baeldung.com/spring-security-registration)

## Authentication Protocols

[Basic access authentication - Wikiwand](http://www.wikiwand.com/en/Basic_access_authentication)
[Digest access authentication - Wikiwand](http://www.wikiwand.com/en/Digest_access_authentication)
[Secure Remote Password protocol - Wikiwand](http://www.wikiwand.com/en/Secure_Remote_Password_protocol)

does not to mandate SSL/TLS

[RFC 2617 - HTTP Authentication: Basic and Digest Access Authentication](https://tools.ietf.org/html/rfc2617)
[RFC 7235 - Hypertext Transfer Protocol (HTTP/1.1): Authentication](https://tools.ietf.org/html/rfc7235)

`Access-Control-Allow-Origin: *` does not allow requests to supply credentials like HTTP authentication, client-side SSL certificates, or cookies. You have to use `Access-Control-Allow-Headers: Authorization, X-Token` to allow those headers.

Use MAC with server nonce instead of send password, allows authentication over non-secure channel.
[Message authentication code - Wikiwand](https://www.wikiwand.com/en/Message_authentication_code)
[HMAC - Wikiwand](https://www.wikiwand.com/en/HMAC) hash-based message authentication code
[hapijs/hawk: HTTP Holder-Of-Key Authentication Scheme](https://github.com/hapijs/hawk)

## Auth Server

[tarent/loginsrv: JWT login microservice with plugable backends such as OAuth2, Google, Github, htpasswd, osiam, ..](https://github.com/tarent/loginsrv)
[leesei/docker-auth-server: Dockerized JWT key server](https://github.com/leesei/docker-auth-server)

[Magic: Future-proof passwordless authentication](https://magic.link/) paid service
[Developer-Friendly Passwordless Auth | CSS-Tricks](https://css-tricks.com/developer-friendly-passwordless-auth/)

## Multi-factor Authentication (MFA)

[Multi-factor authentication - Wikiwand](https://www.wikiwand.com/en/Multi-factor_authentication)
[What is multifactor authentication (MFA)? - Definition from WhatIs.com](https://searchsecurity.techtarget.com/definition/multifactor-authentication-MFA)

## TOTP

[Time-based One-time Password algorithm - Wikiwand](https://www.wikiwand.com/en/Time-based_One-time_Password_algorithm)
[RFC 6238: TOTP: Time-Based One-Time Password Algorithm](https://www.rfc-editor.org/rfc/rfc6238.html)

[Google Authenticator - Wikiwand](https://www.wikiwand.com/en/Google_Authenticator)
[Google 2-Step Verification](https://www.google.com/landing/2step/)
[Setting up Google Authenticator is as easy as scanning a QR code](https://www.androidguys.com/tips-tools/setting-up-google-authenticator-is-as-easy-as-scanning-a-qr-code/)

[LastPass Authenticator](https://support.logmeininc.com/lastpass/help/lastpass-authenticator-lp030014)
[Use 1Password as an authenticator for sites with two-factor authentication](https://support.1password.com/one-time-passwords/)
[Guides - Authy](https://authy.com/guides/)

[Advanced Protection Program](https://landing.google.com/advancedprotection/)
[Use your Android phone's built-in security key - Google Account Help](https://support.google.com/accounts/answer/9289445?p=phone-security-key)

## FIDO

[FIDO Alliance - Open Authentication Standards More Secure than Passwords](https://fidoalliance.org/)
[FIDO2: Moving the World Beyond Passwords using WebAuthn & CTAP](https://fidoalliance.org/fido2/)
[FIDO2 Project - Wikiwand](https://www.wikiwand.com/en/FIDO2_Project)
[How FIDO Works - Standard Public Key Cryptography & User Privacy](https://fidoalliance.org/how-fido-works/)
[The ultimate account security is now in your pocket](https://www.blog.google/technology/safety-security/your-android-phone-is-a-security-key/amp/)

[Apple, the FIDO Alliance and the future of passwords | Computerworld](https://www.computerworld.com/video/101679/apple-the-fido-alliance-and-the-future-of-passwords)

physical keys
[FIDO2 | Yubico](https://www.yubico.com/solutions/fido2/)
[Titan Security Key Bundle, FIDO U2F BT & NFC - Google Store](https://store.google.com/us/product/titan_security_key_kit?hl=en-US)

## WebAuthn

[WebAuthn.io](https://webauthn.io/)
[WebAuthn - Wikiwand](https://www.wikiwand.com/en/WebAuthn)
[Web Authentication API - Web APIs | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Web_Authentication_API)
[Web Authentication: An API for accessing Public Key Credentials Level 1](https://www.w3.org/TR/webauthn/)

[Going Passwordless With WebAuthn | Blog | Curity](https://curity.io/blog/going-passwordless-with-webauthn/)
[Enabling Strong Authentication with WebAuthn | Web | Google Developers](https://developers.google.com/web/updates/2018/05/webauthn)
[Your First WebAuthn](https://codelabs.developers.google.com/codelabs/webauthn-reauth/index.html)
[Introduction to Web Authentication: The New W3C Spec](https://auth0.com/blog/introduction-to-web-authentication/)
[一起來了解 Web Authentication | TechBridge 技術共筆部落格](https://blog.techbridge.cc/2019/08/17/webauthn-intro/)

## ACL

[Role-based access control - Wikiwand](https://www.wikiwand.com/en/Role-based_access_control)
[XACML - Wikiwand](https://www.wikiwand.com/en/XACML)

[The Identity Cookbook: Blockchain for Identity: Access Request Management](http://www.theidentitycookbook.com/2016/06/blockchain-for-identity-access-request.html)
[Improving Enterprise Business Process Management Systems: Enrich RBAC and ABAC with ProBAC, #infosec #security #BPM](http://improving-bpm-systems.blogspot.hk/2015/01/enrich-rbac-and-abac-with-probac.html)

## Blockchain

[The Identity Cookbook: Blockchain for Identity: Access Request Management](http://www.theidentitycookbook.com/2016/06/blockchain-for-identity-access-request.html)
[Anatomy of a zero-knowledge web application - Clipperz, register your creations on the blockchain](https://clipperz.is/blog/2007/08/24/anatomy_zero_knowledge_web_application/)

## SQRL

[GRC's |SQRL Secure Quick Reliable Login](https://www.grc.com/sqrl/sqrl.htm)
[SQRL](http://lundborg.io/2013/10/10/SQRL/)

---

# Server Based

Server generates session token and send to client via cookie. The session token acts as a bearer token and is used to look up login/session info in memory or datastore.

[On Securing Web Session Ids – hueniverse](https://hueniverse.com/on-securing-web-session-ids-b90f566b3786)
[expressjs/session: Simple session middleware for Express](https://github.com/expressjs/session)

---

# Asymmetric Key

[BrowserAuth.net](http://www.browserauth.net/) using asymmetric-key for web

[substack/trust-log: manage trust over time](https://github.com/substack/trust-log)
[mafintosh/ghsign: Sign/verify data using your local ssh private key and your public key from Github](https://github.com/mafintosh/ghsign)

---

# Token Based

> "Server Based" and "Token Based" could be a misnomer.
> Some articles says server-based auth bind a client to a specific server but this is not actually true. We can setup a in-memory datastore shared by a cluster of app servers to look up the token upon a client request.
> And tokens in token-based auth may as well be stored in cookies. It's just that all session info are embedded in the token in token-based auth. This separates authentication (key generation by key server) and authorization (role enforcement by app server) and allows for 3rd-party key server architecture.

[The Ins and Outs of Token Based Authentication | Scotch](https://scotch.io/tutorials/the-ins-and-outs-of-token-based-authentication)
[Best practices for token-based authentication in REST API - Google Groups.desktop](https://groups.google.com/forum/#!topic/nodejs/2zCXZ10jFbg)
[Token Based Authentication for Single Page Apps (SPAs)](https://stormpath.com/blog/token-auth-spa)
[Token Authentication: The Secret to Scalable User Management - Stormpath User Identity API](https://stormpath.com/blog/token-authentication-scalable-user-mgmt)
[Token-Based Authentication With AngularJS & NodeJS - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/token-based-authentication-with-angularjs-nodejs--cms-22543)
[Cookies are bad for you: Improving web application security - sitr.us](http://sitr.us/2011/08/26/cookies-are-bad-for-you.html)

[Authentication in SPA (ReactJS and VueJS) the right way](https://medium.com/@jcbaey/authentication-in-spa-reactjs-and-vuejs-the-right-way-e4a9ac5cd9a3)
[Cookies vs Tokens. Getting auth right with Angular.JS](https://auth0.com/blog/2014/01/07/angularjs-authentication-with-cookies-vs-token/)
[10 Things You Should Know about Tokens](https://auth0.com/blog/2014/01/27/ten-things-you-should-know-about-tokens-and-cookies/)

[Stop using JWT for sessions - joepie91's Ramblings](http://cryto.net/~joepie91/blog/2016/06/13/stop-using-jwt-for-sessions/)
[Stop using JWT for sessions, part 2: Why your solution doesn't work - joepie91's Ramblings](http://cryto.net/~joepie91/blog/2016/06/19/stop-using-jwt-for-sessions-part-2-why-your-solution-doesnt-work/)

[A Token Walks into a SPA - YouTube](https://www.youtube.com/watch?list=PLQrl6x_e_AZG0RdzIYVns4eGFxUEF61Lw&v=-usz7XqZikM)
[hapijs/hapi-auth-cookie: Cookie authentication plugin](https://github.com/hapijs/hapi-auth-cookie) is actually a token based authentication

[roblevintennis-passport-api-tokens · GitHub](https://github.com/roblevintennis/passport-api-tokens)

[Why Using Tokens and Cookies Together is Better for Web App Security | by Ashan Fernando | Bits and Pieces](https://blog.bitsrc.io/why-using-tokens-and-cookies-together-is-better-for-web-apps-9d205b7c1961) STS sends JWT to backend to set session cookie
[Goodbye Short Sessions: a proposal for using service-workers to improve cookie management on the web | Web Updates - Google Developers](https://developers.google.com/web/updates/2016/06/2-cookie-handoff?hl=en)

There are three ways to send your access token in a request.

- In an HTTP Authorization header (always works)
- In the URL query string (only works with GET requests)
- In the request body (only works for POST & PUT when body is URL-encoded)

## Bearer token clients

[angular-token-auth/auth.client.js at master · auth0-blog/angular-token-auth](https://github.com/auth0-blog/angular-token-auth/blob/master/auth.client.js)
[talis/bearhug-angular: Response interceptor for elegant bearer-token handling for angular's \$http service](https://github.com/talis/bearhug-angular)

[AuthorizationServer/callback.cshtml at master · IdentityModel/AuthorizationServer](https://github.com/IdentityModel/AuthorizationServer/blob/master/samples/Flows/Implicit Flow (JavaScript)/callback.cshtml)

[sahat/satellizer: Token-based AngularJS Authentication](https://github.com/sahat/satellizer)

## Questions

Token based auth allows for RBAC (Role-Based Access Control), but other method can support RBAC as well (with a session lookup)

OAuth vs JWT vs OpenID

replay attack with bearer token
[OAuth 2.0 (without Signatures) is Bad for the Web | hueniverse](http://hueniverse.com/2010/09/15/oauth-2-0-without-signatures-is-bad-for-the-web/)
[OAuth Bearer Tokens are a Terrible Idea | hueniverse](http://hueniverse.com/2010/09/29/oauth-bearer-tokens-are-a-terrible-idea/)

[auth0/node-auth0: Node.js client library for the Auth0 platform.](https://github.com/auth0/node-auth0)
[node-auth0/examples/nodejs-regular-webapp at master · auth0/node-auth0](https://github.com/auth0/node-auth0/tree/master/examples/nodejs-regular-webapp)
[node-auth0/examples/nodejs-api at master · auth0/node-auth0](https://github.com/auth0/node-auth0/tree/master/examples/nodejs-api)
[auth0/cookie-jwt-auth](https://github.com/auth0/cookie-jwt-auth)
why store back to cookie?

[auth0/spa-jwt-authentication-tutorial - JavaScript](https://github.com/auth0/spa-jwt-authentication-tutorial)

[Adding authentication to your React Flux app](https://auth0.com/blog/2015/04/09/adding-authentication-to-your-react-flux-app/) [repo](https://github.com/auth0/react-flux-jwt-authentication-sample)

[Critical vulnerabilities in JSON Web Token libraries](https://auth0.com/blog/2015/03/31/critical-vulnerabilities-in-json-web-token-libraries/)

### vs OAuth

OAuth2 token is opaque, JWT can be used

[JWT: 2 years later](https://auth0.com/blog/2015/07/21/jwt-json-webtoken-logo/)
[OAuth 2 VS JSON Web Tokens: How to secure an API - Seedbox Technologies | Les Technologies Seedbox](http://www.seedbox.com/en/blog/2015/06/05/oauth-2-vs-json-web-tokens-comment-securiser-un-api/)

[谈谈 OAuth1,OAuth2 异同 | Litten 的博客](http://litten.github.io/2013/08/11/brief-oauth/)
[兔子，胡萝卜与 OAuth 的故事 | Litten 的博客](http://litten.github.io/2013/08/20/oauth-rabbit/)
[What's the difference between OAuth 1.0 and OAuth 2.0? | Packt Hub](https://hub.packtpub.com/what-is-the-difference-between-oauth-1-0-and-2-0/)

## Single Sing On (SSO)

[Implement Single Sign On Authentication](https://auth0.com/learn/how-to-implement-single-sign-on)
[Lock: Single Sign On & Token Based Authentication - Auth0](https://auth0.com/lock)

[auth0/lock - CSS](https://github.com/auth0/lock)
[auth0/lock-passwordless](https://github.com/auth0/lock-passwordless)

## NTLM

[NTLM Authentication Scheme for HTTP](https://www.innovation.ch/personal/ronald/ntlm.html)
[HowTo: Decode and log the username in an NTLM conn... - Pulse Secure Community](https://community.pulsesecure.net/t5/Pulse-Secure-vADC/HowTo-Decode-and-log-the-username-in-an-NTLM-connection/ta-p/28869)

does not to mandate SSL/TLS

## OAuth1

[The OAuth Bible](http://oauthbible.com/)
[OAuth | hueniverse](http://hueniverse.com/oauth/) 1.0
[OAuth | hueniverse](http://hueniverse.com/tagged/oauth/)
[The OAuth 1.0 Guide – hueniverse](https://hueniverse.com/the-oauth-1-0-guide-32503205267e)
[RFC 5849 - The OAuth 1.0 Protocol](http://tools.ietf.org/html/rfc5849)

does not to mandate SSL/TLS

[OAuth and OAuth WRAP: defeating the password anti-pattern | Ars Technica](http://arstechnica.com/information-technology/2010/01/oauth-and-oauth-wrap-defeating-the-password-anti-pattern/) Deprecated for 2.0
[Compromising Twitter’s OAuth security system | Ars Technica](http://arstechnica.com/security/2010/09/twitter-a-case-study-on-how-to-do-oauth-wrong/)
[OAuth Authorization Flow - YDN](https://developer.yahoo.com/oauth/guide/oauth-auth-flow.html)

[geek/OAuth](https://github.com/geek/OAuth)

## OAuth2

[OAuth - Wikiwand](https://www.wikiwand.com/en/OAuth)
[The OAuth Bible](https://oauthbible.com/)

[OAuth.com - OAuth 2.0 Simplified](https://www.oauth.com/)
[OAuth 2.0 Simplified - A guide to building OAuth 2.0 servers](https://oauth2simplified.com/)

[OAuth 2.0 Playground](https://oauth.com/playground/)
[OAuth 2.0 debugger](https://oauthdebugger.com/)
[grant](https://grant.outofindex.com/) OAuth Playground

[OAuth Community Site](http://oauth.net/) 2.0
[OAuth / FrontPage](https://wiki.oauth.net/w/page/12238516/FrontPage)

[RFC 6749 - The OAuth 2.0 Authorization Framework](https://tools.ietf.org/html/rfc6749)
[RFC 6750 - The OAuth 2.0 Authorization Framework: Bearer Token Usage](http://tools.ietf.org/html/rfc6750)
[RFC 8252 - OAuth 2.0 for Native Apps](https://tools.ietf.org/html/rfc8252)
[draft-ietf-oauth-security-topics-12 - OAuth 2.0 Security Best Current Practice](https://tools.ietf.org/html/draft-ietf-oauth-security-topics-12)

[What is OAuth really all about - OAuth tutorial - Java Brains - YouTube](https://www.youtube.com/watch?v=t4-416mg6iU)
[OAuth terminologies and flows explained - OAuth tutorial - Java Brains - YouTube](https://www.youtube.com/watch?v=3pZ3Nh8tgTE)
[OAuth 2.0 and OpenID Connect (in plain English) - YouTube](https://www.youtube.com/watch?v=996OiexHze0)
[An Illustrated Guide to OAuth and OpenID Connect - YouTube](https://www.youtube.com/watch?v=t18YB3xDfXI)
[OAuth 2.0: An Overview - YouTube](https://www.youtube.com/watch?v=CPbvxxslDTU)
[Overview of OAuth 2.0 and OpenID Connect - Using OAuth 2.0 and OpenID Connect with Caché - Caché & Ensemble 2018.1](https://docs.intersystems.com/latest/csp/docbook/DocBook.UI.Page.cls?KEY=GOAUTH_background)
[The unreasonable effectiveness of the Julia programming language – Ars Technica](https://arstechnica.com/science/2020/10/the-unreasonable-effectiveness-of-the-julia-programming-language/?amp=1)

Grant Types

- Authorization Code (front channel login and get auth code, pass to back channel, back channel exchange client secret and auth code for access token)
- Implicit (not recommended, front channel get access token without back channel, should not have refresh token)
- Resource Owner Password Credentials (back channel only, machine to machine)
- Client Credentials (back channel only, make legacy app works)
- Device Code
- Refresh Token

User logins with Identity Provider (IdP), who returns `(id_token, refresh_token)`. `id_token` is usually short lived JWT with TTL in terms of minutes. `refresh_token` is an opaque, one-time token that can be used in lieu of credentials to obtain new `(id_token, refresh_token)` from the IdP. This should be done on client side and `refresh_token` is not to be shared to app server. `refresh_token` has TTL of a user session, say 15-20 minutes, renewed upon each acquisition of new tokens.

[Which OAuth 2.0 Grant should I use?](https://auth0.com/docs/api-auth/which-oauth-flow-to-use)
OAuth 2.0 serves as the authorization framework, the actual authentication occurs with OpenID Connect via access token (received by app from auth server, sent to resource server)

[simov/grant: OAuth Proxy](https://github.com/simov/grant)

[OAuth 2.0 access tokens explained - YouTube](https://www.youtube.com/watch?v=BNEoKexlmA4) bearer token

[Egor Homakov: OAuth2: One access_token To Rule Them All](http://homakov.blogspot.com.ar/2012/08/oauth2-one-accesstoken-to-rule-them-all.html)
[Introducing OAuth 2.0 – hueniverse](https://hueniverse.com/introducing-oauth-2-0-b5681da60ce2)
[Learn OAuth 2.0 - Learning | InterSystems](https://learning.intersystems.com/course/view.php?id=244)
[An Introduction to OAuth 2 | DigitalOcean](https://www.digitalocean.com/community/tutorials/an-introduction-to-oauth-2)
[What is OAuth | How OAuth 2.0 Works | Teleport](https://goteleport.com/blog/how-oauth-authentication-works/)

[OAuth Tips for the Uninitiated - DEV Community 👩‍💻👨‍💻](https://dev.to/antonfrattaroli/oauth-tips-for-the-uninitiated-476e)
[Dancing with OAuth: a step by step guide - DEV Community 👩‍💻👨‍💻](https://dev.to/anabella/dancing-with-oauth-emp)
[OAuth2 for Java Developers: The Basics [Video] - DZone Security](https://dzone.com/articles/oauth2-for-java-developers-the-basics-video)

[foauth.org: OAuth for one](https://foauth.org/) closed due to Trump's policy
[foauth](https://github.com/foauth)

[What is OAuth? What security pros need to know | CSO Online](http://www.csoonline.com/article/3216404/authentication/what-is-oauth-what-security-pros-need-to-know.html)
[Designing a Secure REST (Web) API without OAuth](http://www.thebuzzmedia.com/designing-a-secure-rest-api-without-oauth-authentication/) upload client public key (securely) to server (kind of like passwordless SSH)

[React Authentication with Twitter, Google, Facebook and Github](https://codeburst.io/react-authentication-with-twitter-google-facebook-and-github-862d59583105)
[The Complete React Native Guide to User Authentication with the Amplify Framework - DEV Community 👩‍💻👨‍💻](https://dev.to/dabit3/the-complete-react-native-guide-to-user-authentication-with-the-amplify-framework-ib2)

[PKCE for OAuth 2.0](https://oauth.net/2/pkce/)

[dogeared/OZorkAuth](https://github.com/dogeared/OZorkAuth)

### OpenID

OAuth 2.0 is designed for authorization (permissions), for authentication (identity); hacky way to get user profile and info
OpenID Connect is build upon OAuth 2.0 (with `openid` and `profile` scope) designed for authentication

[OpenID Foundation website](https://openid.net/)
[OpenID Connect | OpenID](https://openid.net/connect/)
[Final: OpenID Connect Core 1.0 incorporating errata set 1](https://openid.net/specs/openid-connect-core-1_0.html)
[RFC 8414 - OAuth 2.0 Authorization Server Metadata](https://tools.ietf.org/html/rfc8414) OAuth Discovery

[OpenID Connect debugger](https://oidcdebugger.com/)
[OpenID Connect Playground](https://openidconnect.net/) ebook

[Security token service - Wikiwand](https://www.wikiwand.com/en/Security_token_service)

[Open Source OAuth 2.0 and OpenID Connect Server - gethydra.sh](https://gethydra.sh/)
[ory/hydra: OpenID Certified™ OpenID Connect & OAuth2 Server (OP, OpenID Provider) - cloud native, security-first, open source API security for your infrastructure. Written in Go. SDKs for any language.](https://github.com/ory/hydra)

[greenpau/caddy-auth-portal: Authentication Plugin for Caddy v2 implementing Form-Based, Basic, Local, LDAP, OpenID Connect, OAuth 2.0 (Github, Google, Facebook, Okta, etc.), SAML Authentication](https://github.com/greenpau/caddy-auth-portal)
[casbin/caddy-authz: Caddy-authz is a middleware for Caddy that blocks or allows requests based on access control policies.](https://github.com/casbin/caddy-authz)
[casbin/casbin: An authorization library that supports access control models like ACL, RBAC, ABAC in Golang](https://github.com/casbin/casbin)

[AppAuth](https://appauth.io/)
[openid/AppAuth-iOS: iOS and macOS SDK for communicating with OAuth 2.0 and OpenID Connect providers.](https://github.com/openid/AppAuth-iOS)
[openid/AppAuth-Android: Android client SDK for communicating with OAuth 2.0 and OpenID Connect providers.](https://github.com/openid/AppAuth-Android)
[openid/AppAuth-JS: JavaScript client SDK for communicating with OAuth 2.0 and OpenID Connect providers.](https://github.com/openid/AppAuth-JS)

[OpenID Connect — Session Management – Ashen De Silva – Medium](https://medium.com/@desilvaashen.15/openid-connect-session-management-d0c8e7dc252b)
[OpenID Connect Backchannel Logout – Ashen De Silva – Medium](https://medium.com/@desilvaashen.15/openid-connect-backchannel-logout-144a3198d2a)

[OpenID | hueniverse](http://hueniverse.com/category/openid/)

### In the Wild

[Google Identity Platform | Google Developers](https://developers.google.com/identity/)
[OAuth 2.0 Playground](https://developers.google.com/oauthplayground/)
[Using OAuth 2.0 to Access Google APIs | Google Identity Platform | Google Developers](https://developers.google.com/identity/protocols/OAuth2)
[Authorizing OAuth Apps - GitHub Docs](https://docs.github.com/en/developers/apps/building-oauth-apps/authorizing-oauth-apps)
[Using OAuth 2.0 for Google APIs | 9bit Studios](http://www.9bitstudios.com/2013/05/using-oauth-2-0-for-google-apis/) dead?
[eBay REST API OAuth2: Plain English Edition – Abe Flansburg – Medium](https://medium.com/@abeflansburg/ebay-rest-api-oauth2-plain-english-edition-1d102a9f719c)

[firebase/firebaseui-web: FirebaseUI is an open-source JavaScript library for Web that provides simple, customizable UI bindings on top of Firebase SDKs to eliminate boilerplate code and promote best practices.](https://github.com/firebase/firebaseui-web)

[Implementing an OAuth Server With Node.js and Express | www.thecodebarbarian.com](http://thecodebarbarian.com/oauth-with-node-js-and-express.html)
[Passport-Free Facebook Login with Node.js | www.thecodebarbarian.com](http://thecodebarbarian.com/passport-free-facebook-login-with-node-js.html)
[GitHub OAuth Login with Node.js | www.thecodebarbarian.com](http://thecodebarbarian.com/github-oauth-login-with-node-js.html)

### boo OAuth2

[RealtimeConf - “OAuth 2.0 - Looking Back and Moving On” by Eran Hammer on Vimeo](https://vimeo.com/52882780)
[OAuth 2.0 and the Road to Hell – hueniverse](https://hueniverse.com/oauth-2-0-and-the-road-to-hell-8eec45921529)
[On Leaving OAuth – hueniverse](https://hueniverse.com/on-leaving-oauth-f8dadb46d93f)
[OAuth Bearer Tokens are a Terrible Idea – hueniverse](https://hueniverse.com/oauth-bearer-tokens-are-a-terrible-idea-1a300fd12e13)
[OAuth 2.0 (without Signatures) is Bad for the Web – hueniverse](https://hueniverse.com/oauth-2-0-without-signatures-is-bad-for-the-web-35eabdfc0ce6)

[6/25 What's Wrong with OAuth2? | Identiverse 2018 - YouTube](https://www.youtube.com/watch?v=OLwz7pIXOWQ)
[Moving On from OAuth 2? – Justin Richer – Medium](https://medium.com/@justinsecurity/moving-on-from-oauth-2-629a00133ade)

[The problem with OAuth for Authentication. | Thread Safe](http://www.thread-safe.com/2012/01/problem-with-oauth-for-authentication.html)

### Logout

[javascript - How to Logout of an Application Where I Used OAuth2 To Login With Google? - Stack Overflow](https://stackoverflow.com/questions/12909332/how-to-logout-of-an-application-where-i-used-oauth2-to-login-with-google)

### Refresh token

[Refresh Tokens: When to Use Them and How They Interact with JWTs](https://auth0.com/blog/refresh-tokens-what-are-they-and-when-to-use-them/)
[Refresh Tokens](https://auth0.com/docs/tokens/refresh-tokens)
[Refresh Token Rotation](https://auth0.com/docs/tokens/refresh-tokens/refresh-token-rotation)

[How to Implement Refresh-Token Functionality (Front-End). | by Ifeanyi Ibekie | The Startup | Medium](https://medium.com/swlh/how-to-implement-refresh-token-functionality-front-end-eff58ce52564)

### Sliding-sessions

Sliding-sessions are sessions that expire after a period of inactivity.

Issue access token upon user action (API calls).

### Libraries

[prose-gatekeeper · GitHub](https://github.com/prose/gatekeeper)
passport
hapi-bell

[Secure a Spring Microservices Architecture with Spring Security and OAuth 2.0 | Okta Developer](https://developer.okta.com/blog/2018/02/13/secure-spring-microservices-with-oauth)

And much more...

## XYZ

[Home | OAuth.xyz](https://oauth.xyz/)

## JWT

[JWT](http://jwt.io) is the spec for how a _non-opaque token_ should be created. This allows token receiver to parse the token and receive meta without database query.
[JSON Web Token - Wikiwand](https://www.wikiwand.com/en/JSON_Web_Token)

[RFC 7515 - JSON Web Signature (JWS)](https://tools.ietf.org/html/rfc7515)
[RFC 7516 - JSON Web Encryption (JWE)](https://tools.ietf.org/html/rfc7516)
[RFC 7517 - JSON Web Key (JWK)](https://tools.ietf.org/html/rfc7517)
[RFC 7518 - JSON Web Algorithms (JWA)](https://tools.ietf.org/html/rfc7518)
[RFC 7519 - JSON Web Token (JWT)](https://tools.ietf.org/html/rfc7519)
[RFC 7520 - JOSE Cookbook](https://tools.ietf.org/html/rfc7520)

JWT = `header.claim.signature`

[JWT, JWS and JWE for Not So Dummies!](https://medium.facilelogin.com/jwt-jws-and-jwe-for-not-so-dummies-b63310d201a3#.egmi2svdf)
[dwyl/learn-json-web-tokens](https://github.com/dwyl/learn-json-web-tokens)
[DjangoCon 2014- JSON Web Tokens - YouTube](https://www.youtube.com/watch?v=825hodQ61bg)
[JWT - JSON Web Token Crash Course (NodeJS & Postgres) - YouTube](https://www.youtube.com/watch?v=T0k-3Ze4NLo)

[Critical flaw alert! Stop using JSON encryption | InfoWorld](http://www.infoworld.com/article/3184582/security/critical-flaw-alert-stop-using-json-encryption.html)
[Critical Vulnerability Uncovered in JSON Encryption](http://blogs.adobe.com/security/2017/03/critical-vulnerability-uncovered-in-json-encryption.html)

[JSON Web Tokens with Public Key Signatures - miguelgrinberg.com](https://blog.miguelgrinberg.com/post/json-web-tokens-with-public-key-signatures)
[How to Secure JWT in a Single-Page Application - DEV Community](https://dev.to/nilanth/how-to-secure-jwt-in-a-single-page-application-cko)

[JSON Web Token Tutorial: Example using AngularJS & Laravel | Toptal](http://www.toptal.com/web/cookie-free-authentication-with-json-web-tokens-an-example-in-laravel-and-angularjs) JWT primer, comparison with server based authentication
[ttkalec/laravel5-angular-jwt: Simple Laravel 5/Angular app that shows how to use the most basic JWT authentication](https://github.com/ttkalec/laravel5-angular-jwt)
[Authentication with Node.js, JWTs, and Oracle Database | JavaScript and Oracle](https://jsao.io/2015/06/authentication-with-node-js-jwts-and-oracle-database/)
[Securing node.js RESTful services with JWT Tokens | Richard Astbury's Blog](http://coderead.wordpress.com/2012/08/16/securing-node-js-restful-services-with-jwt-tokens/)

### In the Contrary

[Stop using JWT for sessions - joepie91's Ramblings](http://cryto.net/~joepie91/blog/2016/06/13/stop-using-jwt-for-sessions/)
[Stop using JWT for sessions, part 2: Why your solution doesn't work - joepie91's Ramblings](http://cryto.net/~joepie91/blog/2016/06/19/stop-using-jwt-for-sessions-part-2-why-your-solution-doesnt-work/)
[Why JWTs Suck as Session Tokens | Okta Developer](https://developer.okta.com/blog/2017/08/17/why-jwts-suck-as-session-tokens)

[JSON Web Tokens Suck - Randall Degges (DevNet Create 2018) - YouTube](https://www.youtube.com/watch?v=JdGOb7AxUo0)

### Server

```js
var myHeaders = {
  alg: "HS256", //denotes the algorithm (shorthand alg) used for the  signature is HMAC SHA-256
  typ: "JWT", //denotes the type (shorthand typ) of token this is
};

var myClaims = {
  sub: "tom@stormpath.com",
  name: "Tom Abbott",
  role: "user",
};

var headers = base64URLencode(myHeaders);
var claims = base64URLencode(myClaims);
var payload = header + "." + claims;

var signature = base64URLencode(HMACSHA256(payload, secret));

var encodedJWT = payload + "." + signature;
```

[netlify/gotrue: An SWT based API for managing users and issuing SWT tokens](https://github.com/netlify/gotrue)
[jawblia/auth: Template for JWT authentication in a MERN app with protected routes](https://github.com/jawblia/auth)

### Videos

[MNUG 2014.08.13 - Lightning talk: JWT: JSON Web Token - YouTube](https://www.youtube.com/watch?v=eWUkxzyB1Rk)
[Introduction to JWT (JSON Web Token) - Securing apps & services - YouTube](https://www.youtube.com/watch?v=oXxbB5kv9OA&feature=youtu.be)
[NodeJS Tutorial | APIs Strike Back: The Rise of JSON Web Tokens - YouTube](https://www.youtube.com/watch?v=vziqErg6NZs) Demo with Express
[JSON Web Token Series - YouTube](https://www.youtube.com/playlist?list=PL8PwA1AFXwLmicLd1JZn6WI3tpQVz3h8t)

### Stormpath

[Use JWT The Right Way!](https://stormpath.com/blog/jwt-the-right-way) JWT primer, tips for security
[Build Secure User Interfaces Using JSON Web Tokens (JWTs)](https://stormpath.com/blog/build-secure-user-interfaces-using-jwts)
[So what's the issue with JWTs in localStorage, exactly? : webdev](https://www.reddit.com/r/webdev/comments/bpcleu/so_whats_the_issue_with_jwts_in_localstorage/)
[Where to Store your JWTs - Cookies vs HTML5 Web Storage - Stormpath User Identity API](https://stormpath.com/blog/where-to-store-your-jwts-cookies-vs-html5-web-storage/) JWT primer, tips for storage and CSURF
**Conclusion**: Store the JWT in `HttpOnly; Secure` cookie. Add `xsrfToken` to JWT for CSURF protection.

### Scotch

[The Anatomy of a JSON Web Token | Scotch](https://scotch.io/tutorials/the-anatomy-of-a-json-web-token)
[Authenticate a Node.js API with JSON Web Tokens | Scotch](https://scotch.io/tutorials/authenticate-a-node-js-api-with-json-web-tokens)

### Auth0

Auth0 is the owner of Node.js `jsonwebtoken` module.

[The Complete Guide to React User Authentication with Auth0](https://auth0.com/blog/complete-guide-to-react-user-authentication/)
[Auth0 React SDK Quickstarts: Login](https://auth0.com/docs/quickstart/spa/react)
[React and Auth0 - YouTube](https://www.youtube.com/playlist?list=PLZ14qQz3cfJL6aoKZ_Ly7jiYrwi9ihviW)
[How to use Auth0 with Node.js and Express | InfoWorld](https://www.infoworld.com/article/3629129/how-to-use-auth0-with-nodejs-and-express.html)

[Pricing - Auth0](https://auth0.com/pricing) 7000 active users free tier

[Using JSON Web Tokens as API Keys](https://auth0.com/blog/2014/12/02/using-json-web-tokens-as-api-keys/)
[Blacklisting JSON Web Token API Keys](https://auth0.com/blog/2015/03/10/blacklist-json-web-token-api-keys/)
[auth0/node-jsonwebtoken](https://github.com/auth0/node-jsonwebtoken)
[auth0/nginx-jwt](https://github.com/auth0/nginx-jwt)
[auth0/jwt-as-api-keys](https://github.com/auth0/jwt-as-api-keys)

### Firebase

[Firebase Authentication](https://firebase.google.com/docs/auth)
[Authenticate with Firebase using Password-Based Accounts using Javascript](https://firebase.google.com/docs/auth/web/password-auth#web-v8)

[Firebase Pricing](https://firebase.google.com/pricing) 10k/month free tier

### Netlify

[netlify/netlify-identity-widget: A zero config, framework free Netlify Identity widget](https://github.com/netlify/netlify-identity-widget)
[Netlify Identity Widget](https://identity.netlify.com/)

[Getting Started with JWT and Identity | Netlify](https://www.netlify.com/blog/2018/01/23/getting-started-with-jwt-and-identity/)
[Authenticate users with Netlify Identity | Netlify Docs](https://docs.netlify.com/visitor-access/identity/)
[netlify/gotrue: An SWT based API for managing users and issuing SWT tokens](https://github.com/netlify/gotrue)
[Introducing Built-in Identity Service to Streamline User Management | Netlify](https://www.netlify.com/blog/2017/09/07/introducing-built-in-identity-service-to-streamline-user-management/)

### JWTenizr

[JWTenizr | jwtenizr](http://jwtenizr.sh/)
[Json Web Token Generator - JWTenizr.sh 0.0.3 released : Adam Bien's Weblog](http://adambien.blog/roller/abien/entry/json_web_token_generator_jwtenizr)

## LDAP

[Lightweight Directory Access Protocol - Wikiwand](https://www.wikiwand.com/en/Lightweight_Directory_Access_Protocol)

[OpenLDAP, Main Page](https://www.openldap.org/)
[LDAP Linux HOWTO](https://www.tldp.org/HOWTO/LDAP-HOWTO/index.html)

[What are the differences between LDAP and Active Directory? - Stack Overflow](https://stackoverflow.com/questions/663402/what-are-the-differences-between-ldap-and-active-directory)
[What are the differences between LDAP and Active Directory authentication? - Stack Overflow](https://stackoverflow.com/questions/16209039/what-are-the-differences-between-ldap-and-active-directory-authentication?rq=1)

[RFC 4511 - Lightweight Directory Access Protocol (LDAP): The Protocol](https://tools.ietf.org/html/rfc4511)

[AD/ADAM vs. LDAP (OpenLDAP and others)](ftp://ftp.uni-duisburg.de/LDAP/Adam-Eval1-0.pdf)
[Allow external LDAP access to O365 / AzureAD – Customer Feedback for Microsoft Office 365](https://office365.uservoice.com/forums/273493-office-365-admin/suggestions/33936427-allow-external-ldap-access-to-o365-azuread)

### Active Directory

[Active Directory - Wikiwand](https://www.wikiwand.com/en/Active_Directory)
[Introduction to Active Directory Infrastructure in Windows Server 2012 - YouTube](https://www.youtube.com/watch?v=hxgz7MR7MGQ)
[Introduction to Active Directory Directory Services Structure in Windows Server 2012 - YouTube](https://www.youtube.com/watch?v=lFwek_OuYZ8)

[Active Directory Deep Dive – Free video tutorials](https://go.veeam.com/learn-active-directory-deep-dive-expert-video-tutorials-ty)
[Active Directory 101 - YouTube](https://www.youtube.com/watch?v=2hXR0UplTds)
[Active Directory and virtualization - YouTube](https://www.youtube.com/watch?v=hqiQZp1N-LI)
[Active Directory and backup - YouTube](https://www.youtube.com/watch?v=eISq3SKuZjA)

## Oz/Hawk

[Auth to See the Wizard – hueniverse](https://hueniverse.com/auth-to-see-the-wizard-4a7c3572f618)
[What's Hawk and how to use it?](http://blog.notmyidea.org/whats-hawk-and-how-to-use-it.html)

[hapijs/hawk: HTTP Holder-Of-Key Authentication Scheme](https://github.com/hapijs/hawk)
[mozilla-services/requests-hawk: Hawk authentication strategy for the requests python library.](https://github.com/mozilla-services/requests-hawk)
[kumar303/mohawk: Python library for Hawk HTTP authorization](https://github.com/kumar303/mohawk)

[outmoded/oz: Web Authorization Protocol](https://github.com/outmoded/oz)
