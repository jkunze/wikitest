\---

confluence-id: 273351948

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-02-14 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Feb 24, 2023

Date
----

14 Feb 2023

Attendees
---------

*   Curtis Mirci, Roxana Maurer, Dave Vieglais, Donny Winston, Karen Hanson

Goals
-----

homepage review, spec transition, persistence statements

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | Community Leaders (chairs and co-chairs email list set up) arka-conduct@googlegroups.com<br><br>https://arks.org/community doesn’t load, but https://arks.org/community/ does …<br><br>John wants a "send an email" form to put on the code of conduct page. So no need to give out an email address of individual chair or co-chair.<br><br>*   there are services to embed a contact form on a static website, e.g. netlify forms (https://www.netlify.com/products/forms/), backed by "serverless functions" (ephemeral container init and running)<br>*   good to have something that works with github pages (where we want to migrate to) |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     | \* nice to have blog post persistence statements once there's some more concrete content to share |
| WG [homepage review](https://docs.google.com/document/d/1n5ETS45fHqJefu74vXKLFZhrXm_VmIB7jT2Yk4zR2_E/edit#heading=h.v83orrqv3vnr) |     | https://docs.google.com/document/d/1n5ETS45fHqJefu74vXKLFZhrXm\_VmIB7jT2Yk4zR2\_E/edit#heading=h.v83orrqv3vnr<br><br>Migration from confluence, perhaps consider something like: https://github.com/sjones4/confluence-to-github<br><br>ensure deliverable(s) associated with each objective:<br><br>*       json schema for NAAN entry record for validation. |
| Ongoing [collection of ARK spec update use cases](https://docs.google.com/document/d/1Yh60RajuAqlBox94iW47_43oeOKEuyzenXExggtpGdU)<br><br>Spec transition implementation – is someone willing to lead? |     | https://docs.google.com/document/d/1Yh60RajuAqlBox94iW47\_43oeOKEuyzenXExggtpGdU<br><br>updates:<br><br>*   length of NAAN is variable. Not restricted to 5-digit numerical values<br>*   no slash after colon (ark:12345/key) is the canonical form, but old form (ark:/12345/key) must still resolve.<br><br>Need concise description of changes. |
| Persistence Statements / "Durability"? [strawman](https://docs.google.com/document/d/1Ej8wup8mK3yS39AdwHDJSclPCh3K9zP-RlkPKaqmxQ4/edit?usp=sharing)<br><br>MVP (minimum viable product) |     | strawman mvp: https://docs.google.com/document/d/1Ej8wup8mK3yS39AdwHDJSclPCh3K9zP-RlkPKaqmxQ4/edit?usp=sharing<br><br>objective: be less overwhelming than https://datascience.codata.org/articles/10.5334/dsj-2017-039/<br><br>NR - non-reassignment  <br>OP - opaque  <br>CC - check character  <br>resolvable |

Action items
------------

- [ ] John Kunze need concise description of ARK spec changes to aid transition plan; blog about it?
- [ ] Dave Vieglais produce documentation and new NAAN schema for validation and form processing (Donny can help)