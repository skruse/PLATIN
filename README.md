# PLATIN
Place and Time Navigator 

a fork and extension of [GeoTemCo](https://github.com/stjaenicke/GeoTemCo)

developed at the [Max-Planck-Institute for the History of Science](http://www.mpiwg-berlin.mpg.de) with funding from [TOPOI](http://topoi.org).

## Introduction

PLATIN is a HTML5-based tool for presentation and analysis of spatial and temporal data, with a focus on historical data.

The projects starting goal was to bring the functionality of the [DARIAH](http://www.dariah.eu) [GeoBrowser](http://dev2.dariah.eu/e4d/‎) to [GeoTemCo](http://www.informatik.uni-leipzig.de/geotemco/). 

Which added the following functionality:
* CSV loading
* loading of URL-specified datasets
* deletion of datasets and refining of datasets
* exporting of datasets (to KML or CSV files)
* an UI that leaned on the GeoBrowser layout
* full-text search of table data
* WMS and KML overlays
* time-intervals 
* upload of data to a data-store

## Important additional features

The widget-architecture of GeoTemCo led to the creation of following additional features:

### Pie Charts

Piechart can be created for each "column" of a dataset. The data can either be the distinct values, 
categorized, or even generated by an own function (that takes the objects value as an argument).

They are interactive with the other widgets, so a selection/highlight of a pie chart slice will 
select/highlight those objects in the other widgets. And a selection/highlight in another widget
will reduce the piechart to those selected/highlighted values.

### Fuzzy Timeline

If the dataset has uncertain time-data (as with historical/archaeological data) this uncertainity 
should be shown and represented in the time-plot. The fuzzy timeline will add an object in such a
way, that its weight is equaly spread across the timespan that is attached to it.

Also it is possible to switch to a bar-chart representation of the data. With bar-intervals of e.g.
1,10,100,... years.

### Directed Line-Overlay

With this widget it is possibile to add "lines" (optionally arrows) between objects on the map.

If objects are clustered the links will be inherited and line thickness will be increased if
lines are doubled by this clustering.

### Dataset coloring on element (DataObject) basis

Each DataObject can have an own color, if objects are clustered together, the cluster color 
is calculated as the average of the RGB values.

### Story-Telling

(This feature is unstable and under heavy development.)

As this tool also has an focus on data-analysis, it can be interesting to
* record the steps of selection/piechart creation/dataset refining
* go back a step or more in this history of data transformation
* branch this history
* save this history
* send this history to other persons
* create a presentation, or animation, of that history
