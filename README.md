# LargeLocalStorage
Webstorage without size limits

===

Usage
----

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
  * Doesn't not emit `Storage` events (not sure how to do)

License
-------

* [Apache2](http://www.apache.org/licenses/LICENSE-2.0)
