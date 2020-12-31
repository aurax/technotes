---
title: Development
tags: Development C++ Delphi Library Books
---

## Search

- [Dev.to](https://dev.to/)
   We're a place where coders share, stay up-to-date and grow their careers.

## Online compilers

- [Ideone](https://ideone.com/)
   is an online compiler and debugging tool which allows you to compile source code and execute it online in more than 60 programming languages. 

## IDE

- [Visual Studio](visualstudio.md)
- [Visual Studio Code](vscode.md)
- [Apache NetBeans](https://netbeans.org/)
  Quickly and easily develop desktop, mobile, and web applications with Java, JavaScript, HTML5, PHP, C/C++ and more.
  Apache NetBeans is free and open source and is governed by the Apache Software Foundation.
- [Embarcadero Dev-C++](https://github.com/Embarcadero/Dev-Cpp)
  A fast, portable, simple, and free C/C++ IDE. Dev C++ has been downloaded over 67796885 times since 2000.
  Embarcadero Dev-C++ is a new and improved fork (sponsored by Embarcadero) of Bloodshed Dev-C++ and Orwell Dev-C++. It is a full-featured Integrated Development Environment (IDE) and code editor for the C/C++ programming language. It uses Mingw port of GCC (GNU Compiler Collection) as its compiler. Embarcadero Dev-C++ can also be used in combination with Cygwin or any other GCC based compiler. Embarcadero Dev-C++ is built using the latest version of Embarcadero Delphi. Embarcadero Dev-C++ has a low memory footprint because it is a native Windows application and does not use Electron.
  - [Download the latest release](https://github.com/Embarcadero/Dev-Cpp/releases)

## Build tools

- [CMake](https://cmake.org/)
  is an extensible, open-source system that manages the build process in an operating system and in a compiler-independent manner. Unlike many cross-platform systems, CMake is designed to be used in conjunction with the native build environment. Simple configuration files placed in each source directory (called CMakeLists.txt files) are used to generate standard build files (e.g., makefiles on Unix and projects/workspaces in Windows MSVC) which are used in the usual way.
- [vcpkg](https://github.com/Microsoft/vcpkg)
  C++ Library Manager for Windows, Linux, and MacOS.

## Debugging

- MSDN: [Measure application performance by analyzing CPU usage](https://docs.microsoft.com/en-us/visualstudio/profiling/beginners-guide-to-performance-profiling?view=vs-2019)
  Find performance issues while you're debugging with the debugger-integrated CPU Usage diagnostic tool. You can also analyze CPU usage without a debugger attached or by targeting a running app.

## Installers

- [issrc](https://github.com/jrsoftware/issrc)
   Inno Setup is a free installer for Windows programs. First introduced in 1997, Inno Setup today rivals and even surpasses many commercial installers in feature set and stability.

## Patterns

- [Entity component system](https://en.wikipedia.org/wiki/Entity_component_system)
  is an architectural pattern that is mostly used in game development. ECS follows the composition over inheritance principle that allows greater flexibility in defining entities where every object in a game's scene is an entity (e.g. enemies, bullets, vehicles, etc.). Every entity consists of one or more components which contains data or state. Therefore, the behavior of an entity can be changed at runtime by systems that add, remove or mutate components. This eliminates the ambiguity problems of deep and wide inheritance hierarchies that are difficult to understand, maintain and extend. Common ECS approaches are highly compatible and often combined with data-oriented design techniques.
- [Data-oriented design](https://en.wikipedia.org/wiki/Data-oriented_design)
  In computing, data-oriented design is a program optimization approach motivated by efficient usage of the CPU cache, used in video game development. The approach is to focus on the data layout, separating and sorting fields according to when they are needed, and to think about transformations of data.

## Books

- [«Типы в языках программирования» Бенджамин Пирс](https://newstar.rinet.ru/~goga/tapl/tapl-toc.html)
- [Free Programming Books](https://github.com/EbookFoundation/free-programming-books)
  This awesome collection contains free programming books, online courses, interactive programming resources, podcasts, and programming playgrounds in many different languages. It has grown to become one of Github’s most popular repositories, with 160,000+ stars, 6000+ commits, 1600+ contributors, and 39,000+ forks.

## Good Practices

### OOP

- [Чем быстрее вы забудете ООП, тем лучше для вас и ваших программ](https://habr.com/ru/post/451982/)
  - Автор оригинала: Dawid Ciężarkiewicz: [The faster you unlearn OOP, the better for you and your software](https://dpc.pw/the-faster-you-unlearn-oop-the-better-for-you-and-your-software)
  "Объектно-ориентированное программирование — чрезвычайно плохая идея, которая могла возникнуть только в Калифорнии."
  Возможно, это только мои ощущения, но объектно-ориентированное программирование кажется стандартной, самой распространённой парадигмой проектирования ПО. Именно его обычно преподают студентам, объясняют в онлайн-туториалах и, по какой-то причине, спонтанно применяют даже тогда, когда не собирались этого делать.

### Clean Code

- "*The proper use of comments is to compensate for our failure to express ourself in code. Note that I used the word failure. I meant it. Comments are always failures.*"
  [Robert C. Martin, Clean Code: A Handbook of Agile Software Craftsmanship](https://www.goodreads.com/quotes/4472522-the-proper-use-of-comments-is-to-compensate-for-our)
- "*Indeed, the ratio of time spent reading versus writing is well over 10 to 1. We are constantly reading old code as part of the effort to write new code. ...[Therefore,] making it easy to read makes it easier to write.*"
  [Robert C. Martin, Clean Code: A Handbook of Agile Software Craftsmanship](https://www.goodreads.com/quotes/835238-indeed-the-ratio-of-time-spent-reading-versus-writing-is)
- [Stop Writing Code Comments](https://blog.usejournal.com/stop-writing-code-comments-28fef5272752)
  The goal of every programmer should be to write code so clean and expressive that code comments are unnecessary. The purpose of every variable, function and class should be implicit in its name and structure.

## CI/CD

- [Buildbot](http://buildbot.net/)
  The Continuous Integration Framework
  [GitHub](https://github.com/buildbot/buildbot)
- [6 best practices for integration testing with continuous integration](https://techbeacon.com/devops/6-best-practices-integration-testing-continuous-integration)

## Testing

- [What is the difference between unit tests and integration tests?](https://www.typemock.com/what-is-the-difference-between-unit-tests-and-integration-tests)
- [Writing Great Unit Tests: Best and Worst Practices](http://blog.stevensanderson.com/2009/08/24/writing-great-unit-tests-best-and-worst-practises/)
  This blog post is aimed at developers with at least a small amount of unit testing experience.
- [Unit Tests, How to Write Testable Code and Why it Matters](https://www.toptal.com/qa/how-to-write-testable-code-and-why-it-matters)
  Unit testing is an essential instrument in the toolbox of any serious software developer. However, it can sometimes be quite difficult to write a good unit test for a particular piece of code. Having difficulty testing their own or someone else’s code, developers often think that their struggles are caused by a lack of some fundamental testing knowledge or secret unit testing techniques.
  
### TDD (Test-Driven Development)

- [Test-driven development and unit testing with examples in C++](http://alexott.net/en/cpp/CppTestingIntro.html)
- [MUC++] Phil Nash - "Test Driven C++"
  We know that testing is important, but writing tests is hard and takes time - and can be demotivating when you want to hack out features.  
  But what if we flipped the whole thing around? It turns out that by writing tests first the dynamic changes in unexpected ways. Testing becomes easier. Adding features becomes easier. The dopamine hit you get from seeing something work becomes more frequent. Time lost to bugs and regressions virtually disappears. You start to get invited to bigger and better parties!  
  Ok, one of those statements is not guaranteed - but the rest are! If you've never tried TDD (perhaps you have heard of it but been skeptical), or maybe had a bad experience in the past, this talk will give you a sound intro to how it works, how you can get started, and what you can expect to achieve.
  - [Part 1](https://youtu.be/MqNqi_OvnXA)
  - [Part 2](https://youtu.be/OZFhRjzaC0o)
  

## Technical Resources

### Memory

- [Computer memory from the ground up (part 1)](https://blog.carlosware.com/2021/01/04/computer-memory-from-the-ground-up-part-1/)
  This is an introductory post about how memory and CPU work together.
- Video: [024. Модель памяти C++ - Андрей Янковский. Jan 22, 2015](https://youtu.be/SIZmLPtcZiE)
  В докладе Андрей расскажет о моделях памяти различных процессоров, о тонкостях реализации неблокирующих алгоритмов и о том, какое отношение всё это имеет к С++.

### Media

## Other

- [Разработчик-«ВЕТЕРАН» / 50 ЛЕТ ОПЫТА в программировании / История Евгения Владимировича Полищука](https://youtu.be/eqsg3Blzmdg)
  история 78го программиста, Евгения Владимировича Полищука, который вот уже более пятидесяти лет несет в себе любовь к программированию и биоинформатике. Через этот выпуск вы узнаете о том, как программировали в 60е, для чего биологам тех времен нужны были системники размером со спортзал и как побеждать на хакатонах в 76 лет. Мы поговорили о языке АЛГОМ, БЭСМ, Днепр-21, НАИРИ-2, СМ-4, Искра, Инф, Алго, Логлане, трансморфозе и даже Боге.
