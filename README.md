Fractal Landscape Generator
================================

# [View the Demo](/index.html) 

Usage
-----

Download http://qiao.github.com/fractal-terrain-generator/lib/terrain.js and include it in your html.

```html
<script type="text/javascript" src="./terrain.js"></script>
```

Then, in your script:

```js
var terrain = generateTerrain(32, 32, 1.0);
```

`generateTerrain` receives three parameters:

* `width`: width of the terrain.
* `height`: height of the terrain.
* `smoothness`: smoothness of the terrain. Higher this value, smoother the terrain. default value is 1.

The result `terrain` will be a (width + 1) &times; (height + 1) two-dimensional array containing the elevation of each vertex.

License
-------

[MIT License](http://www.opensource.org/licenses/mit-license.php)

