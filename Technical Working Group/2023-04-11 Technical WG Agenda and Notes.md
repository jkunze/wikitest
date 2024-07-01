\---

confluence-id: 285900897

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-04-11 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Apr 16, 2023

Date
----

11 Apr 2023

Attendees
---------

*   Dave Vieglais, Karen Hanson, Donny Winston, Greg Janee, Curtis Mirci, Tom Creighton

Goals
-----

Home page finalize, transition plan, standardization

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | *   https://www.pidwijzer.nl/en - Persistent Identifier Guide from Dutch Digital Heritage Network<br>    *   *   no mention of ARKs?<br>*   jk and dw did first ARK workshop. Was very nice. Donny shared copy of slide deck with call participants |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     |     |
| At arks.org/resources updated current spec link (v.18) from an external link to a PDF hosted onsite; updated current spec to landing page for IETF specs (easier to keep updated) |     | dw: clarify messaging around v.18 being "current" (elaborate on this?) vs e.g. v.36<br><br>jk: agreed we should clarify this. punting for now in favor of existing agenda items. |
| Final discussion of WG [homepage review](https://docs.google.com/document/d/1n5ETS45fHqJefu74vXKLFZhrXm_VmIB7jT2Yk4zR2_E/edit#heading=h.v83orrqv3vnr)<br><br>*   KH: counting ARKs via API vs survey (pros/cons) |     | all present: accept proposed changes (no objections raised) |
| IETF standardization update<br><br>*   ARK as [URN namespace](https://www.iana.org/assignments/urn-namespaces/urn-namespaces.xhtml) ? Doesn't preclude pursuing as separate IETF RFC, eg, DOI is getting a URN namespace<br>    *   should be very easy, doesn't require using urn: in front of ARKs<br>    *   would need to remove spec's discussion of URNs and DOIs (a URN namespace)<br>    *   would need to verify a few char set conflicts<br>*   ARK as API rather than as identifier? ARK as centralized silo rather than as distributed (see GJ's April 10 [email about n2t](https://groups.google.com/g/arka-technical-wg/c/BUzCjGe5xmo/m/xaVkEdVWBgAJ))<br>*   Current ARK draft expires April 20 |     | *   Define a URN [namespaces](https://www.iana.org/assignments/urn-namespaces/urn-namespaces.xhtml)?<br>    *   see e.g. [https://www.iana.org/assignments/urn-formal/doi](https://www.iana.org/assignments/urn-formal/doi)<br>    *   Could help in the form of establishing ark as ours.<br>    *   Easier to gain standardization<br>    *   jk: any harm in pursuing this?<br>    *   gj: can this be seen a bit like pursuing a trademark, eg, w3id?<br>    *   dv: will look into registering arkid at w3id<br><br>*   Current draft spec expires April 20.<br>    *   can’t standardize path elements<br>    *   IETF ok with DOI and Handle Informational RFCs that document how their respective domains work; perhaps we should do the same?<br>*   Should we promote arks.org as a global resolver?<br>    *   benefits to having a scalable model - distribute the resolver<br>    *   decentralized vs centralized?<br>    *   Can we continue to advertise decentralized if we have a centralized resolver? Is this a ‘marketing’ issue?<br>    *   would we be betraying ‘first principles’? eg, ARKs not just another silo<br>    *   this issue came up as a result of trying to gain IETF standardization. |
| ARK spec transition<br><br>\* what to call before and after -- call them? V.I and V.II ? old and new?  <br>\* add those names to new spec, and add section about transition?<br><br>*   blog post [https://arks.org/blog/upcoming-changes-to-the-ark-specification/](https://arks.org/blog/upcoming-changes-to-the-ark-specification/)<br>*   Changes (complete?):<br>    *   NAAN should be preceded by "ark:", as in ark:12345/x7th8, but the the V.I format should also be _accepted_ as valid in perpetuity, ie, no links will break because of the transition<br>    *   NAAN can be 1 or more betanumerics (no length limit mentioned)<br>    *   ARK chars:    =   ~   \*   +   @   \_   $        %   -   .   /  <br>           this removes #, adds ~<br>    *   inflections: add ?info  (with ? and ?? reserved for future use, but undefined; ok to keep using them as you do for now)<br>    *   For received ARKs, implementations must support a minimum length of 255 octets for the string composed of the Base Name plus Qualifier<br>*   Draft Transition Plan<br>    <br>    Overall impact should be minimal. The fewer NAANs you deal with, the easier. Timings T1, T2, ..., T6 to be determined later.<br>    <br>    1\. If you produce ARKs, by time T1 you should produce ark:12345 instead of ark:/12345<br>    <br>    2\. If you produce ARKs but only ever produced new format (ark:/12345) ARKs, by time T2 you should prepare to receive your own ARKs in the old format (because others may unwittingly reformat your ARKs)<br>    <br>    3\. If you receive or resolve ARKs, by time T3 you should accept either ark:12345 or ark:/12345, and plan to do that in perpetuity.<br>    <br>    4\. If you receive or resolve ARKs, by time T4 you should accept ARKs at least as long as 255 octets.<br>    <br>    5\. If you validate ARKs, you should by time T5 make sure your validation is relaxed enough to not reject new format NAANs, ARKs with ~ or #, and Name and Qualifier parts longer than 128 octets.<br>    <br>      <br>    6\. If you receive or resolve ARKs, by time T6 you should recognize ?info and (a) not flag it as an error, (b) return metadata or return something other than 404 (eg, return the object as if no inflection). |     | dv: [arks.org](http://arks.org) might be better for tying the spec to than [n2t.net](http://n2t.net); I see big benefit to name branding,  <br>    with [arks.org](http://arks.org) distributed among different orgs  <br>kh: wordsmithing needed, separating centralized software from the service  <br>gj: spec is squishy wrt global resolution  <br>dv: should be trivially obvious where to go to find the resource,  <br>     eg, any local resolver system could to  <br>    see my notes [https://hackmd.io/dor0GlmTSEuLYouGJ6TIjA?view](https://hackmd.io/dor0GlmTSEuLYouGJ6TIjA?view)  <br>    comments welcome<br><br>*   ARK spec transition<br><br>*   Initial plan is T1-T6, each representing a set of implementation requirements.<br>*   Can’t really require adherence to the newer standards.<br>*   Perhaps we can reach out to the contact info in the NAAN registry to at least let them know of the changes and propose upgrading.<br><br>gj: for transition, we don't have levers to force people to do this  <br>jk: maybe use social pressure, list of reference ARKs that should work  <br>dv: we could use contact info in the NAAN registry to reach out<br><br>*   Chat log:<br>    <br>    *   doi is listed at [https://www.iana.org/assignments/urn-namespaces/urn-namespaces.xhtml](https://www.iana.org/assignments/urn-namespaces/urn-namespaces.xhtml)<br>    *   [https://github.com/perma-id/w3id.org](https://github.com/perma-id/w3id.org)<br>    *   [https://github.com/perma-id/w3id.org/tree/master/ARK](https://github.com/perma-id/w3id.org/tree/master/ARK)<br>    <br>    *   https://github.com/perma-id/w3id.org/tree/master/n2t<br>    <br>    *   [https://hackmd.io/dor0GlmTSEuLYouGJ6TIjA?view](https://hackmd.io/dor0GlmTSEuLYouGJ6TIjA?view)<br>    *   (Dave is contact for [w3id.org/n2t](http://w3id.org/n2t) above) |

Action items
------------

- [x] John Kunze accept homepage changes and update lyrasis wiki
- [x] John Kunze create [googledoc transition plan](https://docs.google.com/document/d/1aFgujlL5yE3ZUORXRRkDTDNrlZEQU69lOU6Gc3wlyt4/edit?usp=sharing) and invite comments; need to clarify what existing/current spec means
- [x] Dave Vieglais will look into registering arkid at w3id

Comments:
---------

|     |
| --- |
| Could `ark`  (also) be a [DID method](https://w3c.github.io/did-spec-registries/#did-methods)?<br><br>![](images/icons/contenttypes/comment_16.png) Posted by dwinston at Apr 11, 2023 09:56 |
| I  don't know. What would that look like?<br><br>![](images/icons/contenttypes/comment_16.png) Posted by jak at Apr 11, 2023 10:06 |
| I think it would look like a row in [this table](https://w3c.github.io/did-spec-registries/#did-methods) via a [pull request with a JSON file](https://github.com/w3c/did-spec-registries#adding-a-did-method-to-this-registry). Details on the format of a DID method specification are [here](https://www.w3.org/TR/did-core/#methods).<br><br>So, I think an ARK [DID](https://www.w3.org/TR/did-core/#dfn-decentralized-identifiers) would look like e.g. did:ark:57802 (i.e. an ARK DID would map to an ARK NAAN) and a [DID URL](https://www.w3.org/TR/did-core/#dfn-did-urls) would look like did:ark:57802/dw0/agu (i.e. a "full" ARK).<br><br>![](images/icons/contenttypes/comment_16.png) Posted by dwinston at Apr 11, 2023 11:20 |