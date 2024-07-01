\---

confluence-id: 176491167

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-11-18 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Dec 13, 2019

Date
----

18 Nov 2019

Attendees
---------

*   John Kunze
    
*   Curtis Mirci
*   Greg Janée
*   Karen Hanson
*   Tom Creighton
*   Bertrand Caron
*   Sheila Morrissey
    

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | Announcements | JK  | Personally identifiable information in the NAAN registry.  John is looking at Github actions to automatically strip.  Pre-generated 10,000 NAANs to remove need for running eggnog to mint. |
|     | Continued discussion of ["?info" inflection proposal](https://wiki.duraspace.org/display/ARKs/Inflection+change+proposal) (latest at the end)<br><br>JSON encodings/formats: JSON-LD, geoJSON?<br><br>*   what about comments and repeated element keys, which were possible with ERC? |     | (JK) Proposing ? and ?? be left untouched, "reserved for future use," but ?info would be required.  ?info return metadata would not be detailed in the ARK spec per previous meeting.  Looking for couple volunteers over next month to help brainstorm over what ?info might return. KH, CM, GJ willing to help.<br><br>General discussion on JSON, JSON-LD, etc.  (TC) If intent is for machine readability, then JSON is the answer.  TC's group has adopted JSON-LD extensively.  (GJ) JSON-LD is the mainstream practice on the web, and Data Citation Roadmap paper (Fenner et al) recommends it.  Is there any reason to do something different? (GJ) JSON-LD is implementation/serialization of RDF.  Defined by W3C standard, which specifies content negotiation and application/ld+json content type.  (TC) Good reference on understanding JSON-LD, schema.org, etc.: [https://developers.google.com/search/docs/guides/intro-structured-data](https://developers.google.com/search/docs/guides/intro-structured-data)<br><br>  <br>JK: what about json problems  <br>TC: what's the intent? doesn't always work, eg, config in amazon cloud, eg, comments. YAML is more popular for config, some movement for comments in JSON but not there yet.  <br>KH: has there been discussion of conneg?  <br>TC: yes, we need to know how we get what  <br>SM: for part 3 above, should be focus on vocabulary rather than syntax  <br>TC: agree, focus on content rather in a syntax-neutral way  <br>GJ: what about data citation roadmap paper, which prescribes JSON-LD?  <br>GJ: in my investigation of json-ld, conneg is used to request json-ld, which is considered a serialization of RDF; many people are consolidating on this; no one golden doc that lays it out; most of this driven by the web: html with embedded json-ld  <br>CM: mainstream is probably best  <br>TC: we've adopted json-ld  <br>TC: google recommends use of [schema.org](http://schema.org) classes for json-ld; try [https://developers.google.com/search/docs/guides/intro-structured-data](https://developers.google.com/search/docs/guides/intro-structured-data)  <br>KH: <link header> is another option; matter of choosing which one or both |
|     | Status check on milestones; remaining to-do list, and rough estimates for objectives and deliverables<br><br>([Technical Working Group](Technical-Working-Group_108757991.html))<br><br>*   ARK spec (finish draft, circulate, submit to IETF)<br>*   NAAN procedures<br>*   ARKS counting |     | All deliverables delayed.  Deliverables page, charter need updating.  Will visit topic next meeting. |

Action items
------------

- [x] subgroup will meet to work further on ?info response (notes below)
- [x] John Kunze revise deliverable schedule for next time

2019.11.26 subgroup notes: Greg, Karen, John

GJ: conneg is invisible to resolver? because repo should handle it?  
GJ: is ?info handled differently?  
JK: we need to define this better: when does first resolver vs last resolver  
GJ: \*\* Which Agent handles ?info conneg request – must be defined  
KH: like to have configuration option for NAAN entry to say whether to pass thru or have first resolver  
GJ: geojson seems difficult place to start compared to json-ld  
KH: like the idea of having required core plus optional stuff; prefer minimal json-ld; believe you can use other vocabularies just use multiple @contexts, eg, for geo and dublin kernel  
KH: \* should test whether json-ld extensions would break features  
KH: could be recommended, with optional  
KH: like the idea of: if you do anything, do this