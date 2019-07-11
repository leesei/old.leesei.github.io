---
title: "Visual Studio Code"
categories:
  - app
tags:
  - visual-studio-code
  - settings
  - package-manager
toc: true
date: 2017-06-19 12:47:12
---

[Visual Studio Code - Code Editing. Redefined](https://code.visualstudio.com/)
[VS Code Can Do That?](https://vscodecandothat.com/)

[viatsko/awesome-vscode: 🎨 A curated list of delightful VS Code packages and resources.](https://github.com/viatsko/awesome-vscode)
[Microsoft/vscode-recipes](https://github.com/Microsoft/vscode-recipes)

[Visual Studio Code Is So Popular But Why?](https://blog.eduonix.com/software-development/visual-studio-code-popular/)
[Why I moved away from Atom to Visual Studio Code and my Setup · EQuimper's Blog](https://equimper.me/post/why-i-moved-away-from-atom-to-visual-studio-code-and-my-setup/)
[✨ Immensely upgrade your development environment with these Visual Studio Code extensions](https://medium.com/@wesharehoodies/immensely-upgrade-your-development-environment-with-these-visual-studio-code-extensions-9cd790478530)

[Dan Taylor - Get Productive with Python in Visual Studio Code - YouTube](https://www.youtube.com/watch?v=6YLMWU-5H9o)
[qubitron/pydemo: Get Productive with Python and Visual Studio Code - slides, video, and demo code](https://github.com/qubitron/pydemo)

## Must Read Docs

[Documentation for Visual Studio Code](https://code.visualstudio.com/docs)
[Visual Studio Code Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)

Welcome screen
Interactive Playground

## Project Files (Workspaces)

[Multi-root Workspaces in Visual Studio Code](https://code.visualstudio.com/docs/editor/multi-root-workspaces)

`.code-workspace`

## CLI

[CLI](https://code.visualstudio.com/docs/getstarted/tips-and-tricks#_command-line)

`code --list-extensions`
`code --install-extension <extension>`

## Extension

[Extensions for Visual Studio family of products | Visual Studio Marketplace](https://marketplace.visualstudio.com/)

[My list of Microsoft Visual Code Studio Extensions | virtuallyGhetto](https://www.virtuallyghetto.com/2018/07/my-list-of-microsoft-visual-code-studio-extensions.html)
[✨ Immensely upgrade your development environment with these Visual Studio Code extensions](https://medium.freecodecamp.org/immensely-upgrade-your-development-environment-with-these-visual-studio-code-extensions-9cd790478530)
[Python Development in Visual Studio Code (Setup Guide) – Real Python](https://realpython.com/courses/python-development-visual-studio-code-setup-guide/?__s=9yjm1swp7s426a4xisnd)
[Python Development in Visual Studio Code – Real Python](https://realpython.com/python-development-visual-studio-code/)
[Visual Studio Code Settings and Extensions for Faster JavaScript Development - Codesmith Development](https://codesmithdev.com/visual-studio-code-settings-and-extensions-for-faster-javascript-development/)
[The Ultimate VSCode Setup for JS/React – Productivity Freak – Medium](https://medium.com/productivity-freak/the-ultimate-vscode-setup-for-js-react-6a4f7bd51a2)
[My Favorite VSCode Extensions and Settings — Nick Janetakis](https://nickjanetakis.com/blog/my-favorite-vscode-extensions-and-settings)
[15 Essential Plugins for Visual Studio Code - Tutorialzine](https://tutorialzine.com/2017/06/15-essential-plugins-for-visual-studio-code)
[22 Best Visual Studio Code Extensions for Web Development ― Scotch](https://scotch.io/bar-talk/22-best-visual-studio-code-extensions-for-web-development/amp)
[26 Miraculous VSCode Tools for JavaScript Developers in 2019](https://medium.com/better-programming/26-miraculous-vscode-tools-for-javascript-developers-in-2019-e184131d75af)
[10 Visual Studio Code extensions for every developer | InfoWorld](https://www.infoworld.com/article/3390988/10-visual-studio-code-extensions-for-every-developer.html)

Use "Sublime keybinding"
Set <kbd>Crtl</kbd> + <kbd>U</kbd> to "Open Link"
Set <kbd>Crtl</kbd> + <kbd>F2</kbd> to toggle bookmark, <kbd>F2</kbd> to jump to next bookmark

```json
// Place your key bindings in this file to overwrite the defaults
[
  {
    "key": "shift+alt+t",
    "command": "workbench.action.tasks.test"
  },
  {
    "key": "alt+cmd+[ArrowDown]",
    "command": "workbench.action.terminal.focusNext",
    "when": "terminalFocus"
  },
  {
    "key": "alt+cmd+[ArrowUp]",
    "command": "workbench.action.terminal.focusPrevious",
    "when": "terminalFocus"
  }
]
```


### Writing Extensions

[Visual Studio Code Extensibility Reference](https://code.visualstudio.com/docs/extensionAPI/overview)
[Visual Studio Code API Reference](https://code.visualstudio.com/docs/extensionAPI/vscode-api)
[Visual Studio Code Extension Contribution Points - package.json](https://code.visualstudio.com/docs/extensionAPI/extension-points)
[Microsoft/vscode-extension-samples: Sample code illustrating the VS Code extension API.](https://github.com/Microsoft/vscode-extension-samples)

[Creating an Extension Pack for Visual Studio Code ― Scotch](https://scotch.io/tutorials/creating-an-extension-pack-for-visual-studio-code/amp)
[The Yo Code Visual Studio Code Extension Generator](https://code.visualstudio.com/docs/extensions/yocode)
[My First Visual Code Extension - DEV Community 👩‍💻👨‍💻](https://dev.to/mokkapps/my-first-visual-code-extension-4l5f)
[Why I wrote 33 VSCode extensions and how I manage them](https://medium.com/@fabiospampinato/why-i-wrote-33-vscode-extensions-and-how-i-manage-them-cb61df05e154)

### Color scheme/Themes

[Material Icon Theme - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
[VSCode Great Icons - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=emmanuelbeziat.vscode-great-icons)
[One Dark Pro - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme)

### Syntax/Snippets

Python
C/C++
Java
nginx.conf hint
markdown-extended
Go
Docker
Output Colorizer
colorize
NDJSON Colorizer
Plantuml
[Rainbow CSV - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=mechatroner.rainbow-csv)

### Plugins

[Bookmarks - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
[Code Spell Checker - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
[File Utils - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils) ~= Sidebar Enhancements
[hexdump for VSCode - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=slevesque.vscode-hexdump)
[Kubernetes - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-kubernetes-tools.vscode-kubernetes-tools)
[Prettier - Code formatter - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
[Project Manager - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=alefragnani.project-manager)
[REST Client - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=humao.rest-client)
[Sublime Text Keymap and Settings Importer - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
[Peacock - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=johnpapa.vscode-peacock&wt.mc_id=devto-blog-jopapa)

### Copilit

[Copilot for VS Code - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=Metatype.copilot-vscode)

[Introducing Copilot for VS Code – AngularDoc – Medium](https://medium.com/angulardoc/introducing-copilot-for-vs-code-c1b1a16bdd21)
[前端工程师的必备VS Code插件 -- Copilot - 知乎](https://zhuanlan.zhihu.com/p/62929504)

### Remote Development

[Visual Studio Code Remote Development](https://code.visualstudio.com/docs/remote/remote-overview)
[Removing VS Code Remote Extensions - DEV Community 👩‍💻👨‍💻](https://dev.to/azure/removing-vs-code-remote-extensions-1gol)

#### Live Share

[Visual Studio Live Share | Visual Studio - Visual Studio](https://visualstudio.microsoft.com/services/live-share/)
[Live Share Extension Pack - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-pack)
[VS Live Share Audio - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare-audio)

[Collaborate using Visual Studio Code - Visual Studio Live Share - Visual Studio Live Share | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/liveshare/use/vscode#share-a-terminal)

#### Settings Sync

[Settings Sync - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync&WT.mc_id=vscodecandothat-dotcom-team)

[Visual Studio Code Settings Sync Configurations – Shan Ali Khan – Medium](https://medium.com/@itsShanKhan/visual-studio-code-settings-sync-configurations-ed8dd6fd9753)

`~/.config/Code/User/settings.json`
`~/.config/Code/User/syncLocalSettings.json`
