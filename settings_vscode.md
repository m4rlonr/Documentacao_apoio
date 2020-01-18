# Configurações do VScode para programar com Vue.Js

1. Abra o VScode e baixe as exteções do Prettier e ESLint

 1. Após baixar as extensões aperte as seguintes teclas:<br>`shift + crtl + o` 
 
2. Apague o que tiver escrito na barra e digite:<br>`>Open settings (json)`

3. Agora cole as seguinte configurações:

        {
        "workbench.colorTheme": "Dracula",
        "editor.fontLigatures": true,
        "editor.formatOnSave": true,
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
        "workbench.iconTheme": "material-icon-theme",
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
