# jQuery Datepicker Widget

*Methods*:
* option() - the new options for the date picker.
```js
$( ".selector" ).datepicker( "option", "optionName", "optionValue");
```
## Set day names for the column header

The day names come from the _dayNamesMin_ (Mo,Tu...) option, to set up to _dayNamesShort_(Mon, Tue...) for the longer names:

```js
// 1. Set values for min names
$( ".selector" ).datepicker( "option", "dayNamesMin", ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"]);

// 2. Override defaults
$.datepicker.setDefaults({dayNamesMin: $.datepicker._defaults.dayNamesShort});
```

## Set _setDefaults_

```js
var regional = "de";
var options = $.extend(
        {},
        $.datepicker.regional[regional],
        {
            // custom options
            dayNamesMin: $.datepicker._defaults.dayNamesShort
        }
    );

    $.datepicker.setDefaults(options);
```