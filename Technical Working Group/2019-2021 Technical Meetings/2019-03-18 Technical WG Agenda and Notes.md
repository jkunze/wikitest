\---

confluence-id: 112526247

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-03-18 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Mar 28, 2019

Date
----

15 Mar 2019

Attendees
---------

*   John Kunze
    
*   Bertrand Caron 
    
*   Tom Creighton
    
*   Greg Janée
*   Curtis Mirci
*   Sheila Morrissey
*   Mark Phillips

Goals
-----

*   Review objectives and and establish priorities, workplan, subgroups (if any), etc.

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
| 5m  | Review WG objectives:<br><br>1.  Standardization. Review the ARK specification so that the authors, who are WG members, can finalize it and submit it to the IETF for publication as an Internet RFC.<br>2.  NAAN procedures. Adapt current CDL procedures for updating NAANs and registering new NAANs so that these maintenance activities can be shared by the community, eg, on github. ([The NAAN registry that CDL currently maintains](http://www.cdlib.org/services/uc3/naan_registry.txt) is a text file of globally unique 5-digit Name Assigning Authority Numbers (NAANs) reserved for organizations that wish to assign ARKs.)<br>    <br>3.  Counting ARKs. Work with the [Outreach Working Group](https://wiki.duraspace.org/display/ARKs/Outreach+Working+Group) to implement mechanisms to measure ARK usage world-wide. | JK  | Announcement; the NAAN registry moved from www.cdlib.org to n2t.net this week, with redirects in place to keep the old links stable. |
| 15m | Review relevant [Experts Day meeting results](112525432.html) | JK  |     |
| 5m  | Review of new [RuffGUIDe](https://docs.google.com/document/d/19OQVFVKey4waSc6UjF0jHI9GPl59q9c18eKO_LGWvKo/edit?usp=sharing) counting method | JK  |     |
| 25m | Discussion: priorities, who is available to work, possibility of subgroups, recruitment of new members, ... | All | 1.  STANDARDIZATION.  <br>    John Kunze will be taking lead on shepherding draft thru IETF;<br>    <br>    How we will proceed on draft -- apply changes in notes, plus any other issues from Curtis and Tom; this group will review draft (perhaps GitHub for diff’ing versions); once WG is satisfied, we can publish new Internet Draft (we can continue to publish new drafts as we receive comments from community and resolve and questions raised)<br>    <br>    Bertrand:  do we anticipate more changes?  John: we don’t anticipate many; also there is an advantage in making relatively few changes<br>    <br>    B: some have expressed concern about compatibility with URI spec; should we be tackling this issue?<br>    <br>    J:  there have been emails to AITO group on some of these issues; J will review; suggests caution wrt URI spec compatibility, which could get bogged down; J advocates incremental approach to avoid getting stuck on one subtask at the expense of others; we should consider statement articulating position RE: URI vs. browser compatibility<br>    <br>    Tom concerned, especially with reverse proxies; conforming to browser behaviour rather than specs a problem for them<br>    <br>    B suggests focusing first on draft spec before we start on other 2 deliverables; group agrees this is to be the priority<br>    <br><br>2\. NAAN Procedures.<br><br>John has shared documentation with Bertrand  <br>Current process: Google form which generates email, spreadsheet entry sent to CDL; script to enter contents of request; light review to make sure not spurious request or spam; entry added to registry; publishes; mirrored at BNF, NLM; gets combined with N2T resolver to set up redirection rules<br><br>Bertrand: often when institution requests NAAN, don’t have a resolver; no current mechanism to update entry when resolver available; needed<br><br>Example from Mark:  <br>For those that haven’t seen it working (if there are those on this call). This ARK [ark:/67531/metadc1453742](http://ark/67531/metadc1453742)  <br>when appended to n2t [http://n2t.net/ark:/67531/metadc1453742](http://n2t.net/ark:/67531/metadc1453742)<br><br>3\. COUNTING ARKS.<br><br>Will have some dependencies on NAAN work<br><br>Tom: we have over 3 billion ARKs; to cut down on mis-use, you need an account (but it's free) |
| 10m | Per-objective Leaders? Are objectives pursued in parallel or in sequence? | All | Consensus of group is that first focus should be on finalizing specification and getting it published and through IETF procedures |

Action items
------------

- [ ] Curtis and Tom will review the Notes from ARK "Experts" meetings in 2018 over the next 2 weeks
- [ ] Bertrand will post link to discussions about URI compatibility and other issues that came out of discussion of proposed specification changes and AITO initiative
- [ ] all will review proposed changes from ARKs Experts day;  we will proceed by clearing the deck of “small” problems; then focus on the knottier ones (EG URI vs. browser compatibility)
- [ ] 

everyone in the WG will confirm that the N2T resolver works for their entry in the [NAAN registry](https://n2t.net/e/pub/naan_registry.txt)

- [ ] John will start to document current NAAN procedures