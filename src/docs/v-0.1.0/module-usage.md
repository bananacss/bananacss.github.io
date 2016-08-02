---
title: Home
description: index.
layout: docs.hbs
---

# Module Usage

```js
const bnnCode = '.a {bnn-size: 50px;}';

const config = {};
config.bnnSize = require('./bnnSize.js'),
config.bnnPosition = require('./bnnPosition.js'),
config.bnnGradient = require('./bnnGradient.js'),
config.bnnAlign = require('./bnnAlign.js');

const Banana = require('banana')(config);

let output = Banana.render("./fake_path.bnn", bnnCode);
```
