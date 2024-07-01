\---

confluence-id: 129008934

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-08-05 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified by Sheila Morrissey on Aug 05, 2019

Date
----

05 Aug 2019

Attendees
---------

*   John Kunze
    
*   Sheila Morrissey
    
*   Greg Janée
*   Curtis Mirci
*   Mark Phillips
*   Tom Creighton
*   Roxana Maurer

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements: |     | Some discussion of need for "global" review of spec before release for review so that changes all cohere, more polished view, and can give good high-level<br><br>Curtis and John spoke with some of repondants to poll. Comment from Pablo ? from Argentina that it is hard to find docs on ARKS (where to go - spec out of date, do I go to AITO?)  He went to [arks.cdlib.org](http://arks.cdlib.org) – Need to clean this up quickly  (part of outreach groups remit) (Pablo created Spanish-language ARK wikipedia page, is willing to translate FAQ as well)<br><br>Roxana reporting on enhancements to their  resolvers, etc. ; waiting on final spec for other changes |
|     | (from last time) research handling of query parameters that have no explicit value (eg. ...??) by HTTP servers and reverse proxies. | Tom | No clear one place to go for clarity on behaviors of reverse proxy servers; Specs vs. was is coded;  suggestion is to write a script and test against actual implementations;  Suggestion that Tom will continue to monitor, he will try against top 3 proxies to see results |
|     | question of collapsing ? and ?? |     | Greg: refers to Bertrands suggestion to use query term (non-empty) - why would we not? <br><br>John: question as to whether appearance of English words in standardized query  an issue (internationalization) (eg info)<br><br>2nd issue:  historically IETF reluctant to do anything to standardize query string - although using ? or ?? in effect standardizing anyway<br><br>Tom:  'meta'; ark-info, ark-meta;  maybe also consider as optional method of support is via request-header rather than in query string; would provide greater latitude in describing methods of formatting response <br><br>Mark: value also in having URL-like string that functions<br><br>Greg agrees use cases for both techniques - string easier for "naive" implementation- question would this be an extension header (X-)? <br><br>Tom yes - but style now for non-standardized without X quite common; also agrees, even if we do headers, useful to have query string<br><br>John: given we will approve inflection supported, considering adding one with word -   <br>Sheila - do we continue with ? and ?? - or just words in inflection?  Are issues with resolution making this something we should not use<br><br>John would like to continue; could have language like ?info preferred, reserve? and ?? since that has been in spec for so long<br><br>Curtis - prefers info, about - ? ok  if words, options to add more operations in future<br><br>John - we are moving to, at very least ? means same as ??, and ?? preferred<br><br>Should be one query that gives basic information plus persistence info<br><br>Sheila prefers word, okay with both<br><br>Mark:  has gotten feedback of questions about ? – looks strange to many for usual URLs; also implementations low; using word, making it "look" like query parameter would encourage greater use and implementation;  re "both" - Might be confusing to have 2 ways of doing it; good with collapsing the formerly 2 ops (metadata + Persistence) into one combined op<br><br>Roxana - most eager for clarification, decision so can proceed with implementation; for her ? is way to ask for info, but in web world, in URL, expect query behind it<br><br>Tom finds ? problematic (Jetty strips it out, concerned other servers might do same) - seems more natural to have word; really happy if can add accept headers, they make routing decisions based on that; keyword in query plus accept headers would be very useful<br><br>John - accept header good way to start; hybrid (both query string and header)<br><br>Greg - definitely likes use of words; ? or ?? not obvious to outsiders what difference is - looks like typo - HTTP uses words in lots of places (method names, headers);  query in URL makes it possible to bookmark it - strongly in favor of query term<br><br>Tom: is the the time to dive into what metadata should be returned and what formats<br><br>John suggests caution; perhaps converge on a few well-understood elements (who what when) then permit (any) other name-value pairs to prevent holding up this spec; make it a different working group's work<br><br>Tom - lots of clients that make REST calls; try to get more detailed metadata where clients are asking for it<br><br>Roxana - agrees with John's caution - eg what is the language for metadata (far more problematic than work in query string) ; Luxembourg uses 3 languages;<br><br>John: need to support metadata better, avoid holding up spec for this, but still must be done as perhaps main goal for this group; Spec - generic description of services<br><br>Mark - limited use cases that all ARKS must comply with; then have suggestions, recipes, reference to other document for other use cases<br><br>Sheila should we write up minimum use case description<br><br>John yes tech needs tightening it up to express bare minimum- language encoding richer metadata can happen in subsequent WG (this or other) activity -all |
|     | question of NAAN assignment corresponding to ISSN |     | John: Proposal to construct submission for request to NAAN to allow specification of use of ISSN; restrict to beginning with reserved initial letter;<br><br>Sheila our experience ISSN not totally stable and persistent - worry about complications for NAAN maintenance<br><br>Roxanne - -not an organization, an object managed by an organization; NAAN organization that manages object, NOT the object being managed  BNF have ARKs for catalog records; records merge - re-direct old ARK to new one |
|     | when to open spec review to arks-forum |     |     |

Action items
------------

- [ ] John Kunzewrite up summary of new take on inflections; capture consensus for all to review
- [ ]  John Kunzewill also work on minimizing, clarifying metadata returned by inflections
- [ ] all email any further thoughts on ISSN as NAAN