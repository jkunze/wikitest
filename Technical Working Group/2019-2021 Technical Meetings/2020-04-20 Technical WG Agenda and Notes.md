\---

confluence-id: 187171547

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-04-20 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified by Roxana Maurer on Apr 20, 2020

Date
----

20 Apr 2020

Attendees
---------

*   John Kunze
    
*   Roxana Maurer
    
*   Karen Hanson
    
*   Julien Antoine Raemy
    
*   Mark Phillips
    
*   Bertrand Caron
    
*   Tom Creighton 
    

Goals
-----

*   Recalibration

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | Announcements |     | RM: the [Digital Heritage Network’s Persistent Identifiers project](https://www.pidwijzer.nl/en/about) has lots of info and materials about PIDs, but don't know much about ARKs; maybe Outreach should contact them?  <br>[https://www.pidwijzer.nl/en](https://www.pidwijzer.nl/en)  <br>[https://www.youtube.com/watch?v=rIvManSuguw](https://www.youtube.com/watch?v=rIvManSuguw) |
|     | Better sharing of 99999 NAAN for test/fake ARKs |     | TC: having ability to forward shoulders under one NAAN is much better than using multiple NAANs; also a convention to support temp ARKs may work better than configuration requirement  <br>RM: could make organizational shoulders that look like the organizational NAANs, so by convention you don't collide, which avoids need to register  <br>JR: for INCIPIT project we want test ARKs w.o. using our own NAAN  <br>JK: maybe accommodate both  <br>BC: BNF could probably use this  <br>KH: should shoulders be a temporary shoulder registration?  <br>JK: that wouldn't work for, say EZID; ironically, there's a long-term need for temporary ARKs, eg, whenever you install a bug fix we mint a fake ARK as a basic test to see if things are working |
|     | Meeting frequency and preparation |     | JK: ok to reduce meeting frequency to once a month?  <br>All: ok, canceling first Monday meeting |
|     | Consolidation of recent concept exploration around _X_?info<br><br>*   Revisit basic requirements<br>    *   return basic information about _X_<br>    *   return a persistence statement<br>    *   don't depart too far from original ARK spec  <br>        *   retain ability to add optional richer metadata<br>        *   retain ability to use other formats<br>        *   retain spirit of ERC/ANVL/THUMP and Dublin Kernel "story" metadata<br>*   Concept that _X_ can refer to a landing page, and what that means for _X_?info<br>*   Concept that _X_ can refer to a plunging (non-landing) page, and what that means<br>*   Concept that resolution may in general involve multiple resolvers, any of which might be tasked to respond to _X_?info (tradeoffs)<br>*   Unknown: can/should we support notion of _X_ referring to one or more of these (avoiding the more challenging terminology of the Networked Entity Model):<br>    *   bp (born physical) thing<br>    *   bd (born digital) thing<br>    *   bc (born conceptual, eg, vocabulary term) thing<br>    *   dfp (digital from physical, eg, scanned document)<br>    *   dfd (digital from digital, eg, lower res surrogate from master image)<br>    *   pfp (physical from physical, eg, photographic print of painting)<br>    *   pfd (physical from digital, eg, German wikipedia is printed and bound annually) |     | JK: (summarize agenda item)  <br>MP: dfd -- when do we know that?  <br>MP: important to know why are there so few implementers of some areas  <br>JK: yes, eg, ? and ?? hard to recognize, leading to change to use ?info<br><br>RM: some of this is apropos Mario's email about landing page vs resource  <br>KH: also, for the rmap project, the :/ after ark caused problems; even though the "/" is now deprecated, the ":" by itself still causes a few problems  <br>MP: technical challenges implementing certain things create cost/benefit tradeoff that may not be worth it  <br>JK: other things we're doing to make the cost lower is to change recommendation from ANVL to YAML/JSON<br><br>JK:  Also, we could use a place holder to indicate the count below in the namespace created by the ARK, (a kind of enumeration point, as Smithsonian uses it); this could actually be considered a piece of the counting ARKs project |

Action items
------------

- [x] John Kunze will cancel first Monday of month meeting series
- [ ] John Kunze will talk to Outreach WG about contacting the Digital Heritage Network [info@netwerkdigitaalerfgoed.nl](mailto:info@netwerkdigitaalerfgoed.nl)