\---

confluence-id: 208342525

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-07-13 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Aug 10, 2021

Date
----

13 Jul 2021

Attendees
---------

*   John Kunze 
*   Roxana Maurer 
*   Greg Janée 
*   Karen Hanson 
*   Amir Alwash 
*   Tom Creighton 

Goals
-----

Review proposed specification changes

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| announcements |     |     |
| calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     |     |
| normalizing unicode hyphens<br><br>"Implementors should be prepared to normalize some common invalid characters that may be found in ARKs copy pasted from processed text. For example, when pasting an ARK that was broken during line wrapping, a user may inadvertently introduce newlines and spaces that should be removed, or a variety of dash-like (eg, en dash) Unicode characters that should be removed or converted to hyphens." |     | GJ: "should be prepared" maybe too vague; perhaps this should be "best practice" or "it is recommended..."ACTION: GJ will try to reword this  <br>TC: implementors normalize; is this more for resolvers, or is it a purely a client-side issue?  <br>JK: in some ways it's a publisher problem; but since we have little influence over them it may be best to play defensively  <br>RM: similar situation with malformed PDFs  <br>JK: and same with decades of malformed HTML  <br>GJ: in the spec "normalization" is only currently mentioned only in terms of lexical equivalence; is it ok to leave it that way? |
| more diagrams (2) with ARK part names<br><br>See [http://n2t.net/e/pub/ark.html#name-ark-anatomy-2](http://n2t.net/e/pub/ark.html#name-ark-anatomy-2) |     | GJ: having two diagrams that are so similar is confusing<br><br>TC: I'd agree; I hadn't seen the check digit language before  <br>JK: check digits are still optional but the convention is explained  <br>GJ: are we too constrained by ascii art? maybe it would be good to have an actual diagram  <br>JK: the IETF specs are generally meant to be renderable with plain text  <br>TC: we might want to do a BNF grammar at some point  <br>RM: the diagrams are too similar; the first should be higher level than the second; it seems possible to eliminate some detail from the first?  <br>KH: agreed; or perhaps have more than two diagrams |
| new terms:<br><br>*   first resolver<br>*   resource responder<br>*   metadata responder<br><br>See [http://n2t.net/e/pub/ark.html#name-resolver-chains-2](http://n2t.net/e/pub/ark.html#name-resolver-chains-2) |     | TC: who is the audience for the resolver chain discussion; would be good to have some use cases  <br>JK: example, EZID will go from using N2T as a Metadata Responder to being its own Metadata Responder  <br>JK: an important use case for N2T retaining the ability to be a Metadata Responder is for namespace splitting  <br>TC: yes, we have seen namespace splitting |
| recommend/exemplify link header with resource response? |     | n/a |
| recommend/exemplify link header with metadata response?<br><br>[https://n2t.net/e/pub/ark.html#name-overview-of-the-http-url-map](https://n2t.net/e/pub/ark.html#name-overview-of-the-http-url-map) |     | KH: I like the link header example  <br>TC: agreed; maybe use the full URL instead of relative URL  <br>TC: would expect the "self" reference  <br>JK: missing: converse recommendation of link header for resource retrieval |
| adding [n2t.net](http://n2t.net) as infrastructure; current statement is weak<br><br>[https://n2t.net/e/pub/ark.html#name-finding-a-name-mapping-autho](https://n2t.net/e/pub/ark.html#name-finding-a-name-mapping-autho) |     | JK: we could use a statement about [n2t.net](http://n2t.net) as infrastructure; volunteers? |
| non-normative pointer to ARK extensions at arks.org/specs/<br><br>[https://n2t.net/e/pub/ark.html#name-enhancements-and-related-spe](https://n2t.net/e/pub/ark.html#name-enhancements-and-related-spe) |     | RM: the arks.org/specs/ endpoint is ok  <br>KH: agreed  <br>TC: agreed  <br>TC: nice to be able to see what the latest, up-to-date recommendation is  <br>ACTION: JK to establish specs stub page at endpoint |

Action items
------------

- [ ] Greg Janée will try to reword the statement about normalizing alternate forms of received hyphens
- [x] John Kunze to establish specs stub page at endpoint
- [x] John Kunze to add contrast to the two diagrams