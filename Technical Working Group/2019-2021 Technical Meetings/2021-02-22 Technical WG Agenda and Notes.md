\---

confluence-id: 204865829

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-02-22 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Apr 16, 2021

Date
----

22 Feb 2021

Attendees
---------

*   John Kunze 
*   Dave Vieglais
*   Curtis Mirci 
*   Mark Phillips 
*   Karen Hanson 
*   Roxana Maurer 
*   Greg Janée 

Goals
-----

*   Plan transition to new spec

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements<br><br>New WG member: Dave Vieglais, Natural History Museum and Biodiversity Research Center, University of Kansas |     |     |
|     | upcoming meetings, calls for papers, submission deadlines |     | RDA? DV will check into. _Update from Dave:_ <br><br>_Looks like request for papers is closed for RDA 17 (April 20-22), though posters is still open:_<br><br> _[https://www.rd-alliance.org/rdas-17th-plenary-call-posters](https://www.rd-alliance.org/rdas-17th-plenary-call-posters)_<br><br>_The next RDA plenary 18 is November 8-11, but there's not CfP yet._ |
|     | New spec ([V27](https://datatracker.ietf.org/doc/html/draft-kunze-ark)), with spec changes in response to last time:<br><br>[https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-26.txt&url2=draft-kunze-ark-27.txt](https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-26.txt&url2=draft-kunze-ark-27.txt)<br><br>Note: propose dropping the the sorting of suffixes, eg, .../sect2/para3.en.v5.pdf.gz<br><br>(original rationale for sorting was to support end-user "variant requests" in different orders, eg, does .en.v5 == .v5.en ?)<br><br>Changes since before last meeting:<br><br>[https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-24.txt&url2=draft-kunze-ark-27.txt](https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-24.txt&url2=draft-kunze-ark-27.txt) |     | Clarified "high quality" language.  Pursuant to last discussion, removed requirement to order suffixes during normalization.  JK action item: clean up usages of term "suffix". |
|     | Planning transition from V18 spec to V26+ spec, once it has settled. Requirements for **received ARKs** after transition:<br><br>R1. "/" becomes optional (ark:/12345 = ark:12345), means systems must **not** reject as malformed any ARKs received (eg, externally produced) only because there is no "/" between the "ark:" and the NAAN. <br><br>R2. All implementations, past and future, must **not** reject as malformed any ARK only because there is a "/" between the "ark:" and the NAAN.<br><br>R3. NAAN no longer just 5 digits, means systems must **not** reject as malformed any ARKs received (eg, externally produced) only because the NAAN doesn't match the regex "^\\d{5}$". The new restriction is to a run of one or more betanumeric (0123456789bcdfghjkmnpqrstvwxz) characters.<br><br>Question: should there be a minimum maximum, eg, must accept NAANs of at least 32 octets?<br><br>R4. Length restrictions are relaxed on the string formed from the Name (starting "ark:") plus Qualifier, which means systems must **not** reject as malformed any ARKs received (eg, externally produced) only because the string is longer than 128 octets. At a minimum, implementations that limit its length must accept strings of length 255 octets. |     | NAAN length: useful to have a limit, but 32 seems too big.  Extra characters useful not so much because there will be huge numbers of NAANs, but to support possible distributed namespace control within NAANs.  Consensus: limit in the range 10-16 seems good. |
|     | Planning transition from V18 spec to V26+ spec, once it has settled. Requirements for **generated ARKs** after transition:<br><br>FAQ1: does this transition affect how my implementation is required to store my ARKs (eg, with or without "/")? **NO**<br><br>FAQ2: does this transition affect how my implementation is required to advertise/publish ARKs? _Big change_ – should it be a phased transition over N years?<br><br>FAQ3: is there a validation service to test my ARKs?<br><br>FAQ4: when does the transition take effect? |     | There are no backward incompatible changes, so ARK generators should be fine and no existing ARKs will break. The discussion is limited to encouraging uptake of new shorter form (no "/").<br><br>Dropping the requirement of the slash in ark:/ will create problems for users doing simple string comparison of ARKs.  E.g., RDF mandates that URIs be compared as simple strings (despite the fact that HTTP URIs also have alternative, equivalent forms).  Need to think through the implications here.<br><br>RM: we have published our ARKs from beginning with ark: not ark:/<br><br>MP: good to have a toolkit to compare and/or validate post-transition ARKs |
|     | As we have seen before, a "provisional" [ARK URI scheme](https://tools.ietf.org/html/draft-ark-uri-scheme-00) is listed in the [URI registry](https://www.iana.org/assignments/uri-schemes/uri-schemes.xhtml)<br><br>Do we have a position on it? Endorse? Must have? Would be nice? |     | DV: would be nice to have an endorsed URI spec; do we have use cases for it? |

Action items
------------

- [x] John Kunze clean up usages of term "suffix"
- [x] John Kunze add DV to wiki logins
- [x] DV to look into RDA conference deadlines