\---

confluence-id: 178881810

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-12-16 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified by Karen Hanson on Dec 16, 2019

Date
----

16 Dec 2019

Attendees
---------

*   John Kunze
    
*   Sheila Morrissey
    
*   Karen Hanson
*   Greg Janée
*   Bertrand Caron

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | updated timeline |     | timeline approved |
|     | proposed ARK spec cleanup |     | no objections to broad cleanup of spec, even if they generate noisy diffs |
|     | ongoing [?info inflection proposal](https://wiki.lyrasis.org/display/ARKs/Inflection+change+proposal) discussion<br><br>*   json vs json-ld (rdf)<br>    *   eg, [semantic web issues](http://www.lespetitescases.net/why-I-dont-use-semantic-web-technologies-anymore-even-if-they-still-influence-me)<br>*   accommodating descriptive hierarchy<br>    *   finding aid > box > folder > letter<br>    *   dataset > row > cell<br>    *   article landing page > pdf file |     | KH: article seems to still endorse RDF a bit; there's value in aligning with DataCite  <br>BC: going from XML to JSONLD logic isn't just a question of applying an xslt; we spent several years to come up with xml / mets data model; Gautier Poupeau (author of blob post) designed the dig repo at BnF  <br>BC: agree that for people who have XML-based metadata, it's easy to express it as json; but a json-ld expression requires revising your whole data model and so is much harder and very complicated  <br>GJ: could you explain why it's not just a simple mapping?  <br>BC: because you have to express everything in triples with entity-relationships  <br>JK: why isn't it just a set of key/value pairs?  <br>JK: should we invite Justin L to future subgroup meeting to help us understand? Bertrand, do you want to join as well?  <br>KH: yes, that would find that helpful  <br>BC: yes, I would  <br>GJ: see [https://blog.datacite.org/schema-org-register-dois/](https://blog.datacite.org/schema-org-register-dois/)  <br>BC: for persistence, we'll be defining our own vocabulary  <br>BC: if we went with Dublin Core entity-relationship model, that's simple enough; but if they have to invent their own model, that's much harder; by using linked data, one says that all my data is expressed as triples  <br>KH: see also [https://github.com/rmap-project/rmap-documentation/blob/master/guides/useful-ontologies.md](https://github.com/rmap-project/rmap-documentation/blob/master/guides/useful-ontologies.md)  <br>BC: nice to have a position about how we express metadata, but we have to go further and say, at least for basic metadata, what the recommended model is  <br>JK: \*model\* is important – we need to understand this better as a group  <br>KH: fortunately, vocabulary choice is independent of syntax  <br>BC: at BnF we chose XML and snippets; we could recommend a set of optional return formats; users at many French archives will have a hard time putting out something different from what they already do; this is an argument for giving people options for returned data  <br>KH: make it lightweight, but steer people in certain directions  <br>KH: See the Portland Common Data model  <br>SM: Portico would like a conceptual model for a landing page as an archival unit; it would be an enormous simplification to be able to have a landing page model for this |
|     |     |     |     |

Notes
-----

In follow-up email from KH:

_Reflecting on the discussion, I think it may have gotten lost that when we were discussing JSON-LD a few weeks ago, I believe it was imagined as part of a series of recommendations, not as requirement. If that is still the case, then perhaps it’s not necessary to add a meeting to discuss the pros and cons of linked data further, since implementation would be looser and JSON-LD would be encouraged but not required.  I think it should be perfectly fine for Portico to produce JSON-LD and BNF to produce XML._

_I’m wondering if the guidelines might go something along these lines:_

1.  _At minimum, ?info must resolve to a human readable landing page, and should provide a gateway to machine-readable metadata_
2.  _It is strongly recommended that meta tags with \[something like\] DC are implemented (since they are simple html, and all orgs should be able to do something with those)._
3.  _Secondary to this, we encourage but don’t require JSON-LD with [schema.org](http://schema.org) (and/or DC) on the ?info page (in alignment with the [JDDCP recommendations in the Scientific Data article](https://www.nature.com/articles/s41597-019-0031-8))._ 
4.  _Finally, regardless of whether JSON-LD is implemented, we encourage organizations to use whatever data format\[s\] is appropriate in their context as the machine-readable data version of ?info, but encourage that:_
    1.  _Organizations include DC metadata in this where possible_
    2.  _Organizations utilize either content negotiation or add “&format=\[json|xml|etc\]” property to deal with alternative formats._

_This is just a rough example, but maybe something like this approach might work to give a little structure but plenty of flexibility._

Action items
------------

- [ ] make sure ?info leaves options for people, but steers them towards json
- [ ] add Bertrand to subgroup