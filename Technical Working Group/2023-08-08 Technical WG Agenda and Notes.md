\---

confluence-id: 298811506

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-08-08 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Aug 21, 2023

Date
----

08 Aug 2023

Attendees
---------

*   Lautaro Matas, Tom Creighton, Karen Hanson, Dave Vieglais, Curtic Mirci

Goals
-----

Inline content, ARK spec transition next step

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements<br><br>New working group member: Lautaro Matas |     | lm: i work with LA Referencia and open access repositories; interested in ARKs because cost of DOIs is prohibitive; working on an ARK implementation with blockchain tech, provided by a network of services; I'm living in Spain |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     |     |
| Experimental new shared (available to anyone) NAAN<br><br>92250 - inline (self-contained, in-link) concepts<br><br>To try:<br><br>1.  [https://n2t.net/ark:/92250/sea\_ice](https://n2t.net/ark:/92250/sea_ice)<br>2.  [https://n2t.net/ark:/92250/sea\_ice?info](https://n2t.net/ark:/92250/sea_ice?info)<br><br>(from discussion at [last meeting](https://wiki.lyrasis.org/display/ARKs/2023-07-11+Technical+WG+Agenda+and+Notes))<br><br>Some questions from Greg J.<br><br>> 1\. Is the intention that N2T would treat this NAAN specially, and not resolve such ARKs to any target?  That is, the example ARK resolving to [biscicol.org](http://biscicol.org/) (as it does now) is just a way to demonstrate what N2T would do by itself?<br><br>Yes, the proposer (John Deck) is using [biscicol.org](http://biscicol.org/) simply as a place to test the feasibility and plausibility. Not counting the documentation template in the code, it only takes about 12 lines of javascript to support, so it would be easy to support natively in N2T.<br><br>> 2\. In minting 92250 ARKs, would N2T ignore a target URL and any other supplied metadata bindings?<br><br>There's no such thing as "minting" in this case. These ARKs come into existence only by dreaming them up and writing them down. Although technically possible (assuming an AuthN model existed for these anonymous ARKs) there are no plans for N2T or any other resolver to ever store metadata for them.<br><br>> 3\. Would it be more logical for N2T to return HTTP 204 No Content since there is indeed no content associated with such ARKs?<br><br>That's an interesting idea. It would be nice to have another distinguished "signal" for this case (the NAAN 92250 is one such signal), but to use "204 No Content" may be misleading. There actually is content (which could amount to the equivalent of several paragraphs of text, whatever fits in a modern URL-embedded ARK), but it's carried in the link itself. <br><br>Other questions:<br><br>1.  Are we encouraging people to use this? No, but if you must use this (eg, because its so cheap), it is provides a safer, clearer way than non-resolving URIs. Compare with w3id, purl, yamz.<br>2.  What's the best response format for simple resolution? Currently using YAML, but maybe JSON is better?<br>3.  What's the best response format for ?info inflection? Currently using YAML, but maybe JSON is better? |     | dv: should not be part of the ARK spec, but provided by a particular NAAN  <br>jk: agree generally about keeping it out of the ARK spec  <br>tc: IANA has reserved [example.com](http://example.com) and [example.org](http://example.org) for similar purposes  <br>dv: this is defined in [https://datatracker.ietf.org/doc/html/rfc2606](https://datatracker.ietf.org/doc/html/rfc2606) ; I don't mind a section of [arks.org](http://arks.org) that advertises this, just prefer it not \_in the spec\_  <br>dv: it would be good to start gathering metrics on it's use, to see how wide-spread adoption might be and could be used for interesting studies; metrics could use some GDPR-like warnings  <br>all: json better than yaml |
| ARK spec transition – proposed next step: create meeting series with key stakeholders.<br><br>*   This might be a recurring/ standing agenda item on each Tech WG monthly meeting until the transition is finished<br>*   Key stakeholders are people (possibly new to ARKA) representing large or high profile ARK implementers, such as<br>    *   FamilySearch <br>    *   BnF (Thomas Ledoux?)<br>    *   Smithsonian<br>    *   EZID<br>    *   Internet Archive<br>    *   what about HathiTrust (not on ARKA, but impacted by transition)?<br>    *   others?<br>    *   should we put out a general Call for Participation to the community?<br>*   Confirm feasibility of steps<br>*   Publish steps regularly via blog and social media – how much publicity is enough? Where to publish? |     | tc: yes, ok to ask other people to step forward for transition  <br>dv: one really useful thing would be an indication as to whether the target can support the no-slash form, maybe whether hyphens should be removed before  <br>tc: could use .well-known for this  <br>dv: that and introspection on a periodic basis  <br>kh: Portico will be able to handle this transition; this is the only public view of our ARKs... in the URL and on the record display: [https://access.portico.org/Portico/auView?auId=ark:%2F27927%2Fpgj2js3rtrd](https://access.portico.org/Portico/auView?auId=ark:%2F27927%2Fpgj2js3rtrd)  <br>cm: should be ok with us as well  <br>lm: I think that json es better, more realiable than yaml, in my opinion, because the indenting issues  <br>all: ok to set aside standing agenda item within ARKA tech for transition plan and implementation<br><br>zoom chat  <br>\-----  <br>dv: @Lautaro Matas - I’m very interested in any info you can share on the dARK implementation approach, particularly for ensuring trustworthy resolution. Do you have a link to more info?  <br>lm: @dave we are preparing a documentation site for the end of the year, since we are discussing the resolution and other technical aspects; I will be happy to share and discuss al those aspects with this group or in individual meetings. We have so much to learn from you guys |

Action items
------------

- [ ] John Kunze add standing agenda item to discuss spec transition
- [ ] John Kunze start reaching out to stakeholders as transition partners