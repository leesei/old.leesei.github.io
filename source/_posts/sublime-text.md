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

<!-- more -->

## Must Read Docs

[Sublime Text 3 Documentation](http://www.sublimetext.com/docs/3/)
[Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/)

## Project Files

[Projects - Sublime Text 3 Documentation](http://www.sublimetext.com/docs/3/projects.html)
[Sublime Text 2 Project Bliss - Tuts+ Code Tutorial](http://code.tutsplus.com/tutorials/sublime-text-2-project-bliss--net-27256)

```json
{
    "folders":
    [
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
    "settings":
    {
        "tab_size": 8
    },
    "build_systems":
    [
        {
            "name": "List",
            "shell_cmd": "ls -l"
        }
    ]
}
```

```json
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

## Customization after install

[Home · mrmartineau/SublimeTextSetupWiki Wiki](https://github.com/mrmartineau/SublimeTextSetupWiki/wiki)
[Perfect Workflow in Sublime Text 2 - Tuts+ Course](http://code.tutsplus.com/courses/perfect-workflow-in-sublime-text-2) (The full version on Youtube was taken down.)
[Tag Archive for "sublime-text" | Scotch](https://scotch.io/tag/sublime-text)
[Sublime Text Tutorials - YouTube](https://www.youtube.com/playlist?list=PLLnpHn493BHEYF4EX3sAhVG2rTqCvLnsP)
[Sublime Text Packages](https://github.com/SublimeText/)

[Sublimetext commands and shortcuts | ShortcutFoo](https://www.shortcutfoo.com/app/dojos/sublime-text-2-win)

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

Default packages are located at `<Install Directory>/Packages`.

### Package Control

[Package Control - the Sublime Text package manager](https://packagecontrol.io/)

Follow the instruction to install Package Control via Sublime console.

Installed packages (Package Control > Settings - User):
`<DATA>/Packages/User/Package Control.sublime-settings`
> You can do batch install by editing this file and restarting Sublime Text.

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

[Syntax - Sublime Text 3 Documentation](http://www.sublimetext.com/docs/3/syntax.html)
[Syntax Definitions — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/sublime-text-3/extensibility/syntaxdefs.html)
[Syntax Definitions (reference) — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/reference/syntaxdefs.html)
[Syntax Definitions — Sublime Text Help](http://sublimetext.info/docs/en/extensibility/syntaxdefs.html) (deprecated)

[klorenz / SyntaxHighlightTools — Bitbucket](https://bitbucket.org/klorenz/syntaxhighlighttools) has docs on tmPreferences.

[TmTheme Editor Stats](http://tmtheme-editor.herokuapp.com/stats) to see what scopes are being recognized by themes.

[Sublime Forum • View topic - How to highlight a nested scope?](http://www.sublimetext.com/forum/viewtopic.php?p=48270)
[sublime tmlanguage site:www.sublimetext.com - Google Search](https://www.google.com.hk/search?q=sublime+tmlanguage+site:www.sublimetext.com)

Use [Regex101](https://regex101.com/#python) to test the regex (use `gm` flags).
https://regex101.com/r/cX0eW3

### Snippets Development

[Working with Code Snippets in Sublime Text - Hongkiat](http://www.hongkiat.com/blog/sublime-code-snippets/)
[Quickly Insert Text & Code with Sublime Text Snippets :: Scott Granneman](http://www.granneman.com/webdev/editors/sublime-text/top-features-of-sublime-text/quickly-insert-text-and-code-with-sublime-text-snippets/)

[Snippets — Sublime Text Unofficial Documentation](http://docs.sublimetext.info/en/latest/extensibility/snippets.html)

### Publishing to Package Control

[Docs - Package Control](https://packagecontrol.io/docs#Package_Developers)
[example-repository.json](https://raw.githubusercontent.com/wbond/package_control/master/example-repository.json)

## My Installed Packages

### Color scheme/Themes

Package                               | Remark
--------                              | -------
[Base 16 Color Schemes][]             |
[Dayle Rees Color Schemes][]          |
[Neon Color Scheme][]                 | Using this one
[Theme - Flatland][]                  |
[Theme - Soda][]                      |

[color scheme - Labels - Package Control](https://packagecontrol.io/browse/labels/color%20scheme)
[theme - Labels - Package Control](https://packagecontrol.io/browse/labels/theme)

### Syntax/Snippets

Package                               | Remark
--------                              | -------
[-AngularJS][]                        |
[ApplySyntax][]                       |
[Async Snippets][]                    |
[Awk][]                               |
[Babel][]                             | Supports ES6 and React JSX
[Better CoffeeScript][]               |
[Better JavaScript][]                 |
[Creole][]                            |
[C Improved][]                        |
[Console API Snippets (JavaScript)][] |
Diagram                               | [Syntax](https://github.com/jvantuyl/sublime_diagram_plugin/tree/master/Syntaxes) only
[Dotfiles Syntax Highlighting][]      | Could have added these rules to ApplySyntax or `ShellScript (Bash).sublime-settings`
[fish-shell][]                        |
[Gnuplot][]                           |
[GoSublime][]                         |
[INI][]                               |
[JSFormat][]                          |
[SublimeJSCSFormatter][]              |
[MarkdownEditing][]                   | Also includes color scheme and snippets for Markdown
[nginx][]                             |
[OpenGL Shading Language (GLSL)][]    |
[Python Improved][]                   |
[RAML Syntax Highlighter][]           |
[SCSS][]                              |
[Tmux][]                              |

[language syntax - Labels - Package Control](https://packagecontrol.io/browse/labels/language%20syntax)
[snippets - Labels - Package Control](https://packagecontrol.io/browse/labels/snippets)

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
[OmniMarkupPreviewer][]               |
[Open URL][]                          | Open URL with <kbd>Ctrl</kbd>+<kbd>U</kbd>
[Origami][]                           | Better pane management
[SideBarEnhancements][]               |
[StringEncode][]                      | Not char encode
[StringUtilities][]                   |
[SublimeCodeIntel][]                  |
[SublimeTmpl][]                       | BAD: it hijacks key combo
[SublimeXiki][]                       | [E**x**ecutable w**iki**](http://xiki.org/)
[Text Pastry][]                       | Useful for creating and modifying selections, see [wiki](https://github.com/duydao/Text-Pastry/wiki)
[Terminal][]                          |
[WordHighlight][]                     |

### Plugins development

Package                               | Remark
--------                              | -------
[AAAPackageDev][]                     | *THE* plugin for package development
[PackageResourceViewer][]             | View files in package without the hassle of extrating `.sublime-package`
[ColorSchemeEditor][]                 |
[-SaneSnippets][]                     | Define snippets with sane syntax
[ScopeHunter][]                       | Shows scopes, useful for debugging syntax files

### Linter

Package                               | Remark
--------                              | -------
[SublimeLinter][]                     |
[SublimeLinter-annotations][]         | Highlights *TODO*, *FIXME*
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

[SublimeLinter - Labels - Package Control](https://packagecontrol.io/browse/labels/SublimeLinter)

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
[Better CoffeeScript]: https://packagecontrol.io/packages/Better%20CoffeeScript
[Better JavaScript]: https://packagecontrol.io/packages/Better%20JavaScript
[BetterFindBuffer]: https://packagecontrol.io/packages/BetterFindBuffer
[BracketHighlighter]: https://packagecontrol.io/packages/BracketHighlighter
[C Improved]: https://packagecontrol.io/packages/C%20Improved
[-C++ Starting Kit]: https://packagecontrol.io/packages/C%2B%2B%20Starting%20Kit
[ColorSchemeEditor]: https://packagecontrol.io/packages/ColorSchemeEditor
[Console API Snippets (JavaScript)]: https://packagecontrol.io/packages/Console%20API%20Snippets%20(JavaScript)
[Creole]: https://packagecontrol.io/packages/Creole
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
[Gnuplot]: https://packagecontrol.io/packages/Gnuplot
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
[OmniMarkupPreviewer]: https://packagecontrol.io/packages/OmniMarkupPreviewer
[Open URL]: https://packagecontrol.io/packages/Open%20URL
[OpenGL Shading Language (GLSL)]: https://packagecontrol.io/packages/OpenGL%20Shading%20Language%20(GLSL)
[Origami]: https://packagecontrol.io/packages/Origami
[PackageResourceViewer]: https://packagecontrol.io/packages/PackageResourceViewer
[Python Improved]: https://packagecontrol.io/packages/Python%20Improved
[RAML Syntax Highlighter]:https://packagecontrol.io/packages/RAML%20Syntax%20Highlighter
[-SaneSnippets]: htnginxtps://packagecontrol.io/packages/SaneSnippets
[ScopeHunter]: https://packagecontrol.io/packages/ScopeHunter
[SCSS]: https://packagecontrol.io/packages/SCSS
[SideBarEnhancements]: https://packagecontrol.io/packages/SideBarEnhancements
[StringUtilities]: https://packagecontrol.io/packages/StringUtilities
[StringEncode]: https://packagecontrol.io/packages/StringEncode
[SublimeCodeIntel]: https://packagecontrol.io/packages/SublimeCodeIntel
[SublimeJSCSFormatter]: https://packagecontrol.io/packages/JSCS-Formatter
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
[Tmux]: https://packagecontrol.io/packages/Tmux
[WordHighlight]: https://packagecontrol.io/packages/WordHighlight
