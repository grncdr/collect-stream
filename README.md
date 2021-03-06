
# collect-stream

Collect a readable stream's output and errors.

[![build status](https://secure.travis-ci.org/juliangruber/collect-stream.png)](http://travis-ci.org/juliangruber/collect-stream)

## Usage

Give it a readable stream and a function and it will call latter with the
potential error and a smart representation of the data the stream emitted.

```js
var collect = require('collect-stream');

collect(stringStream, function(err, data) {
  console.log(data); // one string
});

collect(bufferStream, function(err, data) {
  console.log(data); // one buffer
});

collect(objectStream, function(err, data) {
  console.log(data); // an array of objects
});
```

## Installation

```bash
$ npm install collect-stream
```

## License

  MIT