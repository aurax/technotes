---
title:  WebAssembly
tags: WebAssembly C++ C#
data: 2021-01-04
---

## Solutions

- [Emscripten](https://emscripten.org/)
  is a complete compiler toolchain to WebAssembly, using LLVM, with a special focus on speed, size, and the Web platform.
  Compile your existing projects written in C or C++ — or any language that uses LLVM — to browsers, Node.js, or wasm runtimes.
  - [GitHub: Emscripten: An LLVM-to-WebAssembly Compiler](https://github.com/emscripten-core/emscripten)
- [Cheerp](https://leaningtech.com/pages/cheerp.html)
  is an enterprise-grade C/C++ compiler for the Web. Can compile C/C++ into WebAssembly and JavaScript. Open source, with dual licence (GPLv2 & commercial).
  - Article: [Cheerp 2.6 — compiling C++ to WebAssembly and JavaScript](https://medium.com/leaningtech/cheerp-2-6-compiling-cpp-to-wasm-and-javascript-cea4d2f67466)


## Technical Resources

### Common

- Article and Video links are located [here](dev.md)

## Articles

- [Pre-render Blazor WebAssembly at build time to optimize for search engines](https://swimburger.net/blog/dotnet/pre-render-blazor-webassembly-at-build-time-to-optimize-for-search-engines)
  The output of a published Blazor WebAssembly application consists of static files exclusively. Hence these applications can be hosted on static site hosts like Azure Static Web Apps, GitHub Pages, Firebase Hosting, and more. But just like other single page application (SPA) frameworks, Blazor WASM is not properly indexed by search engines. This makes it very hard to do search engine optimization (SEO).
