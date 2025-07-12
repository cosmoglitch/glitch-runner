---
sidebar_label: '0. IDE Setup'
id: dsa-vscode-setup
title: VS Code Setup for DSA with C++
slug: /dsa/vscode-setup
description: Step-by-step guide to setting up VS Code to run C++ code with GCC on Windows.
---

> This guide will help you set up **VS Code + GCC** on Windows to begin your DSA journey in C++.

## Install VS Code
Download and install the latest version of Visual Studio Code from the official website:

[https://code.visualstudio.com/](https://code.visualstudio.com/)

Once installed, open VS Code and set up the initial environment.

## Install GCC (MinGW) Compiler

To run and compile C++ files locally, you need to install a compiler like GCC.

1. Go to: [https://sourceforge.net/projects/mingw-w64/](https://sourceforge.net/projects/mingw-w64/)
2. Download the latest version.
3. During installation:
   - Architecture: `x86_64`
   - Threads: `posix`
   - Exception: `seh`
   - Leave the rest to default
4. Install to a location like: `C:\mingw-w64`
5. Add this to your **System PATH**:
