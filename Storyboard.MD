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

![sensors-19-04070-g003](https://user-images.githubusercontent.com/94603960/200171298-fe996d09-a0e8-4b29-8904-dd184529d417.png)

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
