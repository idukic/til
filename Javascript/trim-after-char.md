# Trim after character

```js
// Get url:
// var href = location.href
var href = "http://localhost:8080/Page?id=123&val=value";
href = href.substring(0, href.indexOf('?'));
```