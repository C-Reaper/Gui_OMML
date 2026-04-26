# Project README

## Overview
This project is a C application that demonstrates the backup options for data on a PC, using multiple methods such as USB debugging, Mi Cloud Backup, and ADB. The application supports different platforms including Linux, Windows, Wine, and WebAssembly.

## Features
- Supports USB debugging to transfer files directly from devices.
- Offers backup through Mi Cloud.
- Utilizes ADB (Android Debug Bridge) for backups on Android devices.
- Built using C/C++ with support for multiple operating systems.

## Project Structure
```
<Project>/
├── build/              # .exe and binary files produced by Main.c
├── bin/                # Shared objects (.so) or dynamic link libraries (.dll) produced by *.c in libs
├── libs/               # Source code for *.c files in bin
├── lib/                # Custom language libraries
├── code/               # Scripts from custom languages like .rex, .ll, and .omml
├── data/               # Data files such as .txt or dumped files
├── assets/             # Images and sound files
├── src/                # Source code
│   ├── Main.c          # Entry point file
│   └── *.h             # Standalone Header-based C-files without *.c implementations
├── Makefile.linux      # Linux build configuration
├── Makefile.windows    # Windows build configuration
├── Makefile.wine       # Wine build configuration for cross-compiling to Windows on Linux
├── Makefile.web        # Emscripten build configuration for WebAssembly
└── README.md           # This file
└── LICENSE
└── .gitignore
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC, Clang)
- Make utility
- Standard development tools
- Libraries needed in specific projects: X11 for Linux, user32, gdi32, winmm for Windows

## Build & Run
To build the project on a Linux system:
```sh
cd <Project>
make -f Makefile.linux all
```

For clean rebuild:
```sh
make -f Makefile.linux clean
make -f Makefile.linux all
```

For executing the built application:
```sh
make -f Makefile.linux exe
```

For Windows, use the following commands:
```sh
cd <Project>
make -f Makefile.windows all
make -f Makefile.windows exe
```

For Wine (cross-compiling to Windows):
```sh
cd <Project>
make -f Makefile.wine all
make -f Makefile.wine exe
```

For WebAssembly:
```sh
cd <Project>
make -f Makefile.web all
make -f Makefile.web exe
```

The project includes multiple makefiles tailored for different platforms, ensuring compatibility and ease of use across various environments.