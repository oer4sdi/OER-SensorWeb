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


## O&M model
<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/201489207-bf9ca213-91a6-4502-8d46-ede5ed704f81.png'>
</p>

Observation and Measurements standard defines models and XML schemas for observations as well as features involved in sampling when making observations. O&M creates a high-level framework for representing sensor system observations, measurements, procedures, and metadata, for the implementation of SWE-enabled architectures. 

Each and every sensor data sources can have different formats and information. This pose an issue when exchanging sensor data. To overcome this interoperability issue, O&M becomes a common standardized data model for handling measurement events in various types of sensors, ranging from thermometers inside a closed process to satellites images of the Earth from space. O&M, in conjunction with other SWE framework open standards such as SensorML and Sensor Observation Service (SOS), provides a system-independent, Internet-enabled method of data exchange between different parts of sensor networks and other systems using sensor information.

Because IP-based environmental sensors are becoming more affordable, anyone can gather and refine detailed environmental information about the world around us, both locally and globally. This way citizens with any background can use these sensors to generate publically available data. Of course, as with everything based on the Internet, as the amount of information and the diversity of the sources producing it grows, so does the quality range of the available information. Organizations that previously deployed and maintained their own sensor networks with proprietary data and control interfaces built for their specific software and hardware systems are shifting to open standards. Even if they do not intend to publish their data on the Internet, they do intend to use IP-based networks for communication. The O&M concepts serve as the foundation for the EU-wide INSPIRE data models for meteorological, climatological, and air quality information, and the structure and capabilities of various environmental observation networks.


#### UML Diagram of Observations
<p align='center'>
  <img src='https://user-images.githubusercontent.com/94603960/204206653-b5fae81b-74f3-4ab5-aac2-6e885dc7c385.png'>
</p>

An observation is part of a procedure that measured a specific observedProperty at a dedicated featureOfInterest for a specific phenomenonTime and saved the result. Since each measurement is flawed to a certain extent, the property resultQuality denotes the Quality of the measurement. We will learn about the entities and properties of observation mentioned in this definition below.

| Entity | Description | Examples |
| ------ | ----------- | -------- |
| Observed Property / Phenomenon | A property measured by a sensor | Temperature, Co2 levels |
| Feature of Interest (FoI) | an abstraction of a real world phenomena which has been georeferenced | Park(Place) |
| Phenomenon Time | The time instant or period of when the Observation happens | The time at which Co2 levels are measured |
| Result | The estimated value of an ObservedProperty from the Observation | Atm Pressure: in Pa(pascal) |
| Result Time | The time of the Observation’s result after processing was generated| The time at which Atm Pressure after processing |

Table 1: Mandatory Properties of an Observation Model

| Entity | Description | Examples |
| ------ | ----------- | -------- |
| Result Quality | 	Describes the quality of the result owing to the fact that sensor data can be faulty to some extent | 
| Valid Time | The time period during which the result may be used. With real time sensor data available, the data is measured and replaced within seconds in some cases |
| Process | The process that performs the measurement | Temperature sensor |

Table 2: Optional Properties of an Observation Model

#### QUIZ - (A drag and drop options that user use correctly mention the terms Eg question : When measuring the height of a tree, the height is the observed ObservableProperty, 20m may be the Result of the Observation, and the tree is the FeatureOfInterest.) H5P format

To illustrate the mapping, an exemplary dataset from the hamburg smart city project is presented subsequently.

```
https://iot.hamburg.de/v1.1/?
```
<img src= 'https://user-images.githubusercontent.com/94603960/202925919-4f7c696d-aa65-4663-88c2-ce0d7486f28d.png' width='500'>

#### QUIZ observation examples

The Observation model approaches data from the perspective of the data user, emphasizing the semantics of the feature-of-interest and its properties. Whether the feature-of-interest is a discrete or continous observation.

### Classification of observation by result type

1. Discrete Observation

![o m-discrobs](https://user-images.githubusercontent.com/94603960/204206594-5803c760-8199-4d10-859d-165a7a80ac99.png)

Observations where the outcome of a single observation may have a single value or multiple values, but if there are multiple values, those values do not change over the course of the observation with respect to either space or time.

Example
```
A well known example would be Flip-a-Coin, where the odds are always 'HEAD' or 'TAIL' - This would be a Boolean type observation.

How about something in GeoSpatial Context?
Buildings and Roads are features that have distinct boundaries or limits are considered discrete. 
In mapping, discrete data can be shown as a point, line, or a polygon. Points could be cities, lines could be road 
networks, and polygons could be provinces in a country. This features would be Geometry type observation.

```

2. Continous Observation

Observations where the outcome of a single observation includes multiple values that change with time, space, or both during the course of the observation. The value of a corresponding observation result shall therefore be a function or coverage, respectively. The target feature may be subjected to numerous observations using various sampling methods, so the sampling methods are associated with the act of observation rather than being inherent in the feature-of-interest.

To model the coverage, a domain geometry decomposition with specialized sub-geometries is defined to represent the associated feature.

![o m-contobs](https://user-images.githubusercontent.com/94603960/204206553-dacd1b3f-535d-4528-85cd-c07a9fcb9821.png)

What would be a best example for Continous Observation? 
```
Weather is not predictable and is a good example for Continous Observation. 
'Temperature' for example, changes over space and time. So depending on your analysis, if you want temperature from various sources(places) 
that comes under a coverage.
Think of any continous Observation?
```

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

## Sensor Web and Internet of Things

The terms Internet of Things and Web of Things refer to approaches to integrating smart devices into the Internet. The Internet of Things (IoT) is a network of physical objects—"things"—embedded with sensors, software, and other technologies for connecting and exchanging data with other devices and systems via the internet. In the context of Sensorweb, the ‘things’ here are ‘Sensors’. Physical things (e.g, Sensors) can share and collect data with minimal human intervention thanks to low-cost computing technologies.

The Web of Things (WoT) is a set of standards developed by the World Wide Web Consortium (W3C) to improve the interoperability, and usability of the Internet of Things (IoT). From a technological standpoint, this means that the smart device (e.g., a sensor) is addressable via standard HTTP operations (GET, POST, PUT, etc.), enabling RESTful access to sensor data (Bröring et al, 2011 a). In short, WoT is a subset of IoT and is based on software standards like REST, HTTP, and URIs to allow devices to communicate with one another. 

<details><summary>TERMINOLOGIES</summary>
<p>

***REST*** : REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, allowing systems to communicate more easily with one another.

***HTTP*** : Hypertext Transfer Protocol is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers, but it can also be used for other purposes.(https://developer.mozilla.org/en-US/docs/Web/HTTP)

***URI*** : A Uniform Resource Identifier is a unique sequence of characters that identifies a logical or physical resource used by web technologies. In short, URI is a unique id for the resources.
  
</p>
</details>

The Open Geospatial Consortium's Sensor Web Enablement (SWE) framework is a well-established approach for integrating sensors with the Web. A smart device, according to Bröring et al. (2011 b), may respond to data requests using SWE-standardized formats. To be more specific, sensor metadata should be encoded using SensorML, and observation data as O&M. With these format constraints, any other application/component may retrieve the smart device's sensor data in an interoperable, standardized manner.  SWE specifications such as SOS; SPS, and SES are powerful for use cases that are broad and often complex(e.g. disaster management or early warning systems). However, use cases that do not require the full functionality of SWE's data altering, sensor discovery, tasking, and event handling may be easier to realize with the Web of Things approach by treating sensor objects as things. (Liang et al.) The SensorThings API is an open standard, builds on Web protocols and the OGC Sensor Web Enablement standards, and applies an easy-to-use REST-like style.

The OGC SensorThings API is recommended for organizations that require web-based platforms to manage, store, share, and analyze IoT-based sensor observation data. Application developers can use this open standard to connect to various IoT devices and create innovative applications without having to worry about the heterogeneous protocols of various IoT devices, gateways, and services. (Liang et al, 2016)

Github repository for OGC sensorthings API:
> https://github.com/opengeospatial/sensorthings

The SensorThings API may simplify connections between devices-to-devices and devices-to-applications by utilizing efficient REST binding, including a reduced JSON encoding, and the MQTT protocol for sensor access making it a lightweight SWE approach. 

The OGC SensorThings API data model consists of two parts: (1) the Sensing part and (2) the Tasking part. 

The Sensing part allows IoT devices and applications to CREATE, READ, UPDATE, and DELETE (i.e., HTTP POST, GET, PATCH, and DELETE) IoT data and metadata in a SensorThings service.


### SensorThings API - Sensing Part

![SensorThingsAPI](https://user-images.githubusercontent.com/94603960/202159021-0e31f412-6f36-43c0-b5bf-10f73b63d77f.png)

The Sensing part is designed based on the OGC/ISO Observation and Measurement (O&M) model. A Thing represents an IoT device or system. A Thing has a Location that is associated with one or more Datastreams. Each Datastream has many Observations from the Sensor and observes one ObservedProperty with one Sensor. Each Observation read by the Sensor identifies a single FeatureOfInterest. These relationships, when combined, provide a flexible standard way to describe and model any sensing system. It enables SensorThings to function as a unified data exchange system for heterogeneous devices across any organization. 

<details><summary>TERMINOLOGIES</summary>
<p>

| Terms | Definitions |
| ----- | ----------- |
| Things | The OGC SensorThings API adheres to the ITU-T definition, which states that a thing is an object of the physical world (physical things) or the information world (virtual things) that can be identified and integrated into communication networks [ITU-T]. |
| Location | The Location entity locates the Thing or the Things it associated with. A Thing’s Location entity is defined as the last known location of the Thing |
| Historical Location | The times of the current (i.e., last known) and previous locations of the Thing |
| DataStream | A Datastream groups a collection of Observations measuring the same ObservedProperty and produced by the same Sensor |

</p>
</details>



