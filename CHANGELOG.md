# TR-106 Change Log

*See <https://data-model-template.broadband-forum.org> for the current TR-106 specification.*

## 2022-01-27: [TR-106 Amendment 11](https://www.broadband-forum.org/download/TR-106_Amendment-11.pdf)

*Tag: [v1.11.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.11.0)*

Specification:
* Clarified `forcedEnabled` and `forceDefaultEnabled` for USP
* Clarified impact of deprecating or obsoleting profile items
* Documented new description templates
* Documented new `secured` attribute

DM Schema (`cwmp-datamodel-1-9.xsd`):
* Allowed the `version` attribute in component references
* Allowed `minEntries` and `maxEntries` in command and event argument objects
* Allowed `status` attribute in profile command/event arguments
* Added `secured` attribute

DM Report Schema (cwmp-datamodel-report-1-0.xsd):
* Changed version number to `1-0`, which indicates new markdown-friendly
  wrapped descriptions
* Added `customNumEntriesParameter`, `noDiscriminatorParameter` and
  `noUnionObject` to suppress various warnings

DT Schema (cwmp-devicetype-1-6.xsd)
* Updated to reference `cwmp-datamodel-1-9.xsd`

## 2020-11-05: [TR-106 Amendment 10](https://www.broadband-forum.org/download/TR-106_Amendment-10.pdf)

*Tag: [v1.10.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.10.0)*

* Converted document to markdown
* Various editorial improvements

## 2019-09-04: TR-106 Amendment 9

*Tag: [v1.9.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.9.0)*

* Schema updates; document not updated

## 2018-05-10: [TR-106 Amendment 8](https://www.broadband-forum.org/download/TR-106_Amendment-8.pdf)

*Tag: [v1.8.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.8.0)*

* Added support of USP (mountable objects)
* Removed references to obsolete data models
* Moved device requirements to TR-069

## 2014-09-17: [TR-106 Amendment 7+]

*Tag: ]v1.7.0+](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.7.0+)*

* Support file updates; document not updated

## 2013-10-07: [TR-106 Amendment 7](https://www.broadband-forum.org/download/TR-106_Amendment-7.pdf)

*Tag: [v1.7.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.7.0)*

* Added descriptions of new features in DM Schema (v1.4 & v1.5) and DT Schema (v1.2 & v1.3)
* Added Annex defining additional requirements for BBF standard data models

## 2011-07-01: [TR-106 Amendment 6](https://www.broadband-forum.org/download/TR-106_Amendment-6.pdf)

*Tag: [v1.6.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.6.0)*

* Removed definition of proxying, now defined in TR-069
* Removed Common objects
* Alias Parameter Requirements added

## 2010-11-01: [TR-106 Amendment 5](https://www.broadband-forum.org/download/TR-106_Amendment-5.pdf)

*Tag: [v1.5.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.5.0)*

* Replaced definitions of named data types such as IPAddress with references to normative XML
* Minor changes to DM Schema (v1.3) and DT Schema (v1.1)

## 2010-11-01: [TR-106 Amendment 4](https://www.broadband-forum.org/download/TR-106_Amendment-4.pdf)

*Tag: [v1.4.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.4.0)*

* Moved data model definitions to TR-181 Issue 1

## 2010-02-01: [TR-106 Amendment 3](https://www.broadband-forum.org/download/TR-106_Amendment-3.pdf)

*Tag: [v1.3.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.3.0)*

* Addition of device type XML Schema

## 2008-11-01: [TR-106 Amendment 2](https://www.broadband-forum.org/download/TR-106_Amendment-2.pdf)

*Tag: [v1.2.0](https://github.com/BroadbandForum/data-model-template/releases/tag/v1.2.0)*

* Addition of data model definition XML Schema and normative XML common object and component definitions

## 2006-11-01: [TR-106 Amendment 1](https://www.broadband-forum.org/download/TR-106_Amendment-1.pdf)

* Clarification of original document

## 2005-09-01: TR-106 Amendment 0

* Original (PDF no longer available)
