---
title: Free Pascal resources
tags: Development Pascal
---

## Common

- [Free Pascal](https://www.freepascal.org/)
- [PascalABC.NET](http://pascalabc.net/)
  это язык программирования Паскаль нового поколения, сочетающий простоту классического языка Паскаль, ряд современных расширений и огромные возможности платформы Microsoft .NET. PascalABC.NET разрабатывается под свободной лицензией LGPLv3 в первую очередь как язык программирования для сферы образования и научных исследований и вбирает в себя лучшее, что предлагают другие современные языки, такие как C#, Kotlin, Python, Haskell и другие. PascalABC.NET включает бесплатную, простую и мощную среду разработки с подсказками по коду, автоформатированием и образцами кода для начинающих.
  - [GitHub](https://github.com/pascalabcnet/pascalabcnet)
- [Lazarus IDE](https://www.lazarus-ide.org/)
  Lazarus is a Delphi compatible cross-platform IDE for Rapid Application Development. It has variety of components ready for use and a graphical form designer to easily create complex graphical user interfaces.
  - [GetLazarus](https://www.getlazarus.org/)

## Environment for VSCode

### Plugins

- [OmniPascal](https://www.omnipascal.com/)
  - [VSCode marketplace]
- old
  - [Pascal](https://marketplace.visualstudio.com/items?itemName=alefragnani.pascal)
    It adds support for the Pascal language and its dialects like Delphi and FreePascal.
  - [Pascal Formatter](https://marketplace.visualstudio.com/items?itemName=alefragnani.pascal-formatter)
    It adds Code Formatters for Pascal language and its dialects like Delphi and FreePascal.
    - [GitHub](https://github.com/alefragnani/vscode-pascal-formatter)
  - Additional 4 tools should be installed for the Pascal plugin:
    - See [Installing and Configuring GNU Global](https://marketplace.visualstudio.com/items?itemName=alefragnani.pascal#installing-and-configuring-gnu-global) section.

## Configure tasks.json VSCode for FPC

```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "type": "shell",
            "label": "PAS build active file",
            "command": "fpc",
            "args": [
                "${file}"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            },
            "problemMatcher": []
        }
    ]
}
```

## Lazarus Tips

Please go to Tools-->Configure Build Lazarus, add to the options "-gw -gl -godwarfsets -gh -gt -Co -Cr -Ci -Sa -va" without the quote, then try to rebuild the IDE, maybe this way you will get more information why the build fails. 

You missed the -va in the end. It will force the IDE to show everything, which sometimes helps.

