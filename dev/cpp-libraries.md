---
title:  C++ libraries
tags: C++ Library
data: 2021-01-02
---

## C++ libraries

- [C++ Libraries at libraries.io](https://libraries.io/languages/C++)

## WinRT

- [cppwinrt](https://github.com/microsoft/cppwinrt)
  C++/WinRT is an entirely standard C++ language projection for Windows Runtime (WinRT) APIs, implemented as a header-file-based library, and designed to provide you with first-class access to the modern Windows API. With C++/WinRT, you can author and consume Windows Runtime APIs using any standards-compliant C++17 compiler.

## UI

- [Dear ImGui](https://github.com/ocornut/imgui)
  is **a bloat-free graphical user interface library for C++**. It outputs optimized vertex buffers that you can render anytime in your 3D-pipeline enabled application. It is fast, portable, renderer agnostic and self-contained (no external dependencies).  
  Dear ImGui is designed to **enable fast iterations** and to **empower programmers** to **create content creation tools and visualization / debug tools** (as opposed to UI for the average end-user). It favors simplicity and productivity toward this goal, and lacks certain features normally found in more high-level libraries.  
  Dear ImGui is particularly suited to integration in games engine (for tooling), real-time 3D applications, fullscreen applications, embedded applications, or any applications on consoles platforms where operating system features are non-standard.

## Frameworks

- [Folly](https://github.com/facebook/folly)
  (acronymed loosely after Facebook Open Source Library) is a library of C++14 components designed with practicality and efficiency in mind. Folly contains a variety of core library components used extensively at Facebook. In particular, it's often a dependency of Facebook's other open source C++ efforts and place where those projects can share code.

## Strings (UTF-8)

- [utf8proc](https://github.com/JuliaStrings/utf8proc)
  is a small, clean C library that provides Unicode normalization, case-folding, and other operations for data in the UTF-8 encoding.

## JSON

- [JSON-CPP](https://github.com/codewitch-honey-crisis/JSON-CPP)
  A highly efficient JSON processor that can run on constrained memory environments 
  - Codeproject: [JSON by Design: A Walkthrough of a High Performance JSON Processor](https://www.codeproject.com/Articles/5290815/JSON-by-Design-A-Walkthrough-of-a-High-Performance)
    This article is written with an eye toward software design - specifically of an extremely scalable and portable JSON processor.

## Serialization

- [Binn](https://github.com/liteserver/binn)
  is a binary data serialization format designed to be compact, fast and easy to use. The elements are stored with their sizes to increase the read performance. The library uses zero-copy when reading strings, blobs and containers. The strings are null terminated so when read the library returns a pointer to them inside the buffer, avoiding memory allocation and data copying.

## Cryptography

- [Crypto++: free C++ Class Library of Cryptographic Schemes](https://github.com/weidai11/cryptopp)

## Compression

- [Lempel–Ziv–Markov chain algorithm (LZMA, 7-zip)](https://www.7-zip.org/sdk.html)
  The LZMA SDK provides the documentation, samples, header files, libraries, and tools you need to develop applications that use LZMA compression.
  - [wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
- [Zlib](http://zlib.net/)
  A Massively Spiffy Yet Delicately Unobtrusive Compression Library.
  - [GitHub](https://github.com/madler/zlib)
  - [wikipedia](https://en.wikipedia.org/wiki/Zlib)

## Communication

- [eCAL - enhanced Communication Abstraction Layer](https://github.com/continental/ecal)
  is a fast publish-subscribe middleware that can manage inter-process data exchange, as well as inter-host communication.  
  Dependencies:
  - [CMake](https://cmake.org)
  - [Qt5 (>= 5.5)](https://www.qt.io/download)

## Graphics

- [libpng](http://libpng.org/pub/png/libpng.html)
  is the official PNG reference library. It supports almost all PNG features, is extensible, and has been extensively tested for over 23 years. The libpng is available as ANSI C (C89) source code and requires zlib 1.0.4 or later (1.2.5 or later recommended for performance and security reasons).
  - [The home site for development versions](https://libpng.sourceforge.io/)
  - [wikipedia](https://en.wikipedia.org/wiki/Libpng)
- [Diligent Engine](http://diligentgraphics.com/)
  is a lightweight cross-platform graphics API abstraction library. It is designed to take full advantage of Direct3D12, Vulkan and Metal, while supporting older platforms via Direct3D11, OpenGL and OpenGLES. Diligent Engine exposes common front-end API and uses HLSL as universal shading language on all platforms and rendering back-ends. Platform-specific shader representations (GLSL, DX bytecode or SPIRV) can be used with corresponding back-ends. The engine is intended to be used as graphics subsystem in a game engine or any other 3D application.
  - [GitHub](https://github.com/DiligentGraphics/DiligentEngine)
  - [Diligent Core](https://github.com/DiligentGraphics/DiligentCore)
    This module implements Diligent Engine's core functionality: Direct3D11, Direct3D12, OpenGL, OpenGLES, and Vulkan rendering backends as well as basic platform-specific utilities. It is self-contained and can be built by its own. The module's cmake script defines a number of variables that are required to generate build files for other modules, so it must always be handled first.
  - [DiligentSamples](https://github.com/DiligentGraphics/DiligentSamples)
    This module contains tutorials and sample applications intended to demonstrate the usage of Diligent Engine. The module depends on the Core and Tools submodules.
  - Codeproject: [Diligent Engine: A Modern Cross-Platform Low-Level Graphics Library](https://www.codeproject.com/Articles/1216041/Diligent-Engine-A-Modern-Cross-Platform-Low-Level)
    This article introduces Diligent Engine, a modern cross-platform graphics API abstraction library and rendering framework

## Media

- [OpenCV](https://opencv.org/)
  (Open Source Computer Vision) is an open-source library that includes several hundreds of computer vision algorithms.
  - [GitHub](https://github.com/opencv/opencv)
