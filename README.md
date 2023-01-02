<div align="center">
  <h1>@autosoft/jest-preset</h1>
  <a href="https://npmjs.com/package/autosoft/jest-preset">
    <img alt="npm" src="https://img.shields.io/npm/v/@autosoft/jest-preset.svg">
  </a>
  <a href="https://github.com/autosoftoss/jest-preset">
    <img alt="typescript" src="https://img.shields.io/github/languages/top/autosoftoss/jest-preset.svg">
  </a>
</div>

<br />

<blockquote align="center">A base to easily run Jest with SWC.</blockquote>

---

This package bundles [Jest](https://jestjs.io/) and [SWC](https://swc.rs/) together, providing an fast and easy way to run tests.

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
  ...,
  "jest": {
    "preset": "@autosoft/jest-preset"
  }
}
```

Now to run jest, just run `yarn jest` or `npm run jest`.

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
  "testRegex": "test/(.*).test.ts$",
  "transform": {
    "^.+\\.tsx?$": [
      "@swc/jest"
    ]
  }
}
```

<br />

<h2 id="dependencies">Dependencies<a href="https://www.npmjs.com/package/autosoft/jest-preset?activeTab=dependencies"><img align="right" alt="dependencies" src="https://img.shields.io/librariesio/release/npm/@autosoft/jest-preset.svg"></a></h2>

- [@swc/core](https://www.npmjs.com/package/@swc/core): Super-fast alternative for babel
- [@swc/jest](https://www.npmjs.com/package/@swc/jest): Swc integration for jest
- [jest](https://www.npmjs.com/package/jest): Delightful JavaScript Testing.

<br />


<h2 id="license">License <a href="https://opensource.org/licenses/MIT"><img align="right" alt="license" src="https://img.shields.io/npm/l/@autosoft/jest-preset.svg"></a></h2>

[MIT](https://opensource.org/licenses/MIT)
