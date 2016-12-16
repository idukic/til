#Reload the webpage when orientation changes
```js
    $(window).on('orientationchange', function (e) {
        window.location.reload();
    });
```

or 

```js
window.onorientationchange = function() { 
        var orientation = window.orientation; 
            switch(orientation) { 
                case 0:
                case 90:
                case -90: window.location.reload(); 
                break; } 
    };
```
[How to reload the webpage when orientation changes?](http://stackoverflow.com/questions/17708869/how-to-reload-the-webpage-when-orientation-changes)
