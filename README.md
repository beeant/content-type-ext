content-type-ext
================

http header content-type ⇄ file extension

```
npm install content-type-ext
```
```
var ext = require('content-type-ext');
var request = require('request');
request({
  url:'http://some-image-website.com/some-cool-image.jpg',
  method:'GET',
  encoding:'binary'
}, function(err, response, body) {
  var fileExtension = ext.getContentExt(response.headers['content-type']);
  console.log(fileExtension); // jpg
});
```
