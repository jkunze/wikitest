\---

confluence-id: 264995020

confluence-space: %%CONFLUENCE-SPACE%%

\---

2022-11-08 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Dec 12, 2022

Date
----

08 Nov 2022

Attendees
---------

*   Karen Hanson
*   Dave Vieglais
*   John Kunze
*   Donny Winston
*   Mark Phillips
*   Curtis Mirci
*   Tom Creighton
*   Greg Janée
*   Roxana Maurer

Goals
-----

Spec updates, draft CoC, persistence statements, IIIF and ARKs

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | jk: experimenting with beta ARKA stickers – anyone know of a business that accept sticker orders from users and mail directly to them? I've heard of shopify.com but didn't see the right fit.  <br>dw: [redbubble.com](http://redbubble.com) may work like shopify  <br>tc: stickers, is shipping more important than printing?  <br>jk: to me, yes  <br>kh: This is what we use, not sure how it works: [https://www.makestickers.com/](https://www.makestickers.com/) |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html)<br><br>2023 Code4Lib pre-conference<br><br>_From Hardy PottingerSubject: Call for Proposals - 2023 Code4Lib Pre-Conference_<br><br>_We are now accepting pre-conference proposals for the 2023 Code4Lib conference at Princeton University in Princeton, New Jersey. These pre-conferences can either be a 1-day (six hour) or a 1/2-day session (three hour) and will occur on Tuesday, March 14th. These workshops are required to be In-Person ONLY._<br><br>_Code4Lib 2023 is a loosely-structured conference that provides people working at the intersection of libraries/archives/museums/cultural heritage and technology with a chance to share ideas, be inspired, and forge collaborations. For more information about the Code4Lib community, please visit [https://code4lib.org/about/](https://code4lib.org/about/)._<br><br>_The pre-conference sessions give folks a space to share and build knowledge, as well as to teach attendees new skills relevant to library technology. Pre-conference sessions can range from workshops to working sessions._<br><br>_To propose a session, please go to the [2023 submission form](https://forms.gle/e1fgutRMHRxJJwVQ7). If you're looking for inspiration, there are many great examples of pre-conferences from recent years:_ <br><br> _[https://2022.code4lib.org/workshops/](https://2022.code4lib.org/workshops/), [https://2021.code4lib.org/workshops/](https://2021.code4lib.org/workshops/), [https://2020.code4lib.org/workshops/](https://2020.code4lib.org/workshops/), [https://2019.code4lib.org/workshops/](https://2019.code4lib.org/workshops/)._<br><br>_We are taking proposals until November 30, 2022, 5 PM PST / 8 PM EST. After a period of public voting on workshops, we hope to confirm sessions with the facilitators shortly after._ <br><br>_If you have any questions, please do not hesitate to email us - by responding to this email or by contacting Code4Lib.Workshops@gmail.com._<br><br>_Best,_<br><br>_Code4Lib 2023 Pre-conference Committee_ |     | ARK panel turned down for CNI briefings, but it was suggested to resubmit as a CNI pre-recorded briefing<br><br>dw: I would be interested in developing a half-day workshop; I've worked with the carpentries, and its not too much of a stretch for me<br><br>dv: I have some open source ARK code that might be useful to present in a code4lib venue |
| blog posts?<br><br>draft [new ARKs-Service](https://docs.google.com/document/d/1BmhVk8D3SjZD8aGhdOVG3CJX_ftIAjpVXMC4VVSJ_M4/edit) |     | blog post being prepared by U of Toronto Scarborough Library |
| New [markdown format for ARK spec](https://github.com/arks-org/arkspec) |     | dv: converted the ARK spec from XML to markdown  <br>jk: seems to work fine with a next IETF draft publication process  <br>dv: for user-contributed change request, suggest doing PR from a branch for changes to ark spec  <br>all: agreed |
| IIIF connection made<br><br>While the spec recommends opacity in the base identifier, over time the spec has become more relaxed about semantics in extensions. In that vein, the IIIF API specifies certain characters (eg, ! and ^) in extensions in order to request variants of the base image object.<br><br>OTOH, like the ARK spec, the IIIF spec uses characters that should be encoded in URIs.<br><br>Interest in working with IIIF on this issue, or on PIDs in general? |     | mp: a nice thing about iiif is that there's another vendor that can do  <br>    a transcription service that's seamless once you have a iiif API  <br>    we had challenges wrt ARKs and iiif (6 years ago) image API<br><br>dw: it may be interesting to discuss tradeoffs of the use of slashes (/) to identify resource variants versus the ARK spec's discussion using periods (.) for variant delimiting vs having (/) be more geared to hierarchy. see e.g. the image API syntax: [https://iiif.io/api/image/3.0/#21-image-request-uri-syntax](https://iiif.io/api/image/3.0/#21-image-request-uri-syntax) (cf. what Mark is talking about)  <br>image api url format: [https://iiif.io/api/image/3.0/#21-image-request-uri-syntax](https://iiif.io/api/image/3.0/#21-image-request-uri-syntax)  <br>seems like full arks can be embedded in the {identifier} section of the image info request URI with URI Encoding: [https://iiif.io/api/image/3.0/#3-identifier](https://iiif.io/api/image/3.0/#3-identifier)<br><br>dv: chars that look like others can be a problem; I'm keen to participate in IIIF |
| [Code of Conduct draft](https://docs.google.com/document/d/1eIdWzeaRPNliwS3lgM3uN2t7SI4fs_NcnPVXu56XsnY/edit?usp=sharing) – please review by Nov 18 |     | cm: CoC looks good  <br>rm: CoC looks good  <br>kh: CoC looks good  <br>jk: will check with Advisory Group and other working groups |
| Persistence statements status<br><br>subgroup: Rob Lyon (familysearch), Roxana Maurer, Kirsta Stapelfeldt (utsc) + who else |     | rm: very interested in persistence statementsgj: same here  <br>dv: and here |
| docker-arknoid status |     | jk: not much progress, but bugs exist and will be deal with; minter state not persisting with anonymous volumes; would be nice to have minters not run out; would be nice to use arka dockerhub repo instead of personal repo |
| POSI alignment for ARKA/N2T.net? ([https://openscholarlyinfrastructure.org/](https://openscholarlyinfrastructure.org/)) | Donny | did not have time for this item  <br>jk: the ARK/N2T infrastructure planners began using this as a blueprint around 2016 (see [timeline](https://wiki.lyrasis.org/display/ARKs/ARK+infrastructure+timeline)) |

Action items
------------

- [x] jk and dw to talk about possible C4L preconference 3-hour workshop
- [x] jk add ARK spec conversion to markdown to community update blog post
- [ ] jk, dv, gj to meet with persistence statements subgroup
- [ ] jk fix bugs in docker-arknoid