# Settings of vscode for programming

 1. Open vscode and type `shift + crtl + o` 
 1. Erase everything I've been writing and write `>Open settings (json)`
 1. Now paste the settings and save
 ```
 {
    "workbench.colorTheme": "Origamid",
    "editor.fontLigatures": true,
    "vetur.format.defaultFormatter.js": "vscode-typescript",
    // "vetur.format.defaultFormatter.html": "js-beautify-html",
    "javascript.format.insertSpaceBeforeFunctionParenthesis": true,
    "eslint.autoFixOnSave": true,
    "eslint.validate": [
        {
            "language": "vue",
            "autoFix": true
        },
        {
            "language": "html",
            "autoFix": true
        },
        {
            "language": "javascript",
            "autoFix": true
        }
    ],
    "editor.suggestSelection": "first",
    "workbench.iconTheme": "vscode-icons",
    "editor.rulers": [
        80,
        120
    ],
    "terminal.integrated.fontSize": 14,
    "breadcrumbs.enabled": true,
    "editor.parameterHints.enabled": false,
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
    },
    "workbench.startupEditor": "newUntitledFile",
    "window.zoomLevel": 0,
    "git.enableSmartCommit": true
}
 ```
