\---

confluence-id: 335544324

confluence-space: %%CONFLUENCE-SPACE%%

\---

2024-05-14 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on May 15, 2024

Date
----

14 May 2024

Attendees
---------

*   Karen Hanson, Dave Vieglais, Roxana Maurer, Greg Janée, John Kunze

Goals
-----

Infrastructure updates, first use of .well-known convention

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | will shortly announce a pan ARKA group list (union of working groups) |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     |     |
| N2T resolver status |     | dv: put last month's transition on hold because of discrepancies that turned out to be shoulder info presented by N2T; then there was another issue with NAANs in use that weren't documented,<br><br>     eg, [ark:/b5060/d8kw2m](http://ark/b5060/d8kw2m)<br><br>jk: oh yes, that looks like a "shadow ARK" from EZID that wasn't ever supposed to make it out into the wild; we asked people to stop using them, but it looks like that only partly worked  <br>dv: config details remain to be finalized, and all the rest is working fine |
| status of new process for updating documents on static website (arks.org) |     | dv: we're in the process of deconvoluting the procedures, so that pushing change to main that have a release tag will trigger an update to the public site; it should be close to done  <br>gg: who has access and what are the policies and procedures for updating?  <br>dv: we could borrow from the carpentries content guidelines handbook/best practices  <br>[https://docs.carpentries.org/topic\_folders/maintainers/maintainers.html](https://docs.carpentries.org/topic_folders/maintainers/maintainers.html)<br><br>ACTION: gg and jk will work on policies and procedures for updating the static site |
| a first stab at /.well-known/ark\* convention(s); goals<br><br>1.  to start conversation with the IETF RFC editor<br>2.  to tell agents (including humans) things like<br>    1.  do expect to find an ARK service here<br>    2.  what path to find that ARK service<br>    3.  alternate way to get metadata (if ?info is problematic)<br>    4.  ?where to find numbers of ARKs served here<br>    5.  ?site verification/ownership<br><br>Example (strawperson) .well-known/ark.json:<br><br>{  <br>    "service": {  <br>        "path":       "index.php/didascalia/gateway/plugin/pubIdResolver/",  <br>        "metadata":      "index.php/didascalia/gateway/plugin/pubIdMetadata/",  <br>        "counts":    "index.php/didascalia/gateway/plugin/counts",  <br>        "mastodon\_verification":    "953088D7-0726-400C-81DC-945BE8B1115B"    }  <br>} |     | g: is there a risk that no one else will be able to use our .well-known conventions without prior knowledge?  <br>dv: it can be very simple, can start by just listing the location of a known ark service  <br>kh: can this be that simple and satisfy the IETF requirements?  <br>jk: I propose starting very simple and testing the waters  <br>dv: willing to do be on a call with the RFC editor, suggest following openid config naming pattern and calling it "ark" or "arks" without a filename suffix (eg, not ark.json) |
| Leftover topics |     | jk: published very minor revisions to create the v39 spec; ok to point new implementers to it?  <br>all: agreed<br><br>jk: expect a request for a first new shared NAAN shoulder on the 99999/... from a group in Chechia ; any problems expected?  <br>dv: should work <br><br>rm: I'd like to restart the discussion of persistence statements; has there been any progress?jk: it's been on hold, but I'd be very supportive of producing a minimum viable product (MVP); I will send you the names of people who expressed interest in working on this |

Action items
------------

- [ ] John Kunze and Greg Janée will work on policies and procedures for updating the static site; consider using [https://docs.carpentries.org/topic\_folders/maintainers/maintainers.html](https://docs.carpentries.org/topic_folders/maintainers/maintainers.html)

Zoom chat:

08:05:29 From Dave Vieglais to Everyone:  
    [ark:/b5060/d8kw2m](http://ark/b5060/d8kw2m)  
08:06:55 From John Kunze to Everyone:  
    [https://wiki.lyrasis.org/display/ARKs/2024-05-14+Technical+WG+Agenda+and+Notes](https://wiki.lyrasis.org/display/ARKs/2024-05-14+Technical+WG+Agenda+and+Notes)  
08:14:36 From Dave Vieglais to Everyone:  
    [ark:/b5060/d8kw2m](http://ark/b5060/d8kw2m)  
08:32:59 From Roxana Maurer (NLibLux) to Everyone:  
    [https://github.com/roxponinja](https://github.com/roxponinja)  
08:36:04 From Greg Janée to Everyone:  
    [https://docs.carpentries.org/topic\_folders/maintainers/maintainers.html](https://docs.carpentries.org/topic_folders/maintainers/maintainers.html)  
08:39:32 From Dave Vieglais to Everyone:  
    [https://en.wikipedia.org/wiki/Well-known\_URI](https://en.wikipedia.org/wiki/Well-known_URI)  
08:47:56 From Dave Vieglais to Everyone:  
    [https://help.akana.com/content/current/cm/api\_oauth/oauth\_discovery/m\_oauth\_getOpenIdConnectWellknownConfiguration.htm](https://help.akana.com/content/current/cm/api_oauth/oauth_discovery/m_oauth_getOpenIdConnectWellknownConfiguration.htm)