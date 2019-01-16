# Welcome

This is a explanatory guide for the 'Basic Web Map' web map.  This map was built using the ArcGIS API 4.0.

The map can be viewed [here](https://jwparker1797.github.io/BasicWorldMap/map.html), feel free to view and check out the source using dev tools.

Below you will find some explanation of some of the elements demonstrated in the map.

## HTML File

The basic [HTML] (https://github.com/jwparker1797/BasicWorldMap/blob/master/map.html) document is the first file to be created. 

###The page header references a few important items:

```header
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="initial-scale=1, maximum-scale=1, user-scalable=no">
    <link rel="stylesheet" href="https://js.arcgis.com/4.10/esri/css/main.css">
    <script src="https://js.arcgis.com/4.10/"></script>
    <link rel="stylesheet" href="style/mapView.css">
    <title>Basic World Map</title>
</head>
```

This is referencing:
1. ArcGIS API for JavaScript stylesheet
2. ArcGIS API module
3. A custom stylesheet for this specific map

### The body of the page references the map script and provides a div element where the map will live.

```body
<body>
    <script src="scripts/map.js"></script>
    <div id="mapView"></div>
</body>
```

## Script

The script does all of the work to make and display the map.

### Load modules

The first step is to load the necessary modules from the ArcGIS API.

```load modules
require([
    "esri/Map",
    "esri/views/MapView"
], function(Map, MarView){}_;
```

### Build the map

Next you need to create a map object.

```map object
    var map = new Map({
        basemap: "streets"
    });
```

### Create a view

Next make a 2d view that references a node in the html document and the map object.

```view
    var view = new MarView({
        container: "mapView",
        map: map
```

## Custom Style

Next lets create a custom style for the webmap.

### Style Sheet

The following makes the map fill the viewable space.

```style
html,
body,
#mapView {
    padding: 0;
    margin: 0;
    height: 100%;
    width: 100%;
}
```


That's it!  This is the most basic web map.


## Check out more of my work

Go to my [page] (https://jwparker1797.github.io) to check out more of my work.
