\---

confluence-id: 225149387

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-10-12 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Oct 12, 2021

Date
----

12 Oct 2021

Attendees
---------

*   Mark Phillips 
*   Karen Hanson 
*   Curtis Mirci 
*   Amir Alwash 
*   Tom Creighton 
*   John Kunze 

Goals
-----

     New spec diffs; collaboration via github; action items from before

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| announcements |     |     |
| calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     | AA: late November in Switzerland will present ARKetype results to: "P-5 Outcomes: Scientific Information Services for All" |
| Strawman spec collaboration via githup:<br><br>[https://github.com/jkunze/arkspec](https://github.com/jkunze/arkspec) |     | JK: stub repo, not yet populated with ARK draft; need to add collaborators  <br>MP: github repo looks correct; good to show openness, change history; it also signals that we're interested in others' opinions  <br>JK: ok to invite you all as committers?  <br>All: agreed |
| [New spec (29)](https://www.ietf.org/archive/id/draft-kunze-ark-29.txt) plus [diffs 29-28](https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-29.txt&url2=draft-kunze-ark-28.txt) |     |     |
| Action items from last time<br><br>- [x] John Kunze Dave Vieglais Clarify that using a subfolder after the domain and before the ark: is acceptable<br>- [x] John Kunze update [arks.org](http://arks.org) to point to latest version of spec<br>- [x] Mark Phillips Dave Vieglais Mark will research options for managing a spec through GitHub, Dave will come up with ideas/suggestions and work with Mark on a recommendation.<br>- [x] Dave Vieglais Greg Janée Dave will suggest some text for a section or appendix on best practices for transmitting ARKs in URLs (eg, don't be too strict about %-encoding), Greg will review.<br>- [x] John Kunze Changes to normalization steps. Point #5 in normalization fix “uppercase” and based on team discussion, point 6 on Unicode should be very loose, something that is good to be aware of but more of an implementation choice. Need to determine where to move it to if it is moved from here<br>- [x] John Kunze Spec: reduce number of ways to say Base Name (instead of Name or Base) |     | First stab at new wording.<br><br>  <br><br>  <br><br>  <br><br>  <br><br>  <br><br>  <br><br>TC: will review and comment  <br>TC: will try to come up with EBNF for ARKs<br><br>  <br><br>KH, CM, TC: +1 to unicode hyphens |

Action items
------------

- [ ] John Kunze add draft spec to repo and invite collaborators
- [ ] Tom Creighton review and comment on URI best practices doc
- [ ] Tom Creighton draft an EBNF for ARKs