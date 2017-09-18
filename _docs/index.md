---
title: "IOOS Documentation Portal"
keywords: homepage
tags: [getting_started, about, overview]
#sidebar: home_sidebar
sidebar: mydoc_sidebar
topnav: topnav
toc: false
#permalink: index.html
summary: IOOS Documentation Portal is a doorway to IOOS resources on GitHub and otherwise; a collection of links to the guides, conventions, procedures and templates that define the IOOS Data Management And Communication (DMAC) strategy
---


## **Guidelines and Specifications**{: style="color: crimson"}

* * *

### **DMAC Implementation Guidelines for Data Providers**{: style="color: crimson"}

The [Guidance for Implementation of the Integrated Ocean Observing System (IOOS) Data Management and Communications (DMAC) Subsystem](https://ioos.noaa.gov/data/contribute-data/) describes the responsibilities of an IOOS Data Provider published on the official IOOS Web site.

### **IOOS Service Registration**{: style="color: crimson"}

Registration of the IOOS services allows the wide range of various clients to efficiently discover U.S. IOOS data. The [IOOS Service Registration Guide](http://ioos.github.io/registry/) describes the registration process, elaborates on IOOS Catalog and NGDC Registry interaction, and provides examples of Registry querying for metadata. 

<!--
### **IOOS Configuration Management**{: style="color: crimson"}

A [collection of documents](http://ioos.github.io/configuration-management) that describe the IOOS Configuration Management (CM) process, identify CM roles and responsibilities, resources, and formal processes and procedures to ensure that all proposed changes to major DMAC components and applications are evaluated and approved before implementation. The CM is a key process for maintaining the appropriate level of information assurance for DMAC implementation.
-->

### **IOOS SOS Guidelines**{: style="color: crimson"}

A [cookbook](https://ioos.github.io/sos-guidelines/index.html) for IOOS Application Profile of the OGC SOS v1.0 that includes guidelines, templates, and tests essential for service development and deployment:    

* [Overview of IOOS SOS Application Profile](https://ioos.github.io/sos-guidelines/index.html)
* [List of IOOS-specific compliance tests](https://ioos.github.io/sos-guidelines/sos-test-list-summary.html)  
* [IOOS SOS 1.0 Web Service Description Document](https://ioos.github.io/sos-guidelines/sos-wsdd-1-0.html)   
* IOOS SOS Response Templates:
  - [GetCapabilities](https://ioos.github.io/sos-guidelines/sos-getcapabilities.html/)
  - [DescribeSensor for a network of platforms](https://ioos.github.io/sos-guidelines/sml-describesensor-network.html)
  - [DescribeSensor for a single platform](https://ioos.github.io/sos-guidelines/sml-describesensor-station.html)
  - GetObservation:
     * [Generic OM part](https://ioos.github.io/sos-guidelines/om-getobservation.html)
     * [TimeSeries SWE Data Record’s static and dynamic fields for multiple stations with multiple sensors](https://ioos.github.io/sos-guidelines/swe-multistation-timeseries.html)
     * [TimeSeries SWE Data Record’s static and dynamic fields for multiple stations with multiple sensors and QC elements](https://ioos.github.io/sos-guidelines/swe-multistation-timeseries-qc.html)
     * [TimeSeries SWE Data Record’s static and dynamic fields for a single station with a single sensor](https://ioos.github.io/sos-guidelines/swe-singlestation-singleproperty-timeseries.html)
     * [TimeSeriesProfile SWE Data Record’s static and dynamic fields for a station with profiling sensors](https://ioos.github.io/sos-guidelines/swe-singlestation-timeseriesprofile.html)
     * [TimeSeriesProfile SWE Data Record’s static and dynamic fields for a station with profiling sensors and QC elements](https://ioos.github.io/sos-guidelines/swe-singlestation-timeseriesprofile-qc.html)   

### **NetCDF and OPeNDAP**{: style="color: crimson"}

* [IOOS netCDF Guidelines](https://ioos.github.io/ioos-netcdf/)
* [IOOS Compliance Checker](https://github.com/ioos/compliance-checker) - a tool to check local/remote netCDF datasets against a variety of compliance standards. 

<!-- * (https://github.com/dpsnowden/netcdf-guidelines). -->

### **Data Encoding in CSV/TSV**{: style="color: crimson"}

The [IOOS Convention for Observation Data Encoding in CSV/TSV](http://ioos.github.io/ioos-csv-tsv/) document describes the rules and constraints for encoding observation data as plain text Comma-Separated Values (CSV) or Tab-Separated Values (TSV).

### **Asset Identification**{: style="color: crimson"}

The [IOOS Convention for Observing Asset Identifiers](http://ioos.github.io/conventions-for-observing-asset-identifiers/) document describes the set of rules used by the IOOS program to assign identifiers to observing assets like measurement stations, platforms, sensors, etc.

### **Vocabularies**{: style="color: crimson"}

A [collection](https://github.com/ioos/vocabularies) of guidelines on the Controlled Vocabularies usage in IOOS-compliant data services (the link temporarily leads to the GitHub repository itself rather then to the GitHub Pages).

### **Biological Data Services**{: style="color: crimson"} 

A [collection](http://ioos.github.io/biological-data-services/) of documents describing data services for biological objects:

* [Data Enrollment Process](http://ioos.github.io/biological-data-services/biological-data-procedure/) proposed and supported by IOOS DMAC to support sharing and integration of aquatic biological data.
* [IOOS Biological Observations Services](http://ioos.github.io/biological-data-services/biological-observations/) that address the DMAC requirements for biological observations standards and interoperability.

### **Data Services for Animal Telemetry**{: style="color: crimson"}

A [collection](http://ioos.github.io/animal-telemetry/) of documents describing animal telemetry implementation: 

* A brief [description](http://ioos.github.io/animal-telemetry/about/) of the National Animal Telemetry Network (ATN). 
* [Strategic Plan And Recommendations](http://ioos.github.io/animal-telemetry/animal-telemetry-plan/) for a National ATN through U.S. IOOS
* [IOOS Animal Acoustic Telemetry (AAT) Data Project](http://ioos.github.io/animal-telemetry/aat_data_ioostech_wiki/).

### **Passive Acoustics Metadata**{: style="color: crimson"}

The [Metadata Convention for Passive Acoustic Recording](https://ioos.github.io/passive-acoustics/) defines metadata that supports the mission of the National Oceanic and Atmospheric Administration (NOAA) for acquisition, archiving, and dissemination of ocean passive acoustic data. 

<!--
# Contributing and changes

To make changes to this website and add information, see the [Website Deployment Workflow](website_deployment_workflow_updated) page. 

-->


<br><br>

## **Projects**{: style="color: crimson"}

<!-- <a name="System Integration Test"></a> -->

* * *

### **IOOS Catalog of Data and Services**{: style="color: crimson"}

* [The IOOS Web Catalog](http://catalog.ioos.us) (current version)
* [IOOS Catalog GitHub repository for documentation and issues](https://github.com/ioos/catalog)
* Another [GitHub repository](https://github.com/ioos/service-monitor) that holds source codes and modules of the IOOS Service Monitor (old version of the IOOS Catalog)

### **System Integration Test**{: style="color: crimson"}

The [system integration test development site](https://github.com/ioos/system-test) on github contains IPython notebooks demonstrating how to access data from servers in various scenarios. 

### **IOOS ncSOS**{: style="color: crimson"}

The [IOOS ncSOS](https://github.com/asascience-open/ncSOS) adds an OGC SOS service to datasets in your existing THREDDS server. It complies with the [IOOS SWE Milestone 1.0 templates](https://github.com/ioos/sos-guidelines/tree/master/template/milestone1.0) and requires your datasets be in any of the [CF 1.6 Discrete Sampling Geometries](http://cfconventions.org/Data/cf-conventions/cf-conventions-1.6/build/cf-conventions.html#discrete-sampling-geometries).

### **i52N and related activities (sensor web harvesters, test tools, etc.)**{: style="color: crimson"}

*  [i52N-SOS](http://ioos.github.io/i52n-sos/), an IOOS customized build of the [52°North Sensor Observation Service (SOS)](http://52north.org/sos) that extends the stock upstream [52°North SOS](https://github.com/52North/SOS) with IOOS specific encoding formats, test data, and more.
* [IOOS SOS Compliance Test Tool](https://github.com/ioos/ioos-sos-compliance-tests), a set of CTL ([compliance test language](http://portal.opengeospatial.org/files/?artifact_id=33085)) files and utility scripts for thorough standard validation and test of the IOOS SOS implementations.

<!-- * [IOOS SOS Validator](https://github.com/ioos/ioos-sos-validator) for simple schema validation of SOS responses and templates --> 

<br><br>

