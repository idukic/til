#Get value after a special character

You can use .indexOf()/lastIndexOf() and .substr():

```js
var href = "http://localhost:8080/Page?id=123";
href = href.substring(href.indexOf('=') + 1);
```