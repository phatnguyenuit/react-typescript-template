# React Typescript Template

## Boostraped by [create-react-app](https://www.npmjs.com/package/create-react-app)

## Features

- [x] Support absolute imports by using baseUrl in tsconfig.json
- [x] Integrate Prettier to reformat code styles
- [x] Configure ESlint with airbnb and supports: Typescript, React, React-Hooks, Prettier, Imports.
- [x] Configure lint-stage and husky to use pre-commit hook to prevent bad style code pushed to GitHub

## Guides

- Copy dot files and tsconfig.json.
- Install devDependencies packages: `npm install --save-dev eslint @typescript-eslint/eslint-plugin eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks husky lint-staged prettier`
- Add new scripts:

  ```json
  "prettier": "prettier --write src/**/*.{ts,tsx}",
  "lint-staged": "lint-staged",
  "lint:ts": "eslint ./src --ext .ts,.tsx",
  "lint:ts:fix": "npm run lint:ts -- --fix"
  ```

- Add package.json options:

  ```json
  "lint-staged": {
    "src/**/*.{ts,tsx}": [ "eslint . --fix", "git add" ]
  },
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  }
  ```
