\---

confluence-id: 176490184

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-11-04 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Nov 04, 2019

Date
----

04 Nov 2019

Attendees
---------

*   John Kunze
    
*   Curtis Mirci
    
*   Greg Janée
*   Sheila Morrissey
*   Tom Creighton

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | Announcements. |     | New working group member, Karen Hanson, will be replacing Sheila towards the end of the year. |
|     | revisiting new inflection, ?info, as landing page – [new document summarizing discussion so far](https://wiki.duraspace.org/display/ARKs/Inflection+change+proposal)<br><br>Proposed: for any ARK _X_, _X_?info should lead to an HTML-formatted "landing" document (page) with metadata embedded as JSON-LD. The metadata, in human- and machine-readable form, includes<br><br>1.  The ARK _X_<br>2.  Descriptive metadata:<br>    1.  who<br>    2.  what<br>    3.  when<br>    4.  where<br>    5.  how ([metatype](https://n2t.net/e/n2t_apidoc.html), similar to resourcetype)<br>    6.  domain-specific elements (eg, publications vs physical samples vs vocabulary terms)<br>3.  PIDs to first-level variants (versions, formats, change history) and components of _X_, if any<br>4.  PID to the first logical ancestor of _X_<br>    1.  eg, if _X_ is a PDF variant of a document object, this points to the logical object ARK listing _X_ along with its sibling HTML and MSWord forms<br>5.  PID to the **last** logical ancestor of _X_<br>    1.  eg, if _X_ is a section of a chapter of a book, this points to the book logical object<br>6.  Change history, if any<br>7.  Licensing and accessibility information<br>8.  How to cite, including "cite-as" header<br>9.  Persistence statement<br><br>A great example to follow would be the [A data citation roadmap for scholarly data repositories](https://n2t.net/doi:10.1038/s41597-019-0031-8). |     | JK gave a walk through of the proposal sketch<br><br>TC: there's a distinction to be made between aggregation (UML sense) vs containment (ARK sense)<br><br>GJ: overall like the proposal, especially in providing a list of defined slots to populate that are mostly optional; suspect that most people won't have all the fields  <br>GJ: the citation roadmap paper doesn't commit to metadata; perhaps we should recommend something? this proposal differs from others in that the ERC recommendation doesn't distinguish Publisher, while the publishing community recommendation does distinguish Publisher  <br>JK: the Publisher distinction can be made in the domain-specific core elements that follow the kernel/ERC elementsGJ: should have a "how to cite" element  <br>SM: yes, it would be very useful to have citation information  <br>SM: how do we thread the needle between what we want and making things work with standards?  <br>JK: hopefully we can use something like yamz.net to move things forward  <br>SM: recommend to be loose enough in language we use about metadata and not let the ARK spec get bogged down in endless metadata discussions  <br>TC: what if I only want the JSON and not the HTML, eg, what if I use the Accept-Header to ask for JSON-LD? that shouldn't return HTML + JSON, right?  <br>GJ: there may already be standards and conventions on how to do this – I will investigate |

Action items
------------

- [ ] Greg Janée Look into what is expected for html vs json responses.