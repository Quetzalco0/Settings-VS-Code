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
Вот как использовать Prettier в новом проекте. Создайте папку app, и, перейдя в неё, выполните    
следующую команду в командной строке:
```
npm init -y    
```
Благодаря этой команде npm инициализирует новый проект в папке app, создав в ней файл package.json.    
    
Я, в этом материале, буду использовать yarn, но тут можно использовать и npm. Prettier можно    
подключить и к существующему проекту.    
    
Установим пакет prettier в качестве зависимости разработки нашего проекта:    
```
yarn add --dev prettier    
```    
Благодаря этой команде в package.json будет добавлена запись о зависимости разработки, которая    
выглядит так:    
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
Существует три подхода к работе с плохо отформатированным кодом:    
1. Вручную отформатировать этот код.    
    
2. Использовать автоматизированный инструмент.       
    
Я собираюсь выбрать второй вариант. Сейчас в нашем проекте есть соответствующая зависимость, и,    
кроме того, в разделе scripts файла package.json есть запись о Prettier. Понятно, что мы воспользуемся    
для форматирования кода именно этим инструментом. Для того чтобы это сделать, создадим файл    
prettier.config.js в папке app и добавим туда правила для Prettier:    
    
```    
module.exports = {    
  printWidth: 100,    
  singleQuote: true,    
  trailingComma: 'all',    
  bracketSpacing: true,    
  jsxBracketSameLine: false,    
  tabWidth: 4,    
  semi: true,    
};    
```   
    
Разберём эти правила:    
    
-printWidth: 100 — длина строки не должна превышать 100 символов.    
-singleQuote: true — все двойные кавычки будут преобразованы в одинарные. Подробности об    
этом можно почитать в руководстве по стилю от Airbnb. Мне очень нравится это руководство, я    
использую его для повышения качества моего кода.    
-trailingComma: 'all' — обеспечивает наличие запятой после последнего свойства объекта. Вот    
хорошая статья на эту тему.    
-bracketSpacing: true — отвечает за вставку пробелов между телом объекта и фигурными скобками    
в объектных литералах. Если это свойство установлено в true, то объекты, объявленные с    
использованием объектных литералов, будут выглядеть так: { foo: bar }. Если установить его в    
false, то такие конструкции будут выглядеть так: {foo: bar}.    
-jsxBracketSameLine: false — благодаря этому правилу символ > в многострочных JSX-элементах    
будет помещён в последней строке. Вот как выглядит код, если это правило установлено в true:    
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
