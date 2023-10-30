# This is a recommended prettier and eslint configuration for Backend projects (with typescript).

# Create the files
```cmd
$ touch .prettierrc .eslintrc.js
```
Write next code in the `.prettierrc` file.

```json
{
  "trailingComma": "all",
  "tabWidth": 2,
  "singleQuote": false,
  "printWidth": 70,
  "bracketSpacing": true,
  "arrowParens": "always",
  "semi": true,
  "useTabs": false,
  "jsxBracketSameLine": false,
  "endOfLine": "auto",
  "quoteProps": "consistent",
  "bracketSameLine": true
}
```

Write next code in the `.eslintrc.js` file.
```js
module.exports = {
  parser: '@typescript-eslint/parser',
  parserOptions: {
    project: 'tsconfig.json',
    tsconfigRootDir: __dirname,
    sourceType: 'module',
  },
  plugins: ['@typescript-eslint/eslint-plugin'],
  extends: [
    'plugin:@typescript-eslint/recommended',
    'plugin:prettier/recommended',
  ],
  root: true,
  env: {
    node: true,
    jest: true,
  },
  ignorePatterns: ['.eslintrc.js'],
  rules: {
    '@typescript-eslint/interface-name-prefix': 'off',
    '@typescript-eslint/explicit-function-return-type': 'off',
    '@typescript-eslint/explicit-module-boundary-types': 'off',
    '@typescript-eslint/no-explicit-any': 'off',
  },
};

```

# Install the dependencies

> Note: You can use `yarn`, `npm` or `pnpm` to install the dependencies.

```cmd
$ npm i  @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-airbnb-base eslint-config-prettier eslint-plugin-prettier prettier -D
```