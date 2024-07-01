\---

confluence-id: 131531442

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-08-19 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Aug 20, 2019

Date
----

19 Aug 2019

Attendees
---------

*   John Kunze
    
*   Sheila Morrissey
    
*   Greg Janée
*   Curtis Mirci

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | Announcements |     | John has been  meeting with ISGN folks also concerned about PIDs, in their case for physical objects (Geographic, astronomical, archaeological; possible cxn to ARKS |
|     | ISSN as NAAN, part 2<br><br>NAANs originally were for institutions (eg, National Library, Portico, University), but over time, CDL loosened the guidelines (eg, University Library instead of an entire University). With EZID, CDL began to follow  the lead of the publishers and DataCite, assigning ARK NAANs the same way that DOI Prefixes were assigned (eg, departments in organizations, laboratories, virtual organizations such as consortia), and even to individual journals.<br><br>Broadly, NAANs (like Prefixes), were given to groups that asked and could plausibly claim to be significant, stable sources of identifiers. Add to that, that some organizations asked for more than one NAAN (Ithaka/Portico). <br><br>Still undefined for NAANs: what happens when (a) an org goes away or merges, (b) another org asks/offers to take over a frozen namespace, (c) wants to change its NAAN?<br><br>How often would (c) happen and how should we respond? In perspective, if an organization asks for an 8-digit NAAN (whether or not based on an ISSN), how do we respond? Are NAANs-as-ISSNs more or less likely to change than other NAANs? Could we not contain ISSN instability with the same rule that contains NAAN (regardless of origin) instability? | John | John: Review of last week's issues with ISSN as NAAN.  Common notion of what NAAN is has evolved somewhat (see Item column).  Analog to NAAN in DOI was DOI prefix.  Increasingly gave NAANs at finer grains (library, department, laboratory within institution); publishers now attaching DOI to journal.  (Evolved in EZID practice).  Never came up with policy if org wants to change NAAN, merges with another organization.<br><br>eg NAAN for UCSF library; new NAAN for 15-year project in library with 14 million IDs, industry documents library (public health) - <br><br>Greg: NAANs are identifiers, long-term mgt issues apply to them as well; unstated policy we are assigning them to point where IDs are minted (so you - minter- don't have to co-ordinate) – But it is (assumed) responsibility of NAAN owner to manage entire namespace - eg NaaN sub-registrar that manages namespace - but that is not in fact what is happening<br><br>Curtis: originally thought - oh just an identifier -we are not getting message across about how these ids are supposed to be persistent<br><br>John:  FAQ about deletions, try to be open about world as it is rather than world as it should be - same problems with DOIs, handles.  "Aspirationally" persistent - can keep them private - deleting not as issue - but once it's published - you have obligations<br><br>Curtis - "just another way to link to it" - not really thinking of it as persistent ID<br><br>Sheila:  persistence after project money gone, etc - do we need to make NAAN mgt more heavy-weight to be clear about succession obligations, what is commitment to persistence<br><br>Greg: Is it reasonable to ask for successor group? Do we ask commitment?<br><br>John EZID make it part of SLA; objects you are naming are in a stable repository <br><br>Sheila perhaps this needs a discussion with other WGs<br><br>John what is a simple succession plan? eg put copy in IA, pass on bindings to N2T<br><br>Sheila question on what complications (expenses) entailed in managing "sub-schemes" with semantics <br><br>John:  allow request for specific NaaN; just check that it's not already taken<br><br>Greg:  "vanity NAANs"  <br><br>John still have our guidelines<br><br>Sheila: we have to stipulate NO semantics to NAAN number "any resemblance to journal ID living or dead purely a coincidence" |
|     | ARK as URN or URI<br><br>_On Tue, Aug 13, 2019 at 10:44 PM Mario Xerxes Castelán Castro <[mario.xerxes.castelan.castro@gmail.com](mailto:mario.xerxes.castelan.castro@gmail.com)\> wrote:_<br><br>_Hello. Are there plans to register “ark” as an URI scheme or under the existing “urn” scheme? If there are not, I suggest that it is considered. For some purposes where URI are expected it would make sense to be able to use the bare ARK, for example: XML namespaces as in <[ark:/12345/example](http://ark/12345/example)\>. That would give the full persistence assurance that ARKs have, not limited by any particular resolver as is the case if one uses an ARK with NMAH like <[https://n2t.net/ark:/12345/example](https://n2t.net/ark:/12345/example)\>_<br><br>Response:<br><br>Registering "ark" as a URI scheme or URN namespace has been considered in the distant past, and it may be worth considering again. I'd be interested in hearing feedback about this.<br><br>Here are some considerations. As for registering "ark" as a URN namespace, I'm not sure what it would accomplish other than to permit expressing ARKs in the form,<br><br>    1. urn:[ark:/12345/67890](http://ark/12345/67890)<br><br>in addition to the usual form,<br><br>    2. [https://n2t.net/ark:/12345/67890](https://n2t.net/ark:/12345/67890)<br><br>While the urn form (1) is shorter than the usual form (2), it can only be made resolvable by using an even longer form, such as,<br><br>    3. [https://n2t.net/urn:ark:/12345/67890](https://n2t.net/urn:ark:/12345/67890)<br><br>Regarding registering "ark" as a URI scheme, what would an ARK look like and where would resolution take place? Would it be this?<br><br>Form:  <br>    [ark:/12345/67890](http://ark/12345/67890)<br><br>Implicit resolution via:  <br>    [https://n2t.net/ark:/12345/67890](https://n2t.net/ark:/12345/67890)<br><br>It's a nice idea, but (a) does it prevent de-centralization (a feature of ARKs) and (b) given that this sort of thing was tried unsuccessfully in the past with DOIs and Handles, what argument would make ARKs successful here? |     | URN advantage:  publicity<br><br>Handles, DOI not successful registering as URI<br><br>Advantage- consistency for inflections |
|     | alternatives to google for arks-forum<br><br>_On Tue, Aug 13, 2019 at 10:44 PM Mario Xerxes Castelán Castro <[mario.xerxes.castelan.castro@gmail.com](mailto:mario.xerxes.castelan.castro@gmail.com)\> wrote:_<br><br>_Incidentally, I did not find an option to subscribe to this group using an existing e-mail address, so I had to register one with Google. I find that very inconvenient as I would rather using Google services as much as feasible._ |     | Does DuraSpace have a listserv? Or Lyrasis? |
|     | Next Calls:  9.02 is Labor Day; 9.16 is iPRES2019 | Sheila | Cancel 9.02; ask availability for 9.16<br><br>Perhaps 9.09 would be good replacement date |

Action items
------------

- [x] Sheila Morrisseycheck with DuraSpace/Lyrasis to see if we can setup listserv?  Answer: no
- [ ] All - think about ARK as URI or URN; reply on ARKS forum if you have thoughts
- [x] John Kunze email WG about next meeting dates