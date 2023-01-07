<!--BEGIN HEADER-->
<div id="top" align="center">
  <h1>@autosoft/jest-preset</h1>
  <a href="https://npmjs.com/package/@autosoft/jest-preset">
    <img alt="npm" src="https://img.shields.io/npm/v/@autosoft/jest-preset.svg">
  </a>
  <a href="https://github.com/autosoftoss/jest-preset">
    <img alt="typescript" src="https://img.shields.io/github/languages/top/autosoftoss/jest-preset.svg">
  </a>
</div>

<br />

<blockquote align="center">A base to easily run Jest with SWC.</blockquote>

<br />

_If I should maintain this repo, please ⭐️_
<a href="https://github.com/autosoftoss/jest-preset">
  <img align="right" alt="GitHub stars" src="https://img.shields.io/github/stars/autosoftoss/jest-preset?label=%E2%AD%90%EF%B8%8F&style=social">
</a>

_DM me on [Twitter](https://twitter.com/bconnorwhite) if you have questions or suggestions._
<a href="https://twitter.com/bconnorwhite">
  <img align="right" alt="Twitter Follow" src="https://img.shields.io/twitter/url?label=%40bconnorwhite&style=social&url=https%3A%2F%2Ftwitter.com%2Fbconnorwhite">
</a>

---
<!--END HEADER-->

This package bundles [Jest](https://jestjs.io/) and [SWC](https://swc.rs/) together, providing an fast and easy way to run tests.

It comes preconfigured to work with TypeScript and ESM.

## Installation

```sh
yarn add --dev @autosoft/jest-preset
```

```sh
npm install --save-dev @autosoft/jest-preset
```

```sh
pnpm add --save-dev @autosoft/jest-preset
```

## Usage

In your `package.json` file:

```json
{
  "jest": {
    "preset": "@autosoft/jest-preset"
  }
}
```

### Jest

Now to run jest, run `yarn jest` or `npm run jest`.

## Jest Preset

All tests will need to be in the `test` directory and end with `.test.ts`. Additionally, coverage will be collected from all files in the `source` directory.

```json
{
  "collectCoverage": true,
  "collectCoverageFrom": [
    "source/**/*.ts"
  ],
  "coverageProvider": "v8",
  "coverageReporters": [
    "text"
  ],
  "extensionsToTreatAsEsm": [
    ".ts",
    ".tsx"
  ],
  "moduleNameMapper": {
    "^#(.*)": "$1",
    "^(\\.{1,2}/.*)\\.js$": "$1"
  },
  "testRegex": "test/(.*).test.ts$",
  "transform": {
    "^.+\\.tsx?$": [
      "@swc/jest", {
        "jsc": {
          "target": "es2019"
        }
      }
    ]
  }
}
```

<!--BEGIN FOOTER-->

<br />

<h2 id="dependencies">Dependencies<a href="https://www.npmjs.com/package/@autosoft/jest-preset?activeTab=dependencies"><img align="right" alt="dependencies" src="https://img.shields.io/librariesio/release/npm/@autosoft/jest-preset.svg"></a></h2>

- [@swc/core](https://www.npmjs.com/package/@swc/core): Super-fast alternative for babel
- [@swc/jest](https://www.npmjs.com/package/@swc/jest): swc integration for jest
- [jest](https://www.npmjs.com/package/jest): Delightful JavaScript Testing.

<br />

<h3>Dev Dependencies</h3>

- [jsonlint](https://www.npmjs.com/package/jsonlint): Validate JSON

<br />

<h2 id="license">License <a href="https://opensource.org/licenses/MIT"><img align="right" alt="license" src="https://img.shields.io/npm/l/@autosoft/jest-preset.svg"></a></h2>

[MIT](https://opensource.org/licenses/MIT) - _The MIT License_
<!--END FOOTER-->
