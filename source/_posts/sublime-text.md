title: "Sublime Text"
date: 2015-04-02 14:23:03
categories:
- app
tags:
- settings
- sublime-text
toc: true
---

[Sublime Text: The text editor you'll fall in love with](http://www.sublimetext.com/)

<!-- more -->

## Must Read Docs

[Sublime Text 3 Documentation](http://www.sublimetext.com/docs/3/)
[Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/)

## Customization after install

[Home · mrmartineau/SublimeTextSetupWiki Wiki](https://github.com/mrmartineau/SublimeTextSetupWiki/wiki)
[Perfect Workflow in Sublime Text 2 - Tuts+ Course](http://code.tutsplus.com/courses/perfect-workflow-in-sublime-text-2) (The full version on Youtube was taken down.)
[Sublime Text Packages](https://github.com/SublimeText/)

### Console

Use <kbd>Ctrl</kbd>+<kbd>`</kbd> to enter Sublime's Python console

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

### Package Control

[Package Control - the Sublime Text package manager](https://packagecontrol.io/)

Installed packages (Package Control > Settings - User):
`<DATA>/Packages/User/Package Control.sublime-settings`
> You can do batch install by editing this file and restarting Sublime Text.

## Syntax Development

[Syntax Definitions — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/reference/syntaxdefs.html#compatibility-with-textmate)
[TextMate Manual » Language Grammars](http://manual.macromates.com/en/language_grammars)

XCode's `plutil` is used to generate PLIST from JSON.
```sh
plutil -convert xml1 diagram-tmLanguage.json -o diagram.tmLanguage
# reverse
plutil -convert json Data.plist -o Data.json
```

```sh
# this does not work with json
sudo apt-get install libplist-utils
```

## Snippets Development

[Working with Code Snippets in Sublime Text - Hongkiat](http://www.hongkiat.com/blog/sublime-code-snippets/)
[Quickly Insert Text & Code with Sublime Text Snippets :: Scott Granneman](http://www.granneman.com/webdev/editors/sublime-text/top-features-of-sublime-text/quickly-insert-text-and-code-with-sublime-text-snippets/)

## Plugins Development

[How to Create a Sublime Text 2 Plugin - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/how-to-create-a-sublime-text-2-plugin--net-22685)

## My Installed Packages

### Color scheme/Themes

Package                               | Remark
--------                              | -------
[Base 16 Color Schemes][]             |
[Dayle Rees Color Schemes][]          |
[Neon Color Scheme][]                 | Using this one
[Theme - Flatland][]                  |
[Theme - Soda][]                      |

### Syntax/Snippets

Package                               | Remark
--------                              | -------
[-AngularJS][]                        |
[ApplySyntax][]                       |
[Async Snippets][]                    |
[Awk][]                               |
[Babel][]                             | Supports ES6 and React JSX
[Better JavaScript][]                 |
[C Improved][]                        |
[Console API Snippets (JavaScript)][] |
Diagram                               | [Syntax](https://github.com/jvantuyl/sublime_diagram_plugin/tree/master/Syntaxes) only
[Dotfiles Syntax Highlighting][]      | Could have added these rules to ApplySyntax or `ShellScript (Bash).sublime-settings`
[fish-shell][]                        |
[GoSublime][]                         |
[INI][]                               |
[JSFormat][]                          |
[MarkdownEditing][]                   | Also includes theme and snippet for Markdown
[nginx][]                             |
[OpenGL Shading Language (GLSL)][]    |
[Python Improved][]                   |
[RAML Syntax Highlighter][]           |
[ReactJS][]                           |
[SCSS][]                              |

### Plugins

Package                               | Remark
--------                              | -------
[AdvancedNewFile][]                   |
[Alignment][]                         |
[AndroidImport][]                     |
[BetterFindBuffer][]                  |
[BracketHighlighter][]                |
[-C++ Starting Kit][]                 |
[DataConverter][]                     |
[DocBlockr][]                         |
[EasyMotion][]                        |
[EditorConfig][]                      |
[-Emmet][]                            |
[Filter Lines][]                      |
[Function Name Display][]             |
[Github Tools][]                      |
[Keymaps][]                           |
[Move By Symbols][]                   |
[MarkdownTOC][]                       |
[Open URL][]                          |
[Origami][]                           |
[SideBarEnhancements][]               |
[StringEncode][]                      |
[StringUtilities][]                   |
[SublimeCodeIntel][]                  |
[SublimeTmpl][]                       |
[SublimeXiki][]                       | [E*x*ecutable w*iki*](http://xiki.org/)
[Text Pastry][]                       | Useful for creating and modifying selections, see [wiki](https://github.com/duydao/Text-Pastry/wiki)
[Terminal][]                          |
[WordHighlight][]                     |

### Plugins development

Package                               | Remark
--------                              | -------
[AAAPackageDev][]                     |
[PackageResourceViewer][]             |
[-SaneSnippets][]                     |
[ScopeHunter][]                       | Shows scopes, useful for debugging syntax files

### Linter

Package                               | Remark
--------                              | -------
[SublimeLinter][]                     |
[SublimeLinter-annotations][]         |
[Sublime​Linter-cppcheck][]            |
[SublimeLinter-csslint][]             |
[SublimeLinter-html-tidy][]           |
[SublimeLinter-javac][]               |
[SublimeLinter-jshint][]              |
[SublimeLinter-json][]                |
[SublimeLinter-lua][]                 |
[SublimeLinter-pep8][]                |
[SublimeLinter-ruby][]                |
[SublimeLinter-shellcheck][]          |

[AAAPackageDev]: https://packagecontrol.io/packages/AAAPackageDev
[AdvancedNewFile]: https://packagecontrol.io/packages/AdvancedNewFile
[Alignment]: https://packagecontrol.io/packages/Alignment
[AndroidImport]: https://packagecontrol.io/packages/
[-AngularJS]: https://packagecontrol.io/packages/AngularJS
[ApplySyntax]: https://packagecontrol.io/packages/ApplySyntax
[Async Snippets]: https://packagecontrol.io/packages/Async%20Snippets
[Awk]: https://packagecontrol.io/packages/Awk
[Babel]: https://packagecontrol.io/packages/Babel
[Base 16 Color Schemes]: https://packagecontrol.io/packages/Base16%20Color%20Schemes
[Better JavaScript]: https://packagecontrol.io/packages/Better%20JavaScript
[BetterFindBuffer]: https://packagecontrol.io/packages/BetterFindBuffer
[BracketHighlighter]: https://packagecontrol.io/packages/BracketHighlighter
[C Improved]: https://packagecontrol.io/packages/C%20Improved
[-C++ Starting Kit]: https://packagecontrol.io/packages/C%2B%2B%20Starting%20Kit
[Console API Snippets (JavaScript)]: https://packagecontrol.io/packages/Console%20API%20Snippets%20(JavaScript)
[DataConverter]: https://packagecontrol.io/packages/DataConverter
[Dayle Rees Color Schemes]: https://packagecontrol.io/packages/Dayle%20Rees%20Color%20Schemes
[DocBlockr]: https://packagecontrol.io/packages/DocBlockr
[Dotfiles Syntax Highlighting]: https://packagecontrol.io/packages/Dotfiles%20Syntax%20Highlighting
[EasyMotion]: https://packagecontrol.io/packages/EasyMotion
[EditorConfig]: https://packagecontrol.io/packages/EditorConfig
[-Emmet]: https://packagecontrol.io/packages/Emmet
[Filter Lines]: https://packagecontrol.io/packages/Filter%20Lines
[fish-shell]: https://packagecontrol.io/packages/fish-shell
[Function Name Display]: https://packagecontrol.io/packages/Function%20Name%20Display
[Github Tools]: https://packagecontrol.io/packages/Github%20Tools
[GoSublime]: https://packagecontrol.io/packages/GoSublime
[INI]: https://packagecontrol.io/packages/INI
[JSFormat]: https://packagecontrol.io/packages/JSFormat
[Keymaps]: https://packagecontrol.io/packages/Keymaps
[LineEndings]: https://packagecontrol.io/packages/LineEndings
[MarkdownEditing]: https://packagecontrol.io/packages/MarkdownEditing
[MarkdownTOC]: https://packagecontrol.io/packages/MarkdownTOC
[Move By Symbols]: https://packagecontrol.io/packages/Move%20By%20Symbols
[Neon Color Scheme]: https://packagecontrol.io/packages/Neon%20Color%20Scheme
[nginx]: https://packagecontrol.io/packages/nginx
[Open URL]: https://packagecontrol.io/packages/Open%20URL
[OpenGL Shading Language (GLSL)]: https://packagecontrol.io/packages/OpenGL%20Shading%20Language%20(GLSL)
[Origami]: https://packagecontrol.io/packages/Origami
[PackageResourceViewer]: https://packagecontrol.io/packages/PackageResourceViewer
[Python Improved]: https://packagecontrol.io/packages/Python%20Improved
[RAML Syntax Highlighter]:https://packagecontrol.io/packages/RAML%20Syntax%20Highlighter
[ReactJS]: https://packagecontrol.io/packages/ReactJS
[-SaneSnippets]: htnginxtps://packagecontrol.io/packages/SaneSnippets
[ScopeHunter]: https://packagecontrol.io/packages/ScopeHunter
[SCSS]: https://packagecontrol.io/packages/SCSS
[SideBarEnhancements]: https://packagecontrol.io/packages/SideBarEnhancements
[StringUtilities]: https://packagecontrol.io/packages/StringUtilities
[StringEncode]: https://packagecontrol.io/packages/StringEncode
[SublimeCodeIntel]: https://packagecontrol.io/packages/SublimeCodeIntel
[SublimeLinter]: https://packagecontrol.io/packages/SublimeLinter
[SublimeLinter-annotations]: https://packagecontrol.io/packages/SublimeLinter-annotations
[Sublime​Linter-cppcheck]: https://packagecontrol.io/packages/SublimeLinter-cppcheck
[SublimeLinter-csslint]: https://packagecontrol.io/packages/SublimeLinter-csslint
[SublimeLinter-html-tidy]: https://packagecontrol.io/packages/SublimeLinter-html-tidy
[SublimeLinter-javac]: https://packagecontrol.io/packages/SublimeLinter-javac
[SublimeLinter-jshint]: https://packagecontrol.io/packages/SublimeLinter-jshint
[SublimeLinter-json]: https://packagecontrol.io/packages/SublimeLinter-json
[SublimeLinter-lua]: https://packagecontrol.io/packages/SublimeLinter-lua
[SublimeLinter-pep8]: https://packagecontrol.io/packages/SublimeLinter-pep8
[SublimeLinter-ruby]: https://packagecontrol.io/packages/SublimeLinter-ruby
[SublimeLinter-shellcheck]: https://packagecontrol.io/packages/SublimeLinter-shellcheck
[SublimeTmpl]: https://packagecontrol.io/packages/SublimeTmpl
[SublimeXiki]: https://packagecontrol.io/packages/SublimeXiki
[Terminal]: https://packagecontrol.io/packages/Terminal
[Text Pastry]: https://packagecontrol.io/packages/Text%20Pastry
[Theme - Flatland]: https://packagecontrol.io/packages/Theme%20-%20Flatland
[Theme - Soda]: https://packagecontrol.io/packages/Theme%20-%20Soda
[WordHighlight]: https://packagecontrol.io/packages/WordHighlight
