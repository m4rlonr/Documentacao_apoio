# Configurações do VScode para programar com Vue.Js

1.  Abra o VScode e baixe as exteções do Prettier e ESLint

1.  Após baixar as extensões aperte as seguintes teclas:<br>`shift + crtl + o`

1.  Apague o que tiver escrito na barra e digite:<br>`>Open settings (json)`

1.  Agora cole as seguinte configurações:

        {
        //Configurações Marlon
        "workbench.colorTheme": "Dracula",
        "editor.fontFamily": "Fira Code",
        "editor.fontSize": 14,
        "editor.suggestSelection": "first",
        "workbench.iconTheme": "material-icon-theme",
        "editor.fontLigatures": true,
        //
        //Configurações para trabalhar com VueJs
        "editor.formatOnSave": true,
        "vetur.format.defaultFormatter.js": "vscode-typescript",
        // "vetur.format.defaultFormatter.html": "js-beautify-html",
        "javascript.format.insertSpaceBeforeFunctionParenthesis": true,
        "eslint.autoFixOnSave": false,
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
        "editor.rulers": [
          80,
          120
        ],
        "terminal.integrated.fontSize": 14,
        "breadcrumbs.enabled": true,
        "editor.parameterHints.enabled": false,
        "editor.codeActionsOnSave": {
          "source.fixAll.eslint": false
        },
        "workbench.startupEditor": "newUntitledFile",
        "window.zoomLevel": 0,
        "git.enableSmartCommit": true
        }
