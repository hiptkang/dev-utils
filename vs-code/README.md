# VS Code (Visual Studio Code)

## Workspace settings
- file: ${workspaceFolder}/.vscode/settings.json
- settings menu: File > Preferences > Settings [Ctrl+']
- settings for python virtualenv
```js
{
    "python.envFile": "${workspaceFolder}/.env",
    "python.venvPath": "${env:VIRTUAL_ENV}",
    "python.pythonPath": "${env:VIRTUAL_ENV}/bin/python"
}
```
