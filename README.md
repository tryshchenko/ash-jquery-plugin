# ASH jQuery Plugin
Avoid Selectors Hell - is extremely tiny jquery plugin to simplify work with columns in tables

You can use a pretty syntax for your operations:
```javascript
$('table').hideColumn(3);
```

Also you can pass arguments to 'hideColumn', 'toggleColumns', or 'showColumn' functions. You can use 'slow', 'fast', 400 or any other values available for 'hide', 'toggle' and 'show' methods.
```javascript
    $('table').hideColumn(1, 'fast');
    $('table').showColumn(1, 400);
    $('table').toggleColumn(3, 'fast');
```
All these expressions is correct.

Library also provides a simple helper to select column:
```javascript
    $('table').getColumn(2); //it's is a jQuery object.
    //For example: 
    $('table').getColumn(2).css('color', 'red');
    $('table').getColumn(2).addClass('active');
    $('table').getColumn(3).remove();
```

It's a tiny helpers useful for me, and I'll be happy if it will help you.