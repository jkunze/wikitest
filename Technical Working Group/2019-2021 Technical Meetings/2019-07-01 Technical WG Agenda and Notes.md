\---

confluence-id: 125731272

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-07-01 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Jul 05, 2019

Date
----

28 Jun 2019

Attendees
---------

*   John Kunze
    
*   Curtis Mirci
    
*   Greg Janée
*   Bertrand Caron

Goals
-----

*   Spec 22 revisions. Here's a link to the [differences from our baseline draft](https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-18.txt&url2=draft-kunze-ark-22.txt) (18). The main focus of this draft is turning the normalization description into a list of numbered steps on page 17. Please have a look at this before the meeting. 

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     | new map embedded in the FAQ |
|     | 1.  Tom will provide example of their post-encoding (64bit integer in base31 encoding – eg take out 0 vs O)<br>2.  Greg will review text on normalization to make sure his concerns are met<br>3.  All should review their position on externalizing persistence statements<br>4.  Tom will review 5.1.2 more carefully to see if he has issues<br>5.  All should review  section 2.2  Label (language on old and new form language ark:  ark:/)<br>6.  All should please make comments on spec to the list<br><br>  <br>I also made a few very small changes (removing an email address, pointing the NAAN registry at a non-CDL URL). The whole spec needs a thorough review, eg, I'm we might want to drop all of section 4 (but that's a discussion for later). |     | 1.  n/a<br>2.  done – approved<br>    1.  typo: extra comma – fixed<br>    2.  typo: incorrect ref to Appendix A – fixed<br>3.  agreed not to try standardizing on persistence, but simplify section on call it non-normative – Greg and Curtis agreed to review<br>4.  n/a<br>5.  done – approved<br><br>This completes review of all major spec changes discussed at the ARK Summit Experts Day in 2018. All changes approved.<br><br>Pending additional changes to discuss:<br><br>*   strawman proposal: the '?' inflection be made identical to the '??'<br>    *   why? because the latter is much easier to recognize and implement by resolvers, eg, with tomcat and libraries that don't distinguish between a single '?' and an empty query string |

Action items
------------

- [ ] John Kunze Go over survey result data.
- [ ] John Kunze Correct reference to appendix A on page 22.
- [ ] John Kunze Greg Janée  Curtis Mirci Look over the 5.1.1 Generic Policy Service section.
- [ ] Bertrand Caron Write about plans to implement changes for resolver services.
- [ ] @All Look over draft 23 [https://tools.ietf.org/html/draft-kunze-ark-23](https://tools.ietf.org/html/draft-kunze-ark-23), specifically section 4.