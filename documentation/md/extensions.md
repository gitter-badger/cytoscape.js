The extensions below are a curated list.  To add your extension, [please submit a request](https://github.com/cytoscape/cytoscape.js/issues/new?labels=documentation&title=List%20extension%20:%20%3Cyour%20extension%20name%3E&body=Please%20enter%20your%20Github%20URL%20and%20a%20one-line%20description) that includes your extension's URL and a one line description.


## UI extensions

 * [`cerebralweb`](https://github.com/silviafrias/cerebral-web) : Enable fast and interactive visualisation of molecular interaction networks stratified based on subcellular localisation or other custom annotation.
 * [`cxtmenu`](https://github.com/cytoscape/cytoscape.js-cxtmenu) : A circular context menu that allows for one-swipe commands on the graph.
 * [`edge-editation`](https://github.com/frankiex/cytoscape.js-edge-editation) : Adds handles to nodes and allows creation of different types of edges
 * [`edgehandles`](https://github.com/cytoscape/cytoscape.js-edgehandles) : UI for connecting nodes with edges.
 * [`navigator`](https://github.com/cytoscape/cytoscape.js-navigator) : A bird's eye view widget of the graph.
 * [`noderesize`](https://github.com/curupaco/cytoscape.js-noderesize) : A node resize control.
 * [`panzoom`](https://github.com/cytoscape/cytoscape.js-panzoom) : A panzoom UI widget.
 * [`qtip`](https://github.com/cytoscape/cytoscape.js-qtip) : A wrapper that lets you use qTips on graph elements or the graph background.
 * [`supportimages`](https://github.com/jhonatandarosa/cytoscape.js-supportimages) : Support images on Cytoscape.js.
 * [`toolbar`](https://github.com/bdparrish/cytoscape.js-toolbar) : Allow a user to create a custom toolbar to add next to a Cytoscape core instance.


## Layout extensions

 * [`arbor`](https://github.com/cytoscape/cytoscape.js-arbor) : The Arbor physics simulation layout.  It's a basic physics layout.
 * [`cola`](https://github.com/cytoscape/cytoscape.js-cola) : The Cola.js physics simulation layout.  Cola makes beautiful layout results, it animates very smoothly, and it has great options for controlling the layout.
 * [`cose-bilkent`](https://github.com/cytoscape/cytoscape.js-cose-bilkent) : The CoSE layout by Bilkent with enhanced compound node placement.  CoSE Bilkent gives near-perfect end results.  However, it's more expensive than the version of CoSE directly included with Cytoscape.js.
 * [`dagre`](https://github.com/cytoscape/cytoscape.js-dagre) : The Dagre layout for DAGs and trees.
 * [`spread`](https://github.com/cytoscape/cytoscape.js-spread) : The speedy Spread physics simulation layout.  It tries to use all the viewport space, but it can be configured to produce a tighter result.
 * [`springy`](https://github.com/cytoscape/cytoscape.js-springy) : The Springy physics simulation layout.  It's a basic physics layout.


## API

To register an extension, make the following call: `cytoscape( type, name, extension );`

The value of `type` can take on the following values:

 * `'core'` : The extension adds a core function.
 * `'collection'` : The extension adds a collection function.
 * `'layout'` : The extension registers a layout prototype.
 * `'renderer'` : The extension registers a renderer prototype.

The `name` argument indicates the name of the extension.  For example, `cytoscape( 'collection', 'fooBar', function(){ return 'baz'; } )` registers `eles.fooBar()`.



## Autoscaffolding

There exists [a Slush project for Cytoscape.js](https://github.com/cytoscape/slush-cytoscape-extension) such that the full project scaffolding for a new extension is automatically generated for you.  By following the included instructions, you can easily create Cytoscape.js extensions that are well organised, easily maintained, and published to npm, bower, spm, and meteor.



## Multitasking

Multitasking APIs are built into Cytoscape.js for extensions like layouts &mdash; making layout much faster, for example.  The APIs are pulled in from the [Weaver](http://weaver.js.org) library and put on the `cytoscape` object instead of `weaver`.  For example, you can make a thread via `cytoscape.thread()` instead of the usual `weaver.thread()`.
