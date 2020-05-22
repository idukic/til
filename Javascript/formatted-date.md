# Formmated date


## JavaScript Date Output
Independent of input format, JavaScript will (by default) output dates in full text string format:
* e.g. Fri Dec 30 2016 14:55:16 GMT+0000 (GMT Standard Time)

```js
var fullDate = "2016-12-30T14:55:16.9780086+00:00";

var date = new Date(fullDate);  // full text string format
var day = (date.getDate() < 10 ? "0" + date.getDate() : date.getDate());
var month = date.getMonth() + 1;
var month = (month < 10 ? "0" + month : month);
var year = date.getFullYear();
var hh = (date.getHours() < 10 ? "0" + date.getHours() : date.getHours());
var mm = (date.getMinutes() < 10 ? "0" + date.getMinutes() : date.getMinutes());
var ss = (date.getSeconds() < 10 ? "0" + date.getSeconds() : date.getSeconds());

var date = day + "/" + month + "/" + year + " - " + hh + ":" + mm + ":" + ss; 

// date = "30/12/2016 - 14:55:16"
```