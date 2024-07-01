\---

confluence-id: 230819906

confluence-space: %%CONFLUENCE-SPACE%%

\---

2022-02-08 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Feb 08, 2022

Date
----

08 Feb 2022

Attendees
---------

*   Mark Phillips John Kunze Karen Hanson Curtis Mirci Dave Vieglais Tom Creighton 

Goals
-----

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | Texas Conference on Digital Library proposal for a PID workshop with a strong representation of ARKs.   <br>[https://www.tdl.org/tdl-events/tcdl/2022-tcdl/](https://www.tdl.org/tdl-events/tcdl/2022-tcdl/)<br><br>Recently hit 900th NAAN registration |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     | KH very probably be speaking at CNI |
| Any news items we should blog about? |     | JK: blog about/ tweet about RFC news? invite people to [ark@ietf.org](mailto:ark@ietf.org)  <br>DV: could we take advantage to attract review? |
| Reschedule to meet on hour earlier? |     | all: ok |
| Status of ARK spec in RFC Editor queue:<br><br>_\===_  <br>_The Independent Submissions Stream RFC Editor (ISE) has accepted to work_ _on the document with a view to publishing it as an Informational RFC_ _outside the IETF. The ISE's next task is to review the work and then_ _commission some independent reviews. The process from here to a published_ _RFC could be between 3 and 6 months._  <br>  <br>_We have established an email list within the IETF to discuss the work:_ _although this list has so far been quiet, it is very early days._ |     | JK: have you all signed up for [ark@ietf.org](mailto:ark@ietf.org) ? please remember to do  <br>Action: verify who's on the list |
| Seeding the [ark@ietf.org](mailto:ark@ietf.org) discussion<br><br>*   which discussion should we keep more private on the googlegroup? how do we decide? |     | JK: are people ok with [ark@ietf.org](mailto:ark@ietf.org) for wider review, reserve googlegroup for private discussion?  <br>TC, MP: ok  <br>All: "use good judgement" in sending to [ark@ietf.org](mailto:ark@ietf.org) |
| Anticipating questions about URL encoding<br><br>*   includes question of colon ':' and '/' and when to percent-encode them |     | DV: I go back and forth on encoding ark in query string  <br>TC: maybe we should say there's flexibility (like the URI spec), but acknowledge that people tend to like human readable  <br>DV: would be good to have a simple recommendation on publishing ARKs  <br>JK: can we take a page from the web archiving folks?  <br>MP: [https://github.com/iipc/urlcanon](https://github.com/iipc/urlcanon)  <br>JK: use the word "publishing an ARK"?  <br>TC: how about the word "canonical" in prose and link tags?  <br>JK: if we're talking canonical, maybe UUIDs _should_ have hyphens even if we discourage hyphens elsewhere?  <br>JK: who wants to help write section of the ARK specDV: raising hand |
| Planning transition to new spec. Would like to propose a joint operation with Outreach WG. |     | DV: start by communicating should include a list of changes  <br>TC: it will be hard to transition since we use colons as separators |

Action items
------------

- [ ] John Kunze identify people not yet signed on to ietf list
- [ ] John Kunze Dave Vieglais draft spec section on URL encoding recommendations; consider what to say about publishing hyphens, eg, discouraged except where expected, as in UUIDs? (ask Smithsonian about their practice)