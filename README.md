# Leisure-park-design
An ArcGIS Pro project redesigning a harbour using lighted data

**Objective**: To convert the exciting harbour into a new economic zone catering to different investors.

**Tools**: ArcGIS Pro, ArcGIS Online (Webmap, Survey123), AutoCAD

**Data**:
The data is an AutoDesk drawing file (.dwg) showing the harbour and wind turbine factory layout. 

**Data preparation and cleaning**

The data is first imported into ArcGIS Pro using the Conversion Tools from the geoprocessing toolbox. 
From the Conversion tools, the To Geodatabase tool was used to convert the .dwg data to a geodatabase with four feature classes.

Specify the spatial reference and run the tool.

To redesign the harbour, we will focus on the polygon and polyline feature classes, using the delete features menu in the Edit ribbon to delete the layouts of the wind turbines and any sections that are not useful for the new project. 
However, the parking polygons and polylines must be preserved.

**Create Features**

For my project, I chose to design a community leisure centre. The key aspects of the centre include:
Sports facilities which include an indoor gymnasium, pool and auditorium
Water games including a water park
Commercial activities: a cinema, foodcourt and a shopping centre
Infrastructure: the toilets, sitting spots, offices and store rooms
renting zones: electric vehicle charging, mobility rent
Nature zones: consist of landscaped areas and hedges
These were added to the layouts as polygon feature classes.

Each feature created should have the following columns:
Name Text
Area Double
Interest_in Text
Category Text
ArcGIS Pro automatically calculates the length and area of these polygons, however, as part of the exercise, I calculated the area of each polygon using Check Geometry Attributes under Data Management Tools. This menu can also be accessed by right-clicking on a column and selecting the calculate geometry option.

The category for each polygon depends on its size, polygons less than 1000m2 are small, larger than 10,000m2 are large and in between are medium

For the Interest_in column, we need to create coded domains for users to indicate if they are interested in a project or not.

Coded domains can be created by right-clicking on the geodatabase and selecting the domain or from the Domain tool in the toolbox.

**Sharing the work**

To share the final output, the features are extracted as shape files using the conversion tool 

The containing folder is then added to a zip file. To find out more about supported formats, check ArcGIS online documentation here.

**Other activities**:

Web_Area:Other activities include creating a new column, web_area, to re-calculate the area using Arcade. It is better to use the AreaGeodetic function as it is more accurate than the simple Area function. Note that there are minor variations in the calculated area.

