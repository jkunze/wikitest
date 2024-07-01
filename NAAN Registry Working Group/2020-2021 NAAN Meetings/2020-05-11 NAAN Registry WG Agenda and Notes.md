\---

confluence-id: 187172437

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-05-11 NAAN Registry WG Agenda and Notes
============================================

Created by John Kunze, last modified on Oct 30, 2020

Date
----

11 May 2020

Attendees
---------

*   John Kunze
    
*   Brian McBride
*   Julien Antoine Raemy
*   Maria Gould
*   Bertrand Caron
*   aurélien conraux

Goals
-----

*   How to support/permit test ARKs
*   First draft policy statement

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | N2T-based test ARKs for non-EZID users<br><br>This is a much narrower version of the proposal I brought in last month, which was to expand the role of NAAN registry to record shoulders under the four non-institutional NAANs. We need agreement on how INCIPIT might proceed with N2T-based test ARKs that do not conflict with EZID test ARKs. A major benefit of the proposal would be to protect exclusive "test" shoulder access rights of both EZID and INCIPIT.<br><br>Proposed: With its oversight role for the NAAN namespace, this group agrees to reserve, under the 99999 NAAN,<br><br>*   1 shoulder for exclusive use of the INCIPIT service<br>*   1-3 "historical" shoulders for exclusive use of the EZID service (uses for testing longer than 2 weeks)<br><br>Some discussion:<br><br>1.  A 99999 NAAN in ARKs found in the wild signifies a status of "test".<br>2.  No organization owns or was meant to own the 99999 NAAN.<br>3.  Historically, EZID has used 2 shoulders under the 99999 NAAN, taking advantage of these portions of the public/common space as if it had exclusive rights to them. This proposal would formally recognize those rights in the future.<br>4.  This proposal would also grant similar rights to a test shoulder for INCIPIT.<br><br>The current proposal has no impact on the NAAN registry. The test shoulders reserved in this way would be recorded for now in a separate file. | John | *   Important to provide the community with the ability to use a test ARKs under the 99999 NAAN  <br>    MG: opportunity to update docs about test NAAN about how to prevent conflicts  <br>    BC: assumed CDL owned 99999, which is wrong  <br>    MG: there is a need to define an admin framework around reserving shoulders under 99999; need to clarify this  <br>    and think about how to keep it lightweight<br>*   It is unknown if the 99999 NAAN is used outside of EZID service users<br>*   Some users understand that the 99999 NAAN is owned by CDL<br>*   Julien - looking to move forward now with the understanding they may have to amend their work in the future<br>*   2-3 requests over the past 20 years for test arks using the 99999 NAAN<br>*   Brian: what about expiration of test ARKs?  <br>    JK: that's really an N2T problem, based on policy that has never been stipulated by the ARK scheme; might be good to let this alone unless/until we have to deal with it  <br>    Brian: why not have a separate shoulder registry for now  <br>    JK: I will start one for the currently reserved test shoulders  <br>    Bertrand: like Roxana said in the Tech WG, how about registering for a NAAN (12345) automatically<br>*   Suggestion: When you register for a NAAN, there is implicit assignment that your test shoulder would be 99999/Your NAAN; JK will write this up |
|     | First draft policy statement on NAAN assignment and update.<br><br>I pulled some text out of the github repo's [README.md](https://github.com/jkunze/naan_master/blob/master/README.md) file to create a new [Policy.md](https://github.com/jkunze/naan_master/blob/master/Policy.md) file. The biggest change was to add a small section on update policy:<br><br>_Update policy for NAAN curators is mostly about doing one's best to verify that the request is coming from a legitimate source that is authorized to represent the original NAAN-holding organization._<br><br>_The biggest risk is a change to the organizational URL (resolver) for ARKs with that NAAN that rely on N2T, since such a change will affect their resolution. Things to watch out for are (a) mistaken requests and (b) spurious attempts to misdirect someone's ARKs (never happened yet). Things are not always obvious, for example, a request came in for a new organizational URL that, by itself, returned a 404 error; while it seemed like a mistake, and it still returns a 404 error, it is nonetheless a valid base URL for a local ARK resolver._ | John | *   Group needs to work on constructing policy documentation together.<br>*   Bertrand Caron sent out message to archive communities in France to have them update their records in the NAAN Registry (which updates N2T) |

Action items
------------

- [x] Clarify and add documentation pertaining to the "reserved" status of 99999 NAAN John Kunze
- [x] Create document as stub registry of current test shoulders under 99999 NAAN John Kunze
- [x] Document the test shoulders assigned to the 99999 NAAN and how to use it to avoid conflicts John Kunze 
- [x] John Kunze Will add Julien Antoine Raemy Maria Gould aurélien conraux to the github repository
- [x] aurélien conraux Will reach out to Archives départementales de la Mayenne regarding N2T inquiry for updating records regarding organization URL 
- [x] Bertrand Caron Will send out an email message to the English ARKs list to encourage community to update their organization information for the ARK registry