\---

confluence-id: 204865699

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-02-01 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Feb 22, 2021

Date
----

01 Feb 2021

Attendees
---------

*   John Kunze 
*   Bertrand Caron 
*   Karen Hanson 
*   Mark Phillips 
*   Curtis Mirci 
*   Greg Janée 
*   Roxana Maurer 

Goals
-----

*   Spec finalize and implementation plan

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     | JK: first (mailchimp) newsletter failed to go out today; will investigate; suspect RSS feed failure  <br>BC: issue appeared on French forum concerning how n2t normalizes hyphens out of ARKs before redirecting  <br>JK: yes, feature rather than bug; but what do others think? (no disagreement)  <br>Action: BC will send ARK Alliance announcement to French forum |
|     | upcoming meetings, calls for papers, submission deadlines<br><br>*   PASIG<br>*   ARKA newsletter<br>*   Feb 22 IETF submission cutoff |     | Action: JK will inquire about PASIG deadline (since it wasn't available online)  <br>Action: All: please think about topics for the ARKA newsletter  <br>JK: Feb 22 IETF cutoff is just a temporary outage of IETF submissions for a period surrounding each meeting |
|     | new draft spec: <br><br>[https://www.ietf.org/archive/id/draft-kunze-ark-26.txt](https://www.ietf.org/archive/id/draft-kunze-ark-26.txt)<br><br>*   description of shoulders (catch up to FAQ)<br>*   define betanumeric and primordinal (catch up to FAQ)<br>*   replacing non-working examples with (nearly) working examples<br><br>diffs between this spec and last spec discussed<br><br>[https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-24.txt&url2=draft-kunze-ark-26.txt](https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-24.txt&url2=draft-kunze-ark-26.txt) |     | RM: section 1.3 – is it true that "high quality access" is the central duty, and doesn't "high quality" risk being confused with "access to high-quality objects"  <br>JK: definitely _not_ meant to be a statement about quality of the objects, but quality of the access; persistent access is still very important, but the ability to set expectations (weak or strong) could as easily enable a powerful mechanism to promise the opposite (eg, single-use links)  <br>Action: clarify  <br>GJ: what is the use case of multiple suffixes? could we clarify that multiple suffix normalization is for comparing arks rather than publishing them?  <br>GJ: general notion of what normalization is for could use clarification, not just for comparison, but also for resolution; should suffix order matter? why?  <br>Action: clarify  <br>RM: need to clarify whether changing order of suffixes is equivalent  <br>CM: what if suffixes don't match? ok to resolve to parent object so if you can't normalize the user at least sees something  <br>MP: yes, at UNT we might change our minds, and will resolve older qualifiers to the parent object |
|     | Spec to do:<br><br>*   normalization of encodings<br>*   point to structured area for ongoing work (arks.org/labs ?) |     | JK: what's left before RFC submission; where do we continue our work -- using [arks.org/labs](http://arks.org/labs)?  <br>JK: need to catch up shoulder spec docs with shoulder FAQ |
|     | Wikipedia ARK - is this as much Tech WG as Outreach WG? |     | JK: arks.org rollout brought wikipedia page to the fore; some of the problem is that the page has real overlap with spec (Tech WG)  <br>BC: recently reviewed French wikipedia page and will forward results  <br>JK: Action: go back and review where we got with outreach wg |

Action items
------------

- [x] Bertrand Caron will send ARK Alliance announcement to French forum
- [x] John Kunze will inquire about PASIG deadlines
- [x] All: please think about topics for the ARKA newsletter
- [x] John Kunze Roxana Maurer come up with phrasing to clarify "high quality" vs "persistent" access (access not objects) as "central duty" of ARKs
- [x] John Kunze Greg Janée  clarify that multiple suffix normalization is for comparing arks rather than publishing them; see all comments in agenda notes
- [x] 

John Kunze review where Outreach got with wikipedia page