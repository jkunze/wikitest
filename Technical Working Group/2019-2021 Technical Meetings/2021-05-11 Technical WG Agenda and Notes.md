\---

confluence-id: 208341074

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-05-11 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Sep 14, 2021

Date
----

11 May 2021

Attendees
---------

*   John Kunze
    
*   Amir Alwash 
    
*   Curtis Mirci 
*   Karen Hanson 
*   Greg Janée 
*   Dave Vieglais 
*   Tom Creighton 

Goals
-----

*   ARK spec suffixes and signposting

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | upcoming meetings, calls for papers, submission deadlines |     | iPRES 2021 paper/poster submissions has been extended to May 31. iPRES will be a hybrid conference for both attendees and presenters.  [http://ipres2021.ac.cn/dct/page/1](http://ipres2021.ac.cn/dct/page/1) |
|     | **Suffix normalization**. Currently, the spec says the final normalization rule is:<br><br>_R: If there are any components with a period on the left and a slash on the right, either the component and the preceding period must be moved to the end of the Name part or the ARK must be thrown out as malformed._<br><br>I think we all know why, but I’d like to confirm our collective understanding. For example, let’s say that this thing<br><br>ark:12345/b6cd7/8fg.pdf<br><br>contains something called “km”. What is the contained thing’s ARK? It is tempting but improper to say<br><br>(1) ark:12345/b6cd7/8fg.pdf/km<br><br>but rule R says this should be rewritten (forgiving the tempted end user who is guessing that this might lead to a contained thing) or rejected (forgiving the end resolver for having a simple parser). If rewritten, the result would be<br><br>(2) ark:12345/b6cd7/8fg/km.pdf<br><br>The rule was put in to simplify ARK parsing (all suffixes come at the end, all containment comes before all suffixes) and to eliminate confusing questions, such as<br><br>_Does this imply that “pdf/km” is a suffix?_<br><br>_If form (2) suggests a pdf format, what format does “.pdf/km” suggest?_ |     | TC: the reserved nature of the period '.' has always seemed problematic; rejecting seems better than rewriting<br><br>KH: rewriting my have unintended consequences<br><br>GJ: I would never rewrite someone's id; there's no way to determine the correctness of someone's id; maybe we should encourage the / and . to denote containment and/or variants w.o. requiring it<br><br>JK: what if it's the end user who rewrote-by-guessing the provider ARK but got it wrong<br><br>DV: should play well with URL  <br>CM: this seems confusing  <br>All: agree with rejecting instead of rewriting<br><br>ACTION: drop the rewriting option for this normalization step<br><br>TC: could be done via "did you mean..." with a 404 page |
|     | **Signposting revisited.** This was first broached in 2020-03-16 meeting, discussed in [2020-12-21 Technical WG Agenda and Notes](2020-12-21-Technical-WG-Agenda-and-Notes_199525289.html), and recently as an [N2T github issue](https://github.com/jkunze/n2t-eggnog/issues/3).<br><br>Currently, the ARK spec is silent on conveying URLs/ids for related information. Should it instead make a recommendation?<br><br>As has been pointed out, there are “signposting” conventions for this using HTTP response headers. So, with a returned resource, the end resolver could return “here are some links to various kinds of metadata about this resource”. Example:<br><br>Link: rel="describedby" type="application/ld+json";<br><br>Conversely, with returned metadata the resolver could return “here are some links to various forms of the thing that this metadata describes”.<br><br>Btw, how do people feel about using [“cite-as”](https://datatracker.ietf.org/doc/html/rfc8574)?<br><br>*   propose adding it to example session in ARK spec, but leaving real spec to post-RFC tech work |     | TC: this is a great idea; should we recommend RFC8288 controlled vocabulary?<br><br>GJ: this isn't purely in scope for the ARK spec<br><br>DV: yes, but signposting could be added as an implementation guideline<br><br>All: agreed |
|     | Post-RFC tech work – where?<br><br>*   github? lyrasis wiki? arks.org? |     | JK: git for collaborative dev?  <br>DV: a couple example sites we might follow: the simple approach used by ESIP science [https://github.com/ESIPFed/science-on-schema.org/](https://github.com/ESIPFed/science-on-schema.org/)  <br>DV: at other extreme (of learning curve and bells and whistles), there's [https://jupyterbook.org/intro.html](https://jupyterbook.org/intro.html)  <br>TC: I'm ok with github or jupyter  <br>All: github looks promising; will discuss options further |

Action items
------------

- [x] John Kunze drop the rewriting option for this normalization step in the ARK spec