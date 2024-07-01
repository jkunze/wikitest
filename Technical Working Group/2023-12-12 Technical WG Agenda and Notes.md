\---

confluence-id: 315719689

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-12-12 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Dec 15, 2023

Date
----

12 Dec 2023

Attendees
---------

*   Curtis Mirci, Roxana Maurer, Tom Creighton, Karen Hanson, Donny Winston, John Kunze

Goals
-----

ARK Alliance Infrastructure topics

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | Nov 9 CDL told us that arks.org was converted from Wordpress to github pages on Nov 8, and that the n2t.net resolver would be converted Nov 27; we don't know if that's happened |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     | summary of events since last time; renewed call to add events |
| ARK spec transition update<br><br>Proposed stakeholders to approach<br><br>*   FamilySearch, Portico, BnF, Smithsonian, CDL/EZID, IA, Frick<br>*   Code bases: OJS plugin, arklet, arknoid, EZID<br><br>Approach with questionnaire?<br><br>*   Do you currently support resolution of both ark: and ark:/ ?<br>*   Would you be willing to go through this spec transition together with the ARKA Tech WG? |     | tc: who at smithsonian?jk: ricc ferrante  <br>tc: we could approach HathiTrust and DPC as stakeholders in their role as service providers  <br>rm: as a board member, I can say that DPC doesn't endorse any software, but it may be useful that they do things like TechWatch reports  <br>rm: maybe approach ARKetype as a stakeholder?  <br>jk: maybe an inducement to stakeholders to be able to influence transition timing |
| Understanding and monitoring ARK Alliance (ARKA) infrastructure.<br><br>*   Since Nov 8, the arks.org site is driven from master files at github, and we urgently need to share understanding and permissions more broadly<br>*   We used to have 20 people, mostly members of ARKA working groups, with write access, and currently there is only one such person with write access<br>*   There are many deferred maintenance task, including blog posts and a deadline for moving documents from the lyrasis wiki to arks.org |     | dw: yes we need better communication about N2T  <br>tc: what about opening all the source?  <br>dw: open governance isn't the same as open source  <br>dw: here's a note from the creator of the open-source Clojure programming language on this issue: [https://gist.github.com/richhickey/1563cddea1002958f96e7ba9519972d9](https://gist.github.com/richhickey/1563cddea1002958f96e7ba9519972d9)  <br>tc: need more visibility into what's going on with the infrastructure  <br>dw: ok to have a standing agenda item about infrastructure status with liaison that has read access to the ARKA issues list  <br>jk: maybe emailed monthly report?<br><br>kh: I'm able to help with text conversion of lyrasis wiki |
| The [n2t.net](http://n2t.net) resolver either already has or will soon transition to a new resolution regime<br><br>*   ARKA needs tighter communication about infrastructure status, especially large changes such as this<br>*   Propose a new standing agenda item at every ARK Tech meeting check in on current infrastructure status and envisioned changes |     | dw: web frameworks such as React are open-source, but it’s generally understood that they're not community-governed, i.e. Facebook/Meta is the arbiter of changes. So CDL could still be such an arbiter for an open-source (transparently inspectable) codebase. A note from the creator of the open-source Clojure programming language on this issue: [https://gist.github.com/richhickey/1563cddea1002958f96e7ba9519972d9](https://gist.github.com/richhickey/1563cddea1002958f96e7ba9519972d9) |
| **Understanding the new github-based arks.org**<br><br>(from Dave Vieglais)<br><br>The content on [arks.org](http://arks.org/) comes from the [https://github.com/arks-org/arks.github.io](https://github.com/arks-org/arks.github.io) repository.<br><br>Deployment of changes to [arks.org](http://arks.org/) is not automatic, but the manual process is straight forward with a git pull from the main branch of the [arks.github.io](http://arks.github.io/) repository, followed by a build on the [arks.org](http://arks.org/) server.<br><br>As far as managing what goes into the main branch, general best practices for git management should be followed. So develop on a separate branch (within the repo or fork a copy) and make a PR for merging into the main branch. Keep in mind that the main branch should always be representing what is to be shown on [arks.org](http://arks.org/).<br><br>Rendering of drafts is best done locally by the editor. Currently the main branch is rendered to [https://arks-org.github.io/arks.github.io/](https://arks-org.github.io/arks.github.io/) with a GitHub action, so that can be used as kind of a release preview before being pulled to [arks.org](http://arks.org/).<br><br>This entire process will likely be modified to deploy automatically to [arks.org](http://arks.org/) when changes are made on the main branch or perhaps when a tag is made.<br><br>With respect to the Lyrasis Confluence wiki, there are tools that enable conversion from there to Markdown (e.g. [https://github.com/sjones4/confluence-to-github](https://github.com/sjones4/confluence-to-github) ), and certainly at a minimum a confluence export should be done to ensure content is preserved.<br><br>I would suggest keeping the FAQ and other content from Lyrasis in a GitHub wiki, perhaps in the arks-org/[arks.github.io](http://arks.github.io/) repository at [https://github.com/arks-org/arks.github.io/wiki](https://github.com/arks-org/arks.github.io/wiki) (GH wiki content lives separately from the main repository, though can be managed just like a Git repo). |     | dw: so (1) suggest change, (2) merge to main branch (needs write access), (3) rebuild [https://arks-org.github.io/arks.github.io/](https://arks-org.github.io/arks.github.io/) preview (happens automatically via GitHub Action), (4) pull latest of main branch to remote server that hosts [arks.org](http://arks.org) (needs login/write access to server). ?<br><br>dw: issue: there is no publicly visible GH wiki at [https://github.com/arks-org/arks.github.io](https://github.com/arks-org/arks.github.io) (i.e. [https://github.com/arks-org/arks.github.io/wiki](https://github.com/arks-org/arks.github.io/wiki)). Is there one visible to repository _collaborators_?  <br>jk: none visible yet but I think we just have to create it |

Action items
------------

- [ ] next time, follow up on wikidata topics (Bertrand)
- [ ] stakeholder list start: ask HT and ARKetype