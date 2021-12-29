---
title: Fish notes
categories:
  - app
tags:
  - fish-shell
toc: true
date: 2016-02-18 11:24:30
---

[fish shell](http://fishshell.com/)
[fish - ArchWiki](https://wiki.archlinux.org/index.php/Fish)

[Fish shell cheatsheet](https://devhints.io/fish-shell)

[Fish shell playground | rootnroll](https://rootnroll.com/d/fish-shell/)
[jorgebucaran/awesome-fish: A curated list of packages, prompts, and resources for the fish shell.](https://github.com/jorgebucaran/awesome-fish)
[jorgebucaran/fish-cookbook: Tips and recipes for fish, from shell to plate.](https://github.com/jorgebucaran/fish-cookbook)
[The fish Shell](https://mvolkmann.github.io/fish-article/)
[Fish shell notes](https://sbr.pm/technical/fish.html)
[fish shell scripting manual | developerlife.com](https://developerlife.com/2019/10/31/fish-scripting-manual/)

## Tips and Tricks

[fish for zsh users](https://ludios.org/fish-for-zsh-users/)
[friendly interactive shell - Wikiwand](https://www.wikiwand.com/en/Friendly_interactive_shell#/Bash/fish_translation_table)
`ENV_VAR=x command` is unsupported; use `env ENV_VAR=x` command instead.

[Auto-escape pasted text · Issue #2188 · fish-shell/fish-shell · GitHub](https://github.com/fish-shell/fish-shell/issues/2188) Shift+Ctrl+V
[Add support for bracketed paste · fish-shell/fish-shell@db63be7 · GitHub](https://github.com/fish-shell/fish-shell/commit/db63be790984c20ba3a399e233d33b51c73cf4a1)
[bracketed paste mode](https://cirw.in/blog/bracketed-paste)

[When An Alias Should Actually Be An Abbr | sean henderson](https://www.sean.sh/log/when-an-alias-should-actually-be-an-abbr/)

[Global alias a la ZSH · Issue #1963 · fish-shell/fish-shell](https://github.com/fish-shell/fish-shell/issues/1963)

[Quickly Navigate Through Directory History In Fish Shell - OSTechNix](https://ostechnix.com/quickly-navigate-through-directory-history-in-fish-shell/) `cdh`, `prevd`, `nextd`

## Why Fish

Fish featured on Ars:
[Fish: the friendly interactive shell | Ars Technica](http://arstechnica.com/information-technology/2005/12/linux-20051218/2/)
[The fish shell is awesome - Julia Evans](https://jvns.ca/blog/2017/04/23/the-fish-shell-is-awesome/)
[Why you should give a chance to Fish shell - DEV Community 👩‍💻👨‍💻](https://dev.to/jukben/why-you-should-give-a-chance-to-fish-shell-5a0l)
[FISH (Friendly Interactive Shell) by Bash Boomer - YouTube](https://www.youtube.com/watch?v=C2a7jJTh3kU)
[The Fish Shell](https://flaviocopes.com/fish-shell/)
[Why I'm Hooked on Fish Shell (and How to Set it Up Right)](https://spin.atomicobject.com/2017/05/25/fish-shell-overview/)

History search is simply typing and <kbd>Up</kbd>, no more <kbd>Ctrl</kbd>+<kbd>R</kbd> by default.  
But you can bind manually, see [fzf_key_bindings.fish](fzf_key_bindings.fish) or [halostatue/fish-fzf: FZF Helpers for Fish](https://github.com/halostatue/fish-fzf)

## Fish defaults

[fish-shell/share/functions at master · fish-shell/fish-shell](https://github.com/fish-shell/fish-shell/tree/master/share/functions) `/usr/share/fish/functions`

`/usr/share/fish/`

## Debugging

`fish -d 3 script.fish`

[Debugging — fish-shell documentation](https://fishshell.com/docs/current/index.html#debugging) `breakpoint`
[fish_breakpoint_prompt - define the prompt when stopped at a breakpoint — fish-shell documentation](https://fishshell.com/docs/current/cmds/fish_breakpoint_prompt.html?highlight=breakpoint)

[Add support for fish_trace variable to trace execution by ridiculousfish · Pull Request #6255 · fish-shell/fish-shell](https://github.com/fish-shell/fish-shell/pull/6255) `set fish_trace 1`
[Add a way to toggle debug mode in Fish shell · Issue #3427 · fish-shell/fish-shell](https://github.com/fish-shell/fish-shell/issues/3427)

## History

[history - Show and manipulate command history — fish-shell 3 documentation](https://fishshell.com/docs/current/cmds/history.html)

## Parameter expansion

[Wildcards/globbing — fish-shell documentation](https://fishshell.com/docs/current/index.html#wildcards)

[Command substitution — fish-shell documentation](https://fishshell.com/docs/current/index.html#command-substitution)
`(cmd)`

[Brace expansion — fish-shell documentation](https://fishshell.com/docs/current/index.html#expand-brace)
`cp file{,.bak}` backup `file`

[Variable expansion — fish-shell documentation](https://fishshell.com/docs/current/index.html#expand-variable)

[Index range expansion — fish-shell documentation](https://fishshell.com/docs/current/index.html#expand-index-range)

## Process substitution

`bin2 <(bin1)` becomes `bin2 (bin1 | psub)`

[psub - perform process substitution — fish-shell documentation](https://fishshell.com/docs/current/cmds/psub.html)

[shell - Fish error while trying to run command on mac - Stack Overflow](https://stackoverflow.com/questions/48855508/fish-error-while-trying-to-run-command-on-mac/48855746)

## Functions

[Variable scope — fish-shell documentation](https://fishshell.com/docs/current/index.html#variable-scope)

## Autocomplete

Fish will automatically generate autocompletion from man pages for supported commands, written to `~/.local/share/fish/generated_completions/`.  
Use [`fish_update_completions`](https://github.com/fish-shell/fish-shell/blob/master/share/functions/fish_update_completions.fish) to update.

Fish also includes completion of popular packages, located.

[Tutorial — fish-shell documentation](https://fishshell.com/docs/current/tutorial.html#autosuggestions)
To accept autocompletion, press <kbd>Right</kbd> or <kbd>Ctrl</kbd>+<kbd>F</kbd>  
To accept autocompletion to word boundary, use <kbd>Alt</kbd>+<kbd>Right</kbd> or <kbd>Alt</kbd>+<kbd>R</kbd>

[Writing your own completions — fish-shell documentation](https://fishshell.com/docs/current/index.html#writing-your-own-completions)
[complete - edit command specific tab-completions — fish-shell 3 documentation](https://fishshell.com/docs/current/cmds/complete.html)
[A guide for fish shell completions - Fábio Antunes - Medium](https://medium.com/@fabioantunes/a-guide-for-fish-shell-completions-485ac04ac63c)

[cli/docker.fish at master · docker/cli](https://github.com/docker/cli/blob/master/contrib/completion/fish/docker.fish)
[fish-shell/share/completions at master · fish-shell/fish-shell](https://github.com/fish-shell/fish-shell/tree/master/share/completions) also at `/usr/share/fish/completions`

## Fisher

[jorgebucaran/fisher: A package manager for the fish shell.](https://github.com/jorgebucaran/fisher)
[jethrokuan/fzf: Ef-🐟-ient fish keybindings for fzf](https://github.com/jethrokuan/fzf)
[halostatue/fish-fzf: FZF Helpers for Fish](https://github.com/halostatue/fish-fzf)
[laughedelic/pisces: ♓️ Fish shell plugin that helps you to work with paired symbols in the command line](https://github.com/laughedelic/pisces)

[setomits/venv-fish](https://github.com/setomits/venv-fish)
[virtual environments with python and fish](https://gist.github.com/mrchrisadams/9309736)
[Automatically activate/deactivate virtualenv in fish shell](https://gist.github.com/tommyip/cf9099fa6053e30247e5d0318de2fb9e)

```sh
curl -sL https://git.io/fisher | source && fisher install jorgebucaran/fisher

fisher install jorgebucaran/nvm.fish
fisher install jethrokuan/fzf halostatue/fish-fzf
fisher install laughedelic/pisces
fisher install setomits/venv-fish
```

## oh-my-fish

[oh-my-fish/oh-my-fish: The Fish Shell Framework](https://github.com/oh-my-fish/oh-my-fish)
[packages-main/packages at master · oh-my-fish/packages-main](https://github.com/oh-my-fish/packages-main/tree/master/packages)

## Plugins

[Fuzzy cd for fish shell using fzf](https://gist.github.com/chrisnorris/fe57c7855fd87a2636999edf1d4d735b)
[wting/autojump: A cd command that learns - easily navigate directories from the command line](https://github.com/wting/autojump)
[autojump(macOS) + fzf for fish shell](https://gist.github.com/l4u/06502cf680b9a3817efddfb0a9a6ede8)

[edc/bass: Make Bash utilities usable in Fish shell](https://github.com/edc/bass#nvm)

[jorgebucaran/nvm.fish: Node.js version manager lovingly made for Fish.](https://github.com/jorgebucaran/nvm.fish)
[brigand/fast-nvm-fish: a wrapper around node version manager for fish shell with good performance](https://github.com/brigand/fast-nvm-fish)

[onodera-punpun/neet: A script to easily play and manage your anime/drama/series.](https://github.com/onodera-punpun/neet)

[danhper/fish-ssh-agent](https://github.com/danhper/fish-ssh-agent)

[sjl/z-fish: A fork of http://github.com/rupa/z to port it to the Fish shell.](https://github.com/sjl/z-fish)
