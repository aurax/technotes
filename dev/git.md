---
title:  Git
tags: Development Tools Git
data: 2021-01-04
---

## Common

- [Useful Git commands](git-useful-commands.md)

## Tools

- [TortoiseGit](https://tortoisegit.org/)
  supports you by regular tasks, such as committing, showing logs, diffing two versions, creating branches and tags, creating patches and so on.
- [Git SCM to Windows](https://gitforwindows.org/)
  focuses on offering a lightweight, native set of tools that bring the full feature set of the Git SCM to Windows while providing appropriate user interfaces for experienced Git users and novices alike.
- [SourceTree](https://sourcetreeapp.com/)
  simplifies how you interact with your Git repositories so you can focus on coding. Visualize and manage your repositories through Sourcetree's simple Git GUI.
- [KDiff3](http://kdiff3.sourceforge.net/)
  is a diff and merge program.

## Learning

- [Learn Git Branching](https://learngitbranching.js.org/)
  Interested in learning Git? Well you've come to the right place! "Learn Git Branching" is the most visual and interactive way to learn Git on the web; you'll be challenged with exciting levels, given step-by-step demonstrations of powerful features, and maybe even have a bit of fun along the way.
- [Руководство пользователя GIT (для версии 1.5.3 и выше)](http://freesource.info/wiki/RuslanHihin/gitusermanual)
  Данное руководство предназначено для чтения тем, кто имеет базовые знания UNIX и навыки работы с командной строкой, но не имеет знания по git.
  В Главе 1 «Репозитории и Ветки» и в Главе 2 «Изучение истории git» объясняется, как получить и изучить проект используя GIT.
  Читая эти главы, Вы узнаете, как собрать и проверить конкретную версию программного проекта, найти регрессии, и т.п.
  Людям, занимающимся актуальной разработкой, также будет полезна Глава 3 «Разработка с Git» и глава 4 «Совместная разработка».
  Дальнейшие главы охватывают более специализированные темы.
- [The entire Pro Git book (2nd Edition 2014)](https://git-scm.com/book/en/v2)
  written by Scott Chacon and Ben Straub and published by Apress ([Russian version](https://git-scm.com/book/ru/v2))
- [Удачная модель ветвления для Git](https://habr.com/en/post/106912/)
- [Про Git на пальцах (для переходящих с SVN)](https://habr.com/en/post/68341/)

## Get settings

```batch
git config --global --list
```

### Clean credential settings

```batch
git config --local credential.helper ""
# or set wincred type
git config --global credential.helper wincred
```

### Configure user name

```batch
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author
```

## .gitconfig

Edit the .gitconfig file:

```batch
git config --global -e
```

Example of the file:

```bash
[user]
    name = XXX
    email = XXX
[credential]
    helper = manager
    #helper = wincred
    #git config --global credential.helper wincred
[core]
    autocrlf = true
[push]
    default = tracking
[branch]
    autosetuprebase = always
[pull]
    rebase = false
```

### Line endings in Git

The key to dealing with line endings is to make sure your configuration is committed to the repository, using .gitattributes. For most people, this is as simple as creating a file named .gitattributes at the root of your repository that contains one line:

```bash
* text=auto
```

With this set, Windows users will have text files converted from Windows style line endings (\r\n) to Unix style line endings (\n) when they’re added to the repository.

### Why not core.autocrlf?

Originally, Git for Windows introduced a different approach for line endings that you may have seen: core.autocrlf. This is a similar approach to the attributes mechanism: the idea is that a Windows user will set a Git configuration option core.autocrlf=true and their line endings will be converted to Unix style line endings when they add files to the repository.

The difference between these two options is subtle, but critical: the .gitattributes is set in the repository, so its shared with everybody. But core.autocrlf is set in the local Git configuration. That means that everybody has to remember to set it, and set it identically.

Source: [Git for Windows: Line Endings](https://www.edwardthomson.com/blog/git_for_windows_line_endings.html)

Additional:

- [VSCode: Resolving Git line ending issues in containers](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files) (resulting in many modified files)
- [Configuring Git to handle line endings](https://help.github.com/en/github/using-git/configuring-git-to-handle-line-endings) (see "git add –renormalize .")

## Git Features

### Git Subtree

- [git subtree tutorial and demo!](https://youtu.be/t3Qhon7burE)
- [subtree-demo-main](https://github.com/robertodr/subtree-demo-main)
  Demo of Git subtrees. Main repository.
- Youtube: [Getting started with Git using SourceTree - Part 1: Version control](https://youtu.be/UD7PV8auGLg)

### Commands

- commit changes in the Subtree

```batch
git subtree push --prefix folder-name/CommonWidgets https://github.com/repo.git master
# predefined
git remote add -f CommonWidgets  https://github.com/repo.git
```

## Update git repos

- create update.cmd file with following content
- put the file to the root folder where the repositories are located

```bat
@echo off

cls

echo. Remove Obj and Bin folders
rem for /d /r . %%d in (bin,obj) do @if exist "%%d" rmdir /s /q "%%d"
for /d /r . %%d in (bin,obj) do @if exist "%%d" rmdir /s /q "%%d"

echo. Refresh repos
for /f "tokens=*" %%d in ('dir /AD /B /ON') do @call :UpdateRepo "%%d"

echo. Done!
goto :EOF

:UpdateRepo [folder]
if %ERRORLEVEL% NEQ 0 exit /B %ERRORLEVEL%
set repo=%~1
echo.
echo.
echo. Repository '%repo%'
cd "%repo%"
rem git checkout master
git reset --hard HEAD~1
git clean -xdf
git pull
cd ..
goto :EOF
```
