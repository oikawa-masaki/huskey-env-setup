# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type aware lint rules:

- Configure the top-level `parserOptions` property like this:

```js
export default {
  // other rules...
  parserOptions: {
    ecmaVersion: "latest",
    sourceType: "module",
    project: ["./tsconfig.json", "./tsconfig.node.json"],
    tsconfigRootDir: __dirname,
  },
};
```

- Replace `plugin:@typescript-eslint/recommended` to `plugin:@typescript-eslint/recommended-type-checked` or `plugin:@typescript-eslint/strict-type-checked`
- Optionally add `plugin:@typescript-eslint/stylistic-type-checked`
- Install [eslint-plugin-react](https://github.com/jsx-eslint/eslint-plugin-react) and add `plugin:react/recommended` & `plugin:react/jsx-runtime` to the `extends` list

## ESlint + Prettier + huskey

- ESlint
  - 構文ルールを決めるために使用されるライブラリ
  - 静的テストの一部
  - コンパイルする前にコードの記述が正しいか、プロジェクトのルールに沿っているのかチェックすることができる
- 本番環境で使用することはないので、開発環境の -D でインストールします。

```shell
% npm i -D eslint

up to date, audited 335 packages in 565ms

101 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

```shell
% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
? How would you like to use ESLint? …
  To check syntax only
❯ To check syntax and find problems
  To check syntax, find problems, and enforce code style

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
? What type of modules does your project use? …
❯ JavaScript modules (import/export)
  CommonJS (require/exports)
  None of these

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
? Which framework does your project use? …
❯ React
  Vue.js
  None of these

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
? Does your project use TypeScript? …
  No
❯ Yes

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · typescript
? Where does your code run? …  (Press <space> to select, <a> to toggle all, <i> to invert selection)
✔ Browser
  Node

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · typescript
✔ Where does your code run? · browser
The config that you've selected requires the following dependencies:

eslint, globals, @eslint/js, typescript-eslint, eslint-plugin-react
? Would you like to install them now? › No / Yes

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · typescript
✔ Where does your code run? · browser
The config that you've selected requires the following dependencies:

eslint, globals, @eslint/js, typescript-eslint, eslint-plugin-react
✔ Would you like to install them now? · No / Yes
? Which package manager do you want to use? …
❯ npm
  yarn
  pnpm
  bun

% npx eslint --init
You can also run this command directly using 'npm init @eslint/config'.
✔ How would you like to use ESLint? · problems
✔ What type of modules does your project use? · esm
✔ Which framework does your project use? · react
✔ Does your project use TypeScript? · typescript
✔ Where does your code run? · browser
The config that you've selected requires the following dependencies:

eslint, globals, @eslint/js, typescript-eslint, eslint-plugin-react
✔ Would you like to install them now? · No / Yes
✔ Which package manager do you want to use? · npm
☕️Installing...

added 61 packages, changed 10 packages, and audited 396 packages in 5s

141 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
Successfully created /Users/oikawa.masaki/dev/udemy/Introduction-to-React-Testing-with-Vitest/vitest-setup-test/eslint.config.js file.
```

## Prettier

- コード整形

```shell
% npm i -D prettier

added 1 package, and audited 397 packages in 543ms

142 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```

- package.json の修正

```json
"scripts": {
    "dev": "vite",
    "build": "tsc && vite build",
    "lint": "eslint src",
    "lint:fix": "eslint --fix src",
    "preview": "vite preview",
    "test": "vitest",
    "format": "prettier --write src"
  },
```

## husky

```shell
% npm i -D husky

added 1 package, and audited 398 packages in 1s

143 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities

% npx husky init
.git can't be found%

```
