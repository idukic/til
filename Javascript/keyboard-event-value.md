# KeyboardEvent Value

## example: Do not alow negative numbers and 0.

```html
<form>
  <fieldset>
    <label for="target">Add number:</label>
    <input min="1" value="1" type="number" id="target" />
  </fieldset>
</form>
```

```js
$("#target").keypress(function(event) {
  if ( event.which == 45 || event.which == 48 ) {
      event.preventDefault();
   }
});
```
See more:
[KeyboardEvent Value (keyCodes, metaKey, etc)](https://css-tricks.com/snippets/javascript/javascript-keycodes/)