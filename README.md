# Customized React + TypeScript + Vite Template

This repository demonstrates some customizations to Vite's React + Typescript template, improving the ESLint configuration and adding Prettier for formatting.

## How To Use

This repo can be used in two ways:

1. As a template, either [creating a new repo from this template](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) on GitHub, or just copying it. After doing so, update the versions of all dependencies; [`npm-check-updates`](https://www.npmjs.com/package/npm-check-updates) is useful for this.
2. Creating a new project with `npm create vite <project name> -- --template react-ts`, then manually applying the customizations from this repository.

## Changes Made

- ESLint is updated to use the new flat config file format for ESLint 9, as well as the current typescript-eslint toolchain.
- Prettier is added and configured for code formatting - see commit [`897f0ad`](https://github.com/DylanSp/vite-react-ts-customized/commit/897f0ad7afcbfc2345296c0be2c31b51f0830969). Prettier has also been run on all files in this repo. This repo doesn't include any settings to run Prettier automatically on saving a file - set that up in your editor of choice.
  - `prettier`, `eslint-config-prettier`, and `eslint-plugin-prettier` are added as `devDependencies` in `package.json`.
  - `eslintPluginPrettierRecommended` is added to the end of the `extends` array in `eslint.config.js`.
  - `"prettier/prettier": "warn"` is added as an ESLint rule in `eslint.config.js`.
  - `.prettierc.cjs` is added with Prettier settings, though this isn't necessary; trailing commas and an increased line length are just my personal preferences.
- The `dev` and `preview` scripts in `package.json` have the `--host` option added, which enables them to work in GitHub Codespaces - see commit [`d81cf0a`](https://github.com/DylanSp/vite-react-ts-customized/commit/d81cf0a6afbc5770219ebefa8c7c4fd5367465a6). I found this solution [in this GitHub issue for Vite](https://github.com/vitejs/vite/discussions/12561).
