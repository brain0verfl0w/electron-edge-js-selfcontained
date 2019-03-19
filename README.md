.NET and Node.js in-process on Electron
============

*This is `electron-edge-js` fork with fixes to .net core 2.2 and support for self-contained deployment.*

*As for now works only with .net core 2.2 + macOS/Windows*

This is a fork of [edge-js](https://github.com/agracio/edge-js) adapted to support [Electron](https://github.com/electron/electron/).

Compatible with
 * Electron 1.6.x - Node.js v7.4.0.
 * Electron 1.7.x - Node.js v7.9.0.
 * Electron 1.8.x - Node.js v8.2.1.
 * Electron 2.0.x - Node.js v8.9.3.
 * Electron 3.0.x - Node.js v10.2.0.
 * Electron 4.0.4+ - Node.js v10.11.0.

Usage is the same as edge or edge-js, replace `require('edge')` or `require('edge-js')` with `require('electron-edge-js-selfcontained')`:

```bash
npm install electron-edge-js
```

```diff
-var edge = require('edge-js');
+var edge = require('electron-edge-js-selfcontained');

var helloWorld = edge.func(function () {/*
    async (input) => {
        return ".NET Welcomes " + input.ToString();
    }
*/});
```


## Why use `electron-edge-js`?

Electron is built using specific version of Node.js. In order to use `edge` in Electron project you would need to recompile it using the same Node.js version.

`electron-edge-js` comes precompiled with correct Node.js versions.

## Differences from `electron-edge`

* Uses same codebase as `edge-js` that comes with both latest code changes from `edge` project and additional fixes and improvements available in `edge-js` project.
* Supports majority of Electron versions.

## Quick start

Simple app that shows how to work with .NET Core and .NET Standard using compiled C# libraries. https://github.com/agracio/electron-edge-js-quick-start
