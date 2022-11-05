# SensorWeb (Work in Progress!)

## Spatial Data Infrastructure

The ability to access, process, and integrate data from various sources for mapping, visualisation, and other forms of representation and analysis is known as Interoperability. Often organisations such as the European Union share the data among themselves to insure data interoperability. But without specific standards, interoperability is not possible. To ensure the specific needs of each data and its formats, we have Spatial Data Infrastructure (SDI).
A Spatial Data Infrastructure denotes a collection of technologies, policies and institutional arrangements to serve as a basis for discovery, access and processing of geospatial data to ensure interoperability and improved access to spatial data.

SDI's goals are to: 

+ Lower geographic information costs while making geographic data more accessible, 
+ Increase the benefits of using available spatial data, and 
+ Establish key partnerships between states, counties, cities, academia, and the private sector.

OGC standards from the International Organization for Standardization (ISO) Technical Committee 211 are essential elements in SDIs around the world. This is because SDIs are data and service networks, and networks depend on open standards.

Examples: 

Infrastructure for Spatial Information in the European Community (INSPIRE) is a European Union (EU) directive to establish a SDI via the Internet that allows for the standardised sharing of geographic information.

Global Earth Observation System of Systems (GEOSS) facilitates the sharing of environmental data and information collected from the large array of observing systems contributed by countries and organizations within GEO

One such real time observation data would be sensor data. 

## Sensor Data
Data that are collected from various heterogeneous internet of things (IoT) devices. Sensor data is the output of a device that detects and responds to some type of input from the physical environment. The output may be used to provide information or input to another system or to guide a process. Sensors can be used to detect just about any physical element. Here are a few examples of sensors, just to give an idea of the number and diversity of their applications:

+ A photosensor detects the presence of visible light, infrared transmission (IR) and/or ultraviolet (UV) energy. 
+ A temperature sensor detects the land surface temperature on the ground.

For example: In kaggle, a dataset sharing platform we have many sensor datasets. Air Quality Dataset is the most commonly used sensordata. This dataset contains the responses of a gas multisensor device deployed on the field in an Italian city.

***Did you know? Your smartphone is so smart that it can act as a mobile sensor.***

Using Sensor data over other spatial data sources such as remote sensing imageries, CAD has numerous advantages.

Sensors are called “things” in the Internet of Things ecosystem. A sensor network is a computer-accessible network of many, spatially distributed devices that use sensors to monitor environmental conditions such as temperature, pressure. A sensor web is a collection of sensor data and sensor networks that are accessible via the web and can be found and accessed through standard protocols (APIs).

The Open Geospatial Consortium (OGC) aims to make heterogeneous sensor data available for discovery, access and use via interoperable formats and Web services. Much like Hyper Text Markup Language (HTML) and Hypertext Transfer Protocol (HTTP) standards enabled the exchange of any type of information on the Web. Through standardized formats and services the heterogeneity/complexity of different sensor types and measurement outputs is hidden from end-users.

## SWE

The OGC's Sensor Web Enablement (SWE) standards enable developers to make all types of sensors, transducers and sensor data repositories discoverable, accessible and useable via the Web.(OGC) In particular, as main formats, the Observation & Measurement (O&M) standard defines how to model observations and the Sensor Model Language (SensorML) standard may be used to represent metadata about the observing sensor itself.
