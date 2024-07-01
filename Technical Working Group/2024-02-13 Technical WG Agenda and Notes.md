\---

confluence-id: 321585609

confluence-space: %%CONFLUENCE-SPACE%%

\---

2024-02-13 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Feb 13, 2024

Date
----

13 Feb 2024

Attendees
---------

*   Dave Vieglais, Curtis Mirci, Lautaro Matas, Roxana Maurer, Donny Winston, Karen Hanson, Tom Creighton, Greg Janée, John Chodacki

Goals
-----

Updates to resolver, NAAN processing, static web pages

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     | lm: moving forward with blockchain implementation resolver  <br>      [https://n2t.net/ark:/61908/fkwff3000000000001z](https://n2t.net/ark:/61908/fkwff3000000000001z)  <br>    resolver running over decentralized resolver with HA and DNS resolver  <br>       with different servers in different countries  <br>    small proof of concept  <br>    testing with millions of records  <br>dv: will you be sharing the code?  <br>dw: Is there a link (blog post?) that summarizes what you’ve told us?  <br>lm: yes we will be publishing the code for this, along with updated papers; dARK whitepaper ([https://zenodo.org/records/8091668](https://zenodo.org/records/8091668)) has been updated; new paper, docs, code, etc. to be published later this year  <br>rm: any ARKetype news?  <br>jk: yes, its moving from Geneva to Lucerne  <br>rm: at the National Library of Luxembourg, we are upgrading our systems  <br>cm: we updated our local system, but the people receiving them need the extra slash to use their ARKs as URLs, so we're adding a slash back when we send them off  <br>jak: can you find out more abou this use case?  <br>cm: will send more info |
| Any news items we should blog about? Any calls for papers, submission deadlines, upcoming meetings we should note? Please add to [Calendar of events](Calendar-of-events_208341505.html). |     | dw: PIDfest deadline in a few weeks [https://www.pidfest.org/](https://www.pidfest.org/) |
| CDL resolver status update | Dave | dw: CDL refactoring work update; we're working on the processes for creating and editing NAAN records, which is related to the resolver changes, documented here:       <br>          [https://hackmd.io/YfqbdE65Qx-AAlfkd8UJqg?view](https://hackmd.io/YfqbdE65Qx-AAlfkd8UJqg?view)  <br>    ANVL -> JSON for NAAN registry  <br>    JSON schema can be used to validate records structurally  <br>gj: Typo: originazation<br><br>jk: Tool for generating form from JSON schema?  <br>dv: called "JSON editor"  <br>dw: This one? [https://github.com/josdejong/jsoneditor](https://github.com/josdejong/jsoneditor)<br><br>lm: we don't want to over burden the curation process with information that is already validated at national level  <br>lm: is there a way to triage per country or region?  <br>dv: currently there's a single source of truth for the naan registry but maybe we could split out blocks from the candidate naans  <br>jc: bulk uploads might be possible  <br>lm: have similar problems within our project and want to distribute |
| walkthrough of an editing scenario for [arks.org](http://arks.org) content<br><br>[draft doc steps](https://docs.google.com/document/d/13KIygiQ6zWpRfTiLeEru-x5oFsJZb4YW6qbSmVHhkkE/edit?usp=sharing) | John K. | dv: people could use jekyll locally<br><br>lm: we need to implement that and we found this blog post [https://migueldavid.eu/how-to-make-jekyll-multilingual-c13e74c18f1c](https://migueldavid.eu/how-to-make-jekyll-multilingual-c13e74c18f1c) |
| Spec transition status via [best practices draft](https://docs.google.com/document/d/1UOKurRlY54GWoTbr2Nte0Qlp80ap50GJXsqNJqjnwGg/edit?usp=sharing) |     | (ran out of time) |

Saved zoom chat
---------------

08:03:36 From John Kunze to Everyone:  
    [https://wiki.lyrasis.org/display/ARKs/2024-02-13+Technical+WG+Agenda+and+Notes](https://wiki.lyrasis.org/display/ARKs/2024-02-13+Technical+WG+Agenda+and+Notes)  
08:04:15 From Lautaro Matas to Everyone:  
    [https://n2t.net/ark:/61908/fkwff3000000000001z](https://n2t.net/ark:/61908/fkwff3000000000001z)  
08:07:20 From Donny Winston to Everyone:  
    @Lautaro Matas Is there a link (blog post?) that summarizes what you’ve told us?  
08:09:34 From Lautaro Matas to Everyone:  
    we are going to publish a new paper, a documentation site, and all the code later this year  
08:10:11 From Lautaro Matas to Everyone:  
    It will be available for all the comunity  
08:11:57 From Lautaro Matas to Everyone:  
    @Donny Winston This is original paper but it is outdated, we have been working on top of this ideas and we made a lot of changes  [https://zenodo.org/records/8091668](https://zenodo.org/records/8091668)  
08:12:20 From Donny Winston to Everyone:  
    Thanks!  
08:13:11 From Lautaro Matas to Everyone:  
    \* sorry, thats a presentation, but you will find the paper link inside  
08:13:23 From John Kunze to Everyone:  
    [jakkbl@gmail.com](mailto:jakkbl@gmail.com)  
08:16:44 From Donny Winston to Everyone:  
    [https://www.pidfest.org/](https://www.pidfest.org/)  
08:18:39 From Dave Vieglais to Everyone:  
    [https://hackmd.io/YfqbdE65Qx-AAlfkd8UJqg?view](https://hackmd.io/YfqbdE65Qx-AAlfkd8UJqg?view)  
08:24:50 From John Chodacki to Everyone:  
    [https://n2t.net/e/naan\_request](https://n2t.net/e/naan_request)  
08:27:03 From Greg Janée to Everyone:  
    Typo: originazation  
08:31:13 From Roxana Maurer (NLibLux) to Everyone:  
    I have to leave now, see you next time  
08:31:22 From John Chodacki to Everyone:  
    Reacted to "I have to leave now,..." with 👍  
08:33:22 From Lautaro Matas to Everyone:  
    question, it is posible to provide a collections of json files in a single issue  
08:33:24 From Lautaro Matas to Everyone:  
    ?  
08:35:10 From Donny Winston to Everyone:  
    This one [https://github.com/josdejong/jsoneditor](https://github.com/josdejong/jsoneditor) ?  
08:38:09 From Lautaro Matas to Everyone:  
    yes in our case we can provide a list of curated data  
08:38:54 From Lautaro Matas to Everyone:  
    we dont want to over charge the curation process with information that is alreary validated at national level  
08:51:34 From John Kunze to Everyone:  
    [https://wiki.lyrasis.org/display/ARKs/2024-02-13+Technical+WG+Agenda+and+Notes](https://wiki.lyrasis.org/display/ARKs/2024-02-13+Technical+WG+Agenda+and+Notes)  
08:52:48 From Dave Vieglais to Everyone:  
    Replying to "This one [https://git](https://git)..."  
      
    close, [https://github.com/json-editor/json-editor](https://github.com/json-editor/json-editor)  
08:52:58 From Donny Winston to Everyone:  
    Reacted to "close, [https://githu](https://githu)..." with 👍  
08:53:55 From Lautaro Matas to Everyone:  
    are you using Jekyll  right?  
08:54:44 From Dave Vieglais to Everyone:  
    yes, the rendering from markdown to html is done using jekyll.  
08:58:39 From Lautaro Matas to Everyone:  
    great, we are using the same, do you have translations?  
08:59:21 From Lautaro Matas to Everyone:  
    we need to implement that and we found this blog post [https://migueldavid.eu/how-to-make-jekyll-multilingual-c13e74c18f1c](https://migueldavid.eu/how-to-make-jekyll-multilingual-c13e74c18f1c)  
09:01:05 From Greg Janée to Everyone:  
    Off to another meeting,ciao  
09:01:25 From Donny Winston to Everyone:  
    Gtg as well. ciao. Thanks all.