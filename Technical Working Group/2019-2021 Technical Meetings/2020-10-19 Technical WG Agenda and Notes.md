\---

confluence-id: 195167991

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-10-19 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Oct 19, 2020

Date
----

19 Oct 2020

Attendees
---------

*   John Kunze
    
*   Roxana Maurer
    
*   Mark Phillips
*   Karen Hanson
*   Tom Creighton
*   Curtis Mirci

Goals
-----

*   making progress on the ark?info inflection definition

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements<br><br>![](http://n2t.net/e/images/naan_growth.png) |     | *   Grant funded for IDs for physical specimens: archaeological, geo samples, etc.<br>*   N2T resolver enhancement:<br>    *   CORS support<br>    *   Prefix extension mechanism “-dev” added to <br>    *   NaaN registry updates reflected automatically in a graphical fashion<br>    *   New website by National Library Luxembourg: [https://info.persist.lu/en/](https://info.persist.lu/en/)<br>*   A method for encoding IDs: [https://github.com/tcreighton/brevis](https://github.com/tcreighton/brevis) |
|     | [metadata model V2](https://docs.google.com/document/d/1jMpnjit9aVAW_lhnXidsiBi_DDhvzV565xvDfXBvEqg/edit)<br><br>how to make (faster) progress on defining what should come back from an ark?info inflection request |     | *   KH: wishlist is helpful  <br>        looking for something simple to specify, eg, kernel  <br>        but it can wait, so that we finish the spec.  <br>        regarding n2t, it could be a reference or exemplar implementation<br>*   Mark: unless you're creating a place to hang the core metadata,  <br>          here's where you put the core elements, but don't think we should  <br>                be in the business of defining those cores  <br>          point to community mechanisms for defining the cores,  <br>                but don't define themInfo? inflection data: what should be returned?<br>*   Figuring out exactly what should be in the core spec vs extension is not easy.<br>    *   New a couple of pages added to clarify the intent.<br>    *   need use case approach.<br><br>TC: what machines will be requesting this?  <br>JK: I'd say same as the LOD users |
|     | adopt-a-thing (use case)<br><br>*   journals/articles<br>*   natural history specimens<br>*   genealogical records<br>*   archival record/object<br>*   vocabulary terms<br>*   persons<br>*   events<br>*   archaeological artifact<br>*   water sample |     | *   adopt-a-thing<br>    *   various assignments made<br>    *   right now just trying to understand what metadata is of most value in a domain<br><br>TC: what I'd like my users to be able to look at a thing with an ARK and to get  <br>a formal citation to it and to its parent;  <br>      would be willing to sign up for this genealogical citation use case,  <br>      also  possibly for persons  <br>KH: I could do the journal article use case  <br>MP: I'll look into archival record use case  <br>RM: here's an example authority record. is it a person  <br>JK: if it could be a person or org, maybe it's an Agent  <br>KH: how to put structure around, mechanism to bridge between core and kernel  <br>KH: how about pulling out the DataCite examples and applying this to it?MP: reminds me of what IIIF does, eg, here's where pairs go  <br>    define structure  <br>CM: will get advice from Brian about helping with use case |

  

Action items
------------