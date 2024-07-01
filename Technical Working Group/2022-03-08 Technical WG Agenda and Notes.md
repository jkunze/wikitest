\---

confluence-id: 230822046

confluence-space: %%CONFLUENCE-SPACE%%

\---

2022-03-08 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Mar 14, 2022

Date
----

08 Mar 2022

Attendees
---------

*   Tom Creighton, Bertrand Caron, Mark Phillips, Curtis Mirci, Karen Hanson, Roxana Maurer, Greg Janée

Goals
-----

Selection of chair/vice-chair, RFC update, new spec transition plan

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | texas conference moving ahead, no publicity yet |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     |     |
| Any news items we should blog about? |     |     |
| Selection of chair and vice-chair (see Feb 25 email request from new Advisory Group chair). |     | mp: need formalize the roles of chair and vice-chair  <br>mp: verify charter, people, roles,  <br>tc: anyone not here should be considered as volunteering   <br>mp: vice chair is kind of a backstop as default if the chair is can't make it  <br> -  organizing meetings, text for action items,  <br> -  witness the process of organizing  <br> -  cushion for when the chair has to step away  <br>jk: ask Dave to be vice chair?  <br>mp: ok, through the end of the calendar year  <br>tc: agreed |
| Update on preliminary discussion with the RFC Independent Stream Editor<br><br>*   [BCP (Best Current Practice) 190](https://www.rfc-editor.org/rfc/rfc8820.html) (RFC 8820)<br>*   Conflict with reserving path "prefix"<br>*   Conflict with reserving query string<br><br>_On 04.03.22 06:56, Independent Submissions Editor (Eliot Lear) wrote:The question really is... is an web server or client supposed tobehave in any special way when they see ark: somewhere buried in aURL?  This is precisely what .well-known was meant to protect against....I want to go into more detail here.  The point of BCP 190 is to preserve_  <br>_namespaces to the owner of an origin.  That is- you don't get to_  <br>_structure them if you are not the owner.  That includes queries.  The_  <br>_exception we have for that is .well-known.  This is why I am very_  <br>_concerned about the current state of your draft._<br><br>Some initial thoughts (jak's). This means that the IETF might not allow example.org/ark:12345/67890 and the ?info inflection unless they were expressed as something like<br><br>     example.org/.well-known/ark/12345/67890       and<br><br>     example.org/.well-known/ark-info/12345/67890<br><br>I (jak) don't _think_ it means that one site, eg, n2t.net, couldn't recommend publishing as<br><br>     n2t.net/ark:12345/67890<br><br>and letting it redirect to local services that use the .well-known/ark... convention. |     | kh: about the feedback: would it help to separate the resolver piece from the syntax spec?  <br>gj: can see the value in separating, along lines of how handle and doi did it,  <br>    eg, 1. syntax and structure, 2. resolution, 3. metadata  <br>tc: yes  <br>gj: doi's and handles are uri compliant and have structure -- how do they do it?  <br>jk: because they're rooted at one domain (one origin), as opposed to suggesting a path convention for all origins to do it  <br>tc: maybe it could be modeled on how n2t does it, as long as it's not mandated<br><br>rm: if we in Luxembourg don't want to use n2t, do we have to use .well-known?  <br>jk: possibly, if the ARK spec continues to require a path convention<br><br>kh: I second the idea to have a spec describing specifically what [n2t.net](http://n2t.net) does  <br>cm: two documents is less convenient, but maybe necessary |
| New spec transition planning<br><br>*   [New spec blog post draft](https://docs.google.com/document/d/11xce6G9rFG4anJdVH77FnXGluof3NQnfbXAddYTskHY/edit) – go ahead anyway, or talk about new spec transition independent of the RFC process? |     | jk: ok to separate RFC from spec transition?  <br>tc: seems prudent  <br>rm: yes |

Action items
------------