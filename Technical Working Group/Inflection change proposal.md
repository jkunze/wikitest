\---

confluence-id: 176490258

confluence-space: %%CONFLUENCE-SPACE%%

\---

Inflection change proposal
==========================

Created by John Kunze, last modified on Jan 08, 2020

### Problem: existing ARK inflections ? and ?? have not been adopted widely, for reasons that include

*   It can be hard for servers to detect a terminal '?' as different from the absence of a query string. It is in fact impossible in Tomcat, and requires rewrite rules in Apache.
    *   unlike '...??' (legal URL), '...?' is not a "legal" URL, so software libraries don't pass it through
*   Although '?' is intuitive and language-agnostic, it can also be puzzling to some people.
*   The metadata to be returned was only vaguely defined (mostly by example).
*   The metadata syntax (ANVL) was non-standard and largely defined by example.

### Requirements and Desiderata

Karen/Bertrand

1.  At minimum, ?info must resolve to a human readable landing page, and _should_ provide a _gateway_ to machine-readable metadata
2.  It is _strongly recommended_ that meta tags with \[something like\] DC are implemented (I’m suggesting this since they are simple html, and all orgs should be able to do something with those)
3.  Secondary to this,  organizations are encouraged to use whatever data format\[s\] is appropriate in their context as the machine-readable data version of ?info, but _encourage_ that organizations:

1.  1.  utilize an established metadata standard (like DC) where possible
    2.  utilize an established serialization for their metadata such as XML, JSON, or an RDF serialization such as JSON-LD or Turtle.
    3.  express the document type via the “Content-Type:” HTTP header.
    4.  utilize either content negotiation or queries in the form “&format=\[json|xml\]” property to deal with alternative formats.
    
    _Karen: I added c) as a suggestion. I don’t know if you want to indicate a preferred serialization/standard beyond this, or specify minimal metadata fields (the who, what, etc.), or keep it very loose. We could then provide examples that lay out different flavors that are acceptable – I would be willing to contribute an example._ 
    

John

1.  Some continuity with past
    1.  human-readable metadata returned
    2.  machine-readable metadata returned
    3.  including persistence statements
    4.  who/what/when/where paradigm (ERC)
    5.  THUMP-like request protocol -- ?info(X,Y) vs ?info&arg1=X&arg2=Y
2.  Never RDF
    1.  unfortunately, JSON-LD is RDF; see tweet [https://twitter.com/justin\_littman/status/1206944465027584001](https://twitter.com/justin_littman/status/1206944465027584001)
    2.  however, widely used [schema.org](http://schema.org) borrows elements names from JSON-LD and uses them in meta tags, which aren't at risk of RDF complexity

### Proposed solution discussions, in reverse chronological order

**2019.12.15** Draft Inflection Spec: "?info"

The _info inflection_ is a string, "?info", that may be added to an ARK before resolving it in order to request the return of human- and machine-readable metadata describing the identified object and the commitment made to it by its provider. A successful response returns metadata content as HTML intended for human consumption, along with embedded JSON intended for machine consumption. Future extensions are expected that will permit the request and return of alternate formats. Embedded HTML meta tags that repeat some of the metadata using schema.org element names are recommended because not all processors recognize JSON metadata. It is acceptable in the short term also to recognize the older "?" and "??" inflections and to treat them as synonymous with "?info", but their behavior may change in future versions of the ARK specification.

For the sake of discussion, we define some new terms. Resolution of a given ARK (or any URL) may be a multi-stage process starting with the _first resolver_ hostname appearing in the URL form of the ARK when it is submitted for resolution. Examples are n2t.net and ark.bnf.fr. The first resolver may forward (HTTP redirect) to a second resolver, which may in turn forward to another, and so forth. The _content resolver_ is the HTTP server that returns object content directly (ie, without forwarding). The metadata resolver is the HTTP server that, in response to the info inflection, returns metadata content directly. For a given ARK, the metadata resolver may be on a different host from the content resolver. (On the other hand, all three resolvers might also be on the same host.) For example, the N2T.net resolver stores a preservation copy of object metadata and can be configured on a per-ARK basis to respond to the info inflection directly or to forward it.

The object metadata returned in response to the info inflection depends not only on the object's immediate descriptive attributes but also on the object type and its place in a constituent cluster. For example, an ARK identifying a published article could have immediate attributes such as author (who), title (what), and date (when), but also, because it is a publication, additional core attributes such as publisher and length (number of pages). The article, one of eight in a particular issue of a journal, might also have multiple versions, in multiple formats, and might contain logical parts such as Abstract, Article, Appendices, and References. These represent its constituent cluster, which is a set of objects with which a given object has any of the following relationships: hasPart, isPartOf, isSiblingOf, HasFormat, hasVersion. For example, our article isPartOf a journal issue, hasPart References, and hasFormat(s) PDF and HTML. Because of its place in the cluster, the article's metadata should contain a link to the issue of which it is part. Link relationships within the constituent cluster exist independent of whether they are ARKs or whether they are ARKs that use the reserved '/' and '.' characters.

<script type="application/json">  
{  
"id\_requested": "...",  
"id\_normalized": "...",  
"id\_surrogate": "...",   # (optional) different id for digital surrogate, implies requested id is about physical object  
"id\_up1": "...",         # (optional) different id for 1st interesting landing page "above" this level  
"id\_up2": "...",         # (optional) different id for 2nd interesting landing page "above" the up1 level  
"report": {  
  "\_comment": "The next 5 elements are for very broad cross-domain interoperation.",  
  "who": "National Cancer Institute; ICPSR - Interuniversity Consortium for Political and Social Research",  
  "what": "Cancer Surveillance and Epidemiology in the United States and Puerto Rico, 1973–1977",  
  "when": "1984-05-03",  
  "where": "[https://n2t.net/ark:/12345/x408001.v2](https://n2t.net/ark:/12345/x408001.v2)",  
  "how": "(:mtype data) Dataset",  
  "thumbnail": "...",  
  
  "\_comment": "metatype-dependent core",  
  ...,  
  
  "persistence":  {  
    "object": \[ "indefinite", "standard" \],  
    "content": \[ "keeping", "waxing" \],  
    "identifier": \[ "single\_use", "opaque", "intraversioned", "unbranded" \],  
    "provider": \[ "mission", "nonprofit" \]  
 },  
 "cite-as": "[https://n2t.net/ark:/12345/x408001.v2](https://n2t.net/ark:/12345/x408001.v2)",  
  
 "\_comment": "domain-dependent metadata",  
 "name": "Cancer Surveillance and Epidemiology in the United States and Puerto Rico, 1973–1977",  
 "producer": "National Cancer Institute",  
 "archive": "ICPSR - Interuniversity Consortium for Political and Social Research",  
 "datePublished": "1984-05-03",  
 "dateModified": "2015-08-06T11:20:58Z",  
 "version": "v2"  
}  
</script>  
  
<!-- why? because not everyone recognizes JSON script metadata -->  
<meta name="DC.identifier" content="[ark:/12345/x408001.v2](http://ark/12345/x408001.v2)" scheme="DCTERMS.URI"/>  
<meta name="DC.title" content="Cancer Surveillance and Epidemiology in the United States and Puerto Rico, 1973–1977"/>  
<meta name="DC.creator" content="National Cancer Institute"/>  
<meta name="DC.publisher" content="ICPSR - Interuniversity Consortium for Political and Social Research"/>  
<meta name="DC.date" content="1984-05-03" scheme="DCTERMS.W3CDTF"/>  
<meta name="DC.type" content="Dataset"/>

  

**2019.11.26** strawdog JSON

Returns HTML with  
a) embedded GeoJSON, which allows foreign members from JSON-LD  
  why? because of high integration with widespread tools, like google search and instant map integration is visually powerful  
b) embedded HTML meta tags  
  why? because not everyone is extracting JSON-LD tags  
c) metadata elements formatted for human reading per provider preference

<script type="application/ld+json">  
{  
"@context": "[http://schema.org](http://schema.org)",  
"@type": "Dataset",  
"@id": "[https://n2t.net/ark:/12345/x408001.v2](https://n2t.net/ark:/12345/x408001.v2)",  
  
"who": "National Cancer Institute; ICPSR - Interuniversity Consortium for Political and Social Research",  
"what": "Cancer Surveillance and Epidemiology in the United States and Puerto Rico, 1973–1977",  
"when": "1984-05-03",  
"where": "[https://n2t.net/ark:/12345/x408001.v2](https://n2t.net/ark:/12345/x408001.v2)",  
"how": "(:mtype data) Dataset",  
  
"kids": \[  
  "[https://n2t.net/ark:/12345/x408001.v2/file.xsl](https://n2t.net/ark:/12345/x408001.v2/file.xsl)",  
  "[https://n2t.net/ark:/12345/x408001.v2/file.csv](https://n2t.net/ark:/12345/x408001.v2/file.csv)",  
  "[https://n2t.net/ark:/12345/x408001.v2/file.pdf](https://n2t.net/ark:/12345/x408001.v2/file.pdf)"  
\],  
"parent": "[https://n2t.net/ark:/12345/x408001](https://n2t.net/ark:/12345/x408001)",  
"cite-as": "[https://n2t.net/ark:/12345/x408001.v2](https://n2t.net/ark:/12345/x408001.v2)",  
"stickiness": \[  
  "\_see: [https://datascience.codata.org/articles/10.5334/dsj-2017-039/](https://datascience.codata.org/articles/10.5334/dsj-2017-039/)",  
  "indefinite", "keeping", "intraversioned", "standard", "NR", "OP"  
\],  
  
"name": "Cancer Surveillance and Epidemiology in the United States and Puerto Rico, 1973–1977",  
"author": "National Cancer Institute",  
"publisher": "ICPSR - Interuniversity Consortium for Political and Social Research",  
"datePublished": "1984-05-03",  
"dateModified": "2015-08-06T11:20:58Z",  
"version": "v2",  
"Description": "This dataset was produced as part of the Surveillance, Epidemiology, and End Results (SEER) Program to monitor the incidence of cancer and cancer survival rates in the United States, thus carrying out the mandates of the National Cancer Act. The SEER Program had several objectives: to estimate the annual cancer incidence in the United States, to examine trends in cancer patient survival, to identify cancer etiologic factors, and to monitor trends in the incidence of cancer in selected geographic areas with respect to demographic and social characteristics..."}  
</script>  
  
<!-- why? because not everyone recognizes JSON script metadata -->  
<meta name="DC.identifier" content="[ark:/12345/x408001.v2](http://ark/12345/x408001.v2)" scheme="DCTERMS.URI"/>  
<meta name="DC.title" content="Cancer Surveillance and Epidemiology in the United States and Puerto Rico, 1973–1977"/>  
<meta name="DC.creator" content="National Cancer Institute"/>  
<meta name="DC.publisher" content="ICPSR - Interuniversity Consortium for Political and Social Research"/>  
<meta name="DC.date" content="1984-05-03" scheme="DCTERMS.W3CDTF"/>  
<meta name="DC.type" content="Dataset"/>

  

  

**2019.11.04** a different proposal for the new ?info inflection

Proposed: for any ARK _X_, _X_?info should lead to an HTML-formatted "landing" document (page) with metadata embedded as JSON-LD. The metadata, in human- and machine-readable form, includes

1.  The ARK _X_
2.  Descriptive metadata:
    1.  who
    2.  what
    3.  when
    4.  where
    5.  how ([metatype](https://n2t.net/e/n2t_apidoc.html), similar to resourcetype)
    6.  domain-specific elements (eg, publications vs physical samples vs vocabulary terms)
3.  PIDs to first-level variants (versions, formats, change history) and components of _X_, if any
4.  PID to the first (immediate) logical ancestor of _X_
    1.  eg, if _X_ is a PDF variant of a document object, this points to the logical object ARK listing _X_ along with its sibling HTML and MSWord forms
5.  PID to the **last** (root) logical ancestor of _X_
    1.  eg, if _X_ is a section of a chapter of a book, this points to the book logical object
6.  Change history, if any
7.  Licensing and accessibility information
8.  How to cite, including "cite-as" header
9.  Persistence statement

A great example to follow would be the [A data citation roadmap for scholarly data repositories](https://n2t.net/doi:10.1038/s41597-019-0031-8).

**2019.09.16** proposal for a new, explicit word-based inflection: ?info

*   ?info requests metadata
*   ?info required, but spec continues to reserve '?' and '??' as optional synonyms 
*   ?info requests anvl/erc, but the spec permits (as always) alternate formats
    *   continues to use THUMP conventions with parenthesized args
    *   ?info equivalent to ?info()

This is a small adjustment to the spec that doesn't quite specify how to request alternate formats, but cracks open the door to work that we can complete, not in the spec, but in the AITO context. An example of that might be the THUMP request:  
                  ?info()as(application/json)

**2019.08.05** more discussion of collapsing existing ? and ?? into just ??

**2019.07.15** Proposed: suppress '?' inflection (let it be optional), leaving just the '??' inflection

*   as before, '??' requests kernel elements plus any persistence statement
*   '??' easier to implement than '?' (the latter being impossible to detect in Tomcat)
*   '?' may be supported by older implementations (briefer record)
*      ... or should '?' be made identical to '??'  ?