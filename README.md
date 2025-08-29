# love2d-template

This project is a basic template to start new [LÖVE (Love2D)](https://love2d.org/) projects, pre-configured for use with VSCode.

## Features
- Minimal structure to kickstart a Love2D project
- `.vscode/tasks.json` file to run the project quickly using the `Cmd+Shift+B` (macOS) or `Ctrl+Shift+B` (Windows/Linux) shortcut
- Debugging support with VSCode (see below)
- Extension recommendations to improve the development experience


## Debugging


This template is ready to be debugged directly from VSCode. With the required extensions installed, you can set breakpoints and debug your Love2D project just like any other supported language.

> **Important:** To enable debugging, you must add the following line at the top of your `main.lua` (or your main script):
> ```lua
> require("libs.debugger")
> ```

### How to Debug

1. Make sure you have installed the required extensions listed below.
2. Add `require("libs.debugger")` at the top of your `main.lua`.
3. Open your main Lua file (e.g., `main.lua`).
4. Press `F5` or go to the Run and Debug panel and click "Run and Debug".
5. Select the appropriate debug configuration if prompted (e.g., "Local Lua Debugger: Launch Love2D").
6. The project will start with debugging enabled. You can set breakpoints, inspect variables, and step through your code.



## Required Extensions

To use all features of this template, you must install the following VSCode extensions manually:

- `sumneko.lua` (Lua Language Server)
- `janw.love-launcher` (LÖVE Launcher)
- `tomblind.local-lua-debugger-vscode` (Local Lua Debugger)

You can find these requirements in `.vscode/extensions.json` as well.

## How to Run the Project

1. Make sure you have [LÖVE](https://love2d.org/) installed on your system.
2. Open the project in VSCode.
3. Use the shortcut `Cmd+Shift+B` (macOS) or `Ctrl+Shift+B` (Windows/Linux) to run the project.

### Adjusting `tasks.json` and `launch.json` for Your Operating System

Both `.vscode/tasks.json` and `.vscode/launch.json` are configured for macOS by default. You may need to change the path to the Love2D executable for your operating system.

#### Example: tasks.json (macOS default)
```json
{
  "label": "Run LÖVE",
  "type": "shell",
  "command": "/Applications/love.app/Contents/MacOS/love",
  "args": [
    "${workspaceFolder}"
  ]
}
```

#### Example: launch.json (macOS default)
```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Love",
      "type": "lua-local",
      "request": "launch",
      "program": {
        "command": "/Applications/love.app/Contents/MacOS/love"
      },
      "args": [
        "${workspaceFolder}"
      ],
      "scriptRoots": [
        "${workspaceFolder}"
      ]
    }
  ]
}
```

If you are using **Windows**, change the path in both files to your Love2D executable, for example:
```json
"command": "C:/path/to/love.exe"
```

If you are using **Linux**, change it to:
```json
"command": "/usr/bin/love"
```

After editing, save the files and use the shortcut or F5 to run or debug the project.

## About

This template was created to make it easier to start new Love2D projects, providing a ready-to-use VSCode setup, including tasks and extension recommendations.
