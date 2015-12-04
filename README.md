# parent-node-selector

Find a particular parent node of the current element by passing the element and a tag name/css
selector identifier.

### example
```
var parentNodeSelector = require('parent-node-selector')

var childelement = document.getElementbyId('childid')

var parentelement = parentNodeSelector(childelement, 'div#parentid')
```

Given:
```
<!DOCTYPE html>
<html>
    <head>
        <title>parent-node-selector</title>
        <script src="bundle.js"></script>
    </head>
    <body>
        <div id="pageid">
            <div id="parentid">
                <div id="notme">
                    <div id="childid">
                        Child
                    </div>
                </div>
            </div>
        </div>
    </body>
</html>
```

Returns:
```
<div id="parentid">
    <div id="notme">
        <div id="childid">
            Child
        </div>
    </div>
</div>
```

### more examples

You can also:
```
var parentwithclass = parentNodeSelector(childelement, 'div.parentclass')
var parentelement   = parentNodeSelector(childelement, 'div') // get closest parent DIV
```
### prototype example

If running your `parent-node-selector` javascript in a browser you can add this method to the `Node` prototype
object:
```
Node.prototype.parentNodeSelector = require('parent-node-selector')
var childelement = document.getElementbyId('childid')
var parentelement = childelement.parentNodeSelector('div#parentid')
```

### install
```
npm install parent-node-selector
```

### license

MIT
