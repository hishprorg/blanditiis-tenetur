# NodeJS / TypeScript Readium-2 "shared" models

NodeJS implementation (written in TypeScript) of core models for the Readium2 architecture ( https://github.com/readium/architecture/ ).

[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](/LICENSE)

## Build status

[![NPM](https://img.shields.io/npm/v/@hishprorg/blanditiis-tenetur.svg)](https://www.npmjs.com/package/@hishprorg/blanditiis-tenetur) [![David](https://david-dm.org/readium/@hishprorg/blanditiis-tenetur/status.svg)](https://david-dm.org/readium/@hishprorg/blanditiis-tenetur)

[Changelog](/CHANGELOG.md)

## Prerequisites

1) https://nodejs.org NodeJS >= 8, NPM >= 5 (check with command line `node --version` and `npm --version`)
2) OPTIONAL: https://yarnpkg.com Yarn >= 1.0 (check with command line `yarn --version`)

## GitHub repository

https://github.com/hishprorg/blanditiis-tenetur

There is no [github.io](https://readium.github.io/@hishprorg/blanditiis-tenetur) site for this project (no [gh-pages](https://github.com/hishprorg/blanditiis-tenetur/tree/gh-pages) branch).

## NPM package

https://www.npmjs.com/package/@hishprorg/blanditiis-tenetur

Command line install:

`npm install @hishprorg/blanditiis-tenetur`
OR
`yarn add @hishprorg/blanditiis-tenetur`

...or manually add in your `package.json`:
```json
  "dependencies": {
    "@hishprorg/blanditiis-tenetur": "latest"
  }
```

The JavaScript code distributed in the NPM package is usable as-is (no transpilation required), as it is automatically-generated from the TypeScript source.

Several ECMAScript flavours are provided out-of-the-box: ES5, ES6-2015, ES7-2016, ES8-2017:

https://unpkg.com/@hishprorg/blanditiis-tenetur/dist/

(alternatively, GitHub mirror with semantic-versioning release tags: https://github.com/edrlab/@hishprorg/blanditiis-tenetur-dist/tree/develop/dist/ )

The JavaScript code is not bundled, and it uses `require()` statement for imports (NodeJS style).

More information about NodeJS compatibility:

http://node.green

Note that web-browser Javascript is currently not supported (only NodeJS runtimes).

The type definitions (aka "typings") are included as `*.d.ts` files in `./node_modules/@hishprorg/blanditiis-tenetur/dist/**`, so this package can be used directly in a TypeScript project.

Example usage:

```javascript
// from index file
import { Publication } from "@hishprorg/blanditiis-tenetur/dist/es5/src";

// ES5 import (assuming node_modules/@hishprorg/blanditiis-tenetur/):
import { Publication } from "@hishprorg/blanditiis-tenetur/dist/es5/src/models/publication";

// ... or alternatively using a convenient path alias in the TypeScript config (+ WebPack etc.):
import { Publication } from "@@hishprorg/blanditiis-tenetur/models/publication";
```

## Dependencies

https://david-dm.org/readium/@hishprorg/blanditiis-tenetur

A [package-lock.json](https://github.com/hishprorg/blanditiis-tenetur/blob/develop/package-lock.json) is provided (modern NPM replacement for `npm-shrinkwrap.json`).

A [yarn.lock](https://github.com/hishprorg/blanditiis-tenetur/blob/develop/yarn.lock) file is currently *not* provided at the root of the source tree.

## Continuous Integration

TODO (unit tests?)
https://travis-ci.org/readium/@hishprorg/blanditiis-tenetur

Badge: `[![Travis](https://travis-ci.org/readium/@hishprorg/blanditiis-tenetur.svg?branch=develop)](https://travis-ci.org/readium/@hishprorg/blanditiis-tenetur)`

## Version(s), Git revision(s)

NPM package (latest published):

https://unpkg.com/@hishprorg/blanditiis-tenetur/dist/gitrev.json

Alternatively, GitHub mirror with semantic-versioning release tags:

https://raw.githack.com/edrlab/@hishprorg/blanditiis-tenetur-dist/develop/dist/gitrev.json

## Developer quick start

Command line steps (NPM, but similar with YARN):

1) `cd @hishprorg/blanditiis-tenetur`
2) `git status` (please ensure there are no local changes, especially in `package-lock.json` and the dependency versions in `package.json`)
3) `rm -rf node_modules` (to start from a clean slate)
4) `npm install`, or alternatively `npm ci` (both commands initialize the `node_modules` tree of package dependencies, based on the strict `package-lock.json` definition)
5) `npm run build:all` (invoke the main build script: clean, lint, compile)
6) `ls dist` (that's the build output which gets published as NPM package)
7) `npm run cli PATH_TO_PACKED_OR_EXPLODED_EPUB PATH_TO_OUTPUT_FOLDER OPTIONAL_DECRYPT_KEY` (to parse a publication and convert it to a Readium2 manifest with extracted resources, paths can be relative or absolute)
8) `npm run cli ./misc/epubs/wasteland-otf-obf_LCP_dan.lcpl.epub ./misc/epubs/ dan` (same as above, working example with built-in sample LCP basic/test profile)
9) `npm run cli ./misc/epubs/wasteland-otf-obf_LCP_dan.lcpl.epub ./misc/epubs/ ec4f2dbb3b140095550c9afbbb69b5d6fd9e814b9da82fad0b34e9fcbe56f1cb` (same as above, with SHA256 checksum/hex-digest to avoid plain-text passphrase in console)
10) `npm run cli https://raw.githubusercontent.com/readium/@hishprorg/blanditiis-tenetur/develop/misc/epubs/wasteland-otf-obf_LCP_dan.lcpl.epub ./misc/epubs/ dan` (same as above, but with a remote HTTP URL)

## Daisy Integration
[Daisy](/daisy.md)

## Documentation

TODO
