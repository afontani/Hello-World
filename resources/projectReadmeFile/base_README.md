# Los Angeles Department of Water and Power (LADWP) Project Folder

This folder contains the ResStock inputs to model the residential building stock of the LADWP service area. The main inputs that characterize the building stock is the housing characteristics in the `housing_characteristics/` directory. Information about these characteristics can be found in the `resources/housing characteristics info.json` file. This file provides information about all of the housing characteristics and their dependencies and options used in this project of ResStock. And is used to create the dependency wheels, Sankey diagram, and the detailed housing characteristic information all found later in this file.

## Visualization of the Housing Characteristic Dependencies

ResStock is built upon the conditional probabilites of the housing characteristics.  Each housing characteristic has a set of dependencies and dependants.  An interactive dependency and dependents visualization is provided in the links below:

<a href="http://htmlpreview.github.io/?https://github.com/afontani/Hello-World/blob/master/resources/dependencyWheels/dep_wheels.html">Dependencies/Dependants: Dependency Wheel</a>

## Visualization of the Housing Characteristics and Data Sources

the creating of each housing characteristics' probability distribution and their measure inputs are based on multiple data sources. To visualize these connections use the link below.

<a href="https://raw.githack.com/afontani/Hello-World/master/resources/sankeyDiagram/sankey_diagram_data_sources.html">Housing Characteristics and Data Sources</a>

# Detailed Housing Characteristic Information

The information above helps elude to the structure and relationships between the housing characteristics and thier data sources.  A more detailed explaination of each housing characteristic is provided below.

