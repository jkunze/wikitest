\---

confluence-id: 289079442

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-05-09 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on May 16, 2023

Date
----

09 May 2023

Attendees
---------

*   Donny Winston, Karen Hanson, Tom Creighton, John Kunze

Goals
-----

Spec and standard progress

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | Anyone know of a good image generator, eg, for ARKA graphics?  <br>dw: maybe "stable diffusion" or "dall-e" |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html).<br><br>*   Please review [PIDwijzer post](https://docs.google.com/document/d/161p4IxDlC_msVaWBxhtDqVdYO_OmubEnTW1-Mubw6QY/edit)<br>*   Anyone traveling to the upcoming meetings where ARK tutorial has been submitted? |     | kh: i'll be at ipres |
| Standardization update<br><br>*   no conflict with URN namespace registration<br>*   no conflict with URI scheme registration (leave alone?)<br>*   no conflict with [https://github.com/perma-id/w3id.org/tree/master/ARK](https://github.com/perma-id/w3id.org/tree/master/ARK)<br>*   for RFC, use of /.well-known will be required<br>    *   heavy (each ARK) or<br>    *   light (examples: resolver config, which seems typical (RFC6690 CoRE, RFC6415 host metadata, RFC8414 OAuth metadata, Keybase, W3C DID config, W3C Tabular data for web), <br>*   register under W3C DID (Decentralized ID)? |     | all: no objection to URN namespace registration  <br>tc: the heavy use of .well-known seems unnecessary given the precedent, eg, how everyone uses it for OAuth config  <br>jk: I think we need to understand whether we would have to support resolution of every ARK from /.well-known/ark:... It might work if each resolver could continue to support ARKs from its own chosen URL path prefixall: the lightweight use of /.well-known is ok  <br>dw: i like the idea of using .well-known to opt into ARKs  <br>tc: yes, ok to move in this direction  <br>kh: yes, this is good and straightforward  <br>jk: does anyone have time to pursue W3 DID registration?  <br>dw: I brought it up, but don't really have time |
| Draft spec [transition plan](https://docs.google.com/document/d/1aFgujlL5yE3ZUORXRRkDTDNrlZEQU69lOU6Gc3wlyt4/edit#heading=h.1wnsqimx3u90)<br><br>*   Can we come up with strawperson times T0, T1, T2, ...? |     | tc: accepting noslash ARKs needs to come before producing them  <br>tc: I recommend we get the task list (a) complete and (b) dependency-ordered before trying to assign times  <br>tc: ACTION I will review with this in mind  <br>kh: recommend we prioritize clearing the plan with the major ARK producers |

Action items
------------

- [ ] Tom Creighton will review the transition plan with an eye toward completeness and dependency ordering