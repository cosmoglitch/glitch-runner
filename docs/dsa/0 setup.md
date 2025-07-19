---
sidebar_label: '0. IDE Setup'
id: dsa-vscode-setup
title: VS Code Setup for DSA with C++
slug: /dsa/vscode-setup
description: Step-by-step guide to setting up VS Code to run C++ code with GCC on Windows.
---
# Setting Up VS Code + GCC for C++ on Windows

> This comprehensive guide will help you set up **Visual Studio Code** with the **GCC compiler (MinGW)** on Windows, providing a robust environment for your C++ development, especially for your Data Structures and Algorithms (DSA) journey.

---

## 1. Install Visual Studio Code (VS Code)

Visual Studio Code is a free, open-source, and highly customizable code editor from Microsoft. It's an excellent choice for C++ development due to its rich ecosystem of extensions.

1.  **Download VS Code**: Navigate to the official Visual Studio Code website:
    [https://code.visualstudio.com/](https://code.visualstudio.com/)

    Look for the "Download for Windows" button and click it to download the stable installer.

2.  **Run the Installer**: Once the download is complete, locate the `.exe` installer file (e.g., `VSCodeUserSetup-x.xx.x.exe`) and double-click it to start the installation process.

    * Accept the license agreement.
    * It's generally recommended to keep the default installation path.
    * **Crucially**, on the "Select Additional Tasks" screen, ensure you check the following options for convenience:
        * `Add "Open with Code" action to Windows Explorer file context menu`
        * `Add "Open with Code" action to Windows Explorer directory context menu`
        * `Register Code as an editor for supported file types`
        * `Add to PATH (requires shell restart)` - This is very important as it allows you to launch VS Code from your command line.

3.  **Complete Installation**: Click "Install" and then "Finish" once the setup is complete. VS Code should launch automatically.

4.  **Initial VS Code Setup**: Upon first opening, VS Code will present you with a welcome screen. You can customize themes, synchronize settings, and learn basic shortcuts. Feel free to explore or simply close the welcome tab.

---

## 2. Install GCC (MinGW-w64) Compiler

To compile and run C++ code on Windows, you need a C++ compiler. **GCC (GNU Compiler Collection)** is a widely used and powerful compiler. We'll be using **MinGW-w64**, which provides a Windows port of GCC.

1.  **Download MinGW-w64**: Go to the official MinGW-w64 SourceForge page:
    [https://sourceforge.net/projects/mingw-w64/](https://sourceforge.net/projects/mingw-w64/)

    On this page, locate and click the "Download" button for the latest release. This will download a self-extracting archive (e.g., `mingw-w64-install.exe` or a similar file).

2.  **Run the MinGW-w64 Installer**: Execute the downloaded installer.

3.  **Configuration**: During the installation wizard, you will be prompted for several configuration options. It's crucial to select the correct ones:
    * **Version**: Select the latest stable version available (e.g., `8.1.0`).
    * **Architecture**: Choose `x86_64`. This is for 64-bit systems, which most modern computers are.
    * **Threads**: Select `posix`. This provides better multi-threading support and compatibility.
    * **Exception**: Choose `seh`. This is the Structured Exception Handling model, recommended for 64-bit Windows.
    * **Build revision**: Leave this as default (e.g., `0`).

    Leave the rest of the options to their default values.

4.  **Installation Directory**: When asked for the installation folder, choose a simple, easy-to-remember path, preferably directly on your `C:` drive to avoid issues with spaces or long paths. A good location would be:
    `C:\mingw-w64`

5.  **Complete Installation**: Click "Next" and allow the installer to extract all the necessary files. This might take a few minutes.

---

## 3. Add GCC to Your System PATH

After installing MinGW-w64, you need to add its `bin` directory to your system's `PATH` environment variable. This allows you to run GCC commands (like `g++`) directly from any command prompt or terminal.

1.  **Open System Properties**:
    * Press `Win + R` to open the Run dialog.
    * Type `sysdm.cpl` and press Enter. This will open "System Properties".
    * Alternatively, search for "Edit the system environment variables" in the Windows search bar and click the relevant result.

2.  **Access Environment Variables**: In the "System Properties" window, go to the "Advanced" tab and click on the "Environment Variables..." button.

3.  **Edit Path Variable**:
    * In the "Environment Variables" window, under the "System variables" section (the bottom panel), find the variable named `Path` and select it.
    * Click the "Edit..." button.

4.  **Add MinGW-w64 Bin Path**:
    * In the "Edit environment variable" dialog box, click "New".
    * Type the path to the `bin` directory of your MinGW-w64 installation. If you installed it to `C:\mingw-w64`, the path you need to add is:
        `C:\mingw-w64\mingw64\bin`

        **Important**: Double-check this path. Inside `C:\mingw-w64`, there should be a `mingw64` folder, and inside that, a `bin` folder containing `g++.exe`, `gcc.exe`, etc.

    * Click "OK" on all open dialog boxes (`Edit environment variable`, `Environment Variables`, `System Properties`) to save the changes.

5.  **Verify Installation**:
    * Open a **new** Command Prompt or PowerShell window (close any existing ones first to ensure the new PATH is loaded).
    * Type the following command and press Enter:
        `g++ --version`

    If the installation and PATH setup were successful, you should see output similar to this, indicating the GCC version:

    ```bash
    g++ (MinGW.org GCC Build) 8.1.0
    Copyright (C) 2018 Free Software Foundation, Inc.
    This is free software; see the source for copying conditions.  There is NO
    warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
    ```

    If you get an error like `'g++' is not recognized as an internal or external command`, double-check your PATH setup and the installation directory.

---

## What's Next?

Now that you have VS Code and GCC set up, you're ready to start coding in C++!

* **Install VS Code Extensions**: Open VS Code and search for and install essential extensions like:
    * `C/C++` by Microsoft (provides IntelliSense, debugging, and code Browse)
    * `Code Runner` (allows you to run single C++ files easily)

* **Create Your First C++ Program**:
    1.  Create a new folder for your C++ projects (e.g., `C:\Users\YourName\Documents\CppProjects`).
    2.  Open this folder in VS Code (`File > Open Folder...`).
    3.  Create a new file (e.g., `hello.cpp`) and add a simple C++ program:
        ```cpp
        #include <iostream>

        int main() {
            std::cout << "Hello, DSA Journey!" << std::endl;
            return 0;
        }
        ```
    4.  Use the "Run Code" button (often a triangle icon in the top right, provided by Code Runner) or open the Integrated Terminal (`Terminal > New Terminal`) and compile manually:
        ```bash
        g++ hello.cpp -o hello.exe
        ./hello.exe
        ```

Happy coding on your DSA journey!