---
title: Visual Studio Code settings
tags: Development VSCode Plugins
---

## Settings

- [VSCode plugins to be installed](vscode-plugins-install.cmd)

## Common info

- [Integrate with External Tools via Tasks](https://code.visualstudio.com/docs/editor/tasks)
  Lots of tools exist to automate tasks like linting, building, packaging, testing, or deploying software systems. Examples include the TypeScript Compiler, linters like ESLint and TSLint as well as build systems like Make, Ant, Gulp, Jake, Rake, and MSBuild.
- [Command Line Interface (CLI)](https://code.visualstudio.com/docs/editor/command-line)
  Visual Studio Code has a powerful command line interface built-in that lets you control how you launch the editor. You can open files, install extensions, change the display language, and output diagnostics through command-line options (switches).

## Settings

- [User and Workspace Settings](https://code.visualstudio.com/docs/getstarted/settings)
  It is easy to configure Visual Studio Code to your liking through its various settings. Nearly every part of VS Code's editor, user interface, and functional behavior has options you can modify.

The user settings file is located here: `%APPDATA%\Code\User\settings.json`

## Plugins

- [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)
  Synchronize Settings, Snippets, Themes, File Icons, Launch, Keybindings, Workspaces and Extensions Across Multiple Machines Using GitHub Gist.
- [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  All you need to write Markdown (keyboard shortcuts, table of contents, auto preview and more)
- [Markdown Checkboxes](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-checkbox)
- [Shell launcher](https://marketplace.visualstudio.com/items?itemName=Tyriar.shell-launcher)
  Easily launch multiple shell configurations in the terminal
  Type shelllauncher into the search bar. You can then see Shell Launcher: Launch command. Highlight and use any keybinding you like. For example, (Ctrl+Alt+T)
- [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner)
  Run code snippet or code file for multiple languages: C, C++, Java, JavaScript, PHP, Python, Perl, Perl 6, Ruby, Go, Lua, Groovy, PowerShell, BAT/CMD, BASH/SH, F# Script, F# (.NET Core), C# Script, C# (.NET Core), VBScript, TypeScript, CoffeeScript, Scala, Swift, Julia, Crystal, OCaml Script, R, AppleScript, Elixir, Visual Basic .NET, Clojure, Haxe, Objective-C, Rust, Racket, Scheme, AutoHotkey, AutoIt, Kotlin, Dart, Free Pascal, Haskell, Nim, D, Lisp, Kit, V, SCSS, Sass, CUDA, Less, Fortran, and custom command
- [VSAgile](https://marketplace.visualstudio.com/items?itemName=vip20.vscode-agile-board)
  A tool to manage work at personal or organization level through visual representation.

## Save list of VSCode plugins

- [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal)
  In Visual Studio Code, you can open an integrated terminal, initially starting at the root of your workspace. This can be convenient as you don't have to switch windows or alter the state of an existing terminal to perform a quick command-line task.
- [VSCode: Command line extension management](https://code.visualstudio.com/docs/editor/extension-gallery#_command-line-extension-management)
  To make it easier to automate and configure VS Code, it is possible to list, install, and uninstall extensions from the command line.

```powershell
code --list-extensions | % { "call code --force --install-extension $_" }
```

## Useful links

- [awesome-vscode](https://github.com/viatsko/awesome-vscode)
  A curated list of delightful VS Code packages and resources.
- [My favorite Visual Studio Code tips for "how did you do it" kind of people](https://pawelgrzybek.com/my-favourite-visual-studio-code-tips-for-how-did-you-do-it-kind-of-people/)
- VSCode
  - [User and Workspace Settings](https://code.visualstudio.com/docs/getstarted/settings)
    To customize your editor by language, run the global command **Preferences: Configure Language Specific Settings** from the Command Palette (Ctrl+Shift+P) which opens the language picker.
  - [Language Configuration Guide](https://code.visualstudio.com/api/language-extensions/language-configuration-guide)

## Tips and Tricks

- Changing the color of the whitespace indicator
  On the json file accordingly you will need to add (if it's not already there) the next property:

  ```json
  "workbench.colorCustomizations": {
       "editorWhitespace.foreground": "#1e6d9b"
  }
  ```

  The color should be a hex code
- [Visual Studio Code Tips and Tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)
  - Command Palette: Ctrl+Shift+P
  - Quickly open files: Ctrl+P
  - Tip: Type ? to view commands suggestions
  - Open Recent: Ctrl+R - Displays a Quick Pick dropdown with the list from File > Open Recent with recently opened folders and workspaces followed by files
  - Errors and warnings: Ctrl+Shift+M. Quickly jump to errors and warnings in the project. Cycle through errors with F8 or Shift+F8
  - Change language mode: Ctrl+K M.
  - Change your theme: Ctrl+K Ctrl+T
  - Customize your keyboard shortcuts: Ctrl+K Ctrl+S
  - Open User Settings settings.json: Ctrl+,
  - Extensions: Ctrl+Shift+X
  - Integrated Terminal: Ctrl+`
  - Toggle Sidebar: Ctrl+B
  - Toggle Panel: Ctrl+J
  - Zen mode: Ctrl+K Z
  - Side by side editing: Ctrl+\
  - Switch between editors: Ctrl+1, Ctrl+2, Ctrl+3
  - Move to Explorer window: Ctrl+Shift+E
  - Navigation entire history: Ctrl+Tab
    - Navigate back: Alt+Left
    - Navigate forward: Alt+Right

Are you interested in creating your own extension? You can learn how to do this in the [Extension API documentation](https://code.visualstudio.com/api), specifically check out the [documentation on contribution points](https://code.visualstudio.com/api/references/contribution-points).
