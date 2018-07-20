# bsc

[![npm](https://img.shields.io/npm/v/bsc.svg?style=flat-square)](https://www.npmjs.com/package/bsc) [![tests](https://img.shields.io/travis/deepsweet/bsc/master.svg?label=tests&style=flat-square)](https://travis-ci.org/deepsweet/bsc) [![coverage](https://img.shields.io/codecov/c/github/deepsweet/bsc.svg?style=flat-square)](https://codecov.io/github/deepsweet/bsc)

Binary search with comparator.

* tests not only for the result but for how many steps it takes as well
* always return `-1` if nothing has been found, no "insertion point" negative values
* no "lower" or "upper bounds"
* ESM

## Requirements

* Node.js >= 6
* [`esm` loader](https://github.com/standard-things/esm)

## Install

```sh
$ yarn add bsc
# or
$ npm install bsc
```

## Usage

```ts
<A, B>(arr: A[], key: B, comparator: (key: B, mid: A) => number) => number
```

```js
import binarySearch from 'bsc'

const arr = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
const comparator = (key, mid) => key - mid

binarySearch(arr, 2, comparator) // 2
binarySearch(arr, 10, comparator) // -1
```
