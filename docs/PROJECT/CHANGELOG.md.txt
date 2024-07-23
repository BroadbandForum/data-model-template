<!-- do not edit! this file was created from PROJECT.yaml by project-parser.py -->

# TR-106: Data Model Template Change Log

See <https://data-model-template.broadband-forum.org> for the
current TR-106 specification.

## 2024-07-23: [TR-106 Amendment 14]

*Tag: [v1.14.0]*

### TR-106 Document
* Added access type guidance
* Documented the dmr:noNameCheck attribute
* Documented the decimal datatype
* Documented the list value defaults
* Documented markdown syntax (and switch from MediaWiki)
* Cosmetic changes

### DM Data Model Definition Schema (DM Schema)
* Starting from this version, the DM schema version will be the
  same as the specification version
* Removed the status attribute's default
* Supported virtual components
* Permitted changing the version of an existing parameter (sometimes
  needed when using components to define multiple parameters)

### Data Model Report Schema (DMR Schema)
* Added *noNameCheck* to suppress name checks (used for items
  that knowingly disobey the rules)

### Data Model Data Types
* Updated *Alias* component to be virtual (with different CWMP
  and USP versions)

### Data Model Bibliographic References
* Fixed IPDR reference links
* Added more bibrefs

### Device Type Schema (DT Schema)
* Starting from this version, the DT schema version will be the
  same as the specification version

## 2024-01-18: [TR-106 Amendment 13]

*Tag: [v1.13.0]*

### TR-106 Document
* Clarified the requirements regarding vendor-specific prefixes

### Data Model Data Types
* Added an *Alias* component to reduce cut-and-paste in the data
  models
* Added an *Order* type to reduce cut-and-paste in the data models

### Data Model Bibliographic References
* Added more bibrefs

## 2023-06-14: [TR-106 Amendment 12]

*Tag: [v1.12.0]*

### TR-106 Document
* Updated the *Mountable Object* and *Mount Point* descriptions to
  indicate that all top-level objects (other than mount points) are
  mountable
* Updated path scoping rules to indicate that a path that starts
  with a period (`.`) is relative to its mount point (if mounted)
  or to the Root or Service Object (otherwise)
* Updated the *hidden* and *secured* attributes to clarify that they
  can't both be set to *true*, and that for CWMP *secured* means
  the same as *hidden*
* Tightened the *version* attribute definition. It can only be
  used when the version is later than the parent version,
  except that it always has to be specified for Objects and
  Profiles. Also added a new section on the use of the *version*
  attribute
* Clarified that defaults defined in components will be "promoted"
  to *parameter* defaults when used in command or event arguments
* Fixed the rules governing modifications of existing models. The
  basic rule is that the value space can only be expanded, never
  contracted
* Added a new section on the DMR (Data Model Report) Schema

### DM Data Model Definition Schema (DM Schema)
* Supported XSD v1.1, which allows more rigorous validation, e.g.,
  use of appropriate attributes when creating and modifying items
* Added defaults for various attributes, e.g. *access*, *minEntries*
  and *maxEntries* default to *readOnly*, *1* and *1* respectively
* Deprecated the *mountType* attribute's *none* and *mountable*
  values, because mountable objects are now determined automatically
* Made the *uniqueKey/functional* and the *command/async*
  attributes mandatory
* Relaxed rules governing the order of top-level elements such as
  *import*, *dataType* and *component*; they can now occur in any
  order
* Tightened up the use of *dmr:* attributes, which can now only be
  used on elements where they make sense
* Fixed a few bugs, e.g., added a *template* element uniqueness check

### Data Model Report Schema (DMR Schema)
* Added *noUnitsTemplate* to suppress "missing *{{units}}*
  template" warnings
* Added *previousCommand* and *previousEvent* attributes

### Device Type Schema (DT Schema)
* Updated to reference latest published DM Schema version (v1.10)
* Note that the DT Schema is v1.10 to match the DM Schema (DT
  Schema v1.7, v1.8 and v1.9 were skipped)

## 2022-01-27: [TR-106 Amendment 11]

*Tag: [v1.11.0]*

### TR-106 Document
* Clarified *forcedEnabled* and *forceDefaultEnabled* for USP
* Clarified impact of deprecating or obsoleting profile items
* Documented new description templates
* Documented new *secured* attribute

### DM Data Model Definition Schema (DM Schema)
* Allowed the *version* attribute in component references
* Allowed *minEntries* and *maxEntries* in command and event
  argument objects
* Allowed *status* attribute in profile command/event arguments
* Added *secured* attribute

### Data Model Report Schema (DMR Schema)
* Changed version number to *1-0*, which indicates new
  markdown-friendly wrapped descriptions
* Added *customNumEntriesParameter*, *noDiscriminatorParameter*
  and *noUnionObject* to suppress various warnings

### Device Type Schema (DT Schema)
* Updated to reference latest published DM Schema version (v1.9)

## 2020-11-05: [TR-106 Amendment 10]

*Tag: [v1.10.0]*

### TR-106 Document
* Converted document to markdown
* Various editorial improvements

### DM Data Model Definition Schema (DM Schema)
* Allowed command attributes, e.g. mandatory, in component
  definitions

### Device Type Schema (DT Schema)
* Updated to reference latest published DM Schema version (v1.8)
* Supported event and command structures in device type files

## 2019-09-04: TR-106 Amendment 9

*Tag: [v1.9.0]*

* Schema updates; document not updated

### DM Data Model Definition Schema (DM Schema)
* Supported implementation defaults, version attribute,
  description templates, writeOnceReadOnly access type
  and the decimal datatype

### Device Type Schema (DT Schema)
* Updated to reference latest published DM Schema version (v1.7)

### Data Model Data Types
* Added datatypes from versioned files
* Added CWMP and USP versions of the Alias datatype
* Added URI, URL and URL datatypes

### Data Model Bibliographic References
* Added references from versioned files (grouped by category and
  sorted within category)
* Updated references for convention that "TR-nnn" means the latest
  Amendment and Corrigendum
* Added references in support of Device:2.13 DM Instances
* Added references for 3GPP 5G standards in support of Device:2.14
  DM Instances

## 2018-05-10: [TR-106 Amendment 8]

*Tag: [v1.8.0]*

### TR-106 Document
* Added support of USP (mountable objects)
* Removed references to obsolete data models
* Moved device requirements to TR-069

### DM Data Model Definition Schema (DM Schema)
* Supported USP commands, events and mount points

### [XML Catalog](https://en.wikipedia.org/wiki/XML_catalog)
* Original

## 2014-09-17: TR-106 Amendment 7+

*Tag: [v1.7.0+]*

* Support file updates; document not updated

## 2013-09-09: [TR-106 Amendment 7]

*Tag: [v1.7.0]*

### TR-106 Document
* Added descriptions of new features in DM Schema (v1.4 & v1.5) and
  DT Schema (v1.2 & v1.3)
* Added Annex defining additional requirements for BBF standard data
  models

### DM Data Model Definition Schema (DM Schema)
* Added *profile/@minVersion* attribute
* Allowed *uniqueKey* parameters to be in sub-objects
* Added *UUID* data type
* Added *nestedBrackets* attribute, and allowed use of the
  *list* facet in named data type definitions
* Several other minor updates and clarifications

### Device Type Schema (DT Schema)
* Many minor updates and clarifications

## 2011-07-01: [TR-106 Amendment 6]

*Tag: [v1.6.0]*

### TR-106 Document
* Removed definition of proxying, now defined in TR-069
* Removed Common objects
* Alias Parameter Requirements added

### DM Data Model Definition Schema (DM Schema)
* Added top-level *file* attribute

### Device Type Schema (DT Schema)
* Added top-level UUID data type and attribute

## 2010-11-01: [TR-106 Amendment 5]

*Tag: [v1.5.0]*

### TR-106 Document
* Replaced definitions of named data types such as IPAddress with
  references to normative XML
* Minor changes to DM Schema (v1.3) and DT Schema (v1.1)

### DM Data Model Definition Schema (DM Schema)
* Relaxed some referential constraints (in the light of experience)
* Added *description/@action* prefix option
* Added *syntax/@command*

### Device Type Schema (DT Schema)
* Minor changes tracking DM Schema v1.3 changes

## 2010-02-01: [TR-106 Amendment 4]

*Tag: [v1.4.0]*

### TR-106 Document
* Moved data model definitions to TR-181 Issue 1

### DM Data Model Definition Schema (DM Schema)
* Distinguished functional and non-functional keys
* Supported *#.A* relative path syntax

## 2009-09-01: [TR-106 Amendment 3]

*Tag: [v1.3.0]*

### TR-106 Document
* Addition of device type XML Schema

### DM Data Model Definition Schema (DM Schema)
* Made *import/@file* optional
* Supported *range/@step*

### Data Model Report Schema (DMR Schema)
* Added *noUniqueKeys*

### Device Type Schema (DT Schema)
* Original

### DT (Device Type) Features Schema (DTF Schema)
* Original

## 2008-11-01: [TR-106 Amendment 2]

*Tag: [v1.2.0]*

### TR-106 Document
* Addition of data model definition XML Schema and normative XML
  common object and component definitions

### Data Model
* Minor clarifications

### DM Data Model Definition Schema (DM Schema)
* Original

### Data Model Report Schema (DMR Schema)
* Original

## 2006-11-01: [TR-106 Amendment 1]

### TR-106 Document
* Clarification of original document

### Data Model
* Added TR-069 Annex F and G ("TR-111") objects
* Many clarifications to parameter descriptions

## 2005-09-01: [TR-106 Issue 1]

### TR-106 Document
* Original

### Data Model
* Original

[TR-106 Amendment 1]: https://www.broadband-forum.org/download/TR-106_Amendment-1.pdf
[TR-106 Amendment 10]: https://www.broadband-forum.org/download/TR-106_Amendment-10.pdf
[TR-106 Amendment 11]: https://www.broadband-forum.org/download/TR-106_Amendment-11.pdf
[TR-106 Amendment 12]: https://www.broadband-forum.org/download/TR-106_Amendment-12.pdf
[TR-106 Amendment 13]: https://www.broadband-forum.org/download/TR-106_Amendment-13.pdf
[TR-106 Amendment 14]: https://www.broadband-forum.org/download/TR-106_Amendment-14.pdf
[TR-106 Amendment 2]: https://www.broadband-forum.org/download/TR-106_Amendment-2.pdf
[TR-106 Amendment 3]: https://www.broadband-forum.org/download/TR-106_Amendment-3.pdf
[TR-106 Amendment 4]: https://www.broadband-forum.org/download/TR-106_Amendment-4.pdf
[TR-106 Amendment 5]: https://www.broadband-forum.org/download/TR-106_Amendment-5.pdf
[TR-106 Amendment 6]: https://www.broadband-forum.org/download/TR-106_Amendment-6.pdf
[TR-106 Amendment 7]: https://www.broadband-forum.org/download/TR-106_Amendment-7.pdf
[TR-106 Amendment 8]: https://www.broadband-forum.org/download/TR-106_Amendment-8.pdf
[TR-106 Issue 1]: https://www.broadband-forum.org/download/TR-106_Issue-1.pdf
[v1.2.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.2.0
[v1.3.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.3.0
[v1.4.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.4.0
[v1.5.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.5.0
[v1.6.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.6.0
[v1.7.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.7.0
[v1.7.0+]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.7.0+
[v1.8.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.8.0
[v1.9.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.9.0
[v1.10.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.10.0
[v1.11.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.11.0
[v1.12.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.12.0
[v1.13.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.13.0
[v1.14.0]: https://github.com/BroadbandForum/data-model-template/releases/tag/v1.14.0
