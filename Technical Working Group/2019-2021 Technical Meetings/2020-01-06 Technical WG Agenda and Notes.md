\---

confluence-id: 178882930

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-01-06 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Jan 08, 2020

Date
----

06 Jan 2020

Attendees
---------

*   John Kunze
    
*   Karen Hanson
    
*   Bertrand Caron
*   Greg Janée

Goals
-----

*   dive more into ?info inflection in a subgroup meeting

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | requirements and desiderata |     | see new section at top of [Inflection change proposal](Inflection-change-proposal_176490258.html)<br><br>Karen/Bertrand<br><br>1.  At minimum, ?info must resolve to a human readable landing page, and _should_ provide a _gateway_ to machine-readable metadata<br>2.  It is _strongly recommended_ that meta tags with \[something like\] DC are implemented (I’m suggesting this since they are simple html, and all orgs should be able to do something with those)<br>3.  Secondary to this, we encourage organizations to use whatever data format\[s\] is appropriate in their context as the machine-readable data version of ?info, but encourage that:<br>    1.  Organizations include DC and/or schema.org metadata where possible<br>    2.  Organizations use XML or JSON-LD or JSON serializations to express their<br>    3.  Organizations utilize either content negotiation or queries in the form “&format=\[json\|xml\|etc\]” property to deal with alternative formats.<br><br>John<br><br>1.  Some continuity with past<br>    1.  human-readable metadata returned<br>    2.  machine-readable metadata returned<br>    3.  including persistence statements<br>    4.  who/what/when/where paradigm (ERC)<br>    5.  THUMP-like request protocol -- ?info(X,Y) vs ?info&arg1=X&arg2=Y<br>2.  Never RDF<br>    1.  unfortunately, JSON-LD is RDF; see tweet [https://twitter.com/justin\_littman/status/1206944465027584001](https://twitter.com/justin_littman/status/1206944465027584001)<br>    2.  however, widely used [schema.org](http://schema.org/) borrows elements names from JSON-LD and uses them in meta tags, which aren't at risk of RDF complexity |
|     | JSON-LD caution |     | KH and BC: agree with Justin's recommendation  <br>KH: used OpenAPI/Swagger and think it could be a recommendation as a tool  <br>for a rest API, which may be overkill  <br>BC: some BnF expertise  <br>GJ: \* json-ld is used by google, right?  <br>KH: RDF or Linked Data serializations are functionally equivalent,  <br>\- plus or minus graph id  <br>KH: see [https://developers.google.com/search/docs/guides/intro-structured-data](https://developers.google.com/search/docs/guides/intro-structured-data)  <br>GJ: ACTION: will look for google recs: "google json-ld"  <br>KH: very interested in Association Type discussion |

Action items
------------

- [ ] Greg Janéewill will look for google recommendations and report