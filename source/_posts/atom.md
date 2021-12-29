---
title: "Atom"
date: 2015-07-09 00:16:00
categories:
  - app
tags:
  - atom
  - settings
  - package-manager
toc: true
---

[Atom](https://atom.io/)
[Issues · atom/atom](https://github.com/atom/atom/issues)

[Atom Editor Tips and Tricks](http://www.atomtips.com/)
[Atom editor or Sublime Text which one to pick](http://www.atomtips.com/atom-editor-vs-sublime-text/)
[Best of Atom: Features, Plugins, Acting Like Sublime Text | Scotch](https://scotch.io/bar-talk/best-of-atom-features-plugins-acting-like-sublime-text)
[Teletype for Atom](https://teletype.atom.io/)

[The Battle Royale: Atom vs. Sublime - Web Design Weekly](https://web-design-weekly.com/2015/07/30/atom-vs-sublime/)

[A Quick Look At The New Atom IDE - Tutorialzine](https://tutorialzine.com/2017/09/a-quick-look-at-the-new-atom-ide)

> note: [`community/atom`](https://www.archlinux.org/packages/community/x86_64/atom/) in Arch repo is non standard
> [Cannot open markdown link · Issue #23 · atom/link](https://github.com/atom/link/issues/23#issuecomment-306960587)

<!-- more -->

## Must Read Docs

[Atom](https://atom.io/docs/latest/)
[Documentation](https://atom.io/docs)

Terminology:

| SublimeText | Atom    |
| ----------- | ------- |
| Syntax      | Grammar |

## Package Manager

Atom has a built in package manager `apm` to install packages form official repo. It is actually a wrapper for `npm` for the Atom repo so you should find it familiar.
You can do install, search, list with the `apm` CLI. `apm search -p` for packages, `apm search -t` for themes.
You can also directly install to config folder.

[Packages](https://atom.io/packages)
[Themes](https://atom.io/themes)

## Extension Development

[package-generator](https://atom.io/packages/package-generator)
[run-in-atom](https://atom.io/packages/run-in-atom)

[How to Write Atom Packages Using Vanilla JavaScript](http://www.sitepoint.com/write-atom-packages-using-vanilla-javascript/)

### Adding to Context Menu

In `init.coffee`:

```coffee
atom.contextMenu.add {
    'atom-text-editor': [{
        label: 'Bookmark',
        command: 'my-package:toggle'
    }]
}
```

### Theme Development

### Grammar Development

### Snippets Development

[Get productive with Atom Snippets - Atom Editor Tips and Tricks](http://www.atomtips.com/get-productive-atom-snippets/)

### Publishing to Package Control

## My Installed Packages

[Atom Setup | Front End Engineering, May 2015](http://jacobthemyth.gitbooks.io/front-end-engineering-may-2015/content/notes/misc/atom-setup.html)
[New Package Roundup - Atom Blog](http://blog.atom.io/2015/08/06/new-package-roundup.html)

Use [keybinding-resolver](https://atom.io/packages/keybinding-resolver) to check how keystrokes a resolved, use `'native!'` to override package binding.

[goto](https://atom.io/packages/goto) (based on syntax) is better than the built-in [symbols-view](https://atom.io/packages/symbols-view) (based on ctag). But see [Parse headings in markdown as symbols · Issue #52 · v3ss0n/goto](https://github.com/v3ss0n/goto/issues/52).

```sh
> apm ls --no-color -ib

Sublime-Style-Column-Selection@1.7.4
api-workbench@0.8.45
atom-wrap-in-tag@0.6.0
auto-update-plus@0.2.0
browse@1.6.1
build@0.68.0
busy@0.7.0
busy-signal@1.4.3
ctrl-dir-scroll@0.2.3
file-icons@2.1.7
goto@1.8.3
highlight-selected@0.13.1
intentions@1.1.2
language-markdown@0.23.0
linter@2.1.4
linter-markdown@4.0.1
linter-ui-default@1.6.0
markdown-folder@0.5.0
markdown-preview-plus@2.4.9
markdown-scroll-sync@2.1.2
minimap@4.28.2
minimap-cursorline@0.2.0
minimap-find-and-replace@4.5.2
minimap-git-diff@4.3.1
minimap-highlight-selected@4.6.1
minimap-linter@2.0.0
multi-cursor@2.1.5
opened-files@0.3.6
satisfy-dependencies@0.3.1
set-syntax@0.3.2
sort-lines@0.14.0
sublime@0.5.0
sublime-block-comment@0.5.1
sublime-word-navigation@0.2.0
sublimify@0.10.0
tag@0.5.0
text-manipulation@0.6.0
```

### Synchronize settings

[Syncing settings & packages between machines - features - Atom Discussion](https://discuss.atom.io/t/syncing-settings-packages-between-machines/1385/23)

symlink `~/.atom` would be overkill

[How to synchronize packages and settings](http://www.atomtips.com/how-to-synchronize-atom-between-computers/)
[sync-settings](https://atom.io/packages/sync-settings)
[parcel](https://atom.io/packages/parcel)
[package-list](https://atom.io/packages/package-list)
[package-list-downloader](https://atom.io/packages/package-list-downloader)
[package-sync](https://atom.io/packages/package-sync)

### Color scheme/Themes

[atom-material-ui](https://atom.io/themes/atom-material-ui)
[seti-ui](https://atom.io/themes/seti-ui)
[unity-ui](https://atom.io/themes/unity-ui)

[material-design-syntax](https://atom.io/themes/material-design-syntax)

### Grammar/Snippets

[atom-bootstrap3](https://atom.io/packages/atom-bootstrap3)
[react](https://atom.io/packages/react)

[javascript-snippets](https://atom.io/packages/javascript-snippets)
[turbo-javascript](https://atom.io/packages/turbo-javascript)

### Plugins

[atom-alignment](https://atom.io/packages/atom-alignment)
[atom-beautify](https://atom.io/packages/atom-beautify)
[autocomplete-paths](https://atom.io/packages/autocomplete-paths)
[autocomplete-plus](https://atom.io/packages/autocomplete-plus)
[autocomplete-snippets](https://atom.io/packages/autocomplete-snippets)
[bookmarklet](https://atom.io/packages/bookmarklet)
[file-icons](https://atom.io/packages/file-icons)
[git-plus](https://atom.io/packages/git-plus)
[highlight-selected](https://atom.io/packages/highlight-selected)
[markdown-writer](https://atom.io/packages/markdown-writer)
[minimap-cursorline](https://atom.io/packages/minimap-cursorline)
[minimap-find-and-replace](https://atom.io/packages/minimap-find-and-replace)
[minimap-highlight-selected](https://atom.io/packages/minimap-highlight-selected)
[minimap-linter](https://atom.io/packages/minimap-linter)
[minimap](https://atom.io/packages/minimap)
[pigments](https://atom.io/packages/pigments)
[project-manager](https://atom.io/packages/project-manager)
[script](https://atom.io/packages/script)
[set-syntax](https://atom.io/packages/set-syntax)
[sort-lines](https://atom.io/packages/sort-lines)
[sublime](https://atom.io/packages/sublime)

### Plugins development

[Floobits News: Developing Atom Plugins, Part 1: On the Bleeding Edge](https://news.floobits.com/2015/10/12/developing-atom-plugins-on-the-bleeding-edge/)
[Floobits News: Developing Atom Packages, Part 2: So Much Potential, So Many Bugs](https://news.floobits.com/2015/10/14/developing-atom-plugins-so-much-potential-so-many-bugs/)

### Linter

[linter](https://atom.io/packages/linter) ([Linters list](http://atomlinter.github.io/))

[Wallaby.js for Atom text editor · Artem Govorov](http://dm.gl/2015/08/31/wallaby-for-atom/)
