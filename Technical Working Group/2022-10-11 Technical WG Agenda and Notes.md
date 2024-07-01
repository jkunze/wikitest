\---

confluence-id: 255918280

confluence-space: %%CONFLUENCE-SPACE%%

\---

2022-10-11 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Nov 07, 2022

Date
----

11 Oct 2022

Attendees
---------

*   Curtis Mirci, Dave Vieglais, Karen Hanson, Greg Janee, Roxana Maurer, Tom Creighton

Goals
-----

       NISO, resolver, persistence descriptor updates

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements<br><br>*   Arkspec.md<br>*   DeSci.com |     | dv: tried converting the ARK spec to markdown format suitable for IETF publication; if this works it can be a much easier way to manage the text than the XML format  <br>ACTION: jk and dv to meet to do the conversion to new spec<br><br>jk: The DeSci.com folks are quite interested in ARKs as a citation friendly (shortish), possibly mutable objects that reference parts of IPFS and IPNS; interested in endorsing ARKA  <br>all: general agreement that we're interested in desci's explorations in this area and about keeping up awareness  <br>rm: I'd support mentioning them on the website  <br>ACTION: jk: I'll ask them to fill out the expression of interest form, which we already have procedures for |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     | jk: CNI panel proposal (for December 12-13) was submitted |
| Any news items we should blog about? |     |     |
| persistence descriptors<br><br>*   Upcoming meeting with FamilySearch |     | jk: will meet with FamilySearch; please speak up if you're interested in joining<br><br>rm: BnL (National Library of Luxembourg) uses these terms<br><br>persistence: { _// Persistence statements: https://datascience.codata.org/articles/10.5334/dsj-2017-039/_    <br><br>        contentVariance: {  _// how an object’s content will change over time_<br><br>            **type**: **String**,<br><br>            enum: \[<br><br>                "frozen",   _// The bit stream representing previously recorded content will not change._<br><br>                "keeping",  _// Previously recorded content will not change, but character, compression, and markup encodings may change during a format migration, and high-priority security concerns will be acted upon (e.g., software virus decontamination, security patching)._<br><br>                "fixing",   _// Previously recorded content may be corrected at any time, in addition to any change under “keeping”._<br><br>                "rising",   _// Previously recorded content may be improved at any time, for example, with better metadata (datasets), new features (software), or new insights (pre- and post-prints). This encompasses any change under “fixing”._<br><br>                "molting",  _// Previously recorded content may be entirely overwritten at any time with content that preserves thematic continuity (homepages)._<br><br>                "waxing"    _// Change that is limited to appending content in a way that does not in itself disrupt or displace previously recorded content. Examples of waxing objects include live sensor-based data feeds, citation databases, and serial publications._<br><br>            \]<br><br>        },<br><br>        objectAvailability: {   _// the period of time during which the provider expects to keep the object available_<br><br>            **type**: **String**,<br><br>            enum: \[<br><br>                "finite",   _// Availability is expected to end on or around a given date (e.g., limited support for software versions not marked “long term stable”) or trigger event (e.g., single-use link)._<br><br>                "indefinite",   _// The provider has no particular commitment to the object._<br><br>                "lifetime", _// The object is expected to be available as long as the provider exists._<br><br>                "subinfinite"   _// Due to succession arrangements, the object is expected to be available beyond the provider organization’s lifetime._<br><br>            \]<br><br>        },<br><br>        nonReassignment: {  _// (NR) Once assigned and made public, the identifier will not be reassigned._<br><br>            **type**: **Boolean**<br><br>  <br><br>BnL example: [https://persist.lu/ark:70795/m4bk6v?info](https://persist.lu/ark:70795/m4bk6v?info) returns<br><br>{  <br>  "persistence": {  <br>    "objectAvailability": "lifetime",  <br>    "objectContentChange": {  <br>      "contentVariance": "rising",  <br>      "contentGrowthOverTime": false  <br>    },  <br>    "arkNonReassignment": true,  <br>    "arkOpacity": true,  <br>    "arkCheckCharacter": true  <br>  },  <br>  "erc": {  <br>    "what": "Diekircher Wochenblatt",  <br>    "when": "1841-01-23",  <br>    "type": "Newspaper (digitized)",  <br>    "format": "METS/ALTO"  <br>  },  <br>  "status": "public",  <br>  "owner": "Bibliothèque nationale du Luxembourg (=) National Library of Luxembourg (=) BnL",  <br>  "target": "[https://viewer.eluxemburgensia.lu/ark:70795/m4bk6v](https://viewer.eluxemburgensia.lu/ark:70795/m4bk6v)",  <br>  "updated": "2020-06-16T07:06:41.575Z"  <br>} |
| Spec transition, ongoing [collection of ARK spec update use cases](https://docs.google.com/document/d/1ChFEml3HCxm02E8c1yt8BwpGmMzLvsHZSi6O00sgixg) |     | skipped |
| New resolver update from Dave V:<br><br>*   The N2T resolver replacement is being implemented using the Python FastAPI asynchronous web service framework. Goals of the implementation include minimal resource requirements, maintainable codebase, multiple parallel deployment support, emphasis on API access, and compliance with applicable specifications.<br>    <br>    The purposes of the implementation include:<br>    <br>    *   Determine the applicable resolver service given an identifier or portion thereof.<br>    *   Provide information about the resolver(s) available for a given identifier.<br>    *   Periodically evaluate the operation of advertised resolver services.<br>    <br>    Challenges that need to be addressed include dealing with the ARK inflection requests and concocting a resolver service metadata spec.<br>    <br>*   For example, a double “?” (“??”) can be reliably passed through to the web application, appearing as a single “?” since technically the second “?” is the query string. However a single “?” may be consumed at the client, the proxy, the load balancer, the web server, the web server application environment, or the web application framework with no hint to the web application since any of those components may perform some url normalization that removes the single “?” since it is a no-op under HTTP. |     | dv: N2T resolver still has challenges around classic inflections; hope to be finished by end of year  <br>gj: will there be distributed with failover?  <br>d: yes, definitely, possibly a large number of resolvers |
| NISO update |     | jk: no word from NISO yet |
| docker minting tool update<br><br>*   Need to fix minter state<br>*   Added limitations section<br>*   Set expectation of no further (fundamental) development<br><br>SYNOPSIS<br><br>arknoid - tool to create ARK (Archival Resource Key) identifiers<br><br>QUICK START<br><br>If your organization doesn't have a NAAN, request one here:<br><br>    https://n2t.net/e/naan_request<br>    <br><br>After you install docker on your host, build the arknoid container:<br><br>    $ docker run -it -d --rm --name arknoid jakkbl/arknoid<br>    <br><br>Initialize the system with your organization's 5-digit NAAN:<br><br>    $ docker exec -it arknoid arknoid init 12345<br>    <br><br>Mint one ARK string with<br><br>    $ docker exec -it arknoid arknoid mint 1<br>    ark:12345/h74x54g19<br>    <br><br>Mint enough unique ARK strings to assign to your 35865 objects with<br><br>    $ docker exec -it arknoid arknoid mint 36000 > MyFirstARKs<br>    <br><br>You can mint over 70 million ARKs with one minter, and make as many minters as you want whenever you want. Your ARKs will be unique across all minters. |     | jk: that should be fixed  <br>kh: with this tool, it looks like dockerhub become another in the suite of ARKA accounts that we need access to  <br>ACTION: jk: yes, I'll plan to move arknoid to arks-org repo, and away from jakkbl dockerhub<br><br>gj: minter state still seems fragile given that containers disappear  <br>kh: current tool seems not to lose minter state when the container is removed  <br>dv: recommend using docker-compose with volume spec and env variable  <br>ACTION: jk: fix the lost state problem<br><br>dv: also, there's my python tool: noidy [https://github.com/datadavev/noidy](https://github.com/datadavev/noidy) which doesn't run out of strings |

Action items
------------

- [x] John Kunze meet with Dave Vieglais to convert to new markdown spec
- [ ] John Kunze move docker-arknoid to arks-org repo, and away from jakkbl dockerhub, and also fix the lost state problem