# Toptal REST series

<<<<<<< HEAD
[![Maintainability](https://api.codeclimate.com/v1/badges/966e204fd4b23815ceb9/maintainability)](https://codeclimate.com/github/makinhs/toptal-rest-series/maintainability)

A project made for the free _Building a Node.js/TypeScript REST API_ series at the Toptal Engineering Blog:

- [Part 1: Express.js](https://www.toptal.com/express-js/nodejs-typescript-rest-api-pt-1) &rarr; [source tree](https://github.com/makinhs/toptal-rest-series/tree/toptal-article-01)
- [Part 2: Models, Middleware, and Services](https://www.toptal.com/express-js/nodejs-typescript-rest-api-pt-2) &rarr; [source tree](https://github.com/makinhs/toptal-rest-series/tree/toptal-article-02)
- [Part 3: MongoDB, Authentication, and Automated Tests](https://www.toptal.com/express-js/nodejs-typescript-rest-api-pt-3) &rarr; [source tree](https://github.com/makinhs/toptal-rest-series/tree/toptal-article-03)

Visit https://www.toptal.com/blog and subscribe to our newsletter to read great articles!

# Quick Start Guide

To run the cloned codebase directly, you need to have Node.js and Docker installed.

1. Run `npm i` to install dependencies.
2. Run `sudo docker-compose up -d` to get a MongoDB instance running.
3. Make your own `.env` file in the project root, following the key name but not value used in [`.env.example`](https://github.com/makinhs/toptal-rest-series/blob/toptal-article-03/.env.example).
4. From there, any the following should work:
  - `npm run test`
  - `npm run test-debug`
  - `npm start`
  - `npm run debug`
=======
A project made for the free _Building a Node.js/TypeScript REST API_ series at the Toptal Engineering Blog.

This branch contains some setup for linting and prettifying code that is outside the scope of the series.

In addition to the inclusion of `.eslintrc.json` and `.prettierrc` files, some development dependencies were added to `package.json`, namely `@typescript-eslint/eslint-plugin eslint-plugin-mocha eslint-plugin-prettier eslint-config-prettier`.

You likely have to `npm i -g prettier` as well.

From here (after running `npm i`) there are two things you can do.

## One-time Prettification

For this, you can go to the project root, and run:

``` sh
find . -name '*.js' -or -name '*.ts' | grep -v .history | grep -v dist | grep -v node_modules | xargs prettier --write --single-quote
```

## Continuous Prettification and Linting

In this scenario, whenever you save a file in VSCode (or VSCodium) that you were working on, it automatically runs Prettier and ESLint on it.

To set it up, find your `settings.json` file (e.g., `~/.config/VSCodium/User/settings.json`) and add these lines to it:

``` json
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
  "eslint.validate": ["typescript", "javascript"]
```

With that, try making some changes to the project, like adding a line `const neverused    =1;`.  If all went well, Prettier will reformat your code for you, and ESLint will generate warnings in the Problems pane about the unused variable `neverused`.
>>>>>>> origin/toptal-extra-features

## Bonus: Prettification and Linting

Be sure to check the README and relevant files of the [extra features](https://github.com/makinhs/toptal-rest-series/tree/toptal-extra-features) branch for help on setting up Prettier and ESLint the same way they're used in this project.
