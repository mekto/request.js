Request.js
==========

Request.js is a small library for asynchronous http requests.

This library uses methods from ECMAScript 5, so to use it with older browsers (IE7, IE8) use [ES5-Shim](https://github.com/kriskowal/es5-shim/) or [Augment.js](http://augmentjs.com/).

To support JSON in older browsers use [JSON-js](https://github.com/douglascrockford/JSON-js).


Example
-------

``` javascript
var request = Request();

request.send({
  url: '/some-url',
  method: 'post',
  data: {exampleParam: 10},
  success: function(rv) {
    console.log(rv.text);
  }
});
```

You can set options at object creation as follows:

``` javascript
var xhr = Request({
  url: '/add-page',
  method: 'post',
  success: function(rv) {
    alert('Page added');
  }
});

xhr.send({data: {title: 'About Us', content: 'This is short info about us.'}});
xhr.send({data: {title: 'Contact', content: 'Use the form below to contact...'}});
```
