# enpies-node

[![Build Status](https://travis-ci.org/enpies/enpies-node.svg?branch=master)](https://travis-ci.org/enpies/enpies-node)
[![NPM version](https://img.shields.io/npm/v/enpies.svg)](https://www.npmjs.com/package/enpies)

You can sign up for an Enpies account at [https://enpies.com](https://enpies.com)

# Installation

`npm install enpies --save`

# Usage

## Initialization

```js
var Enpies = require('enpies');

var enpies = new Enpies({
    publicKey: 'PUBLICKEY',
    secretKey: 'SECRETKEY',
    uri: 'https://enpies.com'
});
```

### Send E-Mail Survey Request

```js
var params = {
    email: 'customer@mailservice.com',
    delay: '1 hours'
};

enpies.email.send(params, function(err, result)  {

	console.log(err, result);

});
```

### Get The Responses For E-Mail

```js
var params = {
    email: 'customer@mailservice.com'
};

enpies.email.responses(params, function(err, result)  {

	console.log(err, result);

});
```

### Get NPS® Score

```js
var params = {
    start: '2017-02-01',
    end: '2017-02-28',
};

enpies.score.details(params, function(err, result)  {

	console.log(err, result);

});
```