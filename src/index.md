---
title: Home
description: index.
layout: docs.hbs
---

## How to install

Verify if you have [node](http://nodejs.org/) and [npm](https://www.npmjs.org/) installed.

**CLI Tool**

```sh
$ npm install -g bananacss
```

**Node.js Module**

```sh
$ npm install bananacss --save
```

<hr>

## Command Line

*Compile you .bnn file to .css*

```sh
$ banana <input_path>
```

*Watch for changes.*

```sh
$ banana <input_path> -w
```

*Output to dir when passing files.*

```sh
$ banana <input_path> -o <out_path>
```

*Show the project version.*

```sh
$ banana --version
```

*Show all available commands.*

```sh
$ banana --help
```

<hr>

## Module Usage

```js
const bnnCode = '.a {bnn-size: 50px;}';

// features injection
const config = {};
config.bnnSize = require('./bnnSize.js'),
config.bnnPosition = require('./bnnPosition.js'),
config.bnnGradient = require('./bnnGradient.js'),
config.bnnAlign = require('./bnnAlign.js');

const Banana = require('banana')(config);

/* Output the css. */
let output = Banana.render("./fake_path.bnn", bnnCode);
```

<hr>

## Custom properties available

## bnn-size

*Banana code:*
```css
/* style.bnn */
.demo {
  bnn-size: 50px 100px;
}
```

*Result:*
```css
/* style.css */
.demo {
  width: 50px;
  height: 100px;
}
```

## bnn-position

*Banana code:*
```css
/* style.bnn */
.demo {
  bnn-position: 10px 5px 8px 90px;
}
```

*Result:*
```css
/* style.css */
.demo {
  top: 10px;
  right: 5px;
  bottom: 8px;
  left: 90px;
}
```

*Banana code:*
```css
/* style.bnn */
.demo {
  bnn-position: center;
}
```

*Result:*
```css
/* style.css */
.demo {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
```

### bnn-gradient

*Banana code:*
```css
/* style.bnn */
.demo {
  bnn-gradient: #f9e400 #ff9c00 vertical;
}
```

*Result:*
```css
/* style.css */
.demo {
  background-image: linear-gradient(to bottom, #f9e400, #ff9c00);
}
```
### bnn-align

*Banana code:*
```css
/* style.bnn */
.demo {
  bnn-align: center center;
}
```

*Result:*
```css
/* style.css */
.demo {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}
```

*Banana code:*
```css
/* style.bnn */
.demo {
  bnn-align: right bottom;
}
```

*Result:*
```css
/* style.css */
.demo {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-end;
  align-items: flex-end;
}
```

<hr>

## Module Bundler

### @import

*Banana code:*

```css
/* module.bnn */
.demo {
  color: #000;
}
```

```css
/* style.bnn */
@import module.bnn;

.exemplo {
  background: #fff;
}
```

*Result:*
```css
/* style.css */
.demo {
  color: #000;
}

.exemplo {
  background: #fff;
}
```
