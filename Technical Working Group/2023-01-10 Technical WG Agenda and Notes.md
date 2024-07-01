\---

confluence-id: 273350832

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-01-10 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Feb 11, 2023

Date
----

10 Jan 2023

Attendees
---------

*   Curtis Mirci, Karen Hanson, Dave Vieglais, Donny Winston

Goals
-----

Follow up on test resolution, review charter and deliverables for coming year

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     |     |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     | dw: [https://www.knowledgegraph.tech/](https://www.knowledgegraph.tech/) call for papers due Jan 15th, call for workshops/masterclasses due Jan 30th<br><br>jk: Dave, Tim Clark, and I are recording a 20-min briefing for CNI, due out in February; Donny and I presenting 3-hour training at code4lib conference in Princeton in March  <br>kh: I may join you at c4lib since it's so close to me  <br>jk: for the CNI recording, does anyone have recording advice?  <br>dw: this is the "mutual local recording" alternative to Zoom: [https://riverside.fm/](https://riverside.fm/) |
| Any news items we should blog about? |     |     |
| Bug fix at N2T, possible enhancement to "quick" test ARK resolution, per _the documentation_ at [ARK Shoulders FAQ](ARK-Shoulders-FAQ_187180621.html) below. It appears that N2T may not be following the documentation. See [email thread](https://groups.google.com/g/arka-technical-wg/c/H_VYqofrong/m/ba-BqDmHCwAJ?utm_medium=email&utm_source=footer) ending Jan 4.<br><br>### _Is there a quick way to get started creating test ARKs?_<br><br>_Yes. Instead of reserving a 99999 shoulder, if your organization already has its own NAAN, you can immediately create and use a "quick test ARK". This is an ARK that starts with [ark:/99999/9NNNNN\_](http://ark/99999/9NNNNN_), where NNNNN represents the NAAN (preceded by '9' and followed by '\_'). There is no need to register a quick test namespace since it is automatically set aside for each NAAN. As with any prefix, there is an infinite number of possible test ARKs in each NAAN's quick test namespace. Two versions of an example quick test ARK belonging to the BnF (NAAN 12148) are_<br><br>_`https://ark.bnf.fr/ark:/99999/912148_testxyz`_<br><br>   _`https://n2t.net/ark:/99999/912148_testxyz`_<br><br>_Note that [N2T.net](http://N2T.net) is configured to forward any quick test ARK it receives (second version above) to the appropriate local resolver (first version)._<br><br>**That last sentence isn't quite true, as N2T actually forwards the second to:**<br><br>   https://n2t.net/ark:/12148/99999/912148\_testxyz<br><br>which redirects to<br><br>   [http://ark.bnf.fr/ark:/12148/99999/912148\_testxyz](http://ark.bnf.fr/ark:/12148/99999/912148_testxyz) <br><br>That should then allow the local resolver (in this case [bnf.fr](http://bnf.fr/)) to handle the test ARK, as per the [current documentation](https://wiki.lyrasis.org/display/ARKs/ARK+Shoulders+FAQ).<br><br>OTOH, a future enhancement of N2T might conceivably improve this, so that the first redirect went directly to<br><br>   [http://ark.bnf.fr/ark:/99999/912148\_testxyz](http://ark.bnf.fr/ark:/99999/912148_testxyz)<br><br>That way, the local resolver sees the NAAN of 99999 and can treat it as a test NAAN (consistent with how all resolvers should treat a NAAN of 99999). At the moment, a kludge is required to treat the ARK as some special case "object"-as-test-NAAN, where the object is called "99999" within the 12148 NAAN namespace. Not a great design (mea culpa), even if it works for now with a local resolver that can add this code in order to publish "functional" test ARKs. | Bertrand Caron | jk: the behavior of N2T doesn't match the documentation in the Shoulders FAQ for the "quick" test ARK resolution; there's an issue with how N2T forwards these test ARKs because they lose their identity as test ARKs when they arrive at the remote resolver, requiring a non-standard response from the remote resolver (otoh, it's a small use case and an easy hack)  <br>jk: ACTION I'll change the lyrasis documentation with Bertrand and add an issue to GH  <br>dv: ACTION I'll talk to CDL about the test resolution; please reference this issue on GH: [https://github.com/CDLUC3/n2t-admin/issues/4](https://github.com/CDLUC3/n2t-admin/issues/4) |
| working group [home page](https://wiki.lyrasis.org/display/ARKs/Technical+Working+Group) and sidebar cleanup<br><br>*   compress sidebar list of 3 years of meetings <br>*   revisit objectives, deliverables via [this googledoc](https://docs.google.com/document/d/1n5ETS45fHqJefu74vXKLFZhrXm_VmIB7jT2Yk4zR2_E/edit?usp=sharing) |     | all: yes to compressing meetings<br><br>jk: the googledoc proposes some new deliverables (although it may use help from other working groups) that consolidate the arks.org WP site and the Confluence wiki (lyrasis)  <br>dv: converting from WP to GH pages can be very labor intensive and may involve losing some look and feel; converting the Lyrasis confluence wiki may be easier as it looks like there are tools to assist that migration<br><br>j: ACTION everyone please add comments to gdoc WG charter by Jan 24 |
| In the coming weeks, if ARKA were to establish a Mastodon presence, is fosstodon.org a suitable server to start with? See [email of Jan 10](https://groups.google.com/g/arka-technical-wg/c/_KCf0jd7cr4). |     | dw: it would be great for ARKA to have a mastodon presence; besides fosstodon.org, other possible servers include digipres.club I co-run an instance); I think fosstodon is fine  <br>cm: in a search just now, I found a complaint that fosstodon deleted an account  <br>kh: it looks like they were doing product promotion  <br>jk: so maybe fosstodon was simply enforcing their own policy  <br>kh: ... which seems find for ARKA  <br>dw: it is possible to move between servers, so whatever we choose we're not committed for all time  <br>jk: I think you have to wait a month before moving again?  <br>dw: another relevant serve is [glammr.us](http://glammr.us)  <br>jk: also maybe the Internet Archive would host ARKA on their mastodon server  <br>jk: ACTION: please provide feedback by Jan 24<br><br>dw: I'm interested in helping out with [arks.org](http://arks.org) migration, enhancing [arks.org](http://arks.org) functionality, and helping out with Persistence Statements  <br>dw: would like to understand and help N2T remain authoritative and secure wrt individual NMA redirects  <br>dv: it would be good to have your input on that as the new N2T resolver is built |

Action items
------------

- [x] Donny Winston add to [Calendar of events](Calendar-of-events_208341505.html) : [https://www.knowledgegraph.tech/](https://www.knowledgegraph.tech/) call for papers due Jan 15th, call for workshops/masterclasses due Jan 30th
- [ ] John Kunze work with Bertrand Caron to correct documentation and to add test resolution issue to [https://github.com/CDLUC3/n2t-admin/issues/4](https://github.com/CDLUC3/n2t-admin/issues/4)
- [ ] Dave Vieglais talk to CDL about the test resolution issue, possibly low-enough priority to be able to wait for the new resolver
- [x] ALL: by January 24 please provide feedback on reviewing [our WG charter](http://this googledoc)
- [x] ALL: by January 24 please provide feedback on whether fosstodon.org is an acceptable starter server for ARKA