# Has variable truthy value or not?

```js

if(value)  {}

```

*  True if value is not:
- null
- undefined
- NaN
- empty string ("")
- 0
- false

* If you do not know whether a variable exists:

```js

if( typeof var !== 'undefined' ) {
    // var could get resolved and it's defined
}

```

http://stackoverflow.com/questions/5515310/is-there-a-standard-function-to-check-for-null-undefined-or-blank-variables-in