## For Nodejs projects only
### 1. Install packages
```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

```
```
npx install-peerdeps --dev eslint-config-airbnb-base
```
### 2. Create .prettierrc file and put this { }
Because we want default prettier rules

### 3. Create .eslintrc.json file and put below stuff in it.
```
{
  "extends": ["airbnb", "prettier", "plugin:node/recommended"],
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "no-unused-vars": "warn",
    "no-console": "off",
    "func-names": "off",
    "no-process-exit": "off",
    "object-shorthand": "off",
    "class-methods-use-this": "off"
  }
}
``` 

### Reference
* ESLint Rules - https://eslint.org/docs/rules/
* Prettier Options - https://prettier.io/docs/en/options.html
* Airbnb Style Guide - https://github.com/airbnb/javascript


## For Reactjs projects only

### 1. install packages
```
npm i -D eslint eslint-config-prettier eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react eslint-plugin-react-hooks prettier

```
### 2. Create .prettierrc file and put this { }
Because we want default prettier rules

### 3. Create .eslintrc.json file and put below stuff in it.

```
{
  "extends": [
    "eslint:recommended",
    "plugin:import/errors",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "prettier",
    "prettier/react"
  ],
  "rules": {
    "react/prop-types": 0,
    "no-console": 1,
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exhaustive-deps": "warn"
  },
  "plugins": ["react", "import", "jsx-a11y", "react-hooks"],
  "parserOptions": {
    "ecmaVersion": 2018,
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  },
  "settings": {
    "react": {
      "version": "detect"
    }
  }
}
```

