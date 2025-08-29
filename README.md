# love2d-template

This project is a basic template to start new [LÖVE (Love2D)](https://love2d.org/) projects, pre-configured for use with VS Code.

## Features
- Minimal structure to kickstart a Love2D project
- `.vscode/tasks.json` file to run the project quickly using the `Cmd+Shift+B` (macOS) or `Ctrl+Shift+B` (Windows/Linux) shortcut
- Extension recommendations to improve the development experience

## How to Run the Project

1. Make sure you have [LÖVE](https://love2d.org/) installed on your system.
2. Open the project in VS Code.
3. Use the shortcut `Cmd+Shift+B` (macOS) or `Ctrl+Shift+B` (Windows/Linux) to run the project.

### Adjusting `tasks.json` for Your Operating System

The `.vscode/tasks.json` file is configured for macOS by default:
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

If you are using **Windows**, change the `command` field to the path of your Love2D executable, for example:
```json
"command": "C:/path/to/love.exe"
```

If you are using **Linux**, change it to:
```json
"command": "/usr/bin/love"
```

Save the file and use the shortcut again to run the project.

## About

This template was created to make it easier to start new Love2D projects, providing a ready-to-use VS Code setup, including tasks and extension recommendations.
