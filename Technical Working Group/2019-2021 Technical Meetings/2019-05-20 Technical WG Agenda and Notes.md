\---

confluence-id: 117735457

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-05-20 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on May 30, 2019

Date
----

20 May 2019

Attendees
---------

*   John Kunze
    
*   Sheila Morrissey
    
*   Greg Janée
*   Mark Phillips  
*   Roxana Maurer  
*   Tom Creighton

Goals
-----

*   first review of spec changes: [https://www.ietf.org/rfcdiff?url2=draft-kunze-ark-19](https://www.ietf.org/rfcdiff?url2=draft-kunze-ark-19)

General Comments

*   We will begin discussion on these today, but given regrets, will not rush to vote on these
*   Sustainability Group working on survey to find what potential supporters would prioritize, and what support they would be able to give;
*   John has been updating FAQ, Bertrand has been translating; Roxana raised question as to when FAQ should reflect suggested changes in draft?  Since WG has not finished reviewing/approving changes, perhaps not now, but when we change draft, should change FAQ to match.   
*   Greg raised question of outreach on (all) WG activities; should we suggest quarterly summary from each WG for Outreach WG to send out?
*   Move through draft
    *   new co-author
    *   some boilerplate changes 
    *   new domain name arks.org as ARK Maintenance agency; what we expect to see there
    *   More labels added for ARK anatomy
        *   Core Immutable Identity (everything but the resolver service)
        *   Resolver service
        *   Base object name
    *   Clarify difference between resolver service and name
    *   Perhaps consider version syntax and inflections under larger heading of eg. REST API;
    *   Also helpful (FAQ, technical note) on URLs changing (conversion path, upgrade path) what should happen with older version- 302? Other?

  

IIIF - Implementation Notes - [https://iiif.io/api/image/2.0/#appendices](https://iiif.io/api/image/2.0/#appendices)

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | remove #, add ~ |     |     |
|     | ark:/ becomes ark:\[/\] |     | (in many places)  / now optional <br><br>Do we need some sort of guidance/advice on "accepting" / while transitioning; Tom raises general question of content negotiation:  should we indicate version of arks we are transmitting in syntax, rather than depend on content negotiation <br><br>Greg: should we call this deprecated, or indicate old form transitional and indicate how to transition -<br><br>John we have to make explicit support for older form, look for correct language on this<br><br>Minters SHOULD not use slash;<br><br>Resolvers MUST handle /; <br><br>Mark - also should express whether current users should change URLs; <br><br>JOHN where does upgrade path info go?  Separate document?  Appendix? <br><br>Mark will add examples from IIIF |
|     | "resolvers to check for inflections before normalizing" |     | TBD |
|     | more flexible NAAN |     | Same digits as NOID  (section 2.3); would enable mapping other id schemes without conflict in future |
|     | '?' inflection explicitly includes possibility of HTML with embedded metadata |     | TBD |
|     | Max length restriction removed |     | see new text |
|     | Extra: new co-author and IETF boilerplate changes |     |     |
|     | Extra: new anatomical definitions -- Resolver Service, Base Object Name, Core Immutable Identity |     | TBD |
|     | Extra: mention arks.org as Maintenance Agency (not AITO) |     | TBD |
|     | New proposed change: "http:" to become "https:" |     | Reflects change in boilerplate; but also think good idea for arks: AGREED<br><br>_John: deferred to make early important diffs less noisy_ |
|     | New proposed change: NMAH to be renamed NMA (simpler to teach about while still allowing a port designation) |     | John will add to next draft<br><br>_John: deferred to make early important diffs less noisy_ |
|     | Discuss: what about making '?' the same as '??' for easier implementation |     | Possibly related to issue of resolving version |
|     | Identifier length |     | Discussed in expert group discussion last year;  Greg wondering if this is best practice (arbitrary length), plus pragmatic restrictions (db fields);  Challenge for receiving systems would be burden;  Would more conservative approach be better: warning about maximum length (eg anything larger than 255)? Especially since we are transition from hard limit of 128 to no limit - SO lets try new working reflecting current common RDB limits |

Action items
------------

- [x] John will send out draft survey for review
- [ ] All: review FAQ
- [ ] John changes http:// to https:// in all examples in draft 
- [ ] All please comment on other sections/changes as you are able in next day
- [ ] John will put out new draft based on discussion