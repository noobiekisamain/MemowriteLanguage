# Memowrite 📝 THE SOURCE CODE IS OUTDATED!

![Platform - Windows Only](https://img.shields.io/badge/Platform-Windows%20Only-0078D6?style=for-the-badge&logo=windows)
![Language - Python](https://img.shields.io/badge/Language-Python%203.8%2B-3776AB?style=for-the-badge&logo=python)
![IDE - Memowrite Studio](https://img.shields.io/badge/IDE-Memowrite%20Studio-FF6F00?style=for-the-badge)
![Extension - VS Code](https://img.shields.io/badge/VS%20Code-Extension%20Available-007ACC?style=for-the-badge&logo=visualstudiocode)
![Beginner Friendly](https://img.shields.io/badge/beginner-friendly-brightgreen)

**Memowrite** is an expressive, beginner-friendly programming language built on Python[outdated]. It offers a clean, English-like syntax paired with an extensive set of built-in standard libraries for 2D graphics, animation, desktop GUI creation, persistent key-value memory, sound synthesis, and interactive application development.

> ⚠️ **Platform Notice:** Memowrite is built and optimized exclusively for **Windows**. Win32/Windows-specific APIs, launchers (`.exe`), installer configurations, and desktop GUI integrations require a Windows environment.

---

## 📋 Table of Contents

- [Overview & Philosophy](#-overview--philosophy)
- [Key Features](#-key-features)
- [Project Architecture](#-project-architecture)
- [Installation & Setup](#-installation--setup)
  - [Prerequisites](#prerequisites)
  - [Using the Windows Installer](#using-the-windows-installer)
  - [Running from Source](#running-from-source)
- [Language Tour & Syntax](#-language-tour--syntax)
  - [Hello World & Basics](#hello-world--basics)
  - [Variables & Input](#variables--input)
  - [Control Flow & Loops](#control-flow--loops)
  - [Functions](#functions)
  - [Persistent Memory (`File.Memory`)](#persistent-memory-filememory)
- [Built-In Standard Libraries](#-built-in-standard-libraries)
- [Memowrite Studio & Tooling](#-memowrite-studio--tooling)
  - [Memowrite Studio IDE](#memowrite-studio-ide)
  - [VS Code Extension](#vs-code-extension)
- [Included Showcase Examples](#-included-showcase-examples)
- [Building & Packaging](#-building--packaging)
- [License](#-license)

---

## 🌟 Overview & Philosophy

Memowrite aims to bridge the gap between simple scripting languages and full-featured application creation. By providing human-readable keywords alongside immediate visual and persistent state capabilities, developers can prototype games, utilities, and desktop GUI tools without juggling heavy external dependencies.

---

## ⚡ Key Features

- **Readable Syntax**: Clear keywords like `say`, `ask`, `set`, `repeat`, `if`, and `book` make code intuitive and self-documenting.
- **Integrated 2D Graphics Engine**: Direct support for canvas creation, geometric primitive rendering, color manipulation, and animation loops.
- **Built-In GUI Framework**: Construct windows, buttons, input fields, labels, and event listeners directly within Memowrite code.
- **Persistent Key-Value Store (`File.Memory`)**: Seamlessly persist runtime data across sessions with zero configuration database setups.
- **Sound Synthesis**: Audio clips and sound effect synthesis out of the box.
- **Bundled IDE & Extension**: Includes **Memowrite Studio** (a native GUI editor) and a pre-packaged **VS Code Extension** (`memowrite-1.0.0.vsix`) with syntax highlighting and snippet autocompletion.

---

## 🏗️ Project Architecture

```text
memowrite-source/
├── memowrite/                # Core Interpreter & Engine
│   ├── lexer.py              # Lexical Analyzer / Tokenizer
│   ├── parser.py             # AST Construction & Syntax Analysis
│   ├── interpreter.py        # Abstract Syntax Tree Runtime Executor
│   ├── values.py             # Value Types & Environment Definitions
│   ├── errors.py             # Exception Handling & Reporting
│   ├── studio.py             # Memowrite Studio Desktop IDE
│   └── stdlib/               # Standard Libraries
│       ├── builtins.py       # Core primitive functions
│       ├── system.py         # OS, Process & Time utilities
│       ├── colors.py         # Terminal & Canvas styling
│       ├── textplus.py       # String manipulation helpers
│       ├── files.py          # Disk File I/O operations
│       ├── memory.py         # File.Memory persistent store
│       ├── graphics.py       # 2D Canvas & Drawing Engine
│       ├── sound.py          # Audio playback & FX
│       └── gui.py            # Win32/Tkinter GUI framework
├── examples/                 # 25 Complete Example Applications (.mw)
├── launcher/                 # Compiled Windows C Executables
│   ├── memowrite.exe         # CLI Runtime Launcher
│   └── MemowriteStudio.exe   # IDE App Launcher
├── vscode/                   # VS Code Extension Source & .vsix Package
├── installer/                # NSIS Installer Build Scripts (`memowrite.nsi`)
├── branding/                 # Icons (.ico), Logos, and Installer Artwork
└── docs/                     # Language Specs and Documentation
