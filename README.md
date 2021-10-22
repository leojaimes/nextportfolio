# Status

[![Netlify Status](https://api.netlify.com/api/v1/badges/d4bb6ce0-1650-453c-9400-b1ad07853a63/deploy-status)](https://app.netlify.com/sites/leoportolionext/deploys)


# Generatin favicon

https://realfavicongenerator.net/


# Configurar el linter
npm i eslint -D





## How would you like use ESLint=
npx eslint --init 
esto abre una lista de opciones que al final producen el archivo .eslintrc.js donde esta la configuración.


### Install more packages for Eslint
yarn add eslint-config-prettier  eslint-config-standard  eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-react eslint-plugin-standard  -D


### Revisando errores que encuentra el linter
npx eslint .


### Comando para corregir los problemas de estilo de codigo errores etc
 npx eslint . --fix

 el archivo tiene que estar guardado para que lo arregle


# Editor format on save true settings.json ctrl + shitf + p then settings
   "editor.defaultFormatter": "esbenp.prettier-vscode"
   adicional se debe agregar el  .prettierrc.json


````
{
    "[typescript]": {
        "editor.defaultFormatter": "vscode.typescript-language-features"
    },
    "[javascript]": {
      "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[javascriptreact]": {

        "editor.defaultFormatter": "vscode.typescript-language-features"
    },
    "workbench.iconTheme": "vscode-icons",
    "editor.defaultFormatter": "Angular.ng-template",
    "diffEditor.ignoreTrimWhitespace": false,
    "vsicons.dontShowNewVersionMessage": true,
    "editor.detectIndentation": false,
    "timeline.excludeSources": [
        "git-history"
    ],
    "go.formatTool": "goimports",
    "go.useLanguageServer": true,
    "editor.tabSize": 2,
    "ngschematics.componentTypes": [
    
    ],
    "bracket-pair-colorizer-2.colors": [
      "#fafafa",
      "#9F51B6",
      "#F7C244",
      "#F07850",
      "#9CDD29",
      "#C497D4"
  ],
  "angular.ngdk": "",
  "[dart]": {
    "editor.formatOnSave": true,
    "editor.formatOnType": true,
    "editor.rulers": [
      80
    ],
    "editor.selectionHighlight": false,
    "editor.suggest.snippetsPreventQuickSuggestions": false,
    "editor.suggestSelection": "first",
    "editor.tabCompletion": "onlySnippets",
    "editor.wordBasedSuggestions": false
  },
  "dart.openDevTools": "flutter",
  "editor.suggestSelection": "first",
  "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
  "dart.debugExternalLibraries": true,
  "dart.debugSdkLibraries": false,
  "dart.previewLsp": true,
  "todo-tree.tree.showScanModeButton": false,
  "go.toolsManagement.autoUpdate": true,
  "dart.flutterSdkPaths": [
    "C:\\Users\\Acer\\fvm\\versions"
  ],
  "dart.flutterSdkPath": "D:\\Mike\\peliculas\\.fvm\\flutter_sdk",
  "[html]": {
    "editor.defaultFormatter": "lonefy.vscode-JS-CSS-HTML-formatter"
  }
}
````
# Configuración de eslint:

````
const RULES = {
  OFF: 'off',
  WARN: 'warn',
  ERROR: 'error'
}
module.exports = {
  env: {
    browser: true,
    es2021: true,
    node: true
  },
  extends: [
    'standard',
    'plugin:react/recommended'
  ],
  parserOptions: {
    ecmaFeatures: {
      jsx: true
    },
    ecmaVersion: 13,
    sourceType: 'module'
  },
  plugins: [
    'react'
  ],
  rules: {
    'react/react-in-jsx-scope': RULES.OFF,
    'no-unused-vars': RULES.WARN
  },
  settings: {
    react: {
      version: 'detect'
    }
  }
}

````



# Creando tags

````
git tag "prettier-eslint-config"
git describe --tags
git push origin --tags
````

# Instalar husky

Cuando queremos comitear pasa eslint y prettier en el orden correcto.
````
npx mrm lint-staged
````
Husky sirve para no dejar subir codigo sucio o con errores.
