\---

confluence-id: 305692747

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-10-10 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Oct 10, 2023

Date
----

10 Oct 2023

Attendees
---------

*   Curtis Mirci, Dave Vieglais, Karen Hanson, Greg Janee, Roxana Maurer, Lautaro Mata, Bertrand Caron, John Kunze
    

Goals
-----

transition off Wordpress and old N2T resolver

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | got new 45 minute tutorial recording posted on youtube channel, from Czech memory institutions meeting |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     | ARK tutorial accepted at [No Time To Wait](https://mediaarea.net/NoTimeToWait7) conference, 60 minutes, online or onsite, Nov 8 |
| ARK spec transition update<br><br>reframe as resolver and best practices transition? eg, what to do with foreign NAANs? |     | cm: best practices reframing seem reasonablerm: prefer good practices over best practices  <br>jk: Greg and I preferred "not bad practices" because we weren't sure what good practices were<br><br>dv: maybe talk about minor vs major version changes; practices could include what an API should look like  <br>dv: one approach is to go from V1 and the major V2 change of deprecating the :/ in favor of :  <br>dv: there will be significant lag time in reaching all implementors; how up-to-date are the email contacts in NAAN registry?  <br>jk: not very, many out of date in 2018  <br>dv: we'll need to support V1 and V2 for awhile  <br>jk: everyone will always have to support the :/ version in ARKs  <br>gj: won't it be true that not everyone will transition?  <br>cm: do we need v1 flag in metadata?  <br>dv: regexes for V2 will be more relaxed than for V1 in new n2t and [arks.org](http://arks.org)  <br>rm: for foreign NAANs, our resolver sends arks to N2T |
| update on arks.org transition off of Wordpress | Mark | Mark: (from email of Oct 10)  <br><br>Currently the [arks.org](http://arks.org/) website is backed by an instance of Wordpress that is hosted on a Dreamhost server.  There are a few challenges with this setup.  First it requires funding to pay for the hosting and administration to keep the Wordpress instance updated.  While both of these are nominal amounts of funding and time, currently they are managed by just one person.  Another challenge is the process of updating the website, the process is not always clear and there are some single or few points of failure in how things are managed. <br><br>To put pieces in motion to help with these challenges, the UNT Libraries took on the work over the summer to create an instance of the [arks.org](http://arks.org/) website using the static site builder Jekyll.  We made use of the GitHub Pages infrastructure to develop the site and the repository is available here - [https://github.com/arks-org/arks.github.io](https://github.com/arks-org/arks.github.io) with the online version (built automatically from the repository) available here [https://arks-org.github.io/arks.github.io/](https://arks-org.github.io/arks.github.io/) as a beta site. <br><br>While this is still early in the stages of switching things over, the groundwork has been put down so that this transition could happen.  There are benefits of using the GitHub repository for managing the website and content.  The Outreach group is beginning to look at the publishing process and how that can be handled with standard Github mechanisms like Issues, Wiki pages, Merges and Approval processes.  <br><br>As we look at transitioning the [arks.org](http://arks.org/) website from DreamHost to the CDL where it will function as both the website and a resolver, the Jekyll version of the website should allow for easy deployments based on the final architecture of the service. <br><br>I am happy to answer additional questions about the work that we've done on this if anyone has them. <br><br>jk: Just an observation that the Wordpress site is open to anyone in the ARKA to edit, and a dozen people have established credentials. That few of them contribute to arks.org may still be an issue with the new site, but managing changes via github may be more palatable to potential contributors than Wordpress. |
| n2t resolver code refactoring update | Dave | dv: big changes coming, but no user visible changes  <br>dv: [arks.org](http://arks.org) currently hosted on dreamhost, will be changed to static markdown with jekyll (work done by Mark Phillips' people); free hosting on Vercel, but it might go away; working on CDL hosting  <br>jk: pretty snappy response  <br>dv: that because of static pages and caching; ark resolver stage instance going up now at CDL |
| Missing properties for ARKs in Wikidata (Wkd):  <br>[https://www.wikidata.org/wiki/Property:P8091](https://www.wikidata.org/wiki/Property:P8091)  https://www.wikidata.org/wiki/Q2860403<br><br>Upload the [arks.org](http://arks.org/) logo? CC license?  <br>\- The number of assigned ARKs (citation?)  <br>\- Updating the REGEX "ark:/\[0-9\]+/.\*"  <br>\- Other identifier properties based on ARKs as associated properties, [https://www.wikidata.org/wiki/Property:P1659](https://www.wikidata.org/wiki/Property:P1659) | Bertrand | bc: i've taken it on myself to make tweaks to Wkd  <br>jk: next time we'll try to do a summary of the issues<br><br>call for others to contribute to review and refresh of Wkd pages<br><br>ran out of time – to be taken up next time |

Action items
------------