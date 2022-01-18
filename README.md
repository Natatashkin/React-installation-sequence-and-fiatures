# React-installation-sequence-and-fiatures

1. В папку проекта клонируем репозиторий.
2. Устанавливаем Реакт [доки](https://create-react-app.dev/docs/getting-started/#creating-an-app)
    <pre><code>npx create-react-app .</code></pre>
    
3. откатить версию плагина css <pre><code>npm i -D --save-exact mini-css-extract-plugin@2.4.5</code></pre>

4. ## Настройка pre-commit хуков

### 1 - Установка зависимостей

Установить в проект следующие пакеты.

```bash
npm install --save-dev prettier eslint
```

### 2 - Инициализация lint-staged и husky

Пользователям **MacOS** и **Linux** систем необходимо выполнить в терминале следующую команду. Она установит и настроит `husky` и
`lint-staged` в зависимости от инструментов качества кода из зависимостей
проекта в `package.json`.

```bash
npx mrm lint-staged
```

Пользователям **Windows** необходимо выполнить следующую команду. Она делает тоже самое.

```bash
npx mrm@2 lint-staged
```

### 3 - Интерграция плагинов

Ссылки на документацию по интеграции плагинов в популярные редакторы.

- [Prettier editor integration](https://prettier.io/docs/en/editors.html)
- [ESLint editor integration](https://eslint.org/docs/user-guide/integrations)

### 4 - Настройки VSCode

Для комфортной работы, после установки плагинов, нужно добавить несколько
настроек редактора для автосохранения и форматирования файлов.

```json
{
  "files.autoSave": "onFocusChange",
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```
4. Добавить в проект файл .prettierrc.json

```json
{
  "printWidth": 80,
  "tabWidth": 2,
  "useTabs": false,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "all",
  "bracketSpacing": true,
  "jsxBracketSameLine": false,
  "arrowParens": "avoid",
  "proseWrap": "always"
}
```
5. Сразу же настроить .gitignore. 
<pre><code>
# Compiled binary addons (https://nodejs.org/api/addons.html)
build/Release
build
.husky
.vscode
6
</pre></code>

6. Настроить [Deployment](https://create-react-app.dev/docs/deployment#github-pages) gh-pages
Видео [Репеты](https://drive.google.com/file/d/1EOewQyS7V9SHsUbbycwgTNqB59jwhFnG/view)

7. Кодим
