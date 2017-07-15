# request-http2

Request module with HTTP/2 support

This project is a modified fork of [request](https://github.com/request/request) project.
Therefore see [request](https://www.npmjs.com/package/request) for details.

### HTTP/2 requests

Unlike [request](https://github.com/request/request) package, it supports HTTP/2 requests.
Just add `http: true` in the `options` object argument in request method.

For example, see `POST` request below -

```js
  var options = {
    method: 'POST',
      uri: 'https://someurl.com/path',
      http2: true,
      headers: {
        // HEADERS go here
      },
      body: {
        // DATA to be posted
      } ,
      json: true
  };

  request(options, function (error, response, body) {
    if (error) {
      return console.error('upload failed:', error);
    }
    console.log('Server responded with:', body);
  })
```
