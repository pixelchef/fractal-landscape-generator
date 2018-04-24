Fractal Landscape Generator
================================

<html lang="en">

<head>
<meta charset="UTF-8">
<title>Fractal Landscape Generator</title>
<link rel="stylesheet" href="./main.css" />
<link rel="stylesheet" href="./lib/fd-slider/fd-slider.css" />
<link rel="stylesheet" href="./lib/fd-slider/fd-slider-tooltip.css" />
<script type="text/javascript" src="./lib/Three.js"></script>
<script type="text/javascript" src="./lib/RequestAnimationFrame.js"></script>
<script type="text/javascript" src="./lib/Detector.js"></script>
<script type="text/javascript" src="./lib/jquery-1.7.1.min.js"></script>
<script type="text/javascript" src="./lib/jquery.pubsub.js"></script>
<script type="text/javascript" src="./lib/fd-slider/fd-slider.js"></script>
<script type="text/javascript" src="../lib/terrain.js"></script>
</head>

<body>
<div id="sidebar">
<div id="sidebar-inner">
<h1 id="title">Fractal Landscape Generator</h1>

<div id="intro">
<p>
This is a demo of using the
<a href="https://en.wikipedia.org/wiki/Fractal_landscape">diamond-square</a> algorithm to generate a random fractal terrain.
</p>
<p>
The visualization is built with
<a href="https://github.com/mrdoob/three.js">Three.js</a>.
</p>
</div>


<form id="opts">
<label for="size">Size:</label>
<select class="opt" id="opt-size" name="size">
<option value="1">1</option>
<option value="2">2</option>
<option value="4">4</option>
<option value="8">8</option>
<option value="16">16</option>
<option value="32">32</option>
<option value="64" selected="yes">64</option>
<option value="128">128</option>
</select>

<label for="smoothness">Smoothness:</label>
<input class="opt" id="opt-smoothness" type="text" name="smoothness" min="0.1" max="5" step="0.1" value="1.0">
<br>

<label for="z-scale">Z-Scale:</label>
<input class="opt" id="opt-z" type="text" name="z-scale" min="0" max="500" step="20" value="340">
<br>

<button id="new" href="#">Generate New Landscape</button>
</form>
</div>
</div>
<div id="container"></div>


<script type="text/javascript" src="./main.js"></script>
<script type="text/javascript">
TerrainController.init();
</script>
</body>

</html>

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

