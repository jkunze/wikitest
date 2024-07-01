\---

confluence-id: 291799365

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-06-13 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Jun 21, 2023

Date
----

13 Jun 2023

Attendees
---------

*   Karen Hanson, Dave Vieglais, Greg Janee,  Donny Winston, Tom Creighton, John  Kunze

Goals
-----

ARK spec and NAAN schema transition

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     |     |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html).<br><br>*   please do quick review of [community update draft](https://arks.org/?p=1641&preview=1&_ppp=0559e261de) |     | dw: i'll be at IDW (International Data Weeik)<br><br>gj: [https://datacurationnetwork.org/events/annual-meeting/](https://datacurationnetwork.org/events/annual-meeting/)<br><br>dw, kh: blog post looks fine |
| ARK spec [transition plan](https://docs.google.com/document/d/1aFgujlL5yE3ZUORXRRkDTDNrlZEQU69lOU6Gc3wlyt4/edit#heading=h.71xqg8hedqw6)<br><br>*   Tom Creighton analysis of event date ordering and dependencies<br>*   date of interest to NAAN group: when do we advise new NAAN holders to resolve both forms? do we point them to one of the newer specs? |     | We didn't get to this. Will set up a separate meeting. |
| Topic: saving periodic dumps of ARK metadata<br><br>Any thoughts on this exchange around April 20 on the arks-forum? <br><br>AK: "My question was primarily focused on the long-term sustainability of what you are naming secondary content, that is, metadata.It is promising for the future of the ARK system, that there could be enhancements in the latest N2T software that may extend its capabilities in a way that opens the system to more ARK organizations, perhaps enabling them to deposit metadata in external storage."<br><br>DW: "One position on ensuring long-term metadata availability is the "Available data" bullet of <[https://openscholarlyinfrastructure.org/#insurance](https://openscholarlyinfrastructure.org/#insurance)\>, i.e. "Underlying data should be made easily available via periodic data dumps."<br><br>Crossref has adopted this position, and for its allocation of DOIs and stewardship of associated metadata, has so far provided three annual dumps available via torrent ([last blog post](https://www.crossref.org/blog/2022-public-data-file-of-more-than-134-million-metadata-records-now-available/), [search for "Crossref" on academictorrents.com](https://academictorrents.com/browse.php?search=Crossref), [landing page for their last (April 2022) dump](https://academictorrents.com/details/4dcfdf804775f2d92b7a030305fa0350ebef6f3e)). Their last dump, in April 2022, contained 134M records and is 160GB.<br><br>DataCite has not yet provided a similarly clear dump of their DOI holdings, but someone has taken an interest in doing this for them, posting the dumps to [archive.org](http://archive.org/), e.g. [https://archive.org/details/datacite\_dump\_20221118](https://archive.org/details/datacite_dump_20221118) is the latest there.<br><br>This, of course, is still fragmented for DOI holdings, i.e. one needs to gather such dumps from each DOI provider. This is perhaps a practically sustainable situation for the DOI system because the various providers are known and relatively (vs the ARK system) few in number. For the ARK community, I can see clear value in voluntary consolidation of e.g. CC0-licensable metadata across NAAs to a shared store on a periodic (e.g. quarterly or annual) basis. So yes, I also am interested in ongoing discussion on this topic.<br><br>P.S. Another potential "leg" of redundancy is to use Amazon's current Open Data program ([https://aws.amazon.com/opendata/](https://aws.amazon.com/opendata/)) as e.g. the OpenAlex effort does for dumps ([https://docs.openalex.org/download-all-data/download-to-your-machine](https://docs.openalex.org/download-all-data/download-to-your-machine)). I stress "leg" here because by no means am I suggesting any singular dependence whatsoever on this large corporation's current offering of free hosting."<br><br>NT: "It's been interesting following this discussion. I'm glad that Donny is pointing to POSI. Might a lightweight approach to storing additional copies of the n2t metadata are public github and gitlab repositories that could be updated monthly or on some sort of periodic basis through a simple git comitt and push? If additional preservation is desired, internet archive or OSF might be a good choice."<br><br>JK: "I'll make sure to add it to the agenda in the ongoing discussions we are having in the ARK Alliance Advisory Group." |     | dw: I think it'd be useful to have a dump of the fact that, for example, ark:12090/ is intended to pass through to [https://lib.cam.ac.uk/ark:$id](https://lib.cam.ac.uk/ark:$id) . This is currently only known if [https://n2t.net/ark:12090/](https://n2t.net/ark:12090/) resolves.  <br>so at a minimum, a dump of [https://n2t.net/e/pub/naan\_registry.txt](https://n2t.net/e/pub/naan_registry.txt) and each https://n2t.net/ark:<naan>/ response.  <br>one option is the internet archive, depending on our initial scale: [https://archive.org/details/ia\_biblio\_metadata](https://archive.org/details/ia_biblio_metadata)  <br>e.g. the ORCID public data file: [https://archive.org/details/orcid-dump-2021](https://archive.org/details/orcid-dump-2021)<br><br>dv: ideally, naan registry will allow preferred forwarding form, then new orgs could do it<br><br>gj, tc: dumps may not be as useful as oai-pmh  <br>tc: where do the dumps live, where do they come from  <br>gj: POSI say this data should be accessible, without saying how  <br>dw: yes, eg, orcid stores annually in IA, signaling at least intent  <br>tc: would be reasonable for FamilySearch to provide metadata on demain  <br>dv: would be huge to have list of ids minted  <br>dv: wonder if we could recommend that resolvers provide a list of ids<br><br>dw: particularly for an opaque identifier, some descriptive information is helpful. for DOIs for publications, this metadata is typically citation metadata such as (author,title,journal,date,etc)  <br>so the interest would be in archiving the equivalent of (who,what,when,where) as per e.g. the ERC metadata kernel advocated in the ARK draft spec: [https://www.ietf.org/archive/id/draft-kunze-ark-37.html#name-the-electronic-resource-cita](https://www.ietf.org/archive/id/draft-kunze-ark-37.html#name-the-electronic-resource-cita)<br><br>dw: can be hard to put up an API compared to a file  <br>kh: challenging to get everyone to do the same thing  <br>tc: we have to deal with attacks  <br>dv: a list of ARKs would increase the attach surface  <br>dv: It’s more that advertising the list by passes one chunk of work done by scrapers to discover the entry points to the data.  <br>dw: attack surface suggests that some ARKs aren't meant to be open  <br>tc: we have obligations to get data out to partner sites |
| - [ ] Dave Vieglais produce documentation and new NAAN schema for validation and form processing (Donny Winston can help) |     | dv: [https://github.com/CDLUC3/naan\_reg\_public](https://github.com/CDLUC3/naan_reg_public) possibly part of new  <br>    Maria's meeting on proposed naan schema changes |

Action items
------------