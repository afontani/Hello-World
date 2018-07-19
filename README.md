# Los Angeles Department of Water and Power (LADWP) Project Folder

This folder contains the ResStock inputs to model the residential building stock of the LADWP service area. The main inputs that characterize the building stock is the housing characteristics in the `housing_characteristics/` directory. Information about these characteristics can be found in the `resources/housing characteristics info.json` file. This file provides information about all of the housing characteristics and their dependencies and options used in this project of ResStock. And is used to create the dependency wheels, Sankey diagram, and the detailed housing characteristic information all found later in this file.

## Visualization of the Housing Characteristic Dependencies

ResStock is built upon the conditional probabilites of the housing characteristics.  Each housing characteristic has a set of dependencies and dependants.  An interactive dependency and dependents visualization is provided in the links below:

<a href="http://htmlpreview.github.io/?https://github.com/afontani/Hello-World/blob/master/resources/dependencyWheels/dep_wheels.html">Dependencies/Dependants: Dependency Wheel</a>

## Visualization of the Housing Characteristics and Data Sources

the creating of each housing characteristics' probability distribution and their measure inputs are based on multiple data sources. To visualize these connections use the link below.

<a href="https://rawcdn.githack.com/afontani/Hello-World/master/resources/sankeyDiagram/sankey_diagram_data_sources.html">Housing Characteristics and Data Sources</a>

# Detailed Housing Characteristic Information

The information above helps elude to the structure and relationships between the housing characteristics and thier data sources.  A more detailed explaination of each housing characteristic is provided below.

## Area Mean Income
<u>Description:</u> The housing characteristic "Area Mean Income" (AMI) is midpoint of the region's income distribution. In this case the reported area is every census tract, location EPW weather file, and county. Within each census tract the AMI is also reported for different housing vintages, housing size, heating fuel, and cooling type. The AMI distribution is distributed between different owner and renter age ranges.

<u>Category:</u> Demographics and Income

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

2. AHS-2013, (<https://www.census.gov/programs-surveys/ahs/data.2013.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2013, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{AHS 2013 Public Use File (PUF)}},
			year = {2013}}

#### Assumptions: 

NaN

#### Dependencies: 

- Location Census Tract
- Vintage
- Geometry House Size
- HVAC System Cooling Type
- Location EPW
- Location County
- Heating Fuel

#### Options: 

- Owner 0-30
- Owner 30-50
- Owner 50-80
- Owner 80-100
- Owner 100-120
- Owner 120+
- Renter 0-30
- Renter 30-50
- Renter 50-80
- Renter 80-100
- Renter 100-120
- Renter 120+


## Bathroom Spot Vent Hour
<u>Description:</u> The housing characteristic "Bathroom Spot Vent Hour" is a daily schedule designed to capture bathroom fan ventilation.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

#### Assumptions: 

Schedules based on occupancy in the House Simulation Protocols. The schedule is based on Figure 25 in HSP.

#### Dependencies: 

- None

#### Options: 

- Hour0
- Hour1
- Hour2
- Hour3
- Hour4
- Hour5
- Hour6
- Hour7
- Hour8
- Hour9
- Hour10
- Hour11
- Hour12
- Hour13
- Hour14
- Hour15
- Hour16
- Hour17
- Hour18
- Hour19
- Hour20
- Hour21
- Hour22
- Hour23


## Ceiling Fan
<u>Description:</u> The housing characteristic "Ceiling Fan" describes the usage of ceiling fans in the household and their schedule of use during the weekday, weekend, and seasonal factors.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. Parker-2010, (<http://www.fsec.ucf.edu/en/publications/pdf/FSEC-CR-1837-10-R01.pdf>)

	<u>Bibtex Citation</u>


2. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

3. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

The ceiling fan is currently being treated as a plug load and the schedule is being treated in the same way. The schedules are from the schedules are taken from Pinckard 2005 as other MELs. The power data and national average is take from Parker 2010.

#### Dependencies: 

- None

#### Options: 

- National Average


## Clothes Dryer
<u>Description:</u> The housing characteristic "Clothes Dryer" describes the home's clothes dryer by its fuel type, combined energy factor (CEF), usage relative to the national average, and hourly usage schedule for weekdays and weekends.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The types with manual usage level split is from RECS 2009. The performance metrics are from HSP-2014. There is spot venting from the clothes dryer and the energy consumption from the clothes dryer lags the clothes washer by 1-hour. The schedules are from the building America analysis spreadsheets which date back to Pratt et al. 1989.

#### Dependencies: 

- Heating Fuel
- Location Region
- Usage Level

#### Options: 

- Gas, 80% Usage
- Gas, 100% Usage
- Gas, 120% Usage
- Propane, 80% Usage
- Propane, 100% Usage
- Propane, 120% Usage
- Electric, 80% Usage
- Electric, 100% Usage
- Electric, 120% Usage
- None


## Clothes Washer
<u>Description:</u> The housing characteristic "Clothes Washer" describes a home's clothes washer by different usage levels and standard or EnergyStar clothes washers.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. ENERGY STAR, (<https://www.energystar.gov/products/appliances/clothes_washers>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnvironmentalProtectionAgency2018, address = {Washington, D.C., USA},
			author = {{U.S. Environmental Protection Agency}},
			title = {{ENERGY STAR}},
			url = {https://www.energystar.gov/},
			year = {2018} }

3. DHWESG, (<https://www.energy.gov/eere/buildings/downloads/building-america-dhw-event-schedule-generator>)

	<u>Bibtex Citation</u>

		@techreport{Weitzel2014, abstract = {A developing body of work is forming that collects data on domestic hot water consumption, water use behaviors, and energy efficiency of various distribution systems. A full distribution system developed in TRNSYS has been validated using field monitoring data and then exercised in a number of climates to understand climate impact on performance. This study builds upon previous analysis modelling work to evaluate differing distribution systems and the sensitivities of water heating energy and water use efficiency to variations of climate, load, distribution type, insulation and compact plumbing practices. Overall 124 different TRNSYS models were simulated. Of the configurations evaluated, distribution losses account for 13-29{\%} of the total water heating energy use and water use efficiency ranges from 11-22{\%}. The base case, an uninsulated trunk and branch system sees the most improvement in energy consumption by insulating and locating the water heater central to all fixtures. Demand recirculation systems are not projected to provide significant energy savings and in some cases increase energy consumption. Water use is most efficient with demand recirculation systems, followed by the insulated trunk and branch system with a central water heater. Compact plumbing practices and insulation have the most impact on energy consumption (2-6{\%} for insulation and 3-4{\%} per 10 gallons of enclosed volume reduced). The results of this work are useful in informing future development of water heating best practices guides as well as more accurate (and simulation time efficient) distribution models for annual whole house simulation programs.},
			address = {Washington, D.C., USA},
			author = {Weitzel, E and Hoeschele, M},
			institution = {U.S. Department of Energy},
			keywords = {ARBI,Building America,DHW,DOE/GO-102014-4515,HWSIM,NREL/SR-5500-62848,Residential Buildings,September 2014,TRNSYS,demand recirculation_,distribution systems,domestic hot water,hot water,hot water distribution systems,plumbing,residential,water heating},
			number = {September},
			title = {{Evaluating Domestic Hot Water Distribution System Options With Validated Analysis Models}},
			url = {https://www.nrel.gov/docs/fy14osti/62848.pdf},
			year = {2014} }

#### Assumptions: 

The types with manual usage level split is from RECS 2009. The performance metrics are from ENERGYSTAR Requirements. The schedules are from the DHWESG.

#### Dependencies: 

- Usage Level

#### Options: 

- Standard, 80% Usage
- Standard, 100% Usage
- Standard, 120% Usage
- EnergyStar, 80% Usage
- EnergyStar, 100% Usage
- EnergyStar, 120% Usage


## Cooking Range
<u>Description:</u> The housing characteristic "Cooking Range" describes the home's cooking range by usage amount, the fuel type, the performance and usage schedule.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

4. Pratt 1989, (<https://elcap.nwcouncil.org/Documents/Electric%20Energy%20Use%20Single%20Family.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Pratt1989, address = {Richland, WA, USA},
			author = {Pratt, R. G. and Conner, C. C. and Richman, E. E. and Ritland, K. G. and Sandusky, W. F. and Taylor, M. E.},
			institution = {Pacific Northwest National Laboratory},
			number = {DOE/BP-13795-21},
			publisher = {Bonneville Power Administration},
			title = {{Description of Electric Energy Use in Single-Family Residences in the Pacific Northwest}},
			url = {https://elcap.nwcouncil.org/Documents/Electric Energy Use Single Family.pdf},
			year = {1989} }

#### Assumptions: 

Types with manual usage level split is from RECS 2009. The schedule can be found in the 2014-HSP and the Building America Analysis Spreadsheets. These schedules are based on Pratt et al. 1989.

#### Dependencies: 

- Heating Fuel
- Location Region
- Usage Level

#### Options: 

- Gas, 80% Usage
- Gas, 100% Usage
- Gas, 120% Usage
- Propane, 80% Usage
- Propane, 100% Usage
- Propane, 120% Usage
- Electric, 80% Usage
- Electric, 100% Usage
- Electric, 120% Usage
- None


## Cooling Setpoint
<u>Description:</u> The housing characteristic "Cooling Setpoint" describes the cooling setpoint temperature for the homes based on the associated weather file.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

A regression was performed based on the cooling set points vs CDD in RECS 2009. The RECS labels are used for the options.

#### Dependencies: 

- Location EPW

#### Options: 

- 72F
- 73F
- 74F
- 75F
- 76F
- 77F


## Days Shifted
<u>Description:</u> The housing characteristic "Days Shifted" allows for the simulation to start on various days of the year for the whole building stock.

<u>Category:</u> Occupancy

#### Data Sources:

1. No Data Source Needed

#### Assumptions: 

NaN

#### Dependencies: 

- None

#### Options: 

- Day0
- Day1
- Day2
- Day3
- Day4
- Day5
- Day6
- Day7
- Day8
- Day9
- Day10
- Day11
- Day12
- Day13
- Day14
- Day15
- Day16
- Day17
- Day18
- Day19
- Day20
- Day21
- Day22
- Day23
- Day24
- Day25
- Day26
- Day27
- Day28
- Day29
- Day30
- Day31
- Day32
- Day33
- Day34
- Day35
- Day36
- Day37
- Day38
- Day39
- Day40
- Day41
- Day42
- Day43
- Day44
- Day45
- Day46
- Day47
- Day48
- Day49
- Day50
- Day51
- Day52
- Day53
- Day54
- Day55
- Day56
- Day57
- Day58
- Day59
- Day60
- Day61
- Day62
- Day63
- Day64
- Day65
- Day66
- Day67
- Day68
- Day69
- Day70
- Day71
- Day72
- Day73
- Day74
- Day75
- Day76
- Day77
- Day78
- Day79
- Day80
- Day81
- Day82
- Day83
- Day84
- Day85
- Day86
- Day87
- Day88
- Day89
- Day90
- Day91
- Day92
- Day93
- Day94
- Day95
- Day96
- Day97
- Day98
- Day99
- Day100
- Day101
- Day102
- Day103
- Day104
- Day105
- Day106
- Day107
- Day108
- Day109
- Day110
- Day111
- Day112
- Day113
- Day114
- Day115
- Day116
- Day117
- Day118
- Day119
- Day120
- Day121
- Day122
- Day123
- Day124
- Day125
- Day126
- Day127
- Day128
- Day129
- Day130
- Day131
- Day132
- Day133
- Day134
- Day135
- Day136
- Day137
- Day138
- Day139
- Day140
- Day141
- Day142
- Day143
- Day144
- Day145
- Day146
- Day147
- Day148
- Day149
- Day150
- Day151
- Day152
- Day153
- Day154
- Day155
- Day156
- Day157
- Day158
- Day159
- Day160
- Day161
- Day162
- Day163
- Day164
- Day165
- Day166
- Day167
- Day168
- Day169
- Day170
- Day171
- Day172
- Day173
- Day174
- Day175
- Day176
- Day177
- Day178
- Day179
- Day180
- Day181
- Day182
- Day183
- Day184
- Day185
- Day186
- Day187
- Day188
- Day189
- Day190
- Day191
- Day192
- Day193
- Day194
- Day195
- Day196
- Day197
- Day198
- Day199
- Day200
- Day201
- Day202
- Day203
- Day204
- Day205
- Day206
- Day207
- Day208
- Day209
- Day210
- Day211
- Day212
- Day213
- Day214
- Day215
- Day216
- Day217
- Day218
- Day219
- Day220
- Day221
- Day222
- Day223
- Day224
- Day225
- Day226
- Day227
- Day228
- Day229
- Day230
- Day231
- Day232
- Day233
- Day234
- Day235
- Day236
- Day237
- Day238
- Day239
- Day240
- Day241
- Day242
- Day243
- Day244
- Day245
- Day246
- Day247
- Day248
- Day249
- Day250
- Day251
- Day252
- Day253
- Day254
- Day255
- Day256
- Day257
- Day258
- Day259
- Day260
- Day261
- Day262
- Day263
- Day264
- Day265
- Day266
- Day267
- Day268
- Day269
- Day270
- Day271
- Day272
- Day273
- Day274
- Day275
- Day276
- Day277
- Day278
- Day279
- Day280
- Day281
- Day282
- Day283
- Day284
- Day285
- Day286
- Day287
- Day288
- Day289
- Day290
- Day291
- Day292
- Day293
- Day294
- Day295
- Day296
- Day297
- Day298
- Day299
- Day300
- Day301
- Day302
- Day303
- Day304
- Day305
- Day306
- Day307
- Day308
- Day309
- Day310
- Day311
- Day312
- Day313
- Day314
- Day315
- Day316
- Day317
- Day318
- Day319
- Day320
- Day321
- Day322
- Day323
- Day324
- Day325
- Day326
- Day327
- Day328
- Day329
- Day330
- Day331
- Day332
- Day333
- Day334
- Day335
- Day336
- Day337
- Day338
- Day339
- Day340
- Day341
- Day342
- Day343
- Day344
- Day345
- Day346
- Day347
- Day348
- Day349
- Day350
- Day351
- Day352
- Day353
- Day354
- Day355
- Day356
- Day357
- Day358
- Day359
- Day360
- Day361
- Day362
- Day363
- Day364


## Dehumidifier
<u>Description:</u> The housing characteristic "Dehumidifier" is used to describe the dehumidifiers in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. Not Used

#### Assumptions: 

Housing characteristic not used

#### Dependencies: 

- None

#### Options: 

- None


## Dishwasher
<u>Description:</u> The housing characteristic "Dishwasher" described the dishwashers in the building stock. The dishwashers are described by their electric rating, usage level relative to average, number of place settings that can fit in the dishwasher, and the annual energy guide gas cost.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. DHWESG, (<https://www.energy.gov/eere/buildings/downloads/building-america-dhw-event-schedule-generator>)

	<u>Bibtex Citation</u>

		@techreport{Weitzel2014, abstract = {A developing body of work is forming that collects data on domestic hot water consumption, water use behaviors, and energy efficiency of various distribution systems. A full distribution system developed in TRNSYS has been validated using field monitoring data and then exercised in a number of climates to understand climate impact on performance. This study builds upon previous analysis modelling work to evaluate differing distribution systems and the sensitivities of water heating energy and water use efficiency to variations of climate, load, distribution type, insulation and compact plumbing practices. Overall 124 different TRNSYS models were simulated. Of the configurations evaluated, distribution losses account for 13-29{\%} of the total water heating energy use and water use efficiency ranges from 11-22{\%}. The base case, an uninsulated trunk and branch system sees the most improvement in energy consumption by insulating and locating the water heater central to all fixtures. Demand recirculation systems are not projected to provide significant energy savings and in some cases increase energy consumption. Water use is most efficient with demand recirculation systems, followed by the insulated trunk and branch system with a central water heater. Compact plumbing practices and insulation have the most impact on energy consumption (2-6{\%} for insulation and 3-4{\%} per 10 gallons of enclosed volume reduced). The results of this work are useful in informing future development of water heating best practices guides as well as more accurate (and simulation time efficient) distribution models for annual whole house simulation programs.},
			address = {Washington, D.C., USA},
			author = {Weitzel, E and Hoeschele, M},
			institution = {U.S. Department of Energy},
			keywords = {ARBI,Building America,DHW,DOE/GO-102014-4515,HWSIM,NREL/SR-5500-62848,Residential Buildings,September 2014,TRNSYS,demand recirculation_,distribution systems,domestic hot water,hot water,hot water distribution systems,plumbing,residential,water heating},
			number = {September},
			title = {{Evaluating Domestic Hot Water Distribution System Options With Validated Analysis Models}},
			url = {https://www.nrel.gov/docs/fy14osti/62848.pdf},
			year = {2014} }

#### Assumptions: 

Usage Level

#### Dependencies: 

- Usage Level

#### Options: 

- 318 Rated kWh, 80% Usage
- 318 Rated kWh, 100% Usage
- 318 Rated kWh, 120% Usage
- 290 Rated kWh, 80% Usage
- 290 Rated kWh, 100% Usage
- 290 Rated kWh, 120% Usage


## Door Area
<u>Description:</u> The housing characteristic "Door Area" specifies the area of the doors in the house, which is based on standard construction practices for the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

#### Assumptions: 

Assume that the standard height is 80 in and standard width is 36 in.

#### Dependencies: 

- None

#### Options: 

- 20 ft^2


## Doors
<u>Description:</u> The housing characteristic "Doors" describes the material and U-value of the doors in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

#### Assumptions: 

HSP-2014

#### Dependencies: 

- None

#### Options: 

- Fiberglass


## Ducts
<u>Description:</u> The housing characteristic "Ducts" describes the air ducts in the building stock. The ducts are described by their insulation level, air leakage percentage, and whether the ducts are in the conditioned space.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. PNNL-2009, (<https://www.pnnl.gov/main/publications/external/technical_reports/PNNL-17979.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Halverson2009, abstract = {This report is part of a series of reports on building energy efficiency codes in countries associated with the Asian Pacific Partnership (APP) - Australia, South Korea, Japan, China, India, and the United States of America (U.S.). This reports gives an overview of the development of building energy codes in U.S., including national energy policies related to building energy codes, history of building energy codes, recent national projects and activities to promote building energy codes. The report also provides a review of current building energy codes (such as building envelope, HVAC, lighting, and water heating) for commercial and residential buildings in the U.S.},
			address = {Richland, WA, USA},
			author = {Halverson, M.A. and Shui, B and Evans, M},
			doi = {10.2172/978981},
			institution = {Pacific Northwest National Laboratory},booktitle = {PNNL-17979},
			title = {{Country Report on Building Energy Codes in the United States}},
			url = {https://www.pnnl.gov/main/publications/external/technical{\_}reports/PNNL-17979.pdf},
			year = {2009} }

2. IECC, (<https://www.lightingdesignlab.com/sites/default/files/pdf/International%20Energy%20Conservation%20Code_IECC_2009.pdf>)

	<u>Bibtex Citation</u>

		@misc{InternationalCodeCouncilInc.2009, address = {Country Club Hills, IL, USA},
			author = {{International Code Council Inc.}},
			title = {{2009 International Energy Conservation Code}},
			url = {https://www.lightingdesignlab.com/sites/default/files/pdf/International Energy Conservation Code{\_}IECC{\_}2009.pdf},
			year = {2009} }

#### Assumptions: 

Air leakage distributions are assumed to be normally distributed from the PNNL report.

#### Dependencies: 

- Geometry Foundation Type
- Vintage
- Geometry Building Type

#### Options: 

- 10% Leakage, Uninsulated
- 20% Leakage, Uninsulated
- 30% Leakage, Uninsulated
- 10% Leakage, R-4
- 20% Leakage, R-4
- 30% Leakage, R-4
- 10% Leakage, R-6
- 20% Leakage, R-6
- 30% Leakage, R-6
- 10% Leakage, R-8
- 20% Leakage, R-8
- 30% Leakage, R-8
- In Finished Space


## Eaves
<u>Description:</u> The housing characteristic "Eaves" describes the eave overhang distance for the houses in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

#### Assumptions: 

The average eave length is 2 ft. Expert Elicitation.

#### Dependencies: 

- None

#### Options: 

- 2 ft


## Federal Poverty Level
<u>Description:</u> The housing characteristic "Federal Poverty Level" describes how the population's income corresponds to the federal poverty level. The federal poverty distributions are based on whether the occupant rents or owns the house and what percentage their income corresponds to the federal poverty level for their Census Tract. Within each Census Tract the FPL distributions are also listed by house vintage, house size, heating system type, and cooling system type. Other geographic regions are also listed (Location EPW weather file, and County) to perform other aggregations of the data.

<u>Category:</u> Demographics and Income

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

2. AHS-2013, (<https://www.census.gov/programs-surveys/ahs/data.2013.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2013, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{AHS 2013 Public Use File (PUF)}},
			year = {2013}}

#### Assumptions: 

NaN

#### Dependencies: 

- Location Census Tract
- Vintage
- Geometry House Size
- HVAC System Cooling Type
- Location EPW
- Location County
- Heating Fuel

#### Options: 

- Owner 0-50
- Owner 50-100
- Owner 100-150
- Owner 150-200
- Owner 200-250
- Owner 250-300
- Owner 300+
- Renter 0-50
- Renter 50-100
- Renter 100-150
- Renter 150-200
- Renter 200-250
- Renter 250-300
- Renter 300+


## Geometry Building Floors
<u>Description:</u> The housing characteristic "Geometry Building Floors" describes the number of building floors for the buildings in the building stock. The number of floors is dependent on the building type, the age of the building, and the size of the building.

<u>Category:</u> Geometry

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Vintage
- Geometry House Size

#### Options: 

- 1
- 2
- 3
- 4+


## Geometry Building Number Units MF
<u>Description:</u> The housing characteristic "Geometry Building Number of Units MF" describes the distribution number units of a multi-family building in the building stock.

<u>Category:</u> Geometry

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Geometry Building Floors
- Geometry Number Units ACS bins

#### Options: 

- None
- 2
- 3
- 4
- 6
- 8
- 9
- 12
- 15
- 16
- 18
- 20
- 21
- 24
- 36
- 42
- 54
- 78
- 102
- 160
- 210


## Geometry Building Number Units SFA
<u>Description:</u> The housing characteristic "Geometry Building Number of Units MF" describes the distribution number units of a single-family attached building in the building stock.

<u>Category:</u> Geometry

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Geometry Building Floors
- Geometry Number Units ACS bins

#### Options: 

- None
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9
- 10
- 12
- 15
- 16
- 20
- 24
- 30
- 36
- 50
- 60
- 90
- 144


## Geometry Building Type
<u>Description:</u> The housing characteristic "Geometry Building Type" describes the distribution of the building stock as different types of buildings classes. These classifications are similar to the RECS definitions, but are not exact.

<u>Category:</u> Geometry

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Location Region

#### Options: 

- Mobile Home
- Multi-Family with 2 - 4 Units
- Multi-Family with 5+ Units
- Single-Family Attached
- Single-Family Detached


## Geometry Building Type RECS to ACS
<u>Description:</u> The housing characteristic "Geometry Building Type RECS to ACS" is a mapping TSV file that converts the RECS building type and maps them to the ACS building types.

<u>Category:</u> Geometry

#### Data Sources:

1. No Data Source Needed

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type

#### Options: 

- Mobile Home
- 1 detached
- 1 attached
- 2
- 3 or 4
- 5 to 9
- 10 to 19
- 20 to 49
- 50 or more


## Geometry Foundation Type
<u>Description:</u> The housing characteristic "Geometry Foundation Type" describes the distribution of different foundation types within the building stock and depends on the location of the building and the building type.

<u>Category:</u> Geometry

#### Data Sources:

1. ORNL Map, (<No longer exists>)

	<u>Bibtex Citation</u>

		None

#### Assumptions: 

NaN

#### Dependencies: 

- Location EPW
- Geometry Building Type

#### Options: 

- Pier & Beam
- Unheated Basement
- Heated Basement
- Crawl
- Slab


## Geometry Garage
<u>Description:</u> The housing characteristic "Geometry Garage" describes the presence and size of a garages in the building stock.

<u>Category:</u> Geometry

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Vintage
- Geometry House Size

#### Options: 

- 1 Car
- 2 Car
- 3 Car
- None


## Geometry House Size
<u>Description:</u> The housing characteristic "Geometry House Size" describes the distribution of the floor area of the houses in the building stock and depends on the location, the age, and type of building.

<u>Category:</u> Geometry

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Location Region
- Vintage

#### Options: 

- 0-1499
- 1500-2499
- 2500-3499
- 3500+


## Geometry Is Multifamily Low Rise
<u>Description:</u> The housing characteristic "Geometry Is Multifamily Low Rise" maps the building type to low rise residential buildings, so data can be extracted from low rise buildings only.

<u>Category:</u> Geometry

#### Data Sources:

1. No Data Source Needed

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type

#### Options: 

- TRUE
- FALSE


## Geometry Nearest Neighbor LeftRight
<u>Description:</u> The housing characteristic "Geometry Nearest Neighbor LeftRight" describes the distribution of the nearest neighbor to the left and right of the building for the low rise residential building stock. The building mostly effects the shading algorithm in EnergyPlus due to buildings being very close to one another.

<u>Category:</u> Geometry

#### Data Sources:

1. OSM, (<https://www.openstreetmap.org/#map=4/38.01/-95.84>)

	<u>Bibtex Citation</u>

		@misc{OpenStreetMapFoundation, author = {{OpenStreetMap Foundation}},
			title = {{OpenStreetMaps}},
			url = {https://www.openstreetmap.org/{\#}map=4/38.01/-95.84} }

	<u>Remarks:</u> Data obtained by RadiantLabs. Data not for distribution (http://www.radiantlabs.co/).

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Is Multifamily Low Rise

#### Options: 

- 2
- 4
- 7
- 12
- 27
- None


## Geometry Number Units ACS bins
<u>Description:</u> The housing characteristic "Geometry Building Number of Units ACS" describes the distribution number units of a multi-family building in the building stock according to the ACS bins.

<u>Category:</u> Geometry

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type

#### Options: 

- 5 to 9 Units
- 10 to 19 Units
- 20 to 49 Units
- 50 or more
- <5


## Geometry Perimeter Footprint Ratio
<u>Description:</u> The housing characteristic "Geometry Perimeter Footprint Ratio" describes the distribution of perimeter footprint area ratio of the building stock. The perimeter footprint area ratio is the perimeter of the building footprint divided by the area of the building foot print. This housing characteristic is dependent of the building type and the location.

<u>Category:</u> Geometry

#### Data Sources:

1. OSM, (<https://www.openstreetmap.org/#map=4/38.01/-95.84>)

	<u>Bibtex Citation</u>

		@misc{OpenStreetMapFoundation, author = {{OpenStreetMap Foundation}},
			title = {{OpenStreetMaps}},
			url = {https://www.openstreetmap.org/{\#}map=4/38.01/-95.84} }

	<u>Remarks:</u> Data obtained by RadiantLabs. Data not for distribution (http://www.radiantlabs.co/).

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Location EPW

#### Options: 

- 0.13
- 0.15
- 0.17
- 0.19
- 0.21


## Geometry Shared Walls MF
<u>Description:</u> The housing characteristic "Geometry Shared Walls MF" describes the distribution of residential low rise multifamily buildings with shared walls to other units in the multifamily building.

<u>Category:</u> Geometry

#### Data Sources:

1. OSM, (<https://www.openstreetmap.org/#map=4/38.01/-95.84>)

	<u>Bibtex Citation</u>

		@misc{OpenStreetMapFoundation, author = {{OpenStreetMap Foundation}},
			title = {{OpenStreetMaps}},
			url = {https://www.openstreetmap.org/{\#}map=4/38.01/-95.84} }

	<u>Remarks:</u> Data obtained by RadiantLabs. Data not for distribution (http://www.radiantlabs.co/).

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Is Multifamily Low Rise

#### Options: 

- None
- Left
- LeftBack
- LeftRight
- LeftRightBack


## Geometry Shared Walls SFA
<u>Description:</u> The housing characteristic "Geometry Shared Walls SFA" describes the distribution of residential low rise single family attached buildings with shared walls to other buildings.

<u>Category:</u> Geometry

#### Data Sources:

1. OSM, (<https://www.openstreetmap.org/#map=4/38.01/-95.84>)

	<u>Bibtex Citation</u>

		@misc{OpenStreetMapFoundation, author = {{OpenStreetMap Foundation}},
			title = {{OpenStreetMaps}},
			url = {https://www.openstreetmap.org/{\#}map=4/38.01/-95.84} }

	<u>Remarks:</u> Data obtained by RadiantLabs. Data not for distribution (http://www.radiantlabs.co/).

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Is Multifamily Low Rise

#### Options: 

- LeftBack
- Left
- LeftRight
- LeftRightBack
- None


## Geometry Unit Stories MF
<u>Description:</u> The housing characteristic "Geometry Unit Stories MF" describes the distribution of the number of stories for units in multifamily buildings.

<u>Category:</u> Geometry

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Vintage
- Geometry House Size

#### Options: 

- 1
- 2
- 3
- N/a


## Geometry Unit Stories SF
<u>Description:</u> The housing characteristic "Geometry Unit Stories SF" describes the distribution of the number of stories for units in single-family buildings.

<u>Category:</u> Geometry

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

NaN

#### Dependencies: 

- Geometry Building Type
- Vintage
- Geometry House Size

#### Options: 

- 1
- 2
- 3
- 4+
- N/a


## HVAC System Central
<u>Description:</u> The housing characteristic "HVAC System Central" describes the distribution of different types of HVAC systems and whether these systems are central units for multifamily buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

If the building type is single family attached or single family detached, it is assumed that there is no central system. There is no multiple units for their HVAC system to be shared. If there are no survey counts for multifamily, the assumed distribution is 0.33, 0.33, 0.34 for radiators with boiler steam/HW, fan coil with boiler HW, and PTACs with boiler HW respectively.

#### Dependencies: 

- Geometry Building Type
- Vintage
- Heating Fuel
- HVAC System Is Central
- HVAC System Cooling Type

#### Options: 

- None
- Fan coil with chiller/Boiler
- Fan coil with chiller
- radiators with boiler steam/HW
- fan coil with boiler HW
- PTACs with boiler HW


## HVAC System Combined
<u>Description:</u> The housing characteristic "HVAC System Combined" describes the distribution of HVAC systems types when the heating and cooling is system is combined.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

If the HVAC system is not combined in the "HVAC System Is Combined.tsv," then the option is None. The only systems to be combined are electric heating and electric cooling, Air Source Heat Pumps (ASHPs) with different efficiencies. If the heating fuel type is not electric, then the option is None. The distributions are created from RECS-2009, but the efficiencies based on age are taken from HES (Pinckard et al. 2005).

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined

#### Options: 

- None
- ASHP, SEER 10, 6.2 HSPF
- ASHP, SEER 13, 7.7 HSPF
- ASHP, SEER 15, 8.5 HSPF


## HVAC System Cooling
<u>Description:</u> The housing characteristic "HVAC System Cooling" describes the distribution of different cooling systems and system efficiencies in the buildings of the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

	<u>Remarks:</u> Why are there distributions for Only Heating Shared. In the HVAC system Is Central.tsv-there is only a 1s in Neither Share.

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

	<u>Remarks:</u> Why are there distributions for Only Heating Shared. In the HVAC system Is Central.tsv-there is only a 1s in Neither Share.

#### Assumptions: 

The types are taken from RECS along with the age of the cooling system. The efficiencies are taken from HES If the HVAC system is not combined in the "HVAC System Is Combined.tsv," then the option is None. The only systems to be combined are electric heating and electric cooling, Air Source Heat Pumps (ASHPs) with different efficiencies. If the heating fuel type is not electric, then the option is None. The distributions are created from RECS-2009, but the efficiencies based on age are taken from HES (Pinckard et al. 2005). If there is no data it is assumed that there is no cooling system. If HVAC system is combined, then these system types are not applicable and the option is None. In this case the cooling system is taken from the "HVAC System Combined.tsv".

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined
- HVAC System Is Central

#### Options: 

- None
- AC, SEER 8
- AC, SEER 10
- AC, SEER 13
- AC, SEER 15
- FIXME Room AC, EER 8.5, 20% Conditioned
- FIXME Room AC, EER 10.7, 20% Conditioned


## HVAC System Cooling Type
<u>Description:</u> The housing characteristic "HVAC System Cooling Type" maps different air conditioning system described in "HVAC System Cooling.tsv" with whether the HVAC system is shared with other homes or businesses in "HVAC System Is Central.tsv." The result is that the system is either central, a room air conditioning unit, or none.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. No Data Source Needed

	<u>Remarks:</u> Should the last 2 lines be Option=Room? Should line None- Only Cooling be Option=None?

#### Assumptions: 

NaN

#### Dependencies: 

- HVAC System Cooling
- HVAC System Is Central

#### Options: 

- Central
- None
- Room


## HVAC System Heating Electricity
<u>Description:</u> The housing characteristic "HVAC System Heating Electricity" describes the distribution of electric heating systems in the buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

If the HVAC system is combined, then the option is None. The Heating system is described in the "HVAC System Combined.tsv" file. If the heating fuel is not Electricity, then the option is None. The system types come from RECS 2000 with the age, but the efficiencies come from HES (Pinckard et al. 2005). If the HVAC system is not combined in the "HVAC System Is Combined.tsv," then the option is None. The only systems to be combined are electric heating and electric cooling, Air Source Heat Pumps (ASHPs) with different efficiencies. If the heating fuel type is not electric, then the option is None. The distributions are created from RECS-2009, but the efficiencies based on age are taken from HES (Pinckard et al. 2005).

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined
- HVAC System Is Central

#### Options: 

- None
- Electric Boiler
- Electric Furnace
- Electric Baseboard


## HVAC System Heating Fuel Oil
<u>Description:</u> The housing characteristic "HVAC System Heating Fuel Oil" describes the distribution of fuel oil heating systems in the buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

If the HVAC system is combined, then the option is None. The Heating system is described in the "HVAC System Combined.tsv" file. If the heating fuel is not Fuel Oil, then the option is None. The system types come from RECS 2000 with the age, but the efficiencies come from HES (Pinckard et al. 2005). If the HVAC system is not combined in the "HVAC System Is Combined.tsv," then the option is None. The only systems to be combined are electric heating and electric cooling, Air Source Heat Pumps (ASHPs) with different efficiencies. If the heating fuel type is not electric, then the option is None. The distributions are created from RECS-2009, but the efficiencies based on age are taken from HES (Pinckard et al. 2005).

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined
- HVAC System Is Central

#### Options: 

- None
- Oil Boiler, 90% AFUE
- Oil Boiler, 80% AFUE
- Oil Boiler, 76% AFUE
- Oil Furnace, 95% AFUE
- Oil Furnace, 90% AFUE
- Oil Furnace, 80% AFUE
- Oil Furnace, 76% AFUE
- Oil Wall/Floor Furnace, 68% AFUE
- Oil Wall/Floor Furnace, 60% AFUE


## HVAC System Heating Natural Gas
<u>Description:</u> The housing characteristic "HVAC System Heating Natural Gas" describes the distribution of natural gas heating systems in the buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

If the HVAC system is combined, then the option is None. The Heating system is described in the "HVAC System Combined.tsv" file. If the heating fuel is not Natural Gas, then the option is None. The system types come from RECS 2000 with the age, but the efficiencies come from If the HVAC system is not combined in the "HVAC System Is Combined.tsv," then the option is None. The only systems to be combined are electric heating and electric cooling, Air Source Heat Pumps (ASHPs) with different efficiencies. If the heating fuel type is not electric, then the option is None. The distributions are created from RECS-2009, but the efficiencies based on age are taken from HES (Pinckard et al. 2005).

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined
- HVAC System Is Central

#### Options: 

- None
- Gas Boiler, 80% AFUE
- Gas Boiler, 76% AFUE
- Gas Boiler, 72% AFUE
- Gas Furnace, 96% AFUE
- Gas Furnace, 92.5% AFUE
- Gas Furnace, 80% AFUE
- Gas Furnace, 76% AFUE
- Gas Furnace, 60% AFUE
- Gas Wall/Floor Furnace, 68% AFUE
- Gas Wall/Floor Furnace, 60% AFUE


## HVAC System Heating None
<u>Description:</u> The housing characteristic "HVAC System Heating None" describes the distribution of buildings with no heating system in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. No Data Source Needed

#### Assumptions: 

Since there is not heating system, the only option is None with a 1 in all rows.

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined

#### Options: 

- None


## HVAC System Heating Other Fuel
<u>Description:</u> The housing characteristic "HVAC System Heating Other Fuel" describes the distribution of buildings with heating systems other than Electric, Fuel Oil, Natural Gas, or Propane in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. No Data Source Needed

#### Assumptions: 

It is assumed that the heating system doesn't draw from the electric, fuel oil, natural gas, or propane end uses. Therefore, it is assumed that these systems don't have a heating system.

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined

#### Options: 

- None


## HVAC System Heating Propane
<u>Description:</u> The housing characteristic "HVAC System Heating Propane" describes the distribution of propane heating systems in the buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

If the HVAC system is combined, then the option is None. The Heating system is described in the "HVAC System Combined.tsv" file. If the heating fuel is not Propane, then the option is None. The system types come from RECS 2000 with the age, but the efficiencies come from HES (Pinckard et al. 2005). If the HVAC system is not combined in the "HVAC System Is Combined.tsv," then the option is None. The only systems to be combined are electric heating and electric cooling, Air Source Heat Pumps (ASHPs) with different efficiencies. If the heating fuel type is not electric, then the option is None. The distributions are created from RECS-2009, but the efficiencies based on age are taken from HES (Pinckard et al. 2005).

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Combined
- HVAC System Is Central

#### Options: 

- None
- Propane Boiler, 80% AFUE
- Propane Boiler, 76% AFUE
- Propane Boiler, 72% AFUE
- Propane Furnace, 96% AFUE
- Propane Furnace, 92% AFUE
- Propane Furnace, 80% AFUE
- Propane Furnace, 76% AFUE
- Propane Furnace, 60% AFUE
- Propane Wall/Floor Furnace, 68% AFUE
- Propane Wall/Floor Furnace, 60% AFUE


## HVAC System Is Central
<u>Description:</u> The housing characteristic "HVAC System Is Central" described the distribution of the heating and cooling system being shared with another home, business, farm, etc.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

If there is no data it is assumed that the option is Neither heating or cooling system is shared.

#### Dependencies: 

- Geometry Building Type
- Vintage
- Heating Fuel

#### Options: 

- Both Shared
- Neither Shared
- Only Cooling Shared
- Only Heating Shared


## HVAC System Is Combined
<u>Description:</u> The housing characteristic "HVAC System Is Combined" describes the distribution of HVAC systems that have heating and cooling capabilities.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

If there is no data it is assumed that the Option is No.

#### Dependencies: 

- Location Region
- Vintage
- Heating Fuel
- HVAC System Is Central

#### Options: 

- No
- Yes


## Heating Fuel
<u>Description:</u> The housing characteristic "Heating Fuel" describes the heating fuel type for buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Location EPW
- Vintage

#### Options: 

- Electricity
- Fuel Oil
- Natural Gas
- None
- Other Fuel
- Propane


## Heating Setpoint
<u>Description:</u> The housing characteristic "Heating Setpoint" describes the distribution of the heating system setpoints.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

The heating setpoint is determined by a regression of heating setpoints vs HDD from the RECS 2009 dataset.

#### Dependencies: 

- Location EPW

#### Options: 

- 66F
- 67F
- 68F
- 69F
- 70F


## Hot Water Distribution
<u>Description:</u> The housing characteristic "Hot Water Distribution" describes the distribution of different types of hot water pipe configurations in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. Expert Elicitation

#### Assumptions: 

NaN

#### Dependencies: 

- Vintage

#### Options: 

- Uninsulated, TrunkBranch, Copper
- Uninsulated, HomeRun, PEX


## Hot Water Fixtures
<u>Description:</u> The housing characteristic "Hot Water Fixtures" describes the distribution of different usage levels of showers, sinks, and baths in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. DHWESG, (<https://www.energy.gov/eere/buildings/downloads/building-america-dhw-event-schedule-generator>)

	<u>Bibtex Citation</u>

		@techreport{Weitzel2014, abstract = {A developing body of work is forming that collects data on domestic hot water consumption, water use behaviors, and energy efficiency of various distribution systems. A full distribution system developed in TRNSYS has been validated using field monitoring data and then exercised in a number of climates to understand climate impact on performance. This study builds upon previous analysis modelling work to evaluate differing distribution systems and the sensitivities of water heating energy and water use efficiency to variations of climate, load, distribution type, insulation and compact plumbing practices. Overall 124 different TRNSYS models were simulated. Of the configurations evaluated, distribution losses account for 13-29{\%} of the total water heating energy use and water use efficiency ranges from 11-22{\%}. The base case, an uninsulated trunk and branch system sees the most improvement in energy consumption by insulating and locating the water heater central to all fixtures. Demand recirculation systems are not projected to provide significant energy savings and in some cases increase energy consumption. Water use is most efficient with demand recirculation systems, followed by the insulated trunk and branch system with a central water heater. Compact plumbing practices and insulation have the most impact on energy consumption (2-6{\%} for insulation and 3-4{\%} per 10 gallons of enclosed volume reduced). The results of this work are useful in informing future development of water heating best practices guides as well as more accurate (and simulation time efficient) distribution models for annual whole house simulation programs.},
			address = {Washington, D.C., USA},
			author = {Weitzel, E and Hoeschele, M},
			institution = {U.S. Department of Energy},
			keywords = {ARBI,Building America,DHW,DOE/GO-102014-4515,HWSIM,NREL/SR-5500-62848,Residential Buildings,September 2014,TRNSYS,demand recirculation_,distribution systems,domestic hot water,hot water,hot water distribution systems,plumbing,residential,water heating},
			number = {September},
			title = {{Evaluating Domestic Hot Water Distribution System Options With Validated Analysis Models}},
			url = {https://www.nrel.gov/docs/fy14osti/62848.pdf},
			year = {2014} }

2. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

#### Assumptions: 

NaN

#### Dependencies: 

- Usage Level

#### Options: 

- 50%
- 100%
- 200%


## Infiltration
<u>Description:</u> The housing characteristic "Infiltration" describes the distribution of buildings with different levels of infiltration rated at the air changes per hour at 50 Pascals pressure difference from the outdoors (ACH50) with a blower door test.

<u>Category:</u> Construction

#### Data Sources:

1. LBNL-ResDB, (<http://resdb.lbl.gov/main.php#>)

	<u>Bibtex Citation</u>

		@techreport{Chan2012, abstract = {LBNL Residential Diagnostics Database (ResDB) contains blower door measurements and other diagnostic test results of homes in United States. Of these, approximately 134,000 single-family detached homes have sufficient information for the analysis of air leakage in relation to a number of housing characteristics. We performed regression analysis to consider the correlation between normalized leakage and a number of explanatory variables: IECC climate zone, floor area, height, year built, foundation type, duct location, and other housing characteristics. The regression model explains 68{\%} of the observed variability in normalized leakage. ResDB also contains the before and after retrofit air leakage measurements of approximately 23,000 homes that participated in weatherization assistant programs (WAPs) or residential energy efficiency programs. The two types of programs achieve rather similar reductions in normalized leakage: 30{\%} for WAPs and 20{\%} for other energy programs.},
			address = {Berkeley, CA, USA},
			author = {Chan, Wanyu R. and Joh, Jeffrey and Sherman, Max H.},
			booktitle = {LBNL-5966E},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {Fan pressurization measurements,air infiltration,blower door,retrofit,weatherization},number = {August},
			title = {{Air leakage of US homes: Regression analysis and improvements from retrofit}},
			url = {https://eetd.lbl.gov/sites/all/files/publications/lbnl-5966e.pdf},
			year = {2012} }

#### Assumptions: 

Distributions come from Eq. 1 and Eq. 2 in the report.

#### Dependencies: 

- Geometry Building Type
- Location Region
- Vintage
- Geometry House Size
- Geometry Building Floors

#### Options: 

- 3 ACH50
- 4 ACH50
- 5 ACH50
- 6 ACH50
- 7 ACH50
- 8 ACH50
- 10 ACH50
- 15 ACH50
- 20 ACH50
- 25 ACH50


## Insulation Crawlspace
<u>Description:</u> The housing characteristic "Insulation Crawlspace" describes the distribution of crawlspace insulation and venting configurations for buildings in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

2. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

3. HIRL-1999, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

4. HIRL-2007, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

#### Assumptions: 

If the building was constructed prior to the 1980s, it is assumed that the crawlspace is uninsulated and vented. The option Crawl from the Geometry Foundation Type are the only entries with a crawlspace (else Option=None). For the 1980s the distributions use the 1988 NAHB Survey, For the 1990s the distributions use the 1999 HIRL data, and for the 2000s the distributions use the 2007 HIRL data.

#### Dependencies: 

- Location Region
- Vintage
- Geometry Foundation Type
- Geometry Building Type

#### Options: 

- Uninsulated, Vented
- Wall R-5, Unvented
- Wall R-10, Unvented
- Ceiling R-13, Vented
- Ceiling R-19, Vented
- None


## Insulation Finished Basement
<u>Description:</u> The housing characteristic "Insulation Finished Basement" describes the presence and level of insulation in finished basements in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

2. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

3. HIRL-1999, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

4. HIRL-2008, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

#### Assumptions: 

Any building built before the 1980s is assumed to have an uninsulated finished basement. The option Heated Basement from the Geometry Foundation Type are the only entries with a finished basement (else Option=None). For the 1980s the distributions use the 1988 NAHB Survey, For the 1990s the distributions use the 1999 HIRL data, and for the 2000s the distributions use the 2008 HIRL data.

#### Dependencies: 

- Location Region
- Vintage
- Geometry Foundation Type
- Geometry Building Type

#### Options: 

- Uninsulated
- Wall R-5
- Wall R-10
- Wall R-15
- None


## Insulation Finished Roof
<u>Description:</u> The housing characteristic "Insulation Finished Roof" describes the distribution of the level of insulation for cathedralized roofs.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

#### Assumptions: 

Assume that 50% of the finished roofs are uninsulated and 50% are insulation with R-30.

#### Dependencies: 

- None

#### Options: 

- Uninsulated
- R-30


## Insulation Interzonal Floor
<u>Description:</u> The housing characteristic "Insulation Interzonal Floor" describes the insulation level of interzonal floors in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

2. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

3. IECC, (<https://www.lightingdesignlab.com/sites/default/files/pdf/International%20Energy%20Conservation%20Code_IECC_2009.pdf>)

	<u>Bibtex Citation</u>

		@misc{InternationalCodeCouncilInc.2009, address = {Country Club Hills, IL, USA},
			author = {{International Code Council Inc.}},
			title = {{2009 International Energy Conservation Code}},
			url = {https://www.lightingdesignlab.com/sites/default/files/pdf/International Energy Conservation Code{\_}IECC{\_}2009.pdf},
			year = {2009} }

#### Assumptions: 

An interzonal floor is the same as a pier and beam foundation without the geometry building type and geometry. Foundation type dependencies.

#### Dependencies: 

- Location Region
- Vintage

#### Options: 

- Uninsulated
- R-13
- R-19
- R-30
- R-38


## Insulation Pier Beam
<u>Description:</u> The housing characteristic "Insulation Pier Beam" describes the presence and level of insulation for pier and beam foundations in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

2. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

3. IECC, (<https://www.lightingdesignlab.com/sites/default/files/pdf/International%20Energy%20Conservation%20Code_IECC_2009.pdf>)

	<u>Bibtex Citation</u>

		@misc{InternationalCodeCouncilInc.2009, address = {Country Club Hills, IL, USA},
			author = {{International Code Council Inc.}},
			title = {{2009 International Energy Conservation Code}},
			url = {https://www.lightingdesignlab.com/sites/default/files/pdf/International Energy Conservation Code{\_}IECC{\_}2009.pdf},
			year = {2009} }

#### Assumptions: 

Any building built before the 1980s is assumed to have an uninsulated pier and beam foundation. The option Pier & Beam from the Geometry Foundation Type are the only entries with a pier and beam foundation (else Option=None). For the 1980s the distributions use the 1988 NAHB Survey, For the 1990s the distributions use extrapolations from the 1988 NAHB Survey, and for the 2000s the distributions use the IECC 2009.

#### Dependencies: 

- Location Region
- Vintage
- Geometry Foundation Type
- Geometry Building Type

#### Options: 

- Uninsulated
- R-13
- R-19
- R-30
- R-38
- None


## Insulation Slab
<u>Description:</u> The housing characteristic "Insulation Slab" describes the distribution of level and configuration of the insulation in slab foundations in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

2. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

3. HIRL-1999, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

4. HIRL-2007, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

#### Assumptions: 

If the building was constructed prior to the 1980s, it is assumed that the slab is uninsulated. The option Slab from the Geometry Foundation Type are the only entries with a slab (else Option=None). For the 1980s the distributions use the 1988 NAHB Survey. For the 1990s the distributions use the 1999 HIRL data, and for the 2000s the distributions use the 2007 HIRL data.

#### Dependencies: 

- Location Region
- Vintage
- Geometry Foundation Type
- Geometry Building Type

#### Options: 

- Uninsulated
- 2ft R5 Perimeter, R5 Gap
- 2ft R10 Perimeter, R10 Gap
- 2ft R5 Exterior
- 2ft R10 Exterior
- None


## Insulation Unfinished Attic
<u>Description:</u> The housing characteristic "Insulation Unfinished Attic" describes the level of ceiling insulation in attics in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. RBSA, (<https://neea.org/data/residential-building-stock-assessment>)

	<u>Bibtex Citation</u>

		@techreport{Baylon2011, address = {Seattle, WA, USA},
			author = {Baylon, David and Storm, Poppy and Geraghty, Kevin and Davis, Bob},
			institution = {Northwest Energy Efficiency Alliance},
			title = {{2011 Residential Building Stock Assessment: Single-Family Characteristics and Energy Use}},
			url = {https://neea.org/img/documents/residential-building-stock-assessment-single-family-characteristics-and-energy-use.pdf},
			year = {2011} }

2. HIRL-1999, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

#### Assumptions: 

The data previous to the 1990s is based on RBSA, then each climate zone is adjusted based on the values of the Pacific Northwest. Climate regions 3-8 are extrapolated from RBSA but are the same as the Pacific Northwest. Climate Region 2 is extrapolated from RBSA, but shifted down due to the colder climate. Climate Region 9-11 are extrapolated from RBSA, but are shifted down due to the warmer climate. In the 1990s and 2000s, the data is based on the HIRL 1999 Insulation Report with the exception of CR06 (which is the Pacific Northwest) and used RBSA.

#### Dependencies: 

- Location Region
- Vintage

#### Options: 

- Uninsulated, Vented
- Ceiling R-7, Vented
- Ceiling R-13, Vented
- Ceiling R-19, Vented
- Ceiling R-30, Vented
- Ceiling R-38, Vented
- Ceiling R-49, Vented


## Insulation Unfinished Basement
<u>Description:</u> The housing characteristic "Insulation Unfinished Basement" Describes the insulation level and configuration of unfinished basements in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

2. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

3. HIRL-1999, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

4. HIRL-2008, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

#### Assumptions: 

Any building built before the 1980s is assumed to have an uninsulated unfinished basement. The option Unheated Basement from the Geometry Foundation Type are the only entries with a unfinished basement (else Option=None). For the 1980s the distributions use the 1988 NAHB Survey, For the 1990s the distributions use the 1999 HIRL data, and for the 2000s the distributions use the 2007 HIRL data.

#### Dependencies: 

- Location Region
- Vintage
- Geometry Foundation Type
- Geometry Building Type

#### Options: 

- Uninsulated
- Ceiling R-13
- Ceiling R-19
- None


## Insulation Wall
<u>Description:</u> The housing characteristic "Insulation Wall" describes the distribution of the level of insulation in walls in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Ritschard-1992

	<u>Bibtex Citation</u>

		@techreport{Ritschard1992, address = {Berkeley, CA, USA},
			author = {Ritschard, R.L. and Hanford, J.W. and Sezgen, A.O.},
			institution = {Lawrence Berkeley Laboratory. LBL-30377},
			title = {{Single Family Heating and Cooling Requirements: Assumptions, Methods, and Summary Results}},
			url = {https://cloudfront.escholarship.org/dist/prd/content/qt02v2q58f/qt02v2q58f.pdf?t=p0tnye},
			year = {1992} }

2. BAFDR, (<Missing Entry>)

	<u>Bibtex Citation</u>

		Missing Entry

3. NAHB Survey-1988, (<https://www.nahb.org/>)

	<u>Remarks:</u> Purchased Data from National Association of Home Builders. Not for distribution.

4. HIRL-1999, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

5. HIRL-2008, (<http://www.homeinnovation.com/>)

	<u>Remarks:</u> Purchased Data from Home Innovation Research Laboratory. Not for distribution.

#### Assumptions: 

Climate region 2 is based on BAFDR for all vintages. Before the 1960s it is assumed that walls are insulated wood studs in all regions besides climate region 2. Other climate Regions before the 1980s use Ritschard et al. 1992 and the NAHB 1988 survey. In the 1990s the distributions use the HIRL 1999 Insulation and Sheathing Reports (besides CR02). In the 2000s, the distributions use the 2008 HIRL Insulation and Sheating Reports (besides CR02).

#### Dependencies: 

- Location Region
- Vintage

#### Options: 

- Wood Stud, Uninsulated
- Wood Stud, R-7
- Wood Stud, R-11
- Wood Stud, R-15
- Wood Stud, R-19


## Lighting
<u>Description:</u> The housing characteristic "Lighting" describes the distribution of different lightbulbs used in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. Expert Elicitation

	<u>Remarks:</u> Is there a better source (RECS?)

#### Assumptions: 

NaN

#### Dependencies: 

- None

#### Options: 

- 100% Incandescent
- 60% CFL
- 100% CFL


## Location EPW
<u>Description:</u> The housing characteristic "Location EPW" describes the distribution of the houses in the building stock in different weather regions near the weather file's latitude and longitude.

<u>Category:</u> Location

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Location Region

#### Options: 

- USA_AL_Birmingham.Muni.AP.722280_TMY3.epw
- USA_AL_Huntsville.Intl.AP-Jones.Field.723230_TMY3.epw
- USA_AL_Mobile-Rgnl.AP.722230_TMY3.epw
- USA_AL_Montgomery-Dannelly.Field.722260_TMY3.epw
- USA_AR_Fort.Smith.Rgnl.AP.723440_TMY3.epw
- USA_AR_Little.Rock-Adams.Field.723403_TMY3.epw
- USA_AZ_Flagstaff-Pulliam.AP.723755_TMY3.epw
- USA_AZ_Phoenix-Sky.Harbor.Intl.AP.722780_TMY3.epw
- USA_AZ_Prescott-Love.Field.723723_TMY3.epw
- USA_AZ_Tucson.Intl.AP.722740_TMY3.epw
- USA_CA_Arcata.AP.725945_TMY3.epw
- USA_CA_Bakersfield-Meadows.Field.723840_TMY3.epw
- USA_CA_Barstow.Daggett.AP.723815_TMY3.epw
- USA_CA_Fresno.Air.Terminal.723890_TMY3.epw
- USA_CA_Long.Beach-Daugherty.Field.722970_TMY3.epw
- USA_CA_Los.Angeles.Intl.AP.722950_TMY3.epw
- USA_CA_Sacramento.Exec.AP.724830_TMY3.epw
- USA_CA_San.Diego-Lindbergh.Field.722900_TMY3.epw
- USA_CA_San.Francisco.Intl.AP.724940_TMY3.epw
- USA_CA_Santa.Maria.Public.AP.723940_TMY3.epw
- USA_CO_Alamosa.Muni.AP.724620_TMY3.epw
- USA_CO_Boulder-Broomfield-Jefferson.County.AP.724699_TMY3.epw
- USA_CO_Colorado.Springs-Peterson.Field.724660_TMY3.epw
- USA_CO_Eagle.County.Rgnl.AP.724675_TMY3.epw
- USA_CO_Grand.Junction-Walker.Field.724760_TMY3.epw
- USA_CO_Pueblo.Mem.AP.724640_TMY3.epw
- USA_CT_Bridgeport-Sikorsky.Mem.AP.725040_TMY3.epw
- USA_CT_Hartford-Bradley.Intl.AP.725080_TMY3.epw
- USA_DE_Wilmington-New.Castle.County.AP.724089_TMY3.epw
- USA_FL_Daytona.Beach.Intl.AP.722056_TMY3.epw
- USA_FL_Jacksonville.Intl.AP.722060_TMY3.epw
- USA_FL_Key.West.Intl.AP.722010_TMY3.epw
- USA_FL_Miami.Intl.AP.722020_TMY3.epw
- USA_FL_Orlando.Intl.AP.722050_TMY3.epw
- USA_FL_Tallahassee.Rgnl.AP.722140_TMY3.epw
- USA_FL_West.Palm.Beach.Intl.AP.722030_TMY3.epw
- USA_GA_Athens-Ben.Epps.AP.723110_TMY3.epw
- USA_GA_Atlanta-Hartsfield-Jackson.Intl.AP.722190_TMY3.epw
- USA_GA_Augusta-Bush-Field.722180_TMY3.epw
- USA_GA_Columbus.Metro.AP.722255_TMY3.epw
- USA_GA_Macon-Middle.Georgia.Rgnl.AP.722170_TMY3.epw
- USA_GA_Savannah.Intl.AP.722070_TMY3.epw
- USA_IA_Des.Moines.Intl.AP.725460_TMY3.epw
- USA_IA_Mason.City.Muni.AP.725485_TMY3.epw
- USA_IA_Sioux.City-Sioux.Gateway.AP.725570_TMY3.epw
- USA_IA_Waterloo.Muni.AP.725480_TMY3.epw
- USA_ID_Boise.Air.Terminal.726810_TMY3.epw
- USA_ID_Pocatello.Muni.AP.725780_TMY3.epw
- USA_IL_Chicago-OHare.Intl.AP.725300_TMY3.epw
- USA_IL_Moline-Quad.City.Intl.AP.725440_TMY3.epw
- USA_IL_Peoria-Greater.Peoria.AP.725320_TMY3.epw
- USA_IL_Rockford-Greater.Rockford.AP.725430_TMY3.epw
- USA_IL_Springfield-Capital.AP.724390_TMY3.epw
- USA_IN_Evansville.Rgnl.AP.724320_TMY3.epw
- USA_IN_Fort.Wayne.Intl.AP.725330_TMY3.epw
- USA_IN_Indianapolis.Intl.AP.724380_TMY3.epw
- USA_IN_South.Bend-Michiana.Rgnl.AP.725350_TMY3.epw
- USA_KS_Dodge.City.Rgnl.AP.724510_TMY3.epw
- USA_KS_Goodland-Renner.Field.724650_TMY3.epw
- USA_KS_Topeka-Phillip.Billard.Muni.AP.724560_TMY3.epw
- USA_KS_Wichita-Mid.Continent.AP.724500_TMY3.epw
- USA_KY_Cincinnati-Northern.Kentucky.AP.724210_TMY3.epw
- USA_KY_Lexington-Bluegrass.AP.724220_TMY3.epw
- USA_KY_Louisville-Standiford.Field.724230_TMY3.epw
- USA_LA_Baton.Rouge-Ryan.AP.722317_TMY3.epw
- USA_LA_Lake.Charles.Rgnl.AP.722400_TMY3.epw
- USA_LA_New.Orleans.Intl.AP.722310_TMY3.epw
- USA_LA_Shreveport.Rgnl.AP.722480_TMY3.epw
- USA_MA_Boston-Logan.Intl.AP.725090_TMY3.epw
- USA_MA_Worcester.Rgnl.AP.725095_TMY3.epw
- USA_MD_Baltimore-Washington.Intl.AP.724060_TMY3.epw
- USA_ME_Caribou.Muni.AP.727120_TMY3.epw
- USA_ME_Portland.Intl.Jetport.726060_TMY3.epw
- USA_MI_Alpena.County.Rgnl.AP.726390_TMY3.epw
- USA_MI_Detroit.Metro.AP.725370_TMY3.epw
- USA_MI_Flint-Bishop.Intl.AP.726370_TMY3.epw
- USA_MI_Grand.Rapids-Kent.County.Intl.AP.726350_TMY3.epw
- USA_MI_Houghton-Lake.Roscommon.County.AP.726380_TMY3.epw
- USA_MI_Lansing-Capital.City.AP.725390_TMY3.epw
- USA_MI_Muskegon.County.AP.726360_TMY3.epw
- USA_MI_Sault.Ste.Marie-Sanderson.Field.727340_TMY3.epw
- USA_MI_Traverse.City-Cherry.Capital.AP.726387_TMY3.epw
- USA_MN_Duluth.Intl.AP.727450_TMY3.epw
- USA_MN_International.Falls.Intl.AP.727470_TMY3.epw
- USA_MN_Minneapolis-St.Paul.Intl.AP.726580_TMY3.epw
- USA_MN_Rochester.Intl.AP.726440_TMY3.epw
- USA_MN_St.Cloud.Muni.AP.726550_TMY3.epw
- USA_MO_Columbia.Rgnl.AP.724450_TMY3.epw
- USA_MO_Kansas.City.Intl.AP.724460_TMY3.epw
- USA_MO_Springfield.Rgnl.AP.724400_TMY3.epw
- USA_MO_St.Louis-Lambert.Intl.AP.724340_TMY3.epw
- USA_MS_Jackson.Intl.AP.722350_TMY3.epw
- USA_MS_Meridian-Key.Field.722340_TMY3.epw
- USA_MT_Billings-Logan.Intl.AP.726770_TMY3.epw
- USA_MT_Cut.Bank.Muni.AP.727796_TMY3.epw
- USA_MT_Glasgow.Intl.AP.727680_TMY3.epw
- USA_MT_Great.Falls.Intl.AP.727750_TMY3.epw
- USA_MT_Helena.Rgnl.AP.727720_TMY3.epw
- USA_MT_Kalispell-Glacier.Park.Intl.AP.727790_TMY3.epw
- USA_MT_Lewistown.Muni.AP.726776_TMY3.epw
- USA_MT_Miles.City.Muni.AP.742300_TMY3.epw
- USA_MT_Missoula.Intl.AP.727730_TMY3.epw
- USA_NC_Asheville.Rgnl.AP.723150_TMY3.epw
- USA_NC_Cape.Hatteras.723040_TMY3.epw
- USA_NC_Charlotte-Douglas.Intl.AP.723140_TMY3.epw
- USA_NC_Greensboro-Piedmont.Triad.Intl.AP.723170_TMY3.epw
- USA_NC_Raleigh-Durham.Intl.AP.723060_TMY3.epw
- USA_NC_Wilmington.Intl.AP.723013_TMY3.epw
- USA_ND_Bismarck.Muni.AP.727640_TMY3.epw
- USA_ND_Fargo-Hector.Intl.AP.727530_TMY3.epw
- USA_ND_Minot.Intl.AP.727676_TMY3.epw
- USA_NE_Grand.Island-Central.Nebraska.Rgnl.AP.725520_TMY3.epw
- USA_NE_Norfolk-Karl.Stefan.Mem.AP.725560_TMY3.epw
- USA_NE_North.Platte.Rgnl.AP.725620_TMY3.epw
- USA_NE_Omaha-Eppley.Airfield.725500_TMY3.epw
- USA_NE_Scottsbluff-W.B.Heilig.Field.725660_TMY3.epw
- USA_NH_Concord.Muni.AP.726050_TMY3.epw
- USA_NJ_Atlantic.City.Intl.AP.724070_TMY3.epw
- USA_NJ_Newark.Intl.AP.725020_TMY3.epw
- USA_NM_Albuquerque.Intl.AP.723650_TMY3.epw
- USA_NM_Tucumcari.AP.723676_TMY3.epw
- USA_NV_Elko.Muni.AP.725825_TMY3.epw
- USA_NV_Ely-Yelland.Field.724860_TMY3.epw
- USA_NV_Las.Vegas-McCarran.Intl.AP.723860_TMY3.epw
- USA_NV_Reno-Tahoe.Intl.AP.724880_TMY3.epw
- USA_NV_Tonopah.AP.724855_TMY3.epw
- USA_NV_Winnemucca.Muni.AP.725830_TMY3.epw
- USA_NY_Albany.County.AP.725180_TMY3.epw
- USA_NY_Binghamton-Edwin.A.Link.Field.725150_TMY3.epw
- USA_NY_Buffalo-Greater.Buffalo.Intl.AP.725280_TMY3.epw
- USA_NY_Massena.AP.726223_TMY3.epw
- USA_NY_New.York-J.F.Kennedy.Intl.AP.744860_TMY3.epw
- USA_NY_Rochester-Greater.Rochester.Intl.AP.725290_TMY3.epw
- USA_NY_Syracuse-Hancock.Intl.AP.725190_TMY3.epw
- USA_OH_Akron.Canton.Rgnl.AP.725210_TMY3.epw
- USA_OH_Cleveland-Hopkins.Intl.AP.725240_TMY3.epw
- USA_OH_Columbus-Port.Columbus.Intl.AP.724280_TMY3.epw
- USA_OH_Dayton.Intl.AP.724290_TMY3.epw
- USA_OH_Mansfield-Lahm.Muni.AP.725246_TMY3.epw
- USA_OH_Toledo.Express.AP.725360_TMY3.epw
- USA_OH_Youngstown.Rgnl.AP.725250_TMY3.epw
- USA_OK_Oklahoma.City-Will.Rogers.World.AP.723530_TMY3.epw
- USA_OK_Tulsa.Intl.AP.723560_TMY3.epw
- USA_OR_Astoria.Rgnl.AP.727910_TMY3.epw
- USA_OR_Burns.Muni.AP.726830_TMY3.epw
- USA_OR_Eugene-Mahlon.Sweet.AP.726930_TMY3.epw
- USA_OR_Medford-Rogue.Valley.Intl.AP.725970_TMY3.epw
- USA_OR_North.Bend.Muni.AP.726917_TMY3.epw
- USA_OR_Pendleton-Eastern.Oregon.Rgnl.AP.726880_TMY3.epw
- USA_OR_Portland.Intl.AP.726980_TMY3.epw
- USA_OR_Redmond-Roberts.Field.726835_TMY3.epw
- USA_OR_Salem-McNary.Field.726940_TMY3.epw
- USA_PA_Allentown-Lehigh.Valley.Intl.AP.725170_TMY3.epw
- USA_PA_Bradford.Rgnl.AP.725266_TMY3.epw
- USA_PA_Erie.Intl.AP.725260_TMY3.epw
- USA_PA_Harrisburg-Capital.City.AP.725118_TMY3.epw
- USA_PA_Philadelphia.Intl.AP.724080_TMY3.epw
- USA_PA_Pittsburgh.Intl.AP.725200_TMY3.epw
- USA_PA_Wilkes-Barre-Scranton.Intl.AP.725130_TMY3.epw
- USA_PA_Williamsport.Rgnl.AP.725140_TMY3.epw
- USA_RI_Providence-T.F.Green.State.AP.725070_TMY3.epw
- USA_SC_Charleston.Intl.AP.722080_TMY3.epw
- USA_SC_Columbia.Metro.AP.723100_TMY3.epw
- USA_SC_Greer.Greenville-Spartanburg.AP.723120_TMY3.epw
- USA_SD_Huron.Rgnl.AP.726540_TMY3.epw
- USA_SD_Pierre.Muni.AP.726686_TMY3.epw
- USA_SD_Rapid.City.Rgnl.AP.726620_TMY3.epw
- USA_SD_Sioux.Falls-Foss.Field.726510_TMY3.epw
- USA_TN_Bristol-TriCities.Rgnl.AP.723183_TMY3.epw
- USA_TN_Chattanooga-Lovell.Field.AP.723240_TMY3.epw
- USA_TN_Knoxville-McGhee.Tyson.AP.723260_TMY3.epw
- USA_TN_Memphis.Intl.AP.723340_TMY3.epw
- USA_TN_Nashville.Intl.AP.723270_TMY3.epw
- USA_TX_Abilene.Rgnl.AP.722660_TMY3.epw
- USA_TX_Amarillo.Intl.AP.723630_TMY3.epw
- USA_TX_Austin-Mueller.Muni.AP.722540_TMY3.epw
- USA_TX_Brownsville-South.Padre.Island.AP.722500_TMY3.epw
- USA_TX_Corpus.Christi.Intl.AP.722510_TMY3.epw
- USA_TX_Dallas-Fort.Worth.Intl.AP.722590_TMY3.epw
- USA_TX_El.Paso.Intl.AP.722700_TMY3.epw
- USA_TX_Houston-Bush.Intercontinental.AP.722430_TMY3.epw
- USA_TX_Lubbock.Intl.AP.722670_TMY3.epw
- USA_TX_Lufkin-Angelina.Co.AP.722446_TMY3.epw
- USA_TX_Midland.Intl.AP.722650_TMY3.epw
- USA_TX_Port.Arthur-Jefferson.Co.AP.722410_TMY3.epw
- USA_TX_San.Angelo-Mathis.AP.722630_TMY3.epw
- USA_TX_San.Antonio.Intl.AP.722530_TMY3.epw
- USA_TX_Victoria.Rgnl.AP.722550_TMY3.epw
- USA_TX_Waco.Rgnl.AP.722560_TMY3.epw
- USA_TX_Wichita.Falls.Muni.AP.723510_TMY3.epw
- USA_UT_Cedar.City.Muni.AP.724755_TMY3.epw
- USA_UT_Salt.Lake.City.Intl.AP.725720_TMY3.epw
- USA_VA_Lynchburg.Rgnl.AP-Preston.Glen.Field.724100_TMY3.epw
- USA_VA_Norfolk.Intl.AP.723080_TMY3.epw
- USA_VA_Richmond.Intl.AP.724010_TMY3.epw
- USA_VA_Roanoke.Rgnl.AP-Woodrum.Field.724110_TMY3.epw
- USA_VA_Sterling-Washington.Dulles.Intl.AP.724030_TMY3.epw
- USA_VT_Burlington.Intl.AP.726170_TMY3.epw
- USA_WA_Olympia.AP.727920_TMY3.epw
- USA_WA_Quillayute.State.AP.727970_TMY3.epw
- USA_WA_Seattle-Tacoma.Intl.AP.727930_TMY3.epw
- USA_WA_Spokane.Intl.AP.727850_TMY3.epw
- USA_WA_Yakima.Air.Terminal-McAllister.Field.727810_TMY3.epw
- USA_WI_Eau.Claire.County.AP.726435_TMY3.epw
- USA_WI_Green.Bay-Austin.Straubel.Intl.AP.726450_TMY3.epw
- USA_WI_La.Crosse.Muni.AP.726430_TMY3.epw
- USA_WI_Madison-Dane.County.Rgnl.AP.726410_TMY3.epw
- USA_WI_Milwaukee-Mitchell.Intl.AP.726400_TMY3.epw
- USA_WV_Charleston-Yeager.AP.724140_TMY3.epw
- USA_WV_Elkins-Randolph.County.AP.724170_TMY3.epw
- USA_WV_Huntington-Tri.State.Walker.Long.Field.724250_TMY3.epw
- USA_WY_Casper-Natrona.County.Intl.AP.725690_TMY3.epw
- USA_WY_Cheyenne.Muni.AP.725640_TMY3.epw
- USA_WY_Green.River-Greater.Green.River.Intergalactic.Spaceport.725744_TMY3.epw
- USA_WY_Lander-Hunt.Field.725760_TMY3.epw
- USA_WY_Sheridan.County.AP.726660_TMY3.epw


## Location Region
<u>Description:</u> The housing characteristic "Location Region" describes the distribution of building within the different U.S. Census Regions.

<u>Category:</u> Location

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. US Census Regions, (<https://www2.census.gov/geo/docs/maps-data/maps/reg_div.txt>)

#### Assumptions: 

NaN

#### Dependencies: 

- None

#### Options: 

- CR02
- CR05
- CR03
- CR04
- CR06
- CR07
- CR08
- CR09
- CR10
- CR11


## Mechanical Ventilation
<u>Description:</u> The housing characteristic "Mechanical Ventilation" describes the types of mechanical ventilation used for buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. Not Used

#### Assumptions: 

It is assumed that the buildings do not use mechanical ventilation (i.e. with fans) to aid in increasing the air change rate.

#### Dependencies: 

- None

#### Options: 

- None


## Misc Extra Refrigerator
<u>Description:</u> The housing characteristic "Misc Extra Refrigerator" describes the a second refrigerator in buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pratt 1989, (<https://elcap.nwcouncil.org/Documents/Electric%20Energy%20Use%20Single%20Family.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Pratt1989, address = {Richland, WA, USA},
			author = {Pratt, R. G. and Conner, C. C. and Richman, E. E. and Ritland, K. G. and Sandusky, W. F. and Taylor, M. E.},
			institution = {Pacific Northwest National Laboratory},
			number = {DOE/BP-13795-21},
			publisher = {Bonneville Power Administration},
			title = {{Description of Electric Energy Use in Single-Family Residences in the Pacific Northwest}},
			url = {https://elcap.nwcouncil.org/Documents/Electric Energy Use Single Family.pdf},
			year = {1989} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are from the Building America Analysis Spreadsheets and national average data. Some of the data inputs for the measure are listed in the 2014 HSP. The data for the spreadsheets are based on Pratt et al. 1989.

#### Dependencies: 

- None

#### Options: 

- EF 6.9, National Average


## Misc Freezer
<u>Description:</u> The housing characteristic "Misc Freezer" describes an additional freezers in buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pratt 1989, (<https://elcap.nwcouncil.org/Documents/Electric%20Energy%20Use%20Single%20Family.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Pratt1989, address = {Richland, WA, USA},
			author = {Pratt, R. G. and Conner, C. C. and Richman, E. E. and Ritland, K. G. and Sandusky, W. F. and Taylor, M. E.},
			institution = {Pacific Northwest National Laboratory},
			number = {DOE/BP-13795-21},
			publisher = {Bonneville Power Administration},
			title = {{Description of Electric Energy Use in Single-Family Residences in the Pacific Northwest}},
			url = {https://elcap.nwcouncil.org/Documents/Electric Energy Use Single Family.pdf},
			year = {1989} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are from the Building America Analysis Spreadsheets and national average data. Some of the data inputs for the measure are listed in the 2014 HSP.

#### Dependencies: 

- None

#### Options: 

- EF 12, National Average


## Misc Gas Fireplace
<u>Description:</u> The housing characteristic "Misc Gas Fireplace" describes the use of gas fire places in buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are from the schedules are taken from Pinckard 2005 as other MELs. Some of the data inputs for the measure are listed in the 2014 HSP.

#### Dependencies: 

- None

#### Options: 

- National Average


## Misc Gas Grill
<u>Description:</u> The housing characteristic "Misc Gas Grill" describes the use of gas grills hooked up to the building's gas line in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are from the schedules are taken from Pinckard 2005 as other MELs. Some of the data inputs for the measure are listed in the 2014 HSP.

#### Dependencies: 

- None

#### Options: 

- National Average


## Misc Gas Lighting
<u>Description:</u> The housing characteristic "Misc Gas Lighting" describes the use of gas lighting for buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are from the schedules are taken from Pinckard 2005 as other MELs. Some of the data inputs for the measure are listed in the 2014 HSP.

#### Dependencies: 

- None

#### Options: 

- National Average


## Misc Hot Tub Spa
<u>Description:</u> The housing characteristic "Misc Hot Tub Spa" describes the use of hot tubs/spas in buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are derived from Pinchard-2005. The national average values are taken from 2014 HSP and BA Analysis Spreadsheets.

#### Dependencies: 

- None

#### Options: 

- National Average


## Misc Pool
<u>Description:</u> The housing characteristic "Misc Pool" describes the presence of pools on properties in the buildings stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are derived from Pinchard-2005. The national average values are taken from 2014 HSP and BA Analysis Spreadsheets.

#### Dependencies: 

- None

#### Options: 

- National Average


## Misc Well Pump
<u>Description:</u> The housing characteristic "Misc Well Pump" describes the presence and usage of water well pumps for buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

#### Assumptions: 

The schedules are from the schedules are taken from Pinckard 2005 as other MELs. Some of the data inputs for the measure are listed in the 2014 HSP.

#### Dependencies: 

- None

#### Options: 

- National Average


## Natural Ventilation
<u>Description:</u> The housing characteristic "Natural Ventilation" describes the frequency in which the building uses natural ventilation to increase the air change rate of buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

#### Assumptions: 

The 3-days a week comes from the 2014 HSP in their description on page 50.

#### Dependencies: 

- None

#### Options: 

- Year-Round, 3 days/wk


## Occupants
<u>Description:</u> The housing characteristic "Occupants" describes the number of occupants, size of the internal gains, and occupancy schedules for occupants in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. ASHRAE Handbook 2009, (<https://www.techstreet.com/standards/2017-ashrae-handbook-fundamentals-i-p-includes-cd-in-i-p-and-si-editions?gclid=CjwKCAjwhLHaBRAGEiwAHCgG3sgDxJNKBlb47bVYG9qAWbZbL7DvlOoQtTA0Mng9PsKDLPybrXqyuhoCotcQAvD_BwE&sid=goog&product_id=1975069>)

	<u>Bibtex Citation</u>

		@misc{AmericanSocietyofHeating2009, address = {Atlanta, GA :},
			author = {{American Society of Heating},
			Refrigerating and Air-Conditioning Engineers. T A - T T -},
			edition = {SI ed. NV - 1 online resource (1 volume (various pagings)) : illustrations},
			isbn = {9781615831708 1615831703 9781933742557 1933742550},
			language = {English},publisher = {American Society of Heating, Refrigeration and Air-Conditioning Engineers,},title = {{2009 ASHRAE handbook : fundamentals.}},
			url = {https://www.techstreet.com/standards/2017-ashrae-handbook-fundamentals-i-p-includes-cd-in-i-p-and-si-editions?gclid=CjwKCAjwhLHaBRAGEiwAHCgG3sgDxJNKBlb47bVYG9qAWbZbL7DvlOoQtTA0Mng9PsKDLPybrXqyuhoCotcQAvD_BwE&sid=goog&product_id=1975069},
			year = {2009}}

#### Assumptions: 

The data from the measure comes from the 2014 HSP and ASHRAE Fundamentals Handbook 2009.

#### Dependencies: 

- None

#### Options: 

- Auto


## Orientation
<u>Description:</u> The housing characteristic "Orientation" describes the distribution of orientation of buildings in the building stock.

<u>Category:</u> Geometry

#### Data Sources:

1. OSM, (<https://www.openstreetmap.org/#map=4/38.01/-95.84>)

	<u>Bibtex Citation</u>

		@misc{OpenStreetMapFoundation, author = {{OpenStreetMap Foundation}},
			title = {{OpenStreetMaps}},
			url = {https://www.openstreetmap.org/{\#}map=4/38.01/-95.84} }

	<u>Remarks:</u> Data obtained by RadiantLabs. Data not for distribution (http://www.radiantlabs.co/).

#### Assumptions: 

NaN

#### Dependencies: 

- Location EPW

#### Options: 

- North
- South
- East
- West


## Overhangs
<u>Description:</u> The housing characteristic "Overhangs" describes the distribution and use of overhangs for windows shading on different sides of buildings in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Not Used

#### Assumptions: 

It is assumed that overhangs are not used in the building stock.

#### Dependencies: 

- None

#### Options: 

- None


## PV
<u>Description:</u> The housing characteristic "PV" describes the use of photovoltaic modules for buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. Not Used

#### Assumptions: 

It is assumed that the building stock does not use PV systems.

#### Dependencies: 

- None

#### Options: 

- None


## Plug Loads
<u>Description:</u> The housing characteristic "Plug Loads" describe the distribution of different usage levels of AC electrical plug loads for buildings in the buildings stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

The schedules are from the schedules are taken from Pinckard 2005 as other MELs. Some of the data inputs for the measure are listed in the 2014 HSP.

#### Dependencies: 

- Usage Level

#### Options: 

- 50%
- 100%
- 200%


## Range Spot Vent Hour
<u>Description:</u> The housing characteristic "Range Spot Vent Hour" describes the distribution of when range ventilation is used during cooking for buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

2. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

#### Assumptions: 

Schedules based on Building America Analysis Spreadsheets for cooking range. The schedule can be seen in Figure 22 for the 2014 HSP Range/oven normalized energy use profile.

#### Dependencies: 

- None

#### Options: 

- Hour0
- Hour1
- Hour2
- Hour3
- Hour4
- Hour5
- Hour6
- Hour7
- Hour8
- Hour9
- Hour10
- Hour11
- Hour12
- Hour13
- Hour14
- Hour15
- Hour16
- Hour17
- Hour18
- Hour19
- Hour20
- Hour21
- Hour22
- Hour23


## Refrigerator
<u>Description:</u> The housing characteristic "Refrigerator" describes the usage, performance, and schedules of the primary refrigerator for buildings in the building stock.

<u>Category:</u> Internal Gains and MELs

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

	<u>Remarks:</u> How is the energy factor (EF) calculated and how do you translate michaelbluejay.com table data to efficiency?

2. michaelbluejay.com, (<https://michaelbluejay.com/electricity/>)

	<u>Bibtex Citation</u>

		@misc{Bluejay, author = {Bluejay, Michael},
			title = {{Saving Electricity: How to Save Electricity}},
			url = {https://michaelbluejay.com/electricity/} }

	<u>Remarks:</u> How is the energy factor (EF) calculated and how do you translate michaelbluejay.com table data to efficiency?

3. BA Analysis Spreadsheets, (<https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets>)

	<u>Bibtex Citation</u>

		@misc{U.S.DepartmentofEnergy2011, address = {Washington, D.C., USA},
			author = {{U.S. Department of Energy}},
			title = {{Building America Analysis Spreadsheets}},
			url = {https://www.energy.gov/eere/buildings/building-america-analysis-spreadsheets},
			year = {2011} }

	<u>Remarks:</u> How is the energy factor (EF) calculated and how do you translate michaelbluejay.com table data to efficiency?

4. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

	<u>Remarks:</u> How is the energy factor (EF) calculated and how do you translate michaelbluejay.com table data to efficiency?

5. Pratt 1989, (<https://elcap.nwcouncil.org/Documents/Electric%20Energy%20Use%20Single%20Family.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Pratt1989, address = {Richland, WA, USA},
			author = {Pratt, R. G. and Conner, C. C. and Richman, E. E. and Ritland, K. G. and Sandusky, W. F. and Taylor, M. E.},
			institution = {Pacific Northwest National Laboratory},
			number = {DOE/BP-13795-21},
			publisher = {Bonneville Power Administration},
			title = {{Description of Electric Energy Use in Single-Family Residences in the Pacific Northwest}},
			url = {https://elcap.nwcouncil.org/Documents/Electric Energy Use Single Family.pdf},
			year = {1989} }

	<u>Remarks:</u> How is the energy factor (EF) calculated and how do you translate michaelbluejay.com table data to efficiency?

#### Assumptions: 

The distributions are created from RECS-2009 from the ages of refrigerators, but the efficiencies based on age are taken from michaelbluejay.com. The schedules are from the Building America Analysis Spreadsheets and national average data. Some of the data inputs for the measure are listed in the 2014 HSP. The data for the spreadsheets are based on Pratt et al. 1989.

#### Dependencies: 

- Usage Level

#### Options: 

- EF 6.7
- EF 10.2
- EF 10.5
- EF 15.9


## Roof Material
<u>Description:</u> The housing characteristic "Roof Material" describes the distribution of roofing materials and their thermal properties for buildings in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. HSP-2014, (<https://www.nrel.gov/docs/fy14osti/60988.pdf>)

	<u>Bibtex Citation</u>

		@techreport{Wilson2014, abstract = {Building America's House Simulation Protocols report is designed to assist researchers in tracking the progress of multiyear, whole-building energy reduction against research goals for new and existing homes. These protocols are preloaded into BEopt and use a consistent approach for defining a reference building, so that all projects can be compared to each other. The steps involved in conducting performance analysis include: - Defining the appropriate reference building. Various climate regions, house sizes, and house ages require slightly different reference buildings; this report guides the user through to the most appropriate fit for the project. - Selecting energy upgrades. With an overwhelming number of options and technologies on the market, it can be difficult to narrow down the best choices for reaching savings goals. BEopt software can easily be used to determine the most cost-effective solutions for each project. - Determining the energy savings. After a project has been completed, the measures selected can be compared to the appropriate reference building using BEopt and the overall energy savings can be determined.},
			address = {Golden, Co, USA},
			author = {Wilson, E. and {Engebrecht Metzger},
			C . and Horowitz, S. and Hendron, R.},
			institution = {National Renewable Energy Laboratory},
			isbn = {null},
			keywords = {NREL,building performance simulation,residential buildings},
			number = {December},
			title = {{2014 Building America House Simulation Protocols (NREL/TP-5500-60988)}},
			url = {https://www.nrel.gov/docs/fy14osti/60988.pdf},
			year = {2014} }

#### Assumptions: 

It is assumed that the building stock has only asphalt shingled roofs.

#### Dependencies: 

- None

#### Options: 

- Asphalt Shingles, Medium


## Solar Hot Water
<u>Description:</u> The housing characteristic "Solar Hot Water" describes the solar heating hot water system for buildings in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. Not Used

#### Assumptions: 

It is assumed that solar hot water systems are not used in the building stock.

#### Dependencies: 

- None

#### Options: 

- None


## Usage Level
<u>Description:</u> The housing characteristic "Usage Level" describes the distribution of the population that are High, Medium, and High users of appliances, plug loads, and MELs.

<u>Category:</u> Occupancy

#### Data Sources:

1. No Data Source Needed

#### Assumptions: 

It is assumed that a low user is 25%, a medium user is 50%, and a high user is 25% of the population.

#### Dependencies: 

- None

#### Options: 

- Low
- Medium
- High
- Average


## Vintage
<u>Description:</u> The housing characteristic "Vintage" describes the distribution of when building were built in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. AHS-2013, (<https://www.census.gov/programs-surveys/ahs/data.2013.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2013, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{AHS 2013 Public Use File (PUF)}},
			year = {2013}}

#### Assumptions: 

Single family detached buildings only

#### Dependencies: 

- Location EPW

#### Options: 

- <1950
- 1950s
- 1960s
- 1970s
- 1980s
- 1990s
- 2000s


## Vintage ACS
<u>Description:</u> The housing characteristic "Vintage ACS" describes the distribution of when building were built in the building stock. The ACS indicates the data comes from ACS.

<u>Category:</u> Construction

#### Data Sources:

1. ACS 2011-2015, (<https://www.census.gov/programs-surveys/acs/data/pums.html>)

	<u>Bibtex Citation</u>

		@misc{U.S.CensusBureau2015, address = {Washington, D.C., USA},
			author = {{U.S. Census Bureau}},
			title = {{2011-2015 ACS 5-year PUMS}},
			url = {https://www.census.gov/programs-surveys/acs/data/pums.html},
			year = {2015} }

#### Assumptions: 

NaN

#### Dependencies: 

- Location EPW

#### Options: 

- <1940
- 1940s
- 1950s
- 1960s
- 1970s
- 1980s
- 1990s
- 2000s
- 2010s


## Water Heater
<u>Description:</u> The housing characteristic "Water Heater" describes the distribution of different types of water heaters and heating fuel types in the building stock.

<u>Category:</u> Hot Water, HVAC, and Ventilation

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

2. Pinckard-2005, (<https://www.osti.gov/servlets/purl/842508>)

	<u>Bibtex Citation</u>

		@techreport{Pinckard2005, abstract = {The Home Energy Saver (HES, http://HomeEnergySaver.lbl.gov) is an interactive web site designed to help residential consumers make decisions about energy use in their homes. This report describes the underlying methods and data for estimating energy consumption. Using engineering models, the site estimates energy consumption for six major categories (end uses); heating, cooling, water heating, major appliances, lighting, and miscellaneous equipment. The approach taken by the Home Energy Saver is to provide users with initial results based on a minimum of user input, allowing progressively greater control in specifying the characteristics of the house and energy consuming appliances. Outputs include energy consumption (by fuel and end use), energy-related emissions (carbon dioxide), energy bills (total and by fuel and end use), and energy saving recommendations. Real-world electricity tariffs are used for many locations, making the bill estimates even more accurate. Where information about the house is not available from the user, default values are used based on end-use surveys and engineering studies. An extensive body of qualitative decision-support information augments the analytical results. ii},
			address = {Berkeley, CA, USA},
			author = {Pinckard, Margaret J. and Brown, Richard E. and Mills, Evan and Lutz, James D and Moezzi, Mithra M and Atkinson, Celina and Bolduc, Chris and Homan, Gregory K. and Coughlin, Katie},
			booktitle = {LBNL-51938},
			institution = {Lawrence Berkeley National Laboratory},
			keywords = {calculating residential,documentation residential energy efficiency,home energy saver technical},
			title = {{Documentation of Calculation Methodology , Input Data , and Infrastructure for the Home Energy Saver Web Site}},
			url = {https://www.osti.gov/servlets/purl/842508},
			year = {2005} }

#### Assumptions: 

The types are taken from RECS along with the age of the water heater. The efficiencies are taken from HES (Pinckard et al. 2005). If there is no heating fuel and no data, it is assumed it is a standard electric water heater. If there is no data, it is assumed that the water heater is a standard water heater with the primary heating fuel.

#### Dependencies: 

- Heating Fuel
- Location Region

#### Options: 

- Electric Standard
- Electric Premium
- Electric Tankless
- Gas Standard
- Gas Premium
- Gas Tankless
- Oil Standard
- Oil Premium
- FIXME Oil Indirect
- Propane Standard
- Propane Premium
- Propane Tankless
- FIXME Other Fuel


## Window Areas
<u>Description:</u> The housing characteristic "Window Areas" describes the window-wall-ratio (WWR) distributions for the front, back, left, and right sides of buildings in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. Expert Elicitation

#### Assumptions: 

It is assumed that all buildings in the building stock have a WWR of 0.15 for each side of the building.

#### Dependencies: 

- None

#### Options: 

- F15 B15 L15 R15


## Windows
<u>Description:</u> The housing characteristic "Windows" describes the distribution of single pane, double pane, or no windows for buildings in the building stock.

<u>Category:</u> Construction

#### Data Sources:

1. RECS-2009, (<https://www.eia.gov/consumption/residential/data/2009/>)

	<u>Bibtex Citation</u>

		@misc{U.S.EnergyInformationAdministration2009, address = {Washington, D.C., USA},
			author = {{U.S. Energy Information Administration}},
			title = {{Residential Energy Consumption Survey (RECS)}},
			url = {https://www.eia.gov/consumption/residential/index.php},
			year = {2009} }

#### Assumptions: 

The data mainly comes from RECS, although it is assumed that all buildings in CR03 and CR07 are single pane. Frame type assignments are based on vintage using expert elicitation.

#### Dependencies: 

- Location Region
- Vintage
- Geometry Building Type

#### Options: 

- 1 Pane
- 2+ Pane
- No Windows


