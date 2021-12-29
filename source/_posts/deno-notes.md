---
title: "Deno notes"
date: 2018-06-11 13:08:43
categories:
  - comp.lang
tags:
  - deno
  - typescript
  - notes
toc: true
---

[Deno](https://deno.land/)
[denoland/deno: A secure TypeScript runtime on V8](https://github.com/denoland/deno)
[10 Things I Regret About Node.js - Ryan Dahl - JSConf EU 2018 - YouTube](https://www.youtube.com/watch?v=M3BM9TB-8yA)
[Building a Deno HTTPS Web Server with Self-Signed Certificate - YouTube](https://www.youtube.com/watch?v=I6TcBmNhB78)

- Deno is written in Rust
- [Search Results for 'deno' - crates.io: Rust Package Registry](https://crates.io/search?q=deno)
- making embedding Deno easy

[deno doc](https://doc.deno.land/)
[Introduction | Manual | Deno](https://deno.land/manual@main/introduction)
[Deno 1.0 | Deno Blog](https://deno.com/blog/v1)
[Permissions | Manual | Deno](https://deno.land/manual@main/getting_started/permissions)

[Deno: The next step in Node.js - DEV Community](https://dev.to/siddharthshyniben/deno-the-next-step-in-node-js-ij1)

[What is Deno and will it Replace NodeJS? | by Fernando Doglio | Bits and Pieces](https://blog.bitsrc.io/what-is-deno-and-will-it-replace-nodejs-a13aa1734a74)
[Deno: Will It Replace Node.JS? - YouTube](https://www.youtube.com/watch?v=lcoU9jtsK24)
[Node.js Creator Blasts Node.js, Offers a Secure TypeScript-Based Alternative - The New Stack](https://thenewstack.io/node-js-creator-blasts-node-js-offers-a-secure-typescript-based-alternative/)
[First thoughts on Deno, the JavaScript/TypeScript run-time](https://43081j.com/2019/01/first-look-at-deno)

## Types

```sh
deno types
```

## Libraries

[builtin@stable - deno doc](https://doc.deno.land/builtin/stable)
[std | Deno](https://deno.land/std)
[Third Party Modules | Deno](https://deno.land/x)

[Use import maps in Deno with VSCode and Denon - DEV Community](https://dev.to/roelandmoors/use-import-maps-in-deno-with-vscode-and-denon-25c1)

## Tips and Tricks

[Reload Deno cache after upgrading](https://www.secondstate.io/articles/reload-deno-cache/) errors in `std`

```sh
deno cache --reload my_app.ts
```

[Generate HTML on the server with Deno and JSX - DEV Community](https://dev.to/roelandmoors/generate-html-on-the-server-with-deno-and-jsx-429b)

[Using node modules in Deno. A bad practice but sometimes there is… | by Ada Rose Cannon | Samsung Internet Developers | Aug, 2020 | Medium](https://medium.com/samsung-internet-dev/using-node-modules-in-deno-2885600ed7a9)
