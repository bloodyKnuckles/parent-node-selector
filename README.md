# parent-node-selector

Find a particular parent node of the current element by passing the element and a tag name/css
selector identifier.

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


### install
```
npm install parent-node-selector
```

### license

MIT
