# Housing Characteristics Information

This file provides information about all of the housing characteristics and their dependencies and options used in this project of ResStock.  The information is compiled from the `housing_characteristic_info.json` file in a more readable format.  

## Interactive visualization of the housing characteristic dependencies

<p class="lead">ResStock is built upon the conditional probabilites of the housing characteristics.  Each housing characteristic has a set of dependencies and dependants. In this dependency wheel, each chord in the disc represents a dependency.   Built with <a href="https://github.com/ mbostock/d3">d3.js</a> from the <a href="https://github.com/fzaninotto/DependencyWheel">fzaninotto/DependencyWheel</a> repository.</p>

### Dependency Wheel: Dependencies
The thick part of the cord represents a dependency to the thinner part of the cord. Try hovering on packages to mask other dependencies.

<div id="chart_forward"></div>

### Dependency Wheel: Dependents
The thin part of the cord represents a dependency to the thicker part of the cord. Try hovering on packages to mask other dependencies.
   
<div id="chart_backward"></div>
    
<script src="js/d3.v4.min.js"></script>
<script src="js/d3.dependencyWheel.js"></script>
<script src="js/composerBuilder.js"></script>
<script>
var gitHubApiUrl = 'https://api.github.com/repos/';
var getData = function(target, callback) {
var responses = {
  composerjson: null,
  composerlock: null
};
var checkFinished = function() {
  if (responses.composerjson && responses.composerlock) {
    callback(responses.composerjson, responses.composerlock);
  }
}
d3.xhr(gitHubApiUrl + target + '/contents/composer.json', 'application/vnd.github.VERSION.raw', function(err, composerjson) {
  responses.composerjson = JSON.parse(composerjson.responseText);
  checkFinished();
});
d3.xhr(gitHubApiUrl + target + '/contents/composer.lock', 'application/vnd.github.VERSION.raw', function(err, composerlock) {
  responses.composerlock = JSON.parse(composerlock.responseText);
  checkFinished();
});
};

var chart = d3.chart.dependencyWheel().padding(.05).width(1000).margin(265);

d3.json('data/composer_backward.json', function(composerjson) {
d3.json('data/composer_backward.lock', function(composerlock) {
  var data = buildMatrixFromComposerJsonAndLock(composerjson, composerlock);
  d3.select('#chart_backward')
    .datum(data)
    .call(chart);
});
});

d3.json('data/composer_forward.json', function(composerjson) {
d3.json('data/composer_forward.lock', function(composerlock) {
var data = buildMatrixFromComposerJsonAndLock(composerjson, composerlock);
d3.select('#chart_forward')
.datum(data)
.call(chart);
});
});

</script>
<script type="text/javascript">

var _gaq = _gaq || [];
_gaq.push(['_setAccount', 'UA-26354577-2']);
_gaq.push(['_trackPageview']);

(function() {
var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
})();

</script>
</body>
</html>

## Acronyms used in the housing characteristic information

- ACCA: Air Conditioning Contractors of America
- ACS: American Community Survey
- AHS: American Housing Survey
- BA: Building America
- BAFDR: Building America Field Data Repository
- DHWESG: Domestic Hot Water Event Schedule Generator
- HES: Home Energy Saver
- HIRL: Home Improvement Research Lab
- HSP: House Simulation Protocols
- IECC: International Energy Conservation Code
- LBNL: Lawrence Berkely National Laboratory
- NAHB: National Association of Home Builders
- ORNL: Oak Ridge National Laboratory
- OSM: OpenStreet Maps
- PNNL: Pacific Northwest National Laboratory
- RBSA: Residential Building Stock Assessment
- RECS: Residential Energy Consumption Survey

## The data sources for the housing characteristics

Each housing characteristic was created from mostly published and in some cases purchased data. Some housing characteristics have a single data source while other housing characteristics have multiple data sources. These relationships between the housing characteristics and their data sources are displayed in the Sankey diagram and the legend below.

### Legend
The image below is a legend for the larger Sankey diagram.  The colors on the left side represent the different categories of housing characteristics, while the data source (using the acronyms above) are on the right side in white.

![Sankey Diagram Legend](sankey_hc_data_sources_legend.png)

### Data Sources Sankey Diagram
A Sankey diagram of the housing characteristics and the sources that helped create the conditional distributions and measures in the ".tsv" files and the "option_lookup.tsv" files.

![Sankey Diagram](sankey_hc_data_sources.png)

# Detailed Housing Characteristic Information

The information above helps elude to the structure and relationships between the housing characteristics and thier data sources.  A more detailed explaination of each housing characteristic is provided below.

