\---

confluence-id: 199525289

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-12-21 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Dec 21, 2020

Date
----

21 Dec 2020

Attendees
---------

*   John Kunze
    
*   Mark Phillips
*   Roxana Maurer
*   Greg Janée
*   Curtis Mirci

Goals
-----

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | upcoming meetings, calls for papers, submission deadlines |     | PIDapalooza; IDCC; RDA; iPres |
|     | new draft published (old one expires 12/23)<br><br>proposed: link most up-to-date draft from arks.org |     |     |
|     | *   signposting.org (Dec 4 email from Greg)<br><br>"Relevant to the discussion of returning metadata associated with digital resources.  The recommendation here is to use HTTP headers." |     | GJ: just and fyi; it's actually from 2017; the idea is that resources can link to each other, to a landing page, and to metadata; all done through link headers, returnable with a HEAD request; it's complimentary to the data citation practices (Fenner et al), which embeds metadata in the HTTP payload vs the HTTP headers  <br>RM: I found this stuff very interesting because you can get metadata _along_ with a returned object (immersive experience), but it's still on my "to do" list  <br>MP: curl -I [https://digital.library.unt.edu/ark:/67531/metadc12345/](https://digital.library.unt.edu/ark:/67531/metadc12345/) and they have a number of different examples at [https://signposting.org/identifier/](https://signposting.org/identifier/)   <br>MP: at a minimum, a link header could give a hint that "there's more metadata to request, eg, with an inflection" (as opposed to there's not more, which could avoid frustration) |
|     | proposed: minimalist strategy regarding definition of the ark?info inflection<br><br>Pros:<br><br>*   minimize distance between current draft and envisioned RFC<br>*   leaves door open to finish details in a (in this?) working group<br>*   time already spent on future data modeling will serve to inform and increase confidence in outcome<br><br>Thank you again for bearing with me this year during the exposition of several model sketches, which were my way of thinking out loud about a fairly comprehensive  and ambitious approach to generic data objects and metadata. These modeling exercises have given me confidence in the general direction even though I doubt that any of them have been particularly comprehensible to all of you, let alone persuasive. <br><br>I’m at a familiar milestone in the process where my inclination is to shift away and ignore, without effacing, the long term goals – effectively  just “greying them out”. Instead, with your help I’d like to look down at our feet and consider what concrete baby steps we can take now. What’s the minimum we can add to the ARK spec to achieve the RFC without precluding the long term goals or disrupting current implementations? The baby steps for the “arkinfo model” should be very achievable and move us in a good direction, even if they leave us far from the ambitious goals. <br><br>A first requirement, since the RFC freezes the spec, is<br><br>**R1**. The RFC links to a place where community-based “arkinfo” evolution occurs.<br><br>A second requirement is to explicitly mention the diversity in scope of ARK application.<br><br>**R2**. ARKs are assigned to many different things, for example,<br><br>1.  to a single data file (eg, my.csv),<br>2.  to a single document that _encapsulates_ multiple _variants_ (versions, formats, languages, etc.), which may or may not have their own ARKs,<br>3.  to a hierarchical document such as a book _partitioned_ into _parts_: chapters, sections, paragraphs, etc., which may or may not have their own ARKs,<br>4.  to a _guide_ (landing) page that describes a thing and links to multiple variants and parts,<br>5.  to an object with no metadata,<br>6.  to a vocabulary term (no “object”, just metadata),<br>7.  to an object accompanied by _adjunct_ files, such as provenance, license, change history, etc.,<br>8.  to a physical object with metadata and associated digital surrogates, and<br>9.  to a set (partition) of any of the above objects, which may or may not have their own ARKs.<br><br>Dealing with the landing page (_guide_ attribute) vs “plunging” (immersive, non-landing) page issue is vital to being able to link to metadata no matter what the ARK points to. Let’s define an _arkinfo response_ to be a package of named data elements (whether in JSON, YAML, XML, ANVL, etc) returned when an ARK  is submitted with the “?info” inflection. If the ARK were _K_, then the inflected ARK would be “_K_?info”, which is an _arkinfo request_. As a shorthand, if we don’t say which ARK it was, we can assume the canonical name of “K”.<br><br>**R3**. If K is an _encapsulation_ variant with immediate encapsulation ancestor R, the arkinfo response for K should describe its encapsulation siblings. Example: K is the English language, PDF format of chapter 3 section 2, and the siblings of chapter 3 section 2 also include variants in French and Spanish, and in RTF and HTML formats.<br><br>**R4**. If K is contained as a part with an immediate _partition_ ancestor R, the arkinfo response for K should describe its partition siblings. Example: K is the English language, PDF format of chapter 3 section 2, and the partition siblings also include sections 1, 3, and 4 of chapter 3.<br><br>**R5**. An arkinfo response may include arbitrary metadata.<br><br>**R6**. An arkinfo request can be modified to request alternate formats, eg, JSON, YAML, XML, etc. <br><br>Similar to the traditional ARK spec, perhaps the safest immediate way forward may be to continue to be non-committal and define these baby steps by example rather than by prescription. |     | MP: like decoupling and keeping the RFC simple, doing the evolution externally; have found the non-prescriptive approach to be helpful; getting everything right will take time; the RFC is a kind of parent document that could reference the community spec (that could become other RFCs)<br><br>GJ: to pursue RFC for ARK, what if we simply said that "ark?info" was reserved for future use  <br>JK: very appealing because super minimalist; could just link to community  <br>MP: like the super minimalist approach  <br>RM: agree with Greg's suggestion; still prefer baby steps in community  <br>CM: my only concern is how the user will know what the metadata will look like  <br>RM: don't think divergence is a big concern because not many institutions have done this yet |

Action items
------------