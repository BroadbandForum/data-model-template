<!-- do not edit! this file was created from PROJECT.yaml by project-parser.py -->

### Issue History {.unnumbered .unlisted .new-page}

::: {.list-table .bbf-revision-history aligns=l,l,l,l widths=14,14,14,65}

* - Issue Number
  - Approval Date
  - Issue Editor
  - Changes

* - [Issue 1][TR-106 Issue 1]
  - September 2005
  - * Jeff Bernstein, 2Wire
    * Christele Bouchat, Alcatel
    * Tim Spets, Westell
  - * Original

* - [Amendment 1][TR-106 Amendment 1]
  - November 2006
  - * Jeff Bernstein, 2Wire
    * John Blackford, 2Wire
    * Mike Digdon, SupportSoft
    * Heather Kirksey, Motive
    * William Lupton, 2Wire
    * Anton Okmianski, Cisco
  - * Clarification of original document

* - [Amendment 2][TR-106 Amendment 2]
  - November 2008
  - * William Lupton, 2Wire
    * Håkan Westin, Tilgin
  - * Addition of data model definition XML Schema and normative XML
      common object and component definitions

* - [Amendment 3][TR-106 Amendment 3]
  - September 2009
  - * William Lupton, 2Wire
    * Håkan Westin, Tilgin
  - * Addition of device type XML Schema

* - [Amendment 4][TR-106 Amendment 4]
  - February 2010
  - * William Lupton, 2Wire
    * Paul Sigurdson, Broadband Forum
  - * Moved data model definitions to TR-181 Issue 1

* - [Amendment 5][TR-106 Amendment 5]
  - November 2010
  - * Paul Sigurdson, Broadband Forum
  - * Replaced definitions of named data types such as IPAddress with
      references to normative XML
    * Minor changes to DM Schema (v1.3) and DT Schema (v1.1)

* - [Amendment 6][TR-106 Amendment 6]
  - July 2011
  - * Sarah Banks, Cisco
    * Andrea Colmegna, FASTWEB
    * Tim Spets, Motorola Mobility
  - * Removed definition of proxying, now defined in TR-069
    * Removed Common objects
    * Alias Parameter Requirements added

* - [Amendment 7][TR-106 Amendment 7]
  - September 2013
  - * William Lupton, Cisco
  - * Added descriptions of new features in DM Schema (v1.4 & v1.5) and
      DT Schema (v1.2 & v1.3)
    * Added Annex defining additional requirements for BBF standard data
      models

* - Amendment 7
  - September 2014
  -
  - * Support file updates; document not updated

* - [Amendment 8][TR-106 Amendment 8]
  - May 2018
  - * Jean-Didier Ott, Orange
    * William Lupton, Broadband Forum
  - * Added support of USP (mountable objects)
    * Removed references to obsolete data models
    * Moved device requirements to TR-069

* - Amendment 9
  - September 2019
  -
  - * Document not updated

* - [Amendment 10][TR-106 Amendment 10]
  - November 2020
  - * William Lupton, Broadband Forum
  - * Converted document to markdown
    * Various editorial improvements

* - [Amendment 11][TR-106 Amendment 11]
  - January 2022
  - * William Lupton, Broadband Forum
  - * Clarified *forcedEnabled* and *forceDefaultEnabled* for USP
    * Clarified impact of deprecating or obsoleting profile items
    * Documented new description templates
    * Documented new *secured* attribute

* - [Amendment 12][TR-106 Amendment 12]
  - June 2023
  - * William Lupton, Broadband Forum
  - * Updated the *Mountable Object* and *Mount Point* descriptions to
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

:::

### %bbfWorkArea% Work Area Directors {.unnumbered .unlisted}

* Jason Walls, QA Cafe
* John Blackford, CommScope

### %bbfProjectStream% Project Stream Leaders {.unnumbered .unlisted}

* Daniel Egger, Axiros
* William Lupton, Broadband Forum

[TR-106 Amendment 1]: https://www.broadband-forum.org/download/TR-106_Amendment-1.pdf
[TR-106 Amendment 10]: https://www.broadband-forum.org/download/TR-106_Amendment-10.pdf
[TR-106 Amendment 11]: https://www.broadband-forum.org/download/TR-106_Amendment-11.pdf
[TR-106 Amendment 12]: https://www.broadband-forum.org/download/TR-106_Amendment-12.pdf
[TR-106 Amendment 2]: https://www.broadband-forum.org/download/TR-106_Amendment-2.pdf
[TR-106 Amendment 3]: https://www.broadband-forum.org/download/TR-106_Amendment-3.pdf
[TR-106 Amendment 4]: https://www.broadband-forum.org/download/TR-106_Amendment-4.pdf
[TR-106 Amendment 5]: https://www.broadband-forum.org/download/TR-106_Amendment-5.pdf
[TR-106 Amendment 6]: https://www.broadband-forum.org/download/TR-106_Amendment-6.pdf
[TR-106 Amendment 7]: https://www.broadband-forum.org/download/TR-106_Amendment-7.pdf
[TR-106 Amendment 8]: https://www.broadband-forum.org/download/TR-106_Amendment-8.pdf
[TR-106 Issue 1]: https://www.broadband-forum.org/download/TR-106_Issue-1.pdf
