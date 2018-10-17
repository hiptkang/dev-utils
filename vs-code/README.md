# VS Code (Visual Studio Code)

## Workspace settings
- file: ${workspaceFolder}/.vscode/settings.json
- settings menu: File > Preferences > Settings [Ctrl+']
- settings for python virtualenv (need to do "export VIRTUAL_ENV='~/.ve-tf'")
```js
{
    "python.envFile": "${workspaceFolder}/.env",
    "python.venvPath": "${env:VIRTUAL_ENV}",
    "python.pythonPath": "${env:VIRTUAL_ENV}/bin/python"
}
```
## Workspace debugging settings
- file: ${workspaceFolder}/.vscode/launch.json
- default launch.json
```js
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File (Integrated Terminal)",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "console": "integratedTerminal"
        },
        {
            "name": "Python: Attach",
            "type": "python",
            "request": "attach",
            "port": 5678,
            "host": "localhost"
        },
        {
            "name": "Python: Module",
            "type": "python",
            "request": "launch",
            "module": "enter-your-module-name-here",
            "console": "integratedTerminal"
        },
        {
            "name": "Python: Django",
            "type": "python",
            "request": "launch",
            "program": "${workspaceFolder}/manage.py",
            "console": "integratedTerminal",
            "args": [
                "runserver",
                "--noreload",
                "--nothreading"
            ],
            "django": true
        },
        {
            "name": "Python: Flask",
            "type": "python",
            "request": "launch",
            "module": "flask",
            "env": {
                "FLASK_APP": "app.py"
            },
            "args": [
                "run",
                "--no-debugger",
                "--no-reload"
            ],
            "jinja": true
        },
        {
            "name": "Python: Current File (External Terminal)",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "console": "externalTerminal"
        }
    ]
}
```
