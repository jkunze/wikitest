\---

confluence-id: 187172802

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-05-18 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified by Julien Antoine Raemy on May 18, 2020

Date
----

18 May 2020

Attendees
---------

*   John Kunze
    
*   Roxana Maurer
*   Bertrand Caron
*   Julien Antoine Raemy
*   Tom Creighton
*   Karen Hanson
*   Curtis Mirci

Goals
-----

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | **Test ARK proposal #1 (**May 11 brought to NAAN WG)<br><br>N2T-based test ARKs for non-EZID users<br><br>This is a much narrower version of the proposal brought in last month, which was to expand the role of NAAN registry to record shoulders under the four non-institutional NAANs. We need agreement on how INCIPIT might proceed with N2T-based test ARKs that do not conflict with EZID test ARKs. A major benefit of the proposal would be to protect exclusive "test" shoulder access rights of both EZID and INCIPIT.<br><br>Proposed: With its oversight role for the NAAN namespace, this group agrees to reserve, under the 99999 NAAN,<br><br>*   1 shoulder for exclusive use of the INCIPIT service<br>*   1-3 "historical" shoulders for exclusive use of the EZID service (uses for testing longer than 2 weeks)<br><br>Some discussion:<br><br>1.  A 99999 NAAN in ARKs found in the wild signifies a status of "test".<br>2.  No organization owns or was meant to own the 99999 NAAN.<br>3.  Historically, EZID has used 2 shoulders under the 99999 NAAN, taking advantage of these portions of the public/common space as if it had exclusive rights to them. This proposal would formally recognize those rights in the future.<br>4.  This proposal would also grant similar rights to a test shoulder for INCIPIT.<br><br>The current proposal has no impact on the NAAN registry. The test shoulders reserved in this way would be recorded for now in a separate file. | John |     |
|     | **Test ARK proposal #2** (this might co-exist with or go forward instead of proposal #1)<br><br>In the May 11 NAAN WG discussion, Bertrand reminded us of Roxanna's idea (2020.04.20) of a convention that automatically and implicitly reserves a test shoulder under 99999 whenever a new NAAN, eg 12345, is created.<br><br>Summary proposal: If ark:/12345/foo is registered to redirect to X/foo, then<br><br>ark:/99999/912345\_bar will redirect to X/912345\_bar.<br><br>In general,<br><br>ark:/99999/9<NAAN>\_... will redirect to X/9<NAAN>\_....<br><br>Why surround the NAAN with a 9 on the left and '\_' on the right? Because (a) the 9 preserves the first digit convention for the shoulder (with a digit that is _fixed_) and (b) the '\_' marks the end of the NAAN in case NAANs are assigned that have more than 5 characters. Question: consideration will this interfere with check digit calculation, if any? |     |     |
|     | update on X?info spec – what I'm working on<br><br>1.  modeling, for a networked entity X, when a provider deems one or more physical, digital, or conceptual objects to be "equivalent" when referring to or accessing X, eg, the PDF, the HTML, the CSV file, or the "overview object landing page" that points to them all<br>2.  modeling, for a hierarchical entity X in Y in Z, when an "overview" landing page (eg, Z) is different from a simple "parent" page Y<br>3.  modeling, for hierarchical entity X in Y in Z, when X?info returns only what is recorded for X or when it returns a layered composite: X?info + Y?info + Z?info |     |     |

Action items
------------