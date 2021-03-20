---
title:  C++
tags: Development C++
---

## Common

- [C++ libraries](cpp-libraries.md)
- [Awesome C++](https://github.com/fffaraz/awesome-cpp)
  A curated list of awesome C++ (or C) frameworks, libraries, resources, and shiny things. Inspired by awesome-... stuff.

## Documentation

- [C++ reference](https://en.cppreference.com/w/)
  C++98, C++03, C++11, C++14, C++17, C++20, C++23

## IDE

- [C/C++ for Visual Studio Code](https://code.visualstudio.com/docs/languages/cpp)
  C/C++ support for Visual Studio Code is provided by a Microsoft C/C++ extension to enable cross-platform C and C++ development on Windows, Linux, and macOS.

## Compilers

- [Intel oneAPI C++ and Fortran compiler](https://www.scivision.dev/intel-oneapi-fortran-install/)
  Intel oneAPI (first official release December 8, 2020) is a cross-platform toolset that covers several languages including C, C++, Fortran and Python. Intel oneAPI replaces Intel Parallel Studio. Intel oneAPI including the Fortran compiler is free-to-use and no login is required to download oneAPI.

## Types

- VS: [Data Type Ranges](https://docs.microsoft.com/en-us/cpp/cpp/data-type-ranges?view=msvc-160)
- VS: [Built-in types (C++)](https://docs.microsoft.com/en-us/cpp/cpp/fundamental-types-cpp?view=msvc-160)

## C++ Features

- [One Trick with Private Names and Function Templates](https://www.cppstories.com/2020/12/private-names-trick/)
- [Обзор новых возможностей С++14: Часть 2](https://habr.com/ru/post/198238/)

## Tips and Tricks

- [Creating a more-modern C++ workshop for my workplace](https://www.reddit.com/r/cpp/comments/kjw4dz/creating_a_moremodern_c_workshop_for_my_workplace/)

## Technical Resources

- Additional article and video links are located [here](index.md)

### Common resources

- [Include What You Use](https://www.fluentcpp.com/2021/01/01/include-what-you-use/)
  include-what-you-use is a clang-based library that reworks the #includes sections of a C++ file, be there a header or a .cpp file.
- Video: [Aug 9, 2017: Много копий было сломано: по значению или по ссылке? — Алексей Салмин](https://youtu.be/4M1MlW0sP0Q)
- [Intro to C++20's Concepts - Hendrik Niemeyer](https://youtu.be/vJEKjv0ST_k)
- [Jan 22, 2015: Некоторые паттерны реализации полиморфного поведения в C++ - Дмитрий Леванов](https://youtu.be/uyQa07d9so4)
  Основываясь на опыте разработки Крипты, Дмитрий рассмотрит средства реализации статического и динамического полиморфизма в C++, а также некоторые их паттерны и антипаттерны.

### Virtual functions

- [The cost of dynamic (virtual calls) vs. static (CRTP) dispatch in C++](https://eli.thegreenplace.net/2013/12/05/the-cost-of-dynamic-virtual-calls-vs-static-crtp-dispatch-in-c/)

### Synchronization mechanisms

- Codeproject: [Synchronization with Visual C++ and the Windows API](https://www.codeproject.com/Articles/5278932/Synchronization-with-Visual-Cplusplus-and-the-Wind)
  This is an article about many of the synchronization mechanisms available to C++ developers creating high performance, scalable, software for the Windows platform. To set things in perspective, we start out by creating a simple I/O completion port based server, receiving 5GB/s sent by one hundred concurrent clients.

### Multithreading

- [006. Многопоточность в С++ – Максим Бусел](https://youtu.be/-TuJP8pUBW0)
  std::thread, std::promise, std::future, std::packaged_task (i.e. future+promise+callable+exception-safe), std::async.
  - передача исключений между потоками: `promise<void> p; p.set_exception(std::current_exception());`

### Logging

- Codeproject: [Dynamic Logging](https://www.codeproject.com/Articles/5290897/Dynamic-Logging)

## Articles and Videos

- [Секретный конструктор std::shared_ptr](https://habr.com/ru/post/263751/)
  У std::shared_ptr есть небольшой секрет: очень полезный конструктор, о котором большинство программистов даже не слышали.
  Это псевдонимный конструктор (aliasing constructor). 
- Youtube: [Михаил Матросов — Спецификаторы, квалификаторы и шаблоны](https://youtu.be/G_jcBrrYPAs)
  В этом докладе Михаил попытается разложить по полочкам всё это многообразие ключевых слов. Вспомним про linkage, storage duration и инстанциации шаблонов (и что изменится с приходом модулей в С++20). Разберёмся, какая связь между template и inline, между static и constexpr. Поймём, зачем нам extern, когда у нас есть inline. И осознаем, как нам потребовалось почти 20 лет, чтобы научиться нормально объявлять константы.
- Youtube: [Полухин Антон | C++17](https://youtu.be/GK9gtIrJaBk)
