# React TypeScript eslint prettier 環境構築

## アプリの作成

今回は react-typescript というアプリ名で作成した

`npx create-react-app react-typescript --template typescript`

## ESLint 導入

### ライブラリをインストール

`yarn add -D eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser`

### .eslintrc.js を作成

```
{
  "env": {
    "browser": true,
    "node": true,
    "es2021": true
  },
  "extends": [
    "eslint:recommended",
    //    "standard",
    "plugin:react/recommended",
    "prettier"
  ],
  "parserOptions": {
    "ecmaFeatures": {
      "jsx": true
    },
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": ["react"],
  "rules": {
    "react/react-in-jsx-scope": "off"
  }
}

```

## Prettier 導入

### ライブラリをインストール

`yarn add -D prettier eslint-config-prettier eslint-plugin-prettier`

## .prettierrc を作成

```

{
  "printWidth": 120,
  "useTabs": false,
  "semi": true,
  "singleQuote": true,
  "trailingComma": "es5",
  "bracketSpacing": true,
  "jsxBracketSameLine": false
}

```

## 実行

`yarn start`
