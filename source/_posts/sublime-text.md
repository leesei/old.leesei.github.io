---
title: "Sublime Text"
date: 2015-04-02 14:23:03
categories:
  - app
tags:
  - settings
  - sublime-text
  - package-control
  - package-manager
toc: true
---

[Sublime Text: The text editor you'll fall in love with](http://www.sublimetext.com/)
[Sublime Text Issues](https://github.com/SublimeTextIssues)

[Sublime Text 4 - News - Sublime HQ](https://www.sublimetext.com/blog/articles/sublime-text-4)

<!-- more -->

## Must Read Docs

[Documentation - Sublime Text](http://www.sublimetext.com/docs/)
[Sublime Text Community Documentation](https://docs.sublimetext.io/)

## Project Files

[Projects - Sublime Text 3 Documentation](http://www.sublimetext.com/docs/3/projects.html)
[Sublime Text 2 Project Bliss - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/sublime-text-2-project-bliss--net-27256)

```json
{
  "folders": [
    {
      "path": "src",
      "folder_exclude_patterns": ["backup"],
      "follow_symlinks": true
    },
    {
      "path": "docs",
      "name": "Documentation",
      "file_exclude_patterns": ["*.css"]
    }
  ],
  "settings": {
    "tab_size": 8
  },
  "build_systems": [
    {
      "name": "List",
      "shell_cmd": "ls -l"
    }
  ]
}
```

```js
{
    "folders":
    [
        { // theme
            "path": "/C/wamp/www/wordpress/wp-content/themes/twentyeleven",
            "name": "Twenty Eleven Theme",
            "file_exclude_patterns":[
                "._*",
                "*.ico",
                "*.swf"
            ],
            "folder_exclude_patterns": [
                "images"
            ]
        },
        { // plugins folder
            "path": "/C/wamp/www/wordpress/wp-content/plugins",
            "name": "Plugins Folder",
            "file_exclude_patterns":[
                "._*", // you need to specify this *again*
                "*.bak",
                "*.sample",
                "*.tar",
                "*.tgz",
                "*.zip"
            ],
            "folder_exclude_patterns": [
                "akismet"//,
                // add any other plugins you wish to exclude
            ]
        }
    ],
    "settings":
    {
        "tab_size": 4
    }
}
```

## `PATH` setting

["TERM environment variable not set." when Python build (on mac) - Technical Support - Sublime Forum](https://forum.sublimetext.com/t/term-environment-variable-not-set-when-python-build-on-mac/25495)
[Troubleshooting > Debugging PATH problems — SublimeLinter documentation](http://www.sublimelinter.com/en/latest/troubleshooting.html#debugging-path-problems)

**Make sure your shell do not echo anything to the console when you login.**

`import os; os.environ['PATH']` in Sublime Console
`$SHELL -l -c 'echo ${PATH}'` in terminal, used by SublimeLinter

[Hacking the PATH variable in Sublime Text](http://robdodson.me/hacking-the-path-variable-in-sublime-text/)
[Setting environment variables on login in OS X • Serge Émond](https://xn--sergemond-f4a.ca/en/articles/os-x-environment-at-login/)
[int3h/SublimeFixMacPath: A Sublime Text 2/3 plugin to set the PATH correctly on OS X](https://github.com/int3h/SublimeFixMacPath)

## Customization after install

[Home · mrmartineau/SublimeTextSetupWiki Wiki](https://github.com/mrmartineau/SublimeTextSetupWiki/wiki)
[Perfect Workflow in Sublime Text 2 - Tuts+ Course](http://code.tutsplus.com/courses/perfect-workflow-in-sublime-text-2)
[Sublime Text Perfect Workflow - YouTube](https://www.youtube.com/playlist?list=PLB_IY29eVwsXTToA7tqFV5uaqRw00XMy0)
[Getting Started with SublimeText - YouTube](https://www.youtube.com/watch?v=04gKiTiRlq8)
[Sublime Text Tutorials - YouTube](https://www.youtube.com/playlist?list=PLLnpHn493BHEYF4EX3sAhVG2rTqCvLnsP)
[Tag Archive for "sublime-text" | Scotch](https://scotch.io/tag/sublime-text)
[Sublime Text Packages](https://github.com/SublimeText/)
[15 Awesome Sublime Text Plugins For Web Development - Tutorialzine](https://tutorialzine.com/2016/10/15-awesome-sublime-text-plugins-for-web-development)
[dreikanter/sublime-bookmarks: Sublime Text essential plugins and resources](https://github.com/dreikanter/sublime-bookmarks)

[Sublimetext commands and shortcuts | ShortcutFoo](https://www.shortcutfoo.com/app/dojos/sublime-text-2-win)

### Console

Use <kbd>Ctrl</kbd>+<kbd>\`</kbd> to enter Sublime's Python console

### Install Directory

- **Windows**:
- **OS X**:
- **Linux**: `/opt/sublime_text/`

### Data Directory

- **Windows**: `%APPDATA%\Sublime Text 3`
- **OS X**: `~/Library/Application Support/Sublime Text 3`
- **Linux**: `~/.config/sublime-text-3`

### Package Directory

```python
sublime.packages_path()
```

Default packages are located at `<Install Directory>/Packages`.

### Package Control

[Package Control - the Sublime Text package manager](https://packagecontrol.io/)

Follow the instruction to install Package Control via Sublime console.

Installed packages (Package Control > Settings - User):
`<DATA>/Packages/User/Package Control.sublime-settings`

> You can do batch install by editing this file and restarting Sublime Text.

[Docs for Package Developers - Package Control](https://packagecontrol.io/docs#Package_Developers)
[Submitting a Package - Package Control](https://packagecontrol.io/docs/submitting_a_package#Step_2)

## Extension Development

Sublime Text's extensions are usually compatible with TextMate. This design choice make migration from TextMate easy and helps to build Sublime Text's user base.

It is recommended to use [AAAPackageDev][] to write extensions, which now use YAML over JSON by defaults for the definitions.
[PackageResourceViewer][] is great for viewing files of installed packages (other than visiting the repository).

[Extending Sublime Text — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/extensibility/extensibility.html)

[Sublime Text - Plugin Examples](http://www.sublimetext.com/docs/plugin-examples)
[Sublime Text - Plugin API Reference](http://www.sublimetext.com/docs/api-reference)

[How to Create a Sublime Text 2 Plugin - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/how-to-create-a-sublime-text-2-plugin--net-22685)
[Creating Sublime Text 3 Plugins – Part 1 | Clark/Nikdel/Powell](http://clarknikdelpowell.com/blog/creating-sublime-text-3-plugins-part-1/)
[Creating Sublime Text 3 Plugins – Part 2 | Clark/Nikdel/Powell](http://clarknikdelpowell.com/blog/creating-sublime-text-3-plugins-part-2/)

[SublimeText/PackageTesting](https://github.com/SublimeText/PackageTesting)

Page defines commands in `<name>.sublime-commands`.  
Enter `sublime.log_commands(True)` in console to show commands triggered.

### Theme Development

Actually there are two things here:

- theme of Sublime Text
- color scheme

[TextMate Manual » Themes](http://manual.macromates.com/en/themes)

Online editor:
[TmTheme Editor](http://tmtheme-editor.herokuapp.com/)
[aziz/tmTheme-Editor](https://github.com/aziz/tmTheme-Editor)

Local editor:
[A Guide to Installing ColorSchemeEditor for Sublime Text 3 | MattDMo.com](http://mattdmo.com/guide-to-installing-colorschemeeditor-for-sublime-text-3/)
[facelessuser/ColorSchemeEditor](https://github.com/facelessuser/ColorSchemeEditor)

### Syntax Development

[TextMate Manual » Language Grammars](http://manual.macromates.com/en/language_grammars)
[TextMate Manual » Scope Selectors](http://manual.macromates.com/en/scope_selectors)

[Syntax - Sublime Text 3 Documentation](http://www.sublimetext.com/docs/3/syntax.html) new `.sublime-syntax`
[Syntax Definitions — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/sublime-text-3/extensibility/syntaxdefs.html)
[Syntax Definitions (reference) — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/reference/syntaxdefs.html)
[Syntax Definitions — Sublime Text Help](http://sublimetext.info/docs/en/extensibility/syntaxdefs.html) (deprecated)

[klorenz / SyntaxHighlightTools — Bitbucket](https://bitbucket.org/klorenz/syntaxhighlighttools) has docs on tmPreferences.
[MagicStack/syntaxdev: Unit testing framework for Sublime Text and Atom syntaxes.](https://github.com/MagicStack/syntaxdev)

[TmTheme Editor Stats](http://tmtheme-editor.herokuapp.com/stats) to see what scopes are being recognized by themes.

[Sublime Forum • View topic - How to highlight a nested scope?](http://www.sublimetext.com/forum/viewtopic.php?p=48270)
[sublime tmlanguage site:www.sublimetext.com - Google Search](https://www.google.com.hk/search?q=sublime+tmlanguage+site:www.sublimetext.com)

Use [Regex101](https://regex101.com/#python) to test the regex (use `gm` flags).
https://regex101.com/r/cX0eW3

### Snippets Development

[Working with Code Snippets in Sublime Text - Hongkiat](http://www.hongkiat.com/blog/sublime-code-snippets/)
[Quickly Insert Text & Code with Sublime Text Snippets :: Scott Granneman](http://www.granneman.com/webdev/editors/sublime-text/top-features-of-sublime-text/quickly-insert-text-and-code-with-sublime-text-snippets/)

[Snippets — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/extensibility/snippets.html)
[Completions Files — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/reference/completions.html)

### Publishing to Package Control

[Docs - Package Control](https://packagecontrol.io/docs#Package_Developers)
[example-repository.json](https://raw.githubusercontent.com/wbond/package_control/master/example-repository.json)

## My Installed Packages

[Environment Settings - Packages - Package Control](https://packagecontrol.io/packages/Environment Settings)
[Shell Turtlestein - Packages - Package Control](https://packagecontrol.io/packages/Shell Turtlestein)
[SublimeREPL - Packages - Package Control](https://packagecontrol.io/packages/SublimeREPL)

[Turn Sublime Text 3 into a JavaScript IDE | CSS-Tricks](https://css-tricks.com/turn-sublime-text-3-into-a-javascript-ide/)

### Color scheme/Themes

| Package                      | Remark         |
| ---------------------------- | -------------- |
| [Base 16 Color Schemes][]    |
| [Dayle Rees Color Schemes][] |
| [Neon Color Scheme][]        | Using this one |
| [Theme - Cobalt2][]          | Using this one |
| [Theme - Flatland][]         |
| [Theme - Soda][]             |

[color scheme - Labels - Package Control](https://packagecontrol.io/browse/labels/color%20scheme)
[theme - Labels - Package Control](https://packagecontrol.io/browse/labels/theme)

### Syntax/Snippets

| Package                               | Remark                                                                                                                                                                                                                  |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [-AngularJS][]                        |
| [ApplySyntax][]                       |
| [Async Snippets][]                    |
| [Awk][]                               |
| [Babel][]                             | Supports ES6 and React JSX [babel/babel-sublime#293](https://github.com/babel/babel-sublime/issues/293), [SublimeText-Markdown/MarkdownEditing#438](https://github.com/SublimeText-Markdown/MarkdownEditing/issues/438) |
| [Better CoffeeScript][]               |
| [Better JavaScript][]                 |
| [Creole][]                            |
| [C Improved][]                        |
| [Console API Snippets (JavaScript)][] |
| Diagram                               | [Syntax](https://github.com/jvantuyl/sublime_diagram_plugin/tree/master/Syntaxes) only                                                                                                                                  |
| [DocBlockr_Python][]                  |
| [Dockerfile Syntax Highlighting][]    |
| [Dotfiles Syntax Highlighting][]      | Could have added these rules to ApplySyntax or `ShellScript (Bash).sublime-settings`                                                                                                                                    |
| [EJS][]                               |
| [fish-shell][]                        |
| [Gnuplot][]                           |
| [GoSublime][]                         |
| [INI][]                               |
| [JSFormat][]                          | Currently only used for JSON                                                                                                                                                                                            |
| [LSP][]                               | [LSP docs](https://lsp.readthedocs.io/)                                                                                                                                                                                 |
| [Markdown Extended][]                 |
| [MarkdownEditing][]                   | Also includes color scheme and snippets for Markdown                                                                                                                                                                    |
| [Nunjucks Syntax][]                   |
| [nginx][]                             |
| [OpenGL Shading Language (GLSL)][]    |
| [Python Improved][]                   |
| [RAML Syntax Highlighter][]           |
| [Rust Enhanced][]                     |
| [SCSS][]                              |
| [Tmux][]                              |
| [TOML][]                              |

[language syntax - Labels - Package Control](https://packagecontrol.io/browse/labels/language%20syntax)
[snippets - Labels - Package Control](https://packagecontrol.io/browse/labels/snippets)

### Plugins

| Package                   | Remark                                                                                               |
| ------------------------- | ---------------------------------------------------------------------------------------------------- |
| [AdvancedNewFile][]       |
| [AlignTab][]              |
| [AndroidImport][]         |
| [BetterFindBuffer][]      |
| [BracketHighlighter][]    |
| [-C++ Starting Kit][]     |
| [ColorHelper][]           |
| [DataConverter][]         |
| [DocBlockr][]             |
| [EasyMotion][]            |
| [EditorConfig][]          |
| [-Emmet][]                |
| [Filter Lines][]          |
| [Function Name Display][] |
| [GitHub Tools][]          |
| [Keymaps][]               |
| [Move By Symbols][]       |
| [MarkdownTOC][]           |
| [NodeRequirer][]          |
| [-OmniMarkupPreviewer][]  |
| [Open URL][]              | Open URL with <kbd>Ctrl</kbd>+<kbd>U</kbd>                                                           |
| [Origami][]               | Better pane management                                                                               |
| [SideBarEnhancements][]   |
| [StringEncode][]          | Not char encode                                                                                      |
| [StringUtilities][]       |
| [SublimeCodeIntel][]      |
| [SublimeTmpl][]           | BAD: it hijacks key combo                                                                            |
| [SublimeXiki][]           | [E**x**ecutable w**iki**](http://xiki.org/)                                                          |
| [Text Pastry][]           | Useful for creating and modifying selections, see [wiki](https://github.com/duydao/Text-Pastry/wiki) |
| [Terminal][]              |
| [WordHighlight][]         |
| [YAML Nav][]              |

### Plugins development

| Package                   | Remark                                                                   |
| ------------------------- | ------------------------------------------------------------------------ |
| [AAAPackageDev][]         | _THE_ plugin for package development                                     |
| [PackageResourceViewer][] | View files in package without the hassle of extrating `.sublime-package` |
| [ColorSchemeEditor][]     |
| [-SaneSnippets][]         | Define snippets with sane syntax                                         |
| [ScopeHunter][]           | Shows scopes, useful for debugging syntax files                          |

### Linter

| Package                            | Remark                                                                                             |
| ---------------------------------- | -------------------------------------------------------------------------------------------------- |
| [sublack][]                        |
| [SublimeLinter][]                  |
| [SublimeLinter-annotations][]      | Highlights _TODO_, _FIXME_                                                                         |
| [Sublime​Linter-cppcheck][]        |
| [SublimeLinter-csslint][]          |
| [SublimeLinter-html-tidy][]        | This causes [error](https://github.com/SublimeLinter/SublimeLinter-html-tidy/issues/33) in `paths` |
| [Sublime​Linter-contrib-eslint][]  |
| [SublimeLinter-contrib-htmlhint][] |
| [SublimeLinter-javac][]            |
| [SublimeLinter-json][]             |
| [SublimeLinter-luacheck][]         | [Luacheck documentation](http://luacheck.readthedocs.io/en/stable/)                                |
| [SublimeLinter-pyyaml][]           |
| [SublimeLinter-ruby][]             |
| [SublimeLinter-shellcheck][]       |

[SublimeLinter - Labels - Package Control](https://packagecontrol.io/browse/labels/SublimeLinter)

[aaapackagedev]: https://packagecontrol.io/packages/AAAPackageDev
[advancednewfile]: https://packagecontrol.io/packages/AdvancedNewFile
[aligntab]: https://packagecontrol.io/packages/AlignTab
[androidimport]: https://packagecontrol.io/packages/
[-angularjs]: https://packagecontrol.io/packages/AngularJS
[applysyntax]: https://packagecontrol.io/packages/ApplySyntax
[async snippets]: https://packagecontrol.io/packages/Async%20Snippets
[awk]: https://packagecontrol.io/packages/Awk
[babel]: https://packagecontrol.io/packages/Babel
[base 16 color schemes]: https://packagecontrol.io/packages/Base16%20Color%20Schemes
[better coffeescript]: https://packagecontrol.io/packages/Better%20CoffeeScript
[better javascript]: https://packagecontrol.io/packages/Better%20JavaScript
[betterfindbuffer]: https://packagecontrol.io/packages/BetterFindBuffer
[brackethighlighter]: https://packagecontrol.io/packages/BracketHighlighter
[c improved]: https://packagecontrol.io/packages/C%20Improved
[-c++ starting kit]: https://packagecontrol.io/packages/C%2B%2B%20Starting%20Kit
[colorhelper]: https://packagecontrol.io/packages/ColorHelper
[colorschemeeditor]: https://packagecontrol.io/packages/ColorSchemeEditor
[console api snippets (javascript)]: https://packagecontrol.io/packages/Console%20API%20Snippets%20%28JavaScript%29
[creole]: https://packagecontrol.io/packages/Creole
[dataconverter]: https://packagecontrol.io/packages/DataConverter
[dayle rees color schemes]: https://packagecontrol.io/packages/Dayle%20Rees%20Color%20Schemes
[docblockr]: https://packagecontrol.io/packages/DocBlockr
[docblockr_python]: https://packagecontrol.io/packages/DocBlockr_Python
[dockerfile syntax highlighting]: https://packagecontrol.io/packages/Dockerfile%20Syntax%20Highlighting
[dotfiles syntax highlighting]: https://packagecontrol.io/packages/Dotfiles%20Syntax%20Highlighting
[easymotion]: https://packagecontrol.io/packages/EasyMotion
[editorconfig]: https://packagecontrol.io/packages/EditorConfig
[ejs]: https://packagecontrol.io/packages/EJS
[-emmet]: https://packagecontrol.io/packages/Emmet
[filter lines]: https://packagecontrol.io/packages/Filter%20Lines
[fish-shell]: https://packagecontrol.io/packages/fish-shell
[function name display]: https://packagecontrol.io/packages/Function%20Name%20Display
[github tools]: https://packagecontrol.io/packages/Github%20Tools
[gnuplot]: https://packagecontrol.io/packages/Gnuplot
[gosublime]: https://packagecontrol.io/packages/GoSublime
[ini]: https://packagecontrol.io/packages/INI
[jsformat]: https://packagecontrol.io/packages/JSFormat
[keymaps]: https://packagecontrol.io/packages/Keymaps
[lineendings]: https://packagecontrol.io/packages/LineEndings
[lsp]: (https://packagecontrol.io/packages/LSP)
[markdown extended]: https://packagecontrol.io/packages/Markdown%20Extended
[markdownediting]: https://packagecontrol.io/packages/MarkdownEditing
[markdowntoc]: https://packagecontrol.io/packages/MarkdownTOC
[move by symbols]: https://packagecontrol.io/packages/Move%20By%20Symbols
[neon color scheme]: https://packagecontrol.io/packages/Neon%20Color%20Scheme
[nginx]: https://packagecontrol.io/packages/nginx
[noderequirer]: https://packagecontrol.io/packages/NodeRequirer
[nunjucks syntax]: https://packagecontrol.io/packages/Nunjucks%20Syntax
[-omnimarkuppreviewer]: https://packagecontrol.io/packages/OmniMarkupPreviewer
[open url]: https://packagecontrol.io/packages/Open%20URL
[opengl shading language (glsl)]: https://packagecontrol.io/packages/OpenGL%20Shading%20Language%20(GLSL%29
[origami]: https://packagecontrol.io/packages/Origami
[packageresourceviewer]: https://packagecontrol.io/packages/PackageResourceViewer
[python improved]: https://packagecontrol.io/packages/Python%20Improved
[raml syntax highlighter]: https://packagecontrol.io/packages/RAML%20Syntax%20Highlighter
[rust enhanced]: https://packagecontrol.io/packages/Rust%20Enhanced
[-sanesnippets]: htnginxtps://packagecontrol.io/packages/SaneSnippets
[scopehunter]: https://packagecontrol.io/packages/ScopeHunter
[scss]: https://packagecontrol.io/packages/SCSS
[sidebarenhancements]: https://packagecontrol.io/packages/SideBarEnhancements
[stringencode]: https://packagecontrol.io/packages/StringEncode
[stringutilities]: https://packagecontrol.io/packages/StringUtilities
[sublimecodeintel]: https://packagecontrol.io/packages/SublimeCodeIntel
[standardformat]: https://packagecontrol.io/packages/StandardFormat
[sublack]: https://packagecontrol.io/packages/sublack
[sublimelinter-annotations]: https://packagecontrol.io/packages/SublimeLinter-annotations
[sublime​linter-contrib-eslint]: https://packagecontrol.io/packages/SublimeLinter-contrib-eslint
[sublimelinter-contrib-htmlhint]: https://packagecontrol.io/packages/SublimeLinter-contrib-htmlhint
[sublime​linter-cppcheck]: https://packagecontrol.io/packages/SublimeLinter-cppcheck
[sublimelinter-csslint]: https://packagecontrol.io/packages/SublimeLinter-csslint
[sublimelinter-html-tidy]: https://packagecontrol.io/packages/SublimeLinter-html-tidy
[sublimelinter-javac]: https://packagecontrol.io/packages/SublimeLinter-javac
[sublimelinter-json]: https://packagecontrol.io/packages/SublimeLinter-json
[sublimelinter-luacheck]: https://packagecontrol.io/packages/SublimeLinter-luacheck
[sublimelinter-pyyaml]: https://packagecontrol.io/packages/SublimeLinter-pyyaml
[sublimelinter-ruby]: https://packagecontrol.io/packages/SublimeLinter-ruby
[sublimelinter-shellcheck]: https://packagecontrol.io/packages/SublimeLinter-shellcheck
[sublimelinter]: https://packagecontrol.io/packages/SublimeLinter
[sublimetmpl]: https://packagecontrol.io/packages/SublimeTmpl
[sublimexiki]: https://packagecontrol.io/packages/SublimeXiki
[terminal]: https://packagecontrol.io/packages/Terminal
[text pastry]: https://packagecontrol.io/packages/Text%20Pastry
[theme - cobalt2]: https://packagecontrol.io/packages/Theme%20-%20Cobalt2
[theme - flatland]: https://packagecontrol.io/packages/Theme%20-%20Flatland
[theme - soda]: https://packagecontrol.io/packages/Theme%20-%20Soda
[tmux]: https://packagecontrol.io/packages/Tmux
[toml]: https://packagecontrol.io/packages/TOML
[wordhighlight]: https://packagecontrol.io/packages/WordHighlight
[yaml nav]: https://packagecontrol.io/packages/YAML%20Nav
