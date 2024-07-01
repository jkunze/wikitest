\---

confluence-id: 294453593

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-07-11 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Jul 21, 2023

Date
----

11 Jul 2023

Attendees
---------

*   Dave Vieglais, Donny Winston, Tom Creighton, Greg Janee, John Kunze
    

Goals
-----

Changes to NAAN processing, spec transition step dependency, inline links

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | jk: ARK tutorial at upcoming ESIP conference  <br>dv: ESIP does good hybrid sessions; I won't be able to make it there; one thing that may be useful is a comparison with DOIs; one specific limitation is that the DOI spec says that a DOI resolver service needs to respond to a content negotiation request, such as for JSONLD, by consulting the resolver itself (eg, DataCite) rather than the primary provider; ARKs have more flexible in this regard |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     |     |
| new NAAN schema for validation and form processing |     | dv: please get feedback on NAAN processing changes to Maria  <br>dv: AuthN for NAAN records will be based on email address confirmation; this is still work in progress |
| ARK spec [transition plan](https://docs.google.com/document/d/1aFgujlL5yE3ZUORXRRkDTDNrlZEQU69lOU6Gc3wlyt4/edit#heading=h.71xqg8hedqw6)<br><br>*   Tom Creighton analysis of event date ordering and dependencies<br>*   date of interest to NAAN group: when do we advise new NAAN holders to resolve both forms? do we point them to one of the newer specs?<br><br>  <br><br>Questions:<br><br>*   for widely used tools that "we" control, eg, NOID, should the tool be updated to support new form ARKs? Besides NOID, are there others? |     | ![](attachments/294453593/296681549.png) |
| Speculative section – links with inline/inlink content<br><br>Web edge case for tiny objects carried inside URLs, eg,<br><br>*   IIIF annotations<br>*   semantic web triple ("nanopublication")<br>*   semantic web concept, otherwise undefined (purl.org has lots of these)<br>*   sequence of column headers<br>*   set of related links (special kind of annotation?)<br><br>Might ARKs play a helpful role in one or more of these cases? |     | jk: some interesting use cases have arisen in this area and we'll be doing some experiments with, for example, inline links  <br>gj: there's a [TAG URI](https://en.wikipedia.org/wiki/Tag_URI_scheme) for just this purpose; I don't know why it didn't catch on |

Action items
------------

Attachments:
------------

![](images/icons/bullet_blue.gif) [image-2023-7-11\_7-29-59.png](attachments/294453593/296681549.png) (image/png)