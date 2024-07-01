\---

confluence-id: 199525525

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-01-14 AG Agenda and Notes
==============================

Created by John Kunze, last modified on Jan 14, 2021

Date
----

14 Jan 2021

Attendees
---------

*   John Kunze
    
*   Mark Phillips
    
*   Erin Tripp
*   Kurt Ewoldsen
*   Brian McBride
*   Riccardo Ferrante

Goals
-----

*   rebranding, funding, resolver replica possibility

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements | Erin | We made it to 2021! <br><br>Catalyst Fund call for proposals is open. <br><br>The 2021 LYRASIS Catalyst Fund application cycle is now open and we are accepting proposals and ideas through February 19. Join us for Catalyst Fund: The Application Process & Overview Webinar, a free webinar on January 19 from 3:00 - 4:00 PM Eastern. |
|     | upcoming meetings, calls for papers, submission deadlines<br><br>iPres 2021, Oct 19-22 (Beijing) – Submission deadline March 15<br><br>PIDapalooza on Jan 27<br><br>PASIG 21-23 Sept 2021 (Madrid) (call deadline?)<br><br>CNI March 15-26, deadline Feb 12 | John | PIDapalooza - there will be a number of presentations in different languages. <br><br>PASIG - Tom Cramer and David Minor are running things now.  - [PASIG 2021 Website](https://www.pasig2020memoriademadrid.es/); probably possible to get on the agenda by contacting them<br><br>CNI call is out. Deadline in February.<br><br>ACTION - It would be great if community members could present instead of us usual characters.  Please communicate with your network to see if new presenters can be encouraged to submit. <br><br>Virtual conferences are more of a publishing platform right now. Sessions are getting 30-40% attendance versus registration. |
|     | Islandora and Incipit Updates | Kurt | Islandora interested in ARK support for next version. Access to N2T was made available. No recent updates available. <br><br>Incipit - grant-funded project in Switzerland for ARK management system for Swiss museums. Open source EZID was provided as support. John is providing assistance to modify the codebase of their needs. Potential expansion across the EU if this goes well. They will rename the service ARKetype. <br><br>From Julien Raemy: We will soon launch ARKetype (yes we renamed the service and instead of INCIPIT, which is still the name of the project, we settled for ARKetype) and we will held a 1h30 "Ask Me Anything" kind of event on Wednesday, January 27th (10.30am - 12 noon CET) - so just a few hours before PIDapalooza 2021.<br><br>We will record this session and make it available as soon as possible (see below for the invitation)<br><br>They are presenting at PIDapalooza. |
|     | funding proposal update | John, Mark, Erin | Difficulty reaching Mellon.  <br>  <br>Sloan, (M Phillips) Joshua Greenberg. They have a standing 2-pager one can submit. Planning to send this week. We should have some feedback in about a month (mid\_February)   <br>  <br>IMLS waiting for next cycle in August/September. Possible out of cycle awards in the summer - but rare. |
|     | ETA of "rollout" for rebranding and first newsletter:<br><br>*   [draft rebranding announcement](https://arks.org/blog/announcing-the-ark-alliance/)<br>*   also for newsletter: [community snapshot](https://arks.org/blog/community-update-2021-01-13/)<br>*   coordinate with others for additional publicity (eg, LYRASIS blog)? | John/Erin | Vision for newsletter - it will include a number of blog posts. We'll harvest the blog posts for content. It will go out with MailChimp. Peter has helped with that. We're looking to do this cost-effectively. Content should include community snapshot - numbers, who joined recently, and also the award announcement for physical samples grant. Will learn by doing. We have no subscribers to date. John will subscribe people with their permission.   <br>Erin - Americans can be subscribed automatically - opt out policy. Canadians and Europeans need to be encouraged to opt in.   <br>Encouraging we send out multiple messages - open and click-through rates are 7-8%.   <br>Ricc - are there any campaigns for conferences that we can hop onto? Rick will send info on October iDigBio weekend event.   <br>We will ask PIDapalooza presenters to include one slide to promote the newsletter. <br><br>ACTION - John and Kurt to create slide content so it's easy to add to presentations. <br><br>Looking to have communications out before PIDapalooza. <br><br>ACTION - everyone, review announcement. Please redistribute after Jan 26. <br><br>Erin to redistribute the ARKs rebranding and newsletter to Leaders Circle listserv and on LYRASIS blog (both or one or the other) after Jan 26<br><br>Ricc - pushing to global unique id group, internal and other subscription groups. |
|     | exploring possibility of N2T replica, initially with Smithsonian<br><br>**N2T tech overview**<br><br>N2T provides primary storage for all EZID identifiers, minters for generating unique identifier strings, and resolution for all non-DOI identifiers, including identifiers not maintained by EZID (eg, Internet Archive ARKs).  All functions are served from an Apache web server homed at [n2t.net](http://n2t.net).  <br><br>The N2T web server uses the open-source Eggnog package (formerly Noid) to mint, bind, and resolve identifiers.  Egg is for binding (storing) and resolving, and nog (nice opaque generator) is used for minting.  Eggnog uses the open-source BerkeleyDB software as a fast, scalable database.  Resolution is provided by Apache server rewrite rules hooked up to egg.  Also on N2T are administrative scripts for creating and managing identifier prefixes (shoulders), backing up the database, updating external replicas, and documents to support these functions. All code is open source and available on github. | John/Rick | We hope this will be the first replica but not the last.<br><br>Working to get around a single point of failure and preservation element too. |

Action items
------------