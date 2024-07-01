\---

confluence-id: 120520718

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-06-03 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Jul 07, 2019

Date
----

03 Jun 2019

Attendees
---------

*   John Kunze
    
*   Roxana Maurer
*   Sheila Morrissey
    
*   Greg Janée
*   Curtis Mirci
*   Tom Creighton
*   Bertrand Caron

Goals
-----

Continue review of spec changes, plus review of edits since last meeting:   [https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-18.txt&url2=draft-kunze-ark-21.txt](https://www.ietf.org/rfcdiff?url1=draft-kunze-ark-18.txt&url2=draft-kunze-ark-21.txt)

General Comments

*   Roxana noted that SNAC might be considering moving away from ARKs; John will follow up
*   Adrien has indicated he likely will not be continuing to participate in TWG meetings; consensus was that team as constituted has critical mass, and can continue without looking just now for a replacement
*   All are agreed in finding the "diff" format convenient for tracking changes in draft specification; Discussion items below will refer to locations in that diff (at link above) for today's discussion

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | Section 2 Ark Anatomy |     | *   Terminology clarified: resolving service vs. Mapping authority (host), Base object name (most important part to be opaque),Optional /:  APPROVED |
|     | Section 2.3 |     | *   instead of calling ark:/ “deprecated” call it “older”   APPROVED<br>    <br>*   longer NaaN allowed, stating as policy (separate from standard) that in practice we expect not change to sequences bigger than 5 characters  APPROVED |
|     | 2.6  Character repertoire |     | *   For received ARKs implementations must handle a minimum 255 octets; no statement of maximum, but caution for ARK-generating implementations that if length greater than 255, ARK might not be handled by some receiving implementations  APPROVED<br>    <br>*   ~ instead of / in characters  APPROVED<br>    <br>*   Question arose as to whether we should use all caps wherever such key words as 'must' or 'should' or 'may' appear – Agreed this was not necessary |
|     | 2.7. Normalization and Lexical Equivalence |     | *   Intent: Reserve ability for resolvers to recognize inflections (sixth) –<br>*   Greg suggest formatting as enumerated list, and also correct the enumeration in the text of "fourth and final step", which should be 7th step<br>*   Tom noted that comparing identifiers ark:/ irrelevant – why not strip it out? John noted used case where more than one ID type is being managed, Tom suggested that ID type could be stored as separate flag or attibute (important space saver if managing billions of ids)<br>*   Some discussion of necessity of managing % encoding<br>*   Tom raised question as to why hyphen was considered insignificant; John noted text formatters often insert hyphens, though it breaks URLs, and expect this to happen with ARKs; Roxanne noted that hyphen is significant by one minter (indicates NAAN/subpublisher-id-checksum) example here: [https://github.com/Inist-CNRS/node-inist-ark](https://github.com/Inist-CNRS/node-inist-ark) |
|     | page 28 |     | *   Reference include to paper on persistence statements as placeholder in order to keep spec minimal, and to have discussion on details of persistence statement happen instead through [arks.org](http://arks.org), external to the spec |
|     | 5.1.2 |     | *   Minor text changes |
|     | Reference |     | *   Tom asked if all were actually referenced in spec, or just "additional reading" Per John all actually referenced |
|     | appendix A |     | *   Description of arks.org and work "extra-spec" that is to be handled there |

Action items
------------

- [ ] Tom will provide example of their post-encoding (64bit integer in base31 encoding – eg take out 0 vs O)
- [x] Sheila will forward email re: change in DataCite business model
- [x] John will reach out to CNRS to see if published ARKs that have significant dashes can be mended
- [x] John will reach out to SNAC
- [x] John will turn normalization description into list of numbered steps
- [x] Greg will review text on normalization to make sure his concerns are met
- [ ] All should review their position on externalizing persistence statements
- [ ] Tom will review 5.1.2 more carefully to see if he has issues
- [x] All should review  section 2.2  Label (language on old and new form language ark:  ark:/)
- [x] All should please make comments on spec to the list