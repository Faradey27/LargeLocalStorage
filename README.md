# LargeLocalStorage
Webstorage without size limits
===

Usage
----

for webpack, brunch and other

```javascript
var localStorage = require('largeLocalStorage');
var user = {
  name: 'andrew',
  age: 99
}
var initialValue = JSON.stringify(user);
localStorage.setItem('key', value);
var value = localStorage.getItem('key');
```
----
```javascript
var localStorage = require('largeLocalStorage');
var user = {
  name: 'andrew',
  age: 99
}
var initialValue = JSON.stringify(user);
localStorage.setItem('key', value, function(result){
  if (result.isError) {
    console.info('error');
  }
});
var value = localStorage.getItem('key');
```
Index.html style
===
  Include file largeLocalStorage.js or largeLocalStorage.min.js in your index.html file.
  ```html
    <html>
      <head>
        <title>Your title</title>
      </head>
      <body>
        <script src="path/to/largeLocalStorage.min.js"></script>
        <script src="path/to/yourFiles.min.js"></script>
      </body>
    </html>
  ```
  and then
  ```javascript
  var localStorage = window.largeLocalStorage;
  var user = {
    name: 'andrew',
    age: 99
  }
  var initialValue = JSON.stringify(user);
  localStorage.setItem('key', value);
  var value = localStorage.getItem('key');
  ```

API
---

  * getItem(key)
  * setItem(key, value)
  * removeItem(key)
  * clear()

Notes
---

  * db is read/write in synchronously
  * callback when db is saved
  * Emit `Storage` events

License
-------

* [Apache2](http://www.apache.org/licenses/LICENSE-2.0)
