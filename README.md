# TR-106 -- Data Model Template for CWMP Endpoints and USP Agents

*The latest TR-106 specification can be found at https://data-model-template.broadband-forum.org.*

TR-106 defines the [Broadband Forum](https://www.broadband-forum.org)'s [CWMP](https://www.broadband-forum.org/technical/download/TR-069.pdf) (TR-069) and [USP](https://usp.technology) (TR-369) data modeling framework, including:

* Structural requirements for the data hierarchy
* Requirements for versioning of data models
* Requirements for defining profiles

As part of this data modeling framework, TR-106 defines two XML Schemas:

* The *Data Modeling (DM) Schema*, which is used for defining all CWMP and USP data models. This makes data model definitions rigorous, and helps to reduce the danger that different implementations will interpret data model definitions in different ways

* The *Device Type (DT) Schema*, that allows a device to describe its supported CWMP data models. Note that USP uses a different mechanism (the `GetSupportedDM` message) for this purpose

This repository contains [the above schemas](schemas), [support files](support) (e.g., common bibliographic references and data types), and the [TR-106 specification source](specification). The rendered GitHub Pages documentation can be found at https://data-model-template.broadband-forum.org.

The TR-106 schemas and support files are also available at the [CWMP data models](https://cwmp-data-models.broadband-forum.org) and [USP data models](https://usp-data-models.broadband-forum.org). These sites present integrated views of the CWMP and USP versions of the standard data models, and provide a convenient way of viewing current and past versions of the schemas and support files in context.
