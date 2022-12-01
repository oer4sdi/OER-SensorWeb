# SensorWeb (Work in Progress!)

##### Table of Contents  
1. [Understanding the Concepts](#understanding-the-Concepts)  
2. [O&M model](#o&m-model)
3. [SensorThings API](#sensorthings-API)
4. [Practical Session](#practical-session)


# Understanding the Concepts

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

### SWE OGC Standards
The SWE framework includes multiple formats for interoperable sensor data exchange, as well as Web Service specifications for sensor data access. The list below provides an overview of key SWE standards. A sufficient description of the standard is included where applicable. 

<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/200171298-fe996d09-a0e8-4b29-8904-dd184529d417.png' width='400' height='250'>
</p>

The table below explains briefly about the OGC Standards, in the upcoming chapters we can discuss some of the concepts that are relevant for this course indepth.

| OGC Standards | Description |
|---------------|-------------|
| Information Model and Schema |
| **Observations & Measurements Schema (O&M)** | An OGC-adopted standard that defines conceptual models for encoding sensor observations and measurements in both archived and real-time formats |
| **Sensor Model Language (SensorML)** | A standard that the OGC has adopted that outlines common models and an XML Schema for describing sensors systems and processes Eg, Metadata about the Sensors |
| **PUCK Protocol Standard** | The PUCK standard is the most recent addition to the SWE standards suite. PUCK addresses sensor installation and configuration issues by defining a standard instrument protocol for storing and retrieving metadata and other information from the instrument device itself. This standard is specifically for for RS232 and Ethernet-connected instruments |
| **SWE Common Data Model** | The Sensor Web Enablement (SWE) Common Data Model Encoding Standard specifies low-level data models for exchanging sensor-related data between OGC® Sensor Web Enablement (SWE) framework nodes |
| **SWE Service Model** | This standard defines eight packages that define data types for common use across OGC sensor web enablement. The standard can be downloaded via a link on the website http://www.opengeospatial.org/standards/swes |
| Web Services Portal |
| **Sensor Observations Service (SOS)** | The SOS is the central Web service within the SWE framework for performing CRUD operations. This is the bridge that connects a client to an observation repository or a near real-time sensor channel Eg, With SOS one can retrieve information about the sensorencoded in sensorML |
| **Sensor Planning Service (SPS)** | An OGC standard defining a standard web service interface for requesting user-driven acquisitions and observations. This functions as a bridge between a client and a sensor collection management environment |
| **SensorThings API** | the SensorThings API is targeted to allow homogeneous access to heterogeneous smart sensors within the Web of Things approach. The standard is located at http://docs.opengeospatial.org/is/15-078r6/15-078r6.html |

Some Standards are not considered to be OGC standards, nonetheless they are allowed in the services provided within SWE framework. These are all documents provided by OGC standards.
| Web Service Protocals | Description |
| --------------------- | ----------- |
| **Sensor Alert Service (SAS)** | A discussion paper published by the OGC that describes a web service interface for publishing and subscribing to sensor alerts |
| **Web Notification Services (WNS)** | A document describing the web service interface for asynchronous delivery of messages or alerts from SAS and SPS or other web services. Transactions that take a long time, for example, necessitate functions to support asynchronous communications between a user and the corresponding service, or between two services |

### What is considered as a Sensor Data Source?
#### Sensor data sources - deals with what sources are they? and which is ideal? how the above standards helps? ( QUIZ cum explanation ) - H5P format


# O&M model
<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/201489207-bf9ca213-91a6-4502-8d46-ede5ed704f81.png'>
</p>

Fig : The simplified version of the Observation and Measurements (O&M) model's general schema diagram from Best practises documentation[1]

> Observation and Measurements standard defines models and XML schemas for observations as well as features involved in sampling when making observations.

Because [IP-based](https://en.wikipedia.org/wiki/Internet_Protocol) sensors are becoming more affordable, anyone can gather and refine detailed environmental information about the world around us, both locally and globally. This way citizens with any background can use these sensors to generate publically available data. Of course, as with everything based on the Internet, as the amount of information and the diversity of the sources producing it grows, so does the quality range of the available information. Organizations that previously deployed and maintained their own sensor networks with proprietary data and control interfaces tailored to their specific software and hardware systems are transitioning to open standards. Even if they do not intend to publish their data on the Internet, they do intend to communicate via IP-based networks.

Each and every sensor data sources can have different formats and information. This pose an issue when exchanging sensor data. To overcome this interoperability issue, O&M becomes a common standardized data model for handling measurement events in various types of sensors, ranging from thermometers inside a closed process to satellites images of the Earth from space. O&M creates a high-level framework for representing sensor observations, measurements, procedures, and metadata, for the implementation of SWE-enabled architectures. O&M, in conjunction with other SWE framework open standards such as SensorML and Sensor Observation Service (SOS), provides a system-independent, internet-enabled method of data exchange between different parts of sensor networks and other systems using sensor information.

Did you Know ? 
> The O&M concepts serve as the foundation for the EU-wide INSPIRE data models for meteorological, climatological, and air quality information, and the structure and capabilities of various environmental observation networks.

#### UML Diagram of Observations
<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/204206653-b5fae81b-74f3-4ab5-aac2-6e885dc7c385.png' height='300'>
</p>
Fig : The simplified version of Observation Entity diagram from Best Practises documentation[1]

According to OGC Standards[2],
> an observation is an act associated with the process that measures an observed property at a specific feature of interest for a specific phenomenon time and records the results. 

To define each entity separately, we will use a generic example: `temperature`. Table 1: Mandatory Properties of an Observation Model

| Entity | Description | Example |
| ------ | ----------- | --------------- |
| `Observed Property / Phenomenon` | a property measured by a sensor | Temperature |
| `Feature of Interest (FoI)` | an abstraction of a real world phenomena which has been georeferenced | Park |
| `Phenomenon Time` | the time instant or period of when the observation happens | 2022-03-06T05:00:00.000Z |
| `Result` | the estimated value of an observedproperty from the Observation | 12°c |
| `Result Time` | the time of the observation’s result after processing was generated| 2022-03-07T05:00:00.000Z |

Note: The temporal parameter in geospatial context is phenomenon time. If the Sensor is capable of post processing, then the time at which a result is posted following post processing would be Result Time.

Table 2: Optional Properties of an Observation Model
| Entity | Description | Examples |
| ------ | ----------- | -------- |
| `Result Quality` | describes the quality of the result owing to the fact that sensor data can be faulty to some extent | 
| `Valid Time` | the time period during which the result may be used. With real time sensor data available, the data is measured and replaced within seconds in some cases | 2022-03-07T05:00:00.000Z |
| `Parameter` | describe any event-specific parameter(could be an environmental, an instrument setting or input) | Altitude |
| `Process` | The process that performs the measurement |  change in resistance of the electric current in a sensor measures temperature |

Note:
1. The Parameter is not a feature of interest or an observation procedure. A `park` may be the feature of interest in the temperature case, but since temperature varies with altitude, `altitude` may be an event-specific parameter.
2. A human observer, a simulator, or a process or algorithm applied are all examples of Process instances.

Look at the exemplary dataset from the USGS hoisted in the FROST Server.

> https://labs.waterdata.usgs.gov/sta/v1.1/Observations

#### QUIZ - (A drag and drop options that user use correctly mention the terms Eg question : When measuring the height of a tree, the height is the observed ObservableProperty, 20m may be the Result of the Observation, and the tree is the FeatureOfInterest.) H5P format #### QUIZ observation examples

### Classification of observation by result type
The Observation model approaches data from the perspective of the data user, emphasizing the semantics of the feature-of-interest and its properties. Whether the feature-of-interest is a discrete or continous observation.

1. Observations whose result is constant

Observations where the outcome of a observation may have a single value or multiple values, but if there are multiple values, those values do not change over the course of the observation with respect to either space or time.

![o m-discrobs](https://user-images.githubusercontent.com/94603960/204206594-5803c760-8199-4d10-859d-165a7a80ac99.png)

Example,
```
A well known example would be Flip-a-Coin, where the odds are always 'HEAD' or 'TAIL' - This would be a Boolean type observation.

How about something in GeoSpatial Context?

Buildings and Roads are features that have distinct boundaries or limits are considered discrete. In mapping, discrete data can be shown 
as a point, line, or a polygon. Points could be cities, lines could be road networks, and polygons could be provinces in a country. 
This features would be Geometry type observation.

```
2. Observations whose result is varies

Observations where the outcome of a observation includes multiple values that change with time, space, or both during the course of the observation. The value of a corresponding observation result shall therefore be a function or coverage(domain extent is the spatiotemporal extent of the feature), respectively. The target feature may be subjected to numerous observations using various sampling methods, so the sampling methods are associated with the act of observation rather than being inherent in the feature-of-interest. To model the coverage, a domain geometry decomposition with specialized sub-geometries is defined to represent the associated feature.

![o m-contobs](https://user-images.githubusercontent.com/94603960/204206553-dacd1b3f-535d-4528-85cd-c07a9fcb9821.png)

What would be a best example for Continous Observation? 
```
Weather is unpredictable and is a good example for continous observation. 
'Temperature' for example, changes over space and time. Here temperature is a discretePointCoverage observation.
Think of any continous observation?
```
#### Quiz ( What is discrete and contimous obs)

## Sensor Observation Service

The Sensor Observation Service (SOS) defines a web service interface for retrieving observations and sensor metadata. The service interface also allows new observations to be published, as well as sensor registration and removal.

Latest version specification can be downloaded from,

> http://www.opengeospatial.org/standards/sos

The SOS Implementation Standard is a key component of the SWE architecture, defining network-centric data representations and operations for accessing and integrating sensor data. This observation data may have been collected by in-situ sensors (e.g. river gauges), moving sensor platforms (e.g. satellites or
unmanned aerial vehicles) or networks of static sensors (e.g. seismic arrays).

The following list presents examples of SOS usage:

+ The US National Oceanic and Atmospheric Administration (NOAA) provides quality controlled ocean data and information through its Integrated Ocean Observing System (IOOS®) SOS: 
+ Wales Air’s Sensor Observation Service (SOS) provides a machine readable access point for air pollution measurements hosted on Air quality Wales: https://airquality.gov.wales/sos-waq/service?service=SOS&request=GetCapabilities

![SOS](https://user-images.githubusercontent.com/94603960/201588754-4a0c348c-f3fc-43d4-bd4d-5cd16f794dbc.png)

### SOS operations
<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/201594795-d5c693a2-0cd6-414a-82ee-5a2b4be53758.png' width='700' height='350'>
</p>

# SensorThings API

## Fundamental Concepts

The terms Internet of Things and Web of Things refer to approaches to integrating smart devices into the Internet. The Internet of Things (IoT) is a network of physical objects—"things"—embedded with sensors, software, and other technologies for connecting and exchanging data with other devices and systems via the internet. In the context of Sensorweb, the `things` here are `Sensors`. Physical things (e.g, Sensors) can share and collect data with minimal human intervention thanks to low-cost computing technologies. The Web of Things (WoT) is a set of standards developed by the World Wide Web Consortium (W3C) to improve the interoperability, and usability of the Internet of Things (IoT). From a technological standpoint, this means that the smart device (e.g., a sensor) is addressable via standard HTTP operations (GET, POST, PUT, etc.), enabling [RESTful](https://www.codecademy.com/article/what-is-rest) access to sensor data (Bröring et al, 2011 a). In short, WoT is a subset of IoT and is based on software standards like REST, HTTP, and URIs to allow devices to communicate with one another.

The Open Geospatial Consortium's Sensor Web Enablement (SWE) framework is a well-established approach for integrating sensors with the Web. A smart device, according to Bröring et al. (2011 b), may respond to data requests using SWE-standardized formats. To be more specific, sensor metadata should be encoded using SensorML, and observation data as O&M. With these format constraints, any other application/component may retrieve the smart device's sensor data in an interoperable, standardized manner.  SWE specifications such as SOS; SPS, and SES are powerful for use cases that are broad and often complex(e.g. disaster management or early warning systems). However, use cases that do not require the full functionality of SWE's data altering, sensor discovery, tasking, and event handling may be easier to realize with the Web of Things approach by treating sensor objects as things. (Liang et al.) The SensorThings API is an open standard, builds on Web protocols and the OGC Sensor Web Enablement standards, and applies an easy-to-use REST-like style.

The OGC SensorThings API is recommended for organizations that require web-based platforms to manage, store, share, and analyze IoT-based sensor observation data. Application developers can use this open standard to connect to various IoT devices and create innovative applications without having to worry about the heterogeneous protocols of various IoT devices, gateways, and services. (Liang et al, 2016)

Github repository for OGC sensorthings API:
> https://github.com/opengeospatial/sensorthings

The SensorThings API may simplify connections between devices-to-devices and devices-to-applications by utilizing efficient REST binding, including a reduced JSON encoding, and the MQTT protocol for sensor access making it a lightweight SWE approach. 

The OGC SensorThings API data model consists of two parts: (1) the Sensing part and (2) the Tasking part. The Sensing part allows IoT devices and applications to CREATE, READ, UPDATE, and DELETE (i.e., HTTP POST, GET, PATCH, and DELETE) IoT data and metadata in a SensorThings service.

## SensorThings API - Sensing Part

![sta-entity](https://user-images.githubusercontent.com/94603960/204211187-c0b85e20-eb8d-4521-97f4-18b7823645cb.png)

The Sensing part is designed based on the OGC/ISO Observation and Measurement (O&M) model. A Thing represents an IoT device or system. A Thing has a Location that is associated with one or more Datastreams. Each Datastream has many Observations from the Sensor and observes one ObservedProperty with one Sensor. Each Observation read by the Sensor identifies a single FeatureOfInterest. These relationships, when combined, provide a flexible standard way to describe and model any sensing system. It enables SensorThings to function as a unified data exchange system for heterogeneous devices across any organization. 

| Terms | Definitions | Example |
| ----- | ----------- | ------- |
| `Things` | The OGC SensorThings API adheres to the ITU-T definition, which states that a thing is an object of the physical world (physical things) or the information world (virtual things) that can be identified and integrated into communication networks [ITU-T] | Temperature Monitoring System |
| `Location` | The Location entity locates the Thing or the Things it associated with. A Thing’s Location entity is defined as the last known location of the Thing | Park |
| `Historical Location` | The times of the current (i.e., last known) and previous locations of the Thing | 2021-10-14T18:51:47.342Z |
| `DataStream` | A Datastream groups a collection of Observations measuring the same ObservedProperty and produced by the same Sensor |
| `ObservedProperty` | An ObservedProperty specifies the phenomenon of an Observation | Temperature |
| `Sensor` | an instrument that observes a property or phenomenon | Temperature Sensor |
| `Observation` | an act associated with the process that measures an observed property at a specific feature of interest for a specific phenomenon time and records the results |

Lets take a look into this ROOT URI again:
> https://labs.waterdata.usgs.gov/sta/v1.1/

### URI Components
The first step in performing CRUD actions on resources is to address the target resource(s) via URI. The service root URI, the resource path, and the query options are the three major URI components used here. Furthermore, the service root URI is made up of two parts: (1) the SensorThings service's location and (2) the version number. 

The version number is formatted as shown : "v"majorversionnumber + "." + minorversionnumber

Example URI 
<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/205021951-4a42cd63-765e-433b-9797-fdea27fb94a1.png' height='250'>
</p>

Clients can address to different types of resources by appending the resource path after the service root URI, such as an entity set, an entity, a property, or a navigation property. Finally, after the resource path, clients can use query options to further process the addressed resources, such as sorting by properties or filtering with criteria.

#### Resource Path
The resource path follows the service root URI and can be used to access various entities.

| Usage of Resource Path |  URI | Description |
| -------- | ----------- | -------------------- |
| no resource path | https://labs.waterdata.usgs.gov/sta/v1.1/ | List all the Entity types in a JSON format |
| address an entity set | https://labs.waterdata.usgs.gov/sta/v1.1/Observations | List the Observed Properties of all entities |
| addresses to an specific entity | https://labs.waterdata.usgs.gov/sta/v1.1/Observations('991a6f6c-db7e-11ec-808f-d73c88214e23') | List only the specified entity from a collection of entity set |
| address to a property | https://labs.waterdata.usgs.gov/sta/v1.1/Observations('991a6f6c-db7e-11ec-808f-d73c88214e23')/result | List the property of the specified entity from a collection of entity set |
| address to the property value | https://labs.waterdata.usgs.gov/sta/v1.1/Observations('991a6f6c-db7e-11ec-808f-d73c88214e23')/result/$value | List only the value of the specified entity property from a collection of entity set |

Each and every entity set holds one or more relationship with other entity set. This relationship can be accessed via navigation and association links. The service then returns one or many entities that hold a certain relationship with the specified entity.

| Usage of Resource Path |  URI | Description |
| -------- | ----------- | -------------------- |
| address to a navigation property | https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('0dbbd0a0480c46bd91e67181455231ca')/Observations | request the linked entities by addressing to a navigation property of an entity |
| address to an association property | https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('0dbbd0a0480c46bd91e67181455231ca')/Observations/$ref | request the linked entities’ selfLinks by addressing to an association link of an entity |

Note : users can use navigation properties to link from one entity set to another, users can further extend the resource path with unique identifiers, properties, or links

### Entities

Common Property of an Entity:

The OGC SensorThings API service organizes similar entity types into entity sets. Each entity has an unique id as well as one-to-many properties. Furthermore, when an entity has a relationship with entities from other entity sets, this type of relationship is expressed using navigation properties (i.e., navigationLink and associationLink).

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `id` | ID is a system-generated unique identifier of an entity | One (Mandatory) | USGS-340422107370801 |
| `selfLink` | unique URL of an entity | One (Mandatory) | https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801') |
| `navigationLink` | relative URL that connects relevant information about the entity | One to Many (Mandatory) | Locations@iot.navigationLink |

a) Things

A Thing has one or more Datastreams in which Observations are collected. It is possible to create Things with nested linked Location and Datastream as well as Things without a Location and Datastream. A thing has many to many relationship with Locations. 

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `name` | A label for the Thing | One (Mandatory) | USGS-340422107370801 |
| `description` | short description of the corresponding Thing entity | One (Mandatory) | Well |
| `properties` | A JSON Object containing user-annotated properties as key-value pairs | Zero to One | State |

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')

```
{
"description": "Well",
"@iot.id": "USGS-340422107370801",
"name": "USGS-340422107370801",
"properties": {
  "state": "New Mexico",
  "monitoringLocationAltitudeLandSurface": "6981"
},
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')",
"Locations@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')/Locations",
"MultiDatastreams@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')/MultiDatastreams",
"HistoricalLocations@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')/HistoricalLocations",
"TaskingCapabilities@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')/TaskingCapabilities",
"Datastreams@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Things('USGS-340422107370801')/Datastreams"
}

```
b) Location

The Location entity is responsible for locating the Thing or Things with which it is associated. A Thing's Location entity is defined as the Thing's last known location. There is a chance that a thing's location matches its observations' feature of interest. For IoT applications, especially those involving in-situ sensing, the Thing's location is typically the primary location of interest.

| Property | Description | Multiplicity and Use | Examples |
| -------- | ----------- | -------------------- | -------- |
| `name` | a label for Location entity | One (Mandatory) | USGS-340422107370801 |
| `description` | short description of the corresponding Location entity | One (Mandatory) | Well |
| `encodingType` | GeoJSON encoding type of location property | one (Mandatory) | application/vnd.geo+json |
| `location` | Geographical Position of an entity is defined by encodingType | One (Mandatory) | type, coordinates |

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/Locations('c88aafd6-2d1f-11ec-a798-3b0d4f0899e6')

```
{
"description": "Well",
"encodingType": "application/vnd.geo+json",
"@iot.id": "c88aafd6-2d1f-11ec-a798-3b0d4f0899e6",
"location": {
  "type": "Point",
  "coordinates": [-107.61885,34.07285]
},
"name": "USGS-340422107370801",
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Locations('c88aafd6-2d1f-11ec-a798-3b0d4f0899e6')",
"HistoricalLocations@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Locations('c88aafd6-2d1f-11ec-a798-3b0d4f0899e6')/HistoricalLocations",
"Things@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Locations('c88aafd6-2d1f-11ec-a798-3b0d4f0899e6')/Things"
}

```
c) HistoricalLocation

A Thing’s HistoricalLocation entity set provides the times of the current (i.e., last known) and previous locations of the Thing. The HistoricalLocation can also be created, updated and deleted.

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `time` | Last known time of the Thing at the location | One (Mandatory) | 2021-10-14T18:51:47.342Z |

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/HistoricalLocations('c88af4fa-2d1f-11ec-a798-4b21ccc3d035')
```
{
"@iot.id": "c88af4fa-2d1f-11ec-a798-4b21ccc3d035",
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/HistoricalLocations('c88af4fa-2d1f-11ec-a798-4b21ccc3d035')",
"time": "2021-10-14T18:51:47.342Z",
"Locations@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/HistoricalLocations('c88af4fa-2d1f-11ec-a798-4b21ccc3d035')/Locations",
"Thing@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/HistoricalLocations('c88af4fa-2d1f-11ec-a798-4b21ccc3d035')/Thing"
}
```

d) DataStream

A Datastream groups a collection of Observations measuring the same ObservedProperty that are produced by the same Sensor.

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `name` | A label for the Datastream entity | One (Mandatory) | 40c9fdb920924c43b1afdc4f24ce54ea |
| `description` | The description of the Datastream entity | One (Mandatory) | Water level, depth LSD / USGS-340422107370801-40c9fdb920924c43b1afdc4f24ce54ea |
| `unitOfMeasurement` | A JSON Object containing three key-value pairs: name, symbol, definition for the symbol used | One (Mandatory) | name, symbol |
| `observationType` | The type of Observation (with unique result type), which is used by the service to encode observations | One (Mandatory) | Instantaneous |
| `observedArea` | The spatial bounding box of the spatial extent of all FeaturesOfInterest that belong to the Observations associated with this Datastream | Zero to One (Optional) | here, Type and coordinates in Geojson encoding |
| `phenomenonTime` | The temporal interval of the phenomenon times of all observations belonging to this Datastream | Zero to One (Optional) | 2021-08-15T19:00:00.000Z/2022-05-26T17:00:00.000Z |
| `resultTime` | The temporal interval of the result times of all observations belonging to this Datastream | Zero to One (Optional) | null |

ObservationType has data types derived from Observation and Measurement Model. Check out the 'Classification of observation by result type' section of this article. 

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('40c9fdb920924c43b1afdc4f24ce54ea')

```
{
"description": "Water level, depth LSD / USGS-340422107370801-40c9fdb920924c43b1afdc4f24ce54ea",
"@iot.id": "40c9fdb920924c43b1afdc4f24ce54ea",
"name": "40c9fdb920924c43b1afdc4f24ce54ea",
"observationType": "Instantaneous",
"observedArea": {
  "type": "Point",
  "coordinates": [-107.61885,34.07285]
},
"phenomenonTime": "2021-08-15T19:00:00.000Z/2022-05-26T17:00:00.000Z",
"properties": {
  "ParameterCode": "72019",
  "StatisticCode": "00011"
},
"resultTime": null,
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('40c9fdb920924c43b1afdc4f24ce54ea')",
"unitOfMeasurement": {
  "name": "Feet",
  "symbol": "ft",
  "definition": ""
},
"Observations@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('40c9fdb920924c43b1afdc4f24ce54ea')/Observations",
"Sensor@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('40c9fdb920924c43b1afdc4f24ce54ea')/Sensor",
"ObservedProperty@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('40c9fdb920924c43b1afdc4f24ce54ea')/ObservedProperty",
"Thing@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Datastreams('40c9fdb920924c43b1afdc4f24ce54ea')/Thing"
}
```

e) Sensor

A Sensor is an instrument that observes a property or phenomenon with the goal of producing an estimate of the value of the property

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `name` | a label for Sensor entity | One (Mandatory) | USGS_Sensor |
| `description` | short description of the corresponding Sensor entity | One (Mandatory) | The USGS Sensor |
| `metadata` | The detailed description of the Sensor or system defined by encodingType. | One (Mandatory) |

A sensor Metadata Encoding type can be either pdf or SensorML has described above. Most sensor manufacturers provide their sensor datasheets in a PDF format. As a result, PDF is a Sensor encodingType supported by SensorThings API. The second Sensor encodingType is SensorML.

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/Sensors('USGS_Sensor')
```
{
"description": "The USGS Sensor",
"encodingType": "",
"@iot.id": "USGS_Sensor",
"metadata": "",
"name": "USGS_Sensor",
"properties": {},
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Sensors('USGS_Sensor')",
"MultiDatastreams@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Sensors('USGS_Sensor')/MultiDatastreams",
"Datastreams@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Sensors('USGS_Sensor')/Datastreams"
}
```
f) ObservedProperty

An ObservedProperty specifies the phenomenon of an Observation.

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `name` | A label for the ObservedProperty | One (Mandatory) | Depth to water level, feet below land surface |
| `description` | short description of the Observed Property | One (Mandatory) | Physical |
| `definition` | The URI of the ObservedProperty. | One (Mandatory) | 

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/ObservedProperties('72019')

```
{
"description": "Physical",
"definition": "",
"@iot.id": "72019",
"name": "Depth to water level, feet below land surface",
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/ObservedProperties('72019')",
"Datastreams@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/ObservedProperties('72019')/Datastreams",
"MultiDatastreams@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/ObservedProperties('72019')/MultiDatastreams"
}
```

g) Observation

An Observation is the act of measuring or otherwise determining the value of a property [OGC 10-004r3 and ISO 19156:2011] Check out the Observation and Measurement Model that we discussed in this article.

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/Observations('0ce7bd6c-7e0c-11ec-a1c2-d357d8a6e8ba')
```
{
"@iot.id": "0ce7bd6c-7e0c-11ec-a1c2-d357d8a6e8ba",
"phenomenonTime": "2022-01-20T10:00:00.000Z",
"result": "179.30",
"resultTime": null,
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Observations('0ce7bd6c-7e0c-11ec-a1c2-d357d8a6e8ba')",
"FeatureOfInterest@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Observations('0ce7bd6c-7e0c-11ec-a1c2-d357d8a6e8ba')/FeatureOfInterest",
"Datastream@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Observations('0ce7bd6c-7e0c-11ec-a1c2-d357d8a6e8ba')/Datastream",
"MultiDatastream@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/Observations('0ce7bd6c-7e0c-11ec-a1c2-d357d8a6e8ba')/MultiDatastream"
},
```

h) Feature of Interest

An Observation results in a value being assigned to a phenomenon. The phenomenon is a property of a feature, the latter being the FeatureOfInterest of the Observation [OGC and ISO 19156:2011]. In the context of the Internet of Things, many Observations’ FeatureOfInterest can be the Location of the Thing. Example, the FeatureOfInterest can be the geographical area or volume that is being sensed.

| Property | Description | Multiplicity and Use | Example |
| -------- | ----------- | -------------------- | ------- |
| `name` | A label for the FeatureOfInterest | One (Mandatory) | FoI for location 5891d7a8-2d1b-11ec-a8de-7be125e05952 |
| `description` | short description of the FeatureOfInterest | One (Mandatory) | Generated from location 5891d7a8-2d1b-11ec-a8de-7be125e05952 |
| `feature` | The detailed description of the feature. The data type is defined by encodingType | One (Mandatory) | type, coordinate |

Example link : https://labs.waterdata.usgs.gov/sta/v1.1/FeaturesOfInterest('7a5bbcd4-2d23-11ec-b026-178e2d48f659')

```
{
"description": "Generated from location 5891d7a8-2d1b-11ec-a8de-7be125e05952",
"encodingType": "application/vnd.geo+json",
"feature": {
  "type": "Point",
  "coordinates": [-96.2429583,30.2123138]
},
"@iot.id": "7a5bbcd4-2d23-11ec-b026-178e2d48f659",
"name": "FoI for location 5891d7a8-2d1b-11ec-a8de-7be125e05952",
"@iot.selfLink": "https://labs.waterdata.usgs.gov/sta/v1.1/FeaturesOfInterest('7a5bbcd4-2d23-11ec-b026-178e2d48f659')",
"Observations@iot.navigationLink": "https://labs.waterdata.usgs.gov/sta/v1.1/FeaturesOfInterest('7a5bbcd4-2d23-11ec-b026-178e2d48f659')/Observations"
},
```

#### Query Operations
The use of query options allows for the refinement of requests in order to obtain the necessary information about SensorThings entities in a simple and efficient manner. SensorThings query options are divided into two categories. The first group specifies the properties that the request will return. This group's query options are `$expand` and `$select`. The second group is responsible for limiting, filtering, or re-ordering the request results. This group includes the functions `$orderby`, `$top`, `$skip`, `$count`, and `$filter`.

| Operations | Description | Result |
| ---------- | ----------- | --- |
| `$expand` | to request inline information for related entities in the entity collection requested | /v1.1/Things?$expand=Datastreams |
| `$select` | requests the service to return only the properties explicitly requested by the client | /v1.1/Observations?$select=result,resultTime |
| `$orderby` | sort the response based on properties of requested entity in the specified order | /v1.1/Observations?$orderby=result |
| `$top` | specifies the limit on the number of items returned from a collection of entities | /v1.1/Observations?$top=5 |
| `$skip` | provides the number of the collection's items that must be excluded from the outcome for the query | /v1.1/Observations?$skip=5 |
| `$count` | to retrieve the total number of items in a collection matching the requested entity | /v1.1/Things?$count=true |
| `$filter` | filters a collection of entities that are addressed by a request URL| v1.1/Observations?$filter=Datastream/id eq 1 |

<details><summary>TERMINOLOGIES</summary>
<p>

***REST*** : REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, allowing systems to communicate more easily with one another.

***HTTP*** : Hypertext Transfer Protocol is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes.(https://developer.mozilla.org/en-US/docs/Web/HTTP)

***URI*** : A Uniform Resource Identifier is a unique sequence of characters that identifies a logical or physical resource used by web technologies. In short, URI is a unique id for the resources.
  
</p>
</details>

# Practical Session

## Reference
[1] Best Practices for Using Sensor Web Technology by 52north, https://52north.github.io/sensor-web-tutorial/
[2] OGC Abstract Specification - Geographic information — Observations and measurements,Cox, Simon (2013), http://portal.opengeospatial.org/files/?artifact_id=41579.



