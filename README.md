[![npm](https://img.shields.io/npm/v/npm.svg)](https://www.npmjs.com/package/hastebin-paste)
[![npm downloads](https://img.shields.io/npm/dt/hastebin-paste.svg?maxAge=3600)](https://www.npmjs.com/package/hastebin-paste)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)
[![dependencies Status](https://david-dm.org/Absolute-Development/hastebin-paste/status.svg)](https://david-dm.org/Absolute-Development/hastebin-haste)
[![devDependencies Status](https://david-dm.org/Absolute-Development/hastebin-paste/dev-status.svg)](https://david-dm.org/Absolute-Development/hastebin-paste?type=dev)
[![NPM](https://nodei.co/npm/hastebin-paste.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/hastebin-paste/)


# hastebin-gen
A npm module for generating hastebin links. 
https://www.npmjs.com/package/hastebin-paste

## change log
[1.0.4]Keyword updated

[1.0.1, 1.0.2 and 1.0.3]README updated

[1.0.0]initial publish

## Installation

**NPM:** `npm i hastebin-paste`

# Options

Option      | Type     | Default Value
----------- | -------- | ----------------
`url`       | `string` | `"https://hastebin.com"`
`extension` | `string` | `"js"`

## Examples

**Using .then().catch()**

```javascript
const hastebin = require("hastebin-paste");

// You can change the extension by setting the extension option
hastebin("code", { extension: "txt" }).then(haste => {
    // Logs the created hastebin url to the console
    console.log(haste); // https://hastebin.com/someid.txt
}).catch(error => {
    // Handle error
    console.error(error);
});
```

**Using async/await**

This is assuming that you are in a asynchronous scope

[**Understanding Async/Await**](https://hackernoon.com/understanding-async-await-in-javascript-1d81bb079b2c)

```javascript
const hastebin = require("hastebin-paste");

// You can change the extension by setting the extension option
const haste = await hastebin("code", { extension: "txt" });

// Logs the created hastebin url to the console
console.log(haste); // https://hastebin.com/someid.txt
```

## Example with a custom [**haste-server**](https://github.com/seejohnrun/haste-server) instance

**Using .then().catch()**

```javascript
const hastebin = require("hastebin-paste");

// You can change the extension by setting the extension option
hastebin("code", { url: "https://paste.example.com", extension: "txt" }).then(haste => {
    // Logs the created hastebin url to the console
    console.log(haste); // https://paste.example.com/someid.txt
}).catch(error => {
    // Handle error
    console.error(error);
});
```

**Using async/await**

This is assuming that you are in a asynchronous scope

[**Understanding Async/Await**](https://hackernoon.com/understanding-async-await-in-javascript-1d81bb079b2c)

```javascript
const hastebin = require("hastebin-paste");

// You can change the extension by setting the extension option
const haste = await hastebin("code", { url: "https://paste.example.com", extension: "txt" });

// Logs the created hastebin url to the console
console.log(haste); // https://paste.example.com/someid.txt
```
