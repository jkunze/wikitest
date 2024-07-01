\---

confluence-id: 131532428

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-08-22 Outreach WG Agenda and Notes
=======================================

Created by John Kunze, last modified on Aug 22, 2019

Date
----

22 Aug 2019

Attendees
---------

*   John Kunze
    
*   Peter Sachs Collopy
    
*   Maria Gould
*   Kurt Ewoldsen
*   Tracy Seneca

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | Announcements<br><br>*   ISSNs as NAANs? or NAANs that look like ISSNs<br><br>  <br><br>  <br><br>  <br><br>  <br><br>  <br><br>  <br><br>  <br><br>*   ids for physical samples<br><br>  <br><br>  <br><br>*   ARK as URI scheme? |     | John Kunze: A group in Argentina is interested in using ISSNs as NAANs. They're typically different lengths of digits, but the technical group is making this flexible anyway. In that group, there was some concern that ISSNs don't refer to stable institutions, which was the original intent with NAANs. More recently they've been given out to any significant minter of stable identifiers anyway, regardless of scale; they could be given to a single research group, for example, not necessarily an entire university or other organization. Individual publications can have NAANs in that context. So there could be NAANs that match the ISSNs assigned to the same publishing project, but there won't be an official alliance between the ARK and ISSN organizations. It would be a convenience for the NAAN portion of ARKs that refer to articles to match the ISSN for the journal.<br><br>Peter Sachs Collopy: If the requirement to get a NAAN isn't being a recognized institution, is there a requirement? Are projects denied NAANs?<br><br>John Kunze: We ask for a commitment to persistence, but there isn't a formal set of criteria for eligibility.<br><br>Tracy Seneca: We run Open Journal Systems journals, and it doesn't make sense to associate articles in them with our institutional NAAN, because authors usually aren't affiliated with our institution and because journals sometimes change hands. With this approach, the NAAN could go from one institution to another with the journal.<br><br>John Kunze: I recently attended a meeting on identifiers of physical samples in biodiversity, geology, and archeology. The Smithsonian is assigning 100,000,000 ARKs to their collection objects. This is a form of linked data, connecting the object itself to data about it.<br><br>Tracy Seneca: It would be great to have a writeup on the use of ARKs for physical objects, since that's counterintuitive when one is first learning about ARKs.<br><br>John Kunze: The technical working group is discussing proposing the ARK as a URI scheme. This has seemed tricky in the past since Handle and DOI have failed at this.<br><br>  <br><br>Other announcement<br><br>Maria Gould: Google Translate was pleasantly surprising for translating FAQs. It would be an adequate starting point for translating to Spanish. We'll need to check specialized vocabulary, but it's mostly legible. |
|     | [draft wikipedia article outline](https://wiki.duraspace.org/display/ARKs/Draft+ARK+ToC+for+Wikipedia) ← link<br><br>**Proposed Wikipedia ToC**<br><br>*   ARK Features<br>*   Structure and syntax<br>*   Resolvers and other tools<br>*   Comparison with other identifier schemes<br>*   History and administration<br>*   See also<br>*   Notes and references<br>*   External links | Tracy | Tracy Seneca: I surveyed what similar documents, including Wikipedia pages for other identifier schemes and introductory documentation for ARKs, cover in terms of sections. The ARK Wikipedia article should have a broader audience than other introductions, which are typically for those who are considering adopting ARKs. One key thing to cover in an introductory paragraph is the user community, which appears to be predominantly cultural heritage institutions with digital content. Did we want to include a structure and syntax section?<br><br>Peter Sachs Collopy: I think it's important that such a section not take over the article, as people will come to it to understand what ARKs are and their context, not how to work with them. But incorporating that into an explanation of why it works how it does, like on the DOI Wikipedia page, makes sense to me.<br><br>Tracy Seneca: What order should the pieces go in?<br><br>Peter Sachs Collopy: I'm used to history being the first substantive section on Wikipedia pages, but ideally the introduction should orient people well enough that they can skip to any section without being confused.<br><br>Tracy Seneca: The opening paragraph could include at least a sentence that touches on each of the following sections.<br><br>John Kunze: We can do composing in Google Docs from here, and then migrate into Wikipedia once we have a version we're happy with.<br><br>Peter Sachs Collopy: We can just use plain text in Google Docs with [Wikitext markup](https://en.wikipedia.org/wiki/Help:Cheatsheet), then copy and paste that into Wikipedia.<br><br>Maria Gould: There's a [Wikipedia sandbox](https://en.wikipedia.org/wiki/Wikipedia:Sandbox) to test pasting into.<br><br>Tracy Seneca: We should write the opening paragraph last. |

Action items
------------

- [ ] John Kunze will draft the Wikipedia article sections History and Comparison with Other Identifiers.
- [ ] Tracy Seneca will draft the Features section.
- [ ] Maria Gould will collect external links.
- [ ] Peter Sachs Collopy will draft the Structure and Syntax section.
- [ ] Kurt Ewoldsen will draft the section on Resolvers and Other Tools.