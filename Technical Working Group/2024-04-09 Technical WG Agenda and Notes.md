\---

confluence-id: 328958169

confluence-space: %%CONFLUENCE-SPACE%%

\---

2024-04-09 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Apr 11, 2024

Date
----

09 Apr 2024

Attendees
---------

*   Dave Vieglais, Donny Winston, Tom Creighton, Curtis Mirci, Greg Janee

Goals
-----

Resolver and static site changes

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | dw: will be moving to Copenhagen to start up new company that will support ARKs and other infrastructure  <br>tc: ACTION: will try to coax a Familysearch rep to join this group |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     | dw: didn't make the USRSE deadline and won't be attending PIDFest; should we try for the Force11 conference? |
| N2T resolver status (current target upgrade date April 10) |     | dv: resolver upgrade planned for 8am PT; mostly just domain name change and certificate swapping, so rollback (if needed) will be easy  <br>tc: what technical changes will there be to n2t?  <br>dv: some not widely advertized internal stuff; n2t api changes, and the ?info inflection will return JSON<br><br>dw: ark requests with inflections get passed to [arks.org](http://arks.org) though, right? What inflections will [n2t.net](http://n2t.net) handle natively?  <br>dv: all handled by end resolver<br><br>dv: new n2t code will be available on GH  <br>dv: new public naan registry will work on a JSON version, but for now the  <br>    naan\_registry.txt file will remain<br><br>dw: what license? we should tell people up front  <br>dv: action: will look into open source licensing; probably MIT |
| NAAN request processing status |     | dv: expect upgrade in early summer for naan processing changes |
| static site pages, and working group pages |     |     |
| ARK spec (v38) to be renewed before May 9<br><br>*   opportunity to change recommendation of [V18 spec](https://datatracker.ietf.org/doc/draft-kunze-ark/18/) to [v39 spec](https://datatracker.ietf.org/doc/draft-kunze-ark/)? |     | dv: an alternative is to make : or :/ a config option<br><br>jk: would like to route to a newer spec  <br>dw, dv: yes, newer is better  <br>dw: in fact I've assumed newer is better and implemented it  <br>jk: so did BnL<br><br>dw: The issue of “what should [arks.org](http://arks.org) do for convenience?” (via naan config)  <br>    and “what resource should we direct implementers to?” seem separate. I am  <br>    in favor of linking to v39 as the “current draft recommendation”.<br><br>    The ARK recommendation should be to mint without, to respect what you're  <br>    given, and in perpetuity to use<br><br>dw: will be doing a complete ARK implementation soon and will return with feedback |

Action items
------------