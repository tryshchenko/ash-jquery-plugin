# ASH Native script && jQuery Plugin
Avoid Selectors Hell - is an extremely tiny tool to simplify work with columns in tables


## How to use jQuery version
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

## How to use a native version
Basicaly script provides the similar API:

```javascript
	ash.get('.table').hideColumn(4);
```

As you can understand - difference is in table selection process: in this case ASH handles selectors instead of jQuery.

```javascript
	ash.get('.table').showColumn(2);
	ash.get('.table').toggleColumn(3);
	ash.get('.table').hideColumn(2);
```


Library also provides a simple helper to select column. In case of native library you should use native modifiers: 

```javascript
    var cells = ash.get('.table').getColumn(3); //it's is a js DOM object.
    //For example: 
	for (var i = 0; i < cells.length; i++) {
		cells[i].style.color = 'green';
	}
```

It's a tiny helpers useful for me, and I'll be happy if it will help you.