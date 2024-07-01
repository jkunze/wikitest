\---

confluence-id: 249135189

confluence-space: %%CONFLUENCE-SPACE%%

\---

2022-07-12 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Jul 12, 2022

Date
----

12 Jul 2022

Attendees
---------

*   Karen Hanson, Mark Phillips, Curtis Mirci, Greg Janée, Donny Winston, Tom Creighton
    

Goals
-----

       NISO work item, persistence statements, code of conduct

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | jk: recruiting drive for Outreach  <br>mp: can send an email to recent conference panelists |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     | dw: EU COST ([https://www.cost.eu/uploads/2022/07/COST\_oc-2022-1\_Announcement-HE.pdf](https://www.cost.eu/uploads/2022/07/COST_oc-2022-1_Announcement-HE.pdf)). For funding meetings. Benefits from international co-application.<br><br>dw: first conf on FAIR digital objects is coming up  <br>kh: I will go to Glasgow and iPRES (2 presentations)  <br>jk: would be nice to go to Glasgow to hang out near iPRES  <br>jk: are people missing facetime?  <br>gj: yes!  <br>cm; would like to travel to iPRES but have no funding  <br>tc: same |
| Any news items we should blog about? |     | jk: getting close to 1000 (968) ARK orgs |
| Tool play: noid-docker<br><br>SYNOPSIS                          (./ark)  <br>    ark - admin tool for basic ARK operations<br><br>USAGE  <br>    ark mkminter \[ NAAN \[ Shoulder \] \]  <br>    ark mint \[ Count \[ FQShoulder \] \]  <br>    ark lsminter \[ FQShoulder ... \]  <br>    ark rmminter \[ FQShoulder ... \]<br><br>DESCRIPTION  <br>    This script automates common ARK tasks. The ARK namespace is divided into  <br>    NAANs (Name Assigning Authority Numbers), which are further (sub)divided  <br>    into Shoulders. Shoulders are useful for delegating responsibility within  <br>    NAAN namespaces.<br><br>    The "mkminter" command creates a minter of opaque strings consisting of  <br>    digits, letters (betanumerics actually) and a final check character.  <br>    It takes a 5-digit NAAN (default "99999") and a Shoulder (default  <br>    "fk2") string. A Shoulder string must start with one or more betanumeric  <br>    letters (bcdfghjkmnpqrstvwxz) and end in a digit. The NAAN should be one  <br>    that you have been assigned (eg, 12345) via the global ARK NAAN registry.<br><br>    The "mint" command generates Count (default 1) strings suitable for ARK  <br>    assignments from the "fully qualified" minter name, FQShoulder, which  <br>    consists of the NAAN, a '/', and the Shoulder string. The default minter,  <br>    99999/fk2, generates test ARKs (non-persistent) of the form  <br>    ark:99999/fk2....<br><br>    Use the "lsminter" command either to list all minters or to check for  <br>    the existence of one or more minters named via FQShoulder. |     | jk: playing around with dockerizing noid  <br>kh: Portico might have a war file that wraps up noid  <br>gj: would be nice to see tools installable with pypi and other common installers  <br>dw: this could be very interesting to me since I don't like installing Perl  <br>gj: this harks back to co-equal partners sharing the hosting of n2t |
| [Draft NISO work item](https://docs.google.com/document/d/1BQNK7jVePDQI7jXy3UR8ka-vV8seZkkEur-Gm-Seg7Q/edit?usp=sharing) |     | gj: is there a requirement that there be a NISO member on the team?  <br>kh: if there is, portico is a niso voting member  <br>mp: yes, I think that submitting ARK as a work item is good  <br>tc: agreed  <br>gj: yes, esp. if ietf is going to be difficult; btw, doi is a niso standard (so precedent)  <br>dw: agreed  <br>jk: I haven't given up on ietf yet; anyone want to join in a convo with them?dw: what about .well-known convention?tc: yes, that's been discussed https://datatracker.ietf.org/doc/html/rfc8615dw: https://mydomain.com/.well-known/ark -> "https://mydomain.com/.path/to/arks/" implies that paths of the form "https://mydomain.com/.path/to/arks/ark:12345/..." as ARKs |
| Standardized Persistence policy?<br><br>*   recent discussion about ARKs for "canned searches"<br>*   [https://doi.org/10.5334/dsj-2017-039](https://doi.org/10.5334/dsj-2017-039)  Persistence Statements: Describing Digital Stickiness (2017) |     | tc: persistence statements could be useful; we have parish records with errors, and we need to be able make changes; and when two ARK-identified records need to be merged, we need to be able to explain why user is bing redirected (not stopping at a tombstone); I'll ask some folks if they'd be willing to work on some persistence descriptors |
| Code of Conduct policy (eg, for recruiting new members) – sources to borrow...<br><br>*   DLF, Code4lib, IETF, Stanford Lib, NYPL, etc. |     | mp: code of conduct +1; I think this is also a conversation that we can discuss at the Advisory Group meeting |
| Google workspace (G suite) for ARKA? |     |     |

Action items
------------

- [ ] Tom Creighton will ask some colleagues if they'd be willing to work on some persistence descriptors