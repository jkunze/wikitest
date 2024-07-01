\---

confluence-id: 185991381

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-04-13 NAAN Registry WG Agenda and Notes
============================================

Created by John Kunze, last modified on Apr 13, 2020

Date
----

13 Apr 2020

Attendees
---------

*   John Kunze
    
*   Brian McBride
*   Bertrand Caron
    
*   Maria Gould
*   Julien Antoine Raemy

Goals
-----

*   Second meeting: proposal to register shoulders, Slack integration

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | Proposed: expand the role of NAAN registry to record not only per-institutional NAANs, _but also shoulders under one of the four non-institutional NAANs_<br><br>*   Reminder a shoulder is an extension to a NAAN that subdivides a NAAN namespace, eg, 12345/b3 and 12345/b4 are two sub-namespaces under the 12345 namespace<br>*   99999 test/fake ARKs, meant to look "wrong" (similar to seeing 9999 in a date field) and to not surprise people for not resolving<br>    *   usually generated, usually resolvable for a short period of time<br>    *   EZID.cdlib.org currently has exclusive access to several shoulders under 99999<br>    *   other services (eg, INCIPIT) should be able to reserve shoulders in order to implement test/fake ARKs under 99999, but there is no formal way to prevent collisions if they started to do so<br>    *   global resolution via n2t.net (for those that choose it), in current practice, is driven at the NAAN level, eg, 99999 ARKs are all assumed to originate with EZID (not a good long-term assumption), usually from the 99999/fk4 shoulder. Maybe  99999/fx4 could be for INCIPIT?<br>*   12345 example ARKs, similar to test/fake ARKs, but meant to look less "wrong"<br>    *   eg, "my own NAAN might look like that if it weren't so regular"<br>    *   meant for documentation, sometimes resolvable (possibly for a long time)<br>*   99152 vocabulary terms, eg, metadata terms<br>    *   meant for long-term access, shared across services and institutions<br>    *   EZID.cdlib.org and YAMZ.net already have exclusive access to different shoulders under 99152<br>*   99166 agents (people, groups, institutions)<br>    *   [EZID.cdlib.org](http://EZID.cdlib.org) and SNACC already have exclusive access to different shoulders under 99152<br><br>The question of registering shoulders (outside of EZID) has come up before, and with INCIPIT is a bit more pressing. As with NAANs, the purpose is to prevent name assignment collisions between institutions. One alternative is to create a new special-purpose NAAN (eg, 99998, 99997, ...) for each institution that wants to do test ARKs, but that would dilute the recognizability of test ARKs (recipients would have to memorize an ever growing list of NAANs) and it would clutter the NAAN namespace.<br><br>An advantage of beginning to register shoulders _just for these 4 special-case NAANs_ is that it would formalize existing practice and make it more transparent. It would also provide a framework for addressing a couple anomalies in EZID (for 99152 and 99166). There are other existing practices for assigning shoulders under non-shared NAANs (eg, BnF and EZID practices) that would not be affected by this change. |     | BC: BnF has some plans and interest in this topid  <br>MG: moving users in and out of a service like ezid has its challenges, and it seems easier administratively to not share NAANs  <br>MG: recommend taking a step back to evaluate options, eg, multiple NAANs vs shared shoulders<br><br>General agreement that a clearer understanding of the different options would be good, including the technical, admin, and user impact of each option  <br>JR: incipit is ok with either option<br><br>ACTION: jak will write up options  <br>ACTION: jak will send query to group about who may have webhooks skills to help automate NAAN registration |
|     | Slack integration? |     |     |

Action items
------------