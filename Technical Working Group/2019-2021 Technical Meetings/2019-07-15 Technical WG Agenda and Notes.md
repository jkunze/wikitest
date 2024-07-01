\---

confluence-id: 128024640

confluence-space: %%CONFLUENCE-SPACE%%

\---

2019-07-15 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified by Tom Creighton on Jul 15, 2019

Date
----

12 Jul 2019

Attendees
---------

*   John Kunze
    
*   Roxana Maurer
*   Sheila Morrissey
    
*   Bertrand Caron
*   Greg Janée
*   Tom Creighton
*   Curtis Mirci

Goals
-----

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | An Argentine group interested in using ARKs has asked about handling ISSN numbers as NaaNs. |     | The ISSN serial number standard is controlled by [https://www.issn.org](https://www.issn.org). The idea is that we could somehow automatically generate NaaNs based on an ISSN. Discussion points included the following:<br><br>*   Every ISSN auto register as a NaaN.<br>*   Perhaps start with some letter such as ’S’<br>*   Declare this as a reserved pattern.<br>*   John suggests perhaps this pattern would be an administrative pattern, not part of the standard.<br>*   Discussed various groups doing similar name space allocations. BNF, Luxembourg, FamilySearch, etc. Some great concerns about how to go forward.<br>*   Many open questions. We are just beginning to think about this. |
|     | Proposed: suppress '?' inflection (let it be optional), leaving just the '??' inflection<br><br>*   as before, '??' requests kernel elements plus any persistence statement<br>*   '??' easier to implement than '?'<br>*   '?' may be supported by older implementations (briefer record)<br>*      ... or should '?' be made identical to '??'  ? |     | This point generated considerable discussion among the group members. All agreed that folding the use of the single '?' into the double ('??') makes sense. However, there are still some concerns. Specific discussion points were:<br><br>*   ? is often ignored by software<br>*   ?? will result in a query parameter with just ?<br>*   Perhaps change the standard to ??<br>*   Perhaps inflections could make use of meta characters outside the current spec. Such as ‘!’.<br>*   There is some concern about using a query string that does not include the value. Tom will try to figure out what conventions are supported by reverse proxies and HTTP servers such as HA Proxy, NGINX, Jetty… |
|     | are we ready for next review phase with arks-forum? |     | The next version of the specification did not get published due to the IETF black out period. |

Action items
------------

- [ ] Tom will research handling of query parameters that have no explicit value (eg. ...??) by HTTP servers and reverse proxies.