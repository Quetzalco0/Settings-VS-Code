## EXTENSIONS 
:wrench:**Auto Close Tag**    
:wrench:**Auto Comoplete Tag**    
:wrench:**Auto Rename Tag**    
:wrench:**BEM Helper**    
:wrench:**Better Comments**    
:wrench:**Bracket Pair Colorizer**    
:wrench:**CSS Navigation**    
:wrench:**eCSStractor for VSCode**    
:wrench:**ES7 React/Redux/GraphQL/React-Native snippets**    
:wrench:**ESLint**    
:wrench:**Image preview**    
:wrench:**Live Server**    
:wrench:**Material Icon Theme**    
:wrench:**One Dark Pro**    
:wrench:**Prettier - Code formatter**    
:wrench:**Russian Language Pack for Visual Studio Code**    
:wrench:**SCSS Formatter**    
:wrench:**SCSS IntelliSense**    
:wrench:**Settings Sync**    
:wrench:**Vscode Google Translate**    
:wrench:**Debugger for Chrome**    
:wrench:**indent-rainbow**   
:wrench:**project manager**   
 ## Settings.json
 ```
{    
  "workbench.colorTheme": "One Dark Pro",    
  "workbench.iconTheme": "material-icon-theme",    
  "workbench.startupEditor": "newUntitledFile",    
  "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",    
  "git.autofetch": true,    
  "files.autoSave": "afterDelay",    
  "editor.tabSize": 4,    
  "editor.insertSpaces": false,    
  "editor.detectIndentation": false,    
  "editor.mouseWheelZoom": true,    
  "liveServer.settings.donotShowInfoMsg": true,    
  "vscodeGoogleTranslate.preferredLanguage": "Russian",    
  "editor.codeActionsOnSave": {    
    "source.fixAll.eslint": true    
  },    
  "editor.formatOnSave": true,    
  "sync.gist": "2f66c987318eb6d61b8a9fb1e6b5d9d7"    
}    
```
***
## Настройка Prettier

**npm init -y**    
**yarn add --dev prettier**    
```
{    
  "name": "react-boiler-plate",    
  "version": "1.0.0",    
  "description": "A react boiler plate",    
  "main": "src/index.js",    
  "author": "Adeel Imran",    
  "license": "MIT",    
  "scripts": {    
    __"prettier": "prettier --write src/**/*.js"__   
  },    
  "devDependencies": {    
    "prettier": "^1.14.3"    
  }    
}    
```
***
**Файл: prettier.config.js**
```
module.exports = {    
  printWidth: 100,    
  singleQuote: true,    
  trailingComma: 'all',    
  bracketSpacing: true,    
  jsxBracketSameLine: false,    
  tabWidth: 2,    
  semi: true,    
};    
```
