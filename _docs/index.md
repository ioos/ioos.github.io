---
title: "IOOS Documentation Portal"
keywords: [DMAC, homepage, documentation, guidelines, specifications]
tags: [DMAC, homepage, documentation, guidelines, specifications]
toc: false
#permalink: index.html
summary: IOOS Documentation Portal is a collection of IOOS Data Management and Communication (DMAC) guidelines, specifications, and software tools that allow IOOS data provider organizations to publish their data in an interoperable fashion adhering to DMAC principles.  This page describes the various components and where to find more information on each.
---


## **Guidelines and Specifications**
Technical documentation for the guidelines and specifications that define the DMAC system.
* * *

### **DMAC Implementation Requirements and Guidelines for IOOS Data Providers**
The Data Management and Communication (DMAC) Implementation Requirements site outlines the processes US Integrated Ocean Observing System (IOOS) data providers must comply with in order to properly implement an IOOS DMAC system.  This resource, published on IOOS' official NOAA website, represents the overall procedural requirements in order for data providers to contribute their data to the IOOS data management enterprise.  
* [DMAC Implementation Requirements for IOOS Data Providers](https://ioos.noaa.gov/data/contribute-data/)

The individual documentation sites listed below provide the specific technical guidance as it pertains to the overall high-level requirements outlined in the IOOS Data Contributor site.  The software and tools section contains links to several resources data providers can use to assist in this process.


### **IOOS Metadata Profile**
The IOOS Metadata Profile contains dataset attribution guidelines and examples to help the US IOOS community publish datasets in netCDF and other related data formats in an interoperable manner.  The goal of the metadata profile is to allow users of IOOS' data services, such as ERDDAP, THREDDS, OPeNDAP, and SOS, seamless access and use across individual IOOS data providers' services.
* [IOOS Metadata Profile](https://ioos.github.io/ioos-metadata/)


### **IOOS National Glider DAC Wiki**
The IOOS National Glider DAC is the official Data Assembly Center (DAC) for all IOOS underwater glider activities.  The Wiki provides glider operators and IOOS data providers technical details on the Glider DAC netCDF data format specifications, information on data provider registration and data set submission processes for contributing real-time and delayed-mode glider data sets to the DAC.  The Glider DAC website includes map-based visualizations, data access links, and information about the Underwater Glider User Group (UG2).
* [IOOS National Glider DAC Wiki](https://ioos.github.io/ioosngdac/)
* [IOOS National Glider DAC GitHub](https://github.com/ioos/ioosngdac)
* [IOOS National Glider Website](https://gliders.ioos.us/)


### **IOOS Convention for Observing Asset Identification**
The IOOS Convention for Observing Asset Identification describes the set of rules used by the IOOS program to assign identifiers to observing assets like measurement stations, platforms, sensors, etc.
* [IOOS Convention for Observing Asset Identification](http://ioos.github.io/conventions-for-observing-asset-identifiers/)


### **NCEI Data Archiving Guidelines for IOOS**
This 'cookbook' contains guidelines for IOOS regional data managers to prepare and submit data for archiving at the National Centers for Environmental Information (NCEI).
* [NCEI Data Archiving Guidelines for IOOS](http://ioos.github.io/ncei-archiving-cookbook/)


### **IOOS SOS Guidelines**
The IOOS SOS Guidelines document the technical specifications, guidelines, templates, and tests essential for configuration and deployment of an IOOS DMAC-compliant SOS server.  The IOOS SOS is a profile of the OGC Sensor Web Enablement (SWE) Sensor Observation Service (SOS) v1.0.  The SOS Guidelines site includes the technical specifications of the IOOS SOS Web Service Description Document (WSDD), response templates for IOOS SOS operations (GetCapabilities, DescribeSensor, GetObservation), and a compliance test suite description.
* [IOOS SOS Application Profile Overview](https://ioos.github.io/sos-guidelines/)
* [IOOS SOS 1.0 Web Service Description Document](https://ioos.github.io/sos-guidelines/sos-wsdd-1-0.html)   


### **IOOS Data Encoding in CSV/TSV**
The IOOS Convention for Observation Data Encoding in CSV/TSV describes the rules and constraints for encoding observation data as plain text Comma-Separated Values (CSV) or Tab-Separated Values (TSV).
* [IOOS Convention for Observation Data Encoding in CSV/TSV](http://ioos.github.io/ioos-csv-tsv/)


### **IOOS Controlled Vocabularies**
A collection of guidelines on the Controlled Vocabularies usage in IOOS-compliant data services.
* [IOOS Controlled Vocabularies](https://github.com/ioos/vocabularies)

<!--
### **Data Services for Animal Telemetry**

A [collection](http://ioos.github.io/animal-telemetry/) of documents describing animal telemetry implementation:

* A brief [description](http://ioos.github.io/animal-telemetry/about/) of the National Animal Telemetry Network (ATN).
* [Strategic Plan And Recommendations](http://ioos.github.io/animal-telemetry/animal-telemetry-plan/) for a National ATN through U.S. IOOS
* [IOOS Animal Acoustic Telemetry (AAT) Data Project](http://ioos.github.io/animal-telemetry/aat_data_ioostech_wiki/).
-->

### **Passive Acoustics Metadata**
The Metadata Convention for Passive Acoustic Recording defines metadata that supports the mission of the National Oceanic and Atmospheric Administration (NOAA) for acquisition, archiving, and dissemination of ocean passive acoustic data.
* [Metadata Convention for Passive Acoustic Recording](https://ioos.github.io/passive-acoustics/)

<br><br>


## **Software, Tools, and Projects**
A collection of IOOS-developed software tools that data providers can use to publish DMAC-compliant datasets and services.  Also included in this list are IOOS projects that aggregate datasets throughout the IOOS enterprise as a whole for search and discovery, and demonstrate usage of IOOS DMAC services for scientific analysis.
* * *

### **IOOS Compliance Checker**
The IOOS Compliance Checker is a python based tool for data providers to check for completeness and community standard compliance of local or remote netCDF files against CF and ACDD file standards. The python module can be used as a command-line tool or as a library that can be integrated into other software.  There is also a web-based version of Compliance Checker for users who want to test their own datasets but do not wish to download the software.
* [IOOS Compliance Checker](https://github.com/ioos/compliance-checker)
* [Compliance Checker Web](https://compliance.ioos.us/)


### **IOOS Data Demo Center**
The IOOS Data Demo Center is a collection [Jupyter Notebook](https://jupyter.org/)-based tutorials and examples of how to access and utilize the many IOOS technologies and data sources available. This site is geared towards scientists and environmental managers interested in “diving deep” into the numbers and creating original plots and data analysis. Most notebook examples are written in Python, however, there are also notebooks written in Matlab, and R.
* [IOOS Data Demo Center](https://ioos.github.io/notebooks_demos/)


### **IOOS Data Catalog**
IOOS operates the IOOS Data Catalog to facilitate search and discovery of datasets and services.  The Catalog represents the full enterprise inventory of IOOS network datasets and services.  It is an open data catalog powered by CKAN and pycsw that allows web-based search, discovery, and preview, as well as machine-to-machine query via OGC CS-W service and a custom REST API.  All IOOS data providers must convert their [IOOS Metadata Profile](https://ioos.github.io/#ioos-metadata-profile)-compliant datasets and corresponding services and represent them in ISO 19115 XML metadata records, which can then be registered with the IOOS Data Catalog.  The registration process is handled by the IOOS Harvest Registry, a companion product to the Data Catalog.  The Harvest Registry includes both a web UI and API for programmatic-registration of datasets.
* [IOOS Data Catalog](https://data.ioos.us)
* [IOOS Catalog Documentation Site](https://ioos.github.io/catalog/)
* [IOOS Harvest Registry Service & Data Registration Guide](https://ioos.github.io/catalog/pages/registry/)


### **MBON Portal**
The MBON Portal provides access to and interactive visualizations of data associated with the [Marine Biodiversity Observation Network (MBON)](https://ioos.noaa.gov/project/bio-data/). The portal includes real-time, delayed-mode, and historical data for in situ and remotely-sensed physical, chemical, and biological observations. This observation data is focused on organisms from microbes to whales, including measures of biodiversity (e.g. presence, abundance), productivity, genomics, phenology, and other relevant ecological process measurements or indices. Also featured are habitat characterization and habitat diversity measures, including satellite data and added-value data derived from satellite observations, and neural network model results, such as biogeographical seascape classifications. Featured in this portal are biodiversity indices that have been computed for key biological datasets within the MBON regions.
* [MBON Portal](https://mbon.ioos.us/)
* [MBON Portal Documentation Site](https://ioos.github.io/mbon-docs/)

### **IOOS ncSOS**
The IOOS ncSOS THREDDS plugin adds an OGC SOS service to datasets in your existing THREDDS server. It complies with the [IOOS SWE Milestone 1.0 Templates](https://github.com/ioos/sos-guidelines/tree/master/template/milestone1.0) and requires your datasets be in any of the [CF 1.6 Discrete Sampling Geometries](http://cfconventions.org/Data/cf-conventions/cf-conventions-1.6/build/cf-conventions.html#discrete-sampling-geometries) and attributed according to the [IOOS Metadata Profile](https://ioos.github.io/#ioos-metadata-profile).
* [IOOS ncSOS](https://github.com/asascience-open/ncSOS)


### **i52N SOS and Related Utilities**
The IOOS i52N SOS is an IOOS-customized build of the [52°North OGC Sensor Observation Service](https://github.com/52North/SOS) that is extended with IOOS specific encoding formats, test data, and more.  The IOOS SOS Compliance Test Tool is a set of CTL ([compliance test language](http://portal.opengeospatial.org/files/?artifact_id=33085)) files and utility scripts to validate function of IOOS SOS implementations.
* [i52N-SOS](http://ioos.github.io/i52n-sos/)
* [IOOS SOS Compliance Test Tool](https://github.com/ioos/ioos-sos-compliance-tests)

<!--
### **System Integration Test**
The System Integration Test [site](https://github.com/ioos/system-test) on GitHub contains IPython notebooks demonstrating how to access data from servers in various scenarios.
-->

<!-- * [IOOS SOS Validator](https://github.com/ioos/ioos-sos-validator) for simple schema validation of SOS responses and templates -->

<br><br>
