# MIEngine Breakpoint Bug Example

This repository demonstrates a bug related to breakpoints in the MIEngine.

## Table of Contents

- [Introduction](#introduction)
- [Setup](#setup)
- [Reproducing the Bug](#reproducing-the-bug)
- [Expected Behavior](#expected-behavior)
- [Actual Behavior](#actual-behavior)

## Introduction

This project showcases a specific bug encountered when using breakpoints in the MIEngine, a component used for debugging in Visual Studio.

## Setup

1. Clone the repository:

```sh
git clone https://github.com/yourusername/MIEngine-breakpoint-bug-example.git
```

2. Open the project in Visual Studio.
3. Set up the environment to build and debug the project using the [Visual Studio Code MinGW setup guide](https://code.visualstudio.com/docs/cpp/config-mingw).
4. Generate the `.vscode` directory for each project. In each `.vscode` directory there should be a launch.json, a tasks.json and a settings.json. Examples of each file can be found in the repo.
5. Build each project.

## Reproducing the Bug

1. Launch a heterogeneous debug session using the provided launch configurations (start with app1 then app2).
2. Set a breakpoint in app1 main.cpp file.
3. Observe the behavior when the breakpoint is hit.
4. Use gdb command `-exec info b` in each projects debug console to observe that breakpoint is being set in each file

## Expected Behavior

The breakpoint should only be set in the app1 main.cpp

## Actual Behavior

The breakpoint is set in app1 main.cpp and app2 main.cpp
