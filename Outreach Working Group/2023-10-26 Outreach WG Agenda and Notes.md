\---

confluence-id: 308412417

confluence-space: %%CONFLUENCE-SPACE%%

\---

2023-10-26 Outreach WG Agenda and Notes
=======================================

Created by John Kunze, last modified on Oct 31, 2023

Date
----

26 Oct 2023

Attendees
---------

*   John Jung, Jack O'Malley, John Kunze, Ricc Ferrante

Goals
-----

  

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | Welcome Jack OMalley. Jack is does programming and metadata schema development at the Frick Collection.   <br>jm: I did a lightning talk yesterday for ARLIS mini-conference in NYC ([https://www.arlisny.org/event-5442603](https://www.arlisny.org/event-5442603)); ARKs seemed like a very new concept to this very general audience of art historians, many of whom were probably 5-10 years out of MLIS programs  <br>rf: we are re-engaging with DPLA to explore their goals wrt wikimedia and wikidata  <br>jm: wikidata is one of my core areas, and I'd would be willing to help advise  <br>rf: SI has a wikipedian-in-residence, Andrew Lih (I can ask for an intro), who has done stuff for  the NY Met  <br>jm: I have an ARK use case that I could describe |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     | There is a conference in Prague, JK will be doing a remote ARK tutorial. An in-person tutorial in St. Louis is coming up. Data Documentation Initiative (DDI) is coming up in Slovenia. Web Archiving Conference is coming up in Paris in April.<br><br>rf: I wonder if Jack's use case for ARKs and Wikidata might be an interesting blog topic? Jack agrees that it might. Have we ever thought of trying to get a slot at SXSW? It's in March, 2024. Ricc will look into this one.<br><br>jm: leaving St Louis on morning of 15th, our digi pres people will be htere  <br>rf: is a good blog topic could be ARKs and wikidata; for conferences, what about SXSW ([https://www.sxsw.com/](https://www.sxsw.com/)) for cultural applications? next meeting is in March |
| The Frick has a working server/minter for ARKs that is built on arklet and was completed over the summer. With this demo, the Frick is looking for feedback, potentially leading to a blog post the project. Codebase: https://github.com/squidgetx/arklet-frick/tree/master | Jack O'Malley | The Frick has a working server/minter for ARKs that is build on arklet and was completed over the summer. With this demo, the Frick is looking for feedback, potentially leading to a blog post abbout the project. Codebase: [https://github.com/squidgetx/arklet-frick/tree/master](https://github.com/squidgetx/arklet-frick/tree/master) (Jack O'Malley)  <br>  <br>Jack shares a screen to github repo. The previous metadata librarian identified ARKs as a solution, during a db migration to a new LMS- that accidentally severed the relationship between the catalog and the digital collections. Jack put out an RFP for a developer to build on arklet (from IA) and to add features for their use cases. They have a small IT department, just 2 people, none of them are backend or web server experts- so they couldn't support hosting a resolver. They went with digital ocean and their droplet, along with a digital ocean db. Digital ocean is very cost-effective for them. They get $2K in credit for a nonprofit. Using a docker container for now and thinking about a consortial arrangement with MOMA and Brooklyn Museum or Metropolitan Digital Library folks (who have a robust team).  <br>  <br>The shoulders concept really appealed to groups at Frick for autonomous operation (shoulders give control, each with defined content and metadata conventions). Supports bulk minting- staff can use spreadsheets, CSVs of up to 100 ARKs at a time. Supports suffix passthrough, separable minter and resolver, shoulder rules, extensive metadata. schema is based on dcterms- url, title, type, commitment, identifier, format, relation, source. When he mints a shoulder, he writes a constant standard for people to fill out. ?info and ?json endpoints. Jupyter notebook use case will be to enrich [wikidata.org](http://wikidata.org) Frick presence; the Frick has a really strong digital art history dept, with LinkedData and AI. Aiming for 1-2 million ARKs. |
| Youtube channel video recommendations | John Jung | Our YouTube page is at [https://www.youtube.com/@arks\_org](https://www.youtube.com/@arks_org). JJ created a playlist to store videos from other creators, and will continue to look into ways to improve the homepage here. Some ideas to do that were by creating separate playlists for "introductory" and "advanced" users, or for implementors and administrators. |
| [Blog post template](https://docs.google.com/document/d/1QwnpuyHWoeqTQYVCpLNhF0eZQIOmEND4Aup7zoWIoZ4/edit) pilot | John Kunze, Ricc Ferrante | Blog post template linked to at left. Please provide feedback- JK would like to identify some pilots fort his questionnaire. |

Action items
------------