[![npm](https://img.shields.io/npm/v/npm.svg)](https://www.npmjs.com/package/hastebin-paste)
[![npm downloads](https://img.shields.io/npm/dt/hastebin-paste.svg?maxAge=3600)](https://www.npmjs.com/package/hastebin-paste)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)
[![dependencies Status](https://david-dm.org/Absolute-Development/hastebin-paste/status.svg)](https://david-dm.org/Absolute-Development/hastebin-haste)
[![devDependencies Status](https://david-dm.org/Absolute-Development/hastebin-paste/dev-status.svg)](https://david-dm.org/Absolute-Development/hastebin-paste?type=dev)
[![NPM](https://nodei.co/npm/hastebin-paste.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/hastebin-paste/)


# hastebin-gen
A npm module for generating hastebin links. 
https://www.npmjs.com/package/hastebin-paste



## Installation

**NPM:** `npm i hastebin-paste`

# Options

Option      | Type     | Default Value
----------- | -------- | ---------------------------------------------
`url`       | `string` | `"https://hastebin.com"`
`extension` | `string` | `"txt"`
`message`   | `string` | `"Powered by hastebin-paste, a npm package."`
`prefix`    | `string` | `"The link is: "`
## Examples

**Using .then().catch()**

```javascript
const hastebin = require("hastebin-paste");

// You can change the extension(ex. "js", "txt", default: "txt") by setting the extension option
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

**Using Message and Prefix option**
```js
const hastebin = require("hastebin-paste");
 
// You can change the extension by setting the extension option
hastebin("code", { url: "https://paste.example.com", extention: "txt", message: "example", prefix: "example" }).then(haste => {//set message that comes after the link or set the prefix that comes before the link
    console.log(haste)// Logs the created hastebin url and message you set to the console
    //the output will be "example https://paste.example.com/someid.txt example"
}).catch(error => {
    // Handle error
    console.error(error);
});
```
