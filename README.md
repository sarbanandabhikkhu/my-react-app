<!-- PROJECT Title -->
<br />
<div align="center">
<img src="src/logo.svg" alt="Line Feed" width="150">
  <a href="https://github.com/learnwithsumit/my-react-app"><h3>React Environment Setup</h3></a>
  </h3>
</div>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [How to run](#how-to-run)
- [Editor Setup](#editor-setup)
  - [Plugins](#plugins)
  - [Settings](#settings)
  - [Set Line Breaks](#set-line-breaks)
- [Linting Setup](#linting-setup)
  - [Install Dev Dependencies](#install-dev-dependencies)
  - [Create Linting Configuration file manually](#create-linting-configuration-file-manually)
- [Contact](#contact)

<!-- HOW TO RUN -->

## How to run

Please follow the below instructions to run this project in your computer:

1. Clone this repository
   ```sh
   git clone https://github.com/learnwithsumit/my-react-app.git
   ```
2. Checkout to branch "setup"
   ```sh
   git checkout setup
   ```
3. Run
   ```sh
   yarn
   // or
   npm
   ```
4. Your app should be available in http://localhost:3000

<!-- Editor Setup -->

## Editor Setup

You can use any editor but as I personally prefer VS Code. I will give some instructions about how I prefer VS code to be setup for React applications.

### Plugins

You need to install the below plugins:

- ESLint by Dirk Baeumer
- Prettier - Code formatter by Prettier
- Dracula Official Theme (optional)

### Settings

Follow the below settings for VS Code -

1. Create a new folder called ".vscode" inside the project root folder
2. Create a new file called "settings.json" inside that folder.
3. Paste the below json in the newly created settings.json file and save the file.

```json
{
  // Theme, Minimap, Breadcrumb
  "workbench.colorTheme": "Dracula",
  "editor.minimap.enabled": false,
  "breadcrumbs.enabled": false,
  // config related to code formatting
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "[javascript]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false,
    "editor.defaultFormatter": null
  },
  "javascript.validate.enable": false, //disable all built-in syntax checking
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true,
    "source.fixAll.tslint": true,
    "source.organizeImports": true
  },
  "eslint.alwaysShowStatus": true,
  // emmet
  "emmet.triggerExpansionOnTab": true,
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  }
}
```

If you followed all previous steps, the theme should change and your editor should be ready.

### Set Line Breaks

Make sure in your VS Code Editor, "LF" is selected as line feed instead of CRLF (Carriage return and line feed). To do that, just click LF/CRLF in bottom right corner of editor, click it and change it to "LF". If you dont do that, you will get errors in my setup.

<img src="https://raw.githubusercontent.com/learnwithsumit/think-in-a-react-way/lesson-3/public/line-feed.jpg" alt="Line Feed" width="700">

## Linting Setup

In order to lint and format your React project automatically according to popular airbnb style guide, I recommend you to follow the instructions below.

### Install Dev Dependencies

```sh
yarn add -D prettier babel-eslint eslint-config-prettier eslint-plugin-prettier
npx install-peerdeps --dev eslint-config-airbnb
// or
npm install -D prettier babel-eslint eslint-config-prettier eslint-plugin-prettier
npx install-peerdeps --dev eslint-config-airbnb
```

or You can also add a new script in the scripts section like below to install everything with a single command:

```json
"lint": "yarn add -D prettier babel-eslint eslint-config-prettier eslint-plugin-prettier && npx install-peerdeps --dev eslint-config-airbnb",
// or
"lint": "npm install -D prettier && npm install -D babel-eslint && npx install-peerdeps --dev eslint-config-airbnb && npm install -D eslint-config-prettier eslint-plugin-prettier"
```

and then simply run the below command in the terminal -

```sh
yarn lint #or 'npm run lint'
```

### Create Linting Configuration file manually

Create a `.eslintrc` file in the project root and enter the below contents:

```json
{
  "extends": [
    "airbnb",
    "airbnb/hooks",
    "eslint:recommended",
    "prettier",
    "plugin:jsx-a11y/recommended"
  ],
  "parser": "babel-eslint",
  "parserOptions": {
    "ecmaVersion": 8
  },
  "env": {
    "browser": true,
    "node": true,
    "es6": true,
    "jest": true
  },
  "rules": {
    "react/react-in-jsx-scope": 0,
    "react-hooks/rules-of-hooks": "error",
    "no-console": 0,
    "react/state-in-constructor": 0,
    "indent": 0,
    "linebreak-style": 0,
    "react/prop-types": 0,
    "jsx-a11y/click-events-have-key-events": 0,
    "react/jsx-filename-extension": [
      1,
      {
        "extensions": [".js", ".jsx"]
      }
    ],
    "prettier/prettier": [
      "error",
      {
        "trailingComma": "es5",
        "singleQuote": true,
        "printWidth": 100,
        "tabWidth": 4,
        "semi": true,
        "endOfLine": "auto"
      }
    ]
  },
  "plugins": ["prettier", "react", "react-hooks"]
}
```

<!-- CONTACT -->

## Contact

[![Facebook-Page][facebook-shield]][facebook-url]
[![Instagram][instagram-shield]][instagram-url]
[![LinkedIn][linkedin-shield]][linkedin-url]
[![Youtube][youtube-shield]][youtube-url]

SarbaNanda Bhikkhu - [sarbanandabhikkhu@gmail.com](mailto:sarbanandabhikkhu@gmail.com)

Project Link: [https://github.com/sarbanandabhikkhu/my-react-app](https://github.com/sarbanandabhikkhu/my-react-app)

Youtube Channel: [https://youtube.com/SarbaNandaBhikkhu](https://youtube.com/SarbaNandaBhikkhu)

<!-- MARKDOWN LINKS & IMAGES -->

[facebook-shield]: https://img.shields.io/badge/-Facebook-black.svg?style=flat-square&logo=facebook&color=555&logoColor=white
[facebook-url]: https://facebook.com/sarbanandabhikkhu
[instagram-shield]: https://img.shields.io/badge/-Instagram-black.svg?style=flat-square&logo=instagram&color=555&logoColor=white
[instagram-url]: https://instagram.com/sarbanandabhikkhu
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/company/sarbanandabhikkhu
[youtube-shield]: https://img.shields.io/badge/-Youtube-black.svg?style=flat-square&logo=youtube&color=555&logoColor=white
[youtube-url]: https://youtube.com/SarbaNandaBhikkhu
