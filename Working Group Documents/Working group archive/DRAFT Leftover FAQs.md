\---

confluence-id: 123109431

confluence-space: %%CONFLUENCE-SPACE%%

\---

DRAFT Leftover FAQs
===================

Created by John Kunze, last modified on Jun 27, 2019

/\*<!\[CDATA\[\*/ div.rbtoc1719792987783 {padding: 0px;} div.rbtoc1719792987783 ul {margin-left: 0px;} div.rbtoc1719792987783 li {margin-left: 0px;padding-left: 0px;} /\*\]\]>\*/

*   [Who is using ARKs?](#DRAFTLeftoverFAQs-WhoisusingARKs?)
*   [I've heard of ORCIDs, RORs, and UUIDs – where do they fit in?](#DRAFTLeftoverFAQs-I'veheardofORCIDs,RORs,andUUIDs–wheredotheyfitin?)

### Who is using ARKs?

**This URL is disallowed**

This iframe has been blocked by your administrator as it doesn't comply with the security policy. If you require this iframe please contact your Confluence administrator.

  

What are usage trends for ARKs, DOIs, Handles, PURLs, and URNs?

As of 2019, purely on an incomplete and anecdotal level, here are a few trends that have been observed.

*   ARKs have seen broad adoption in cultural memory institutions – museums, archives, and libraries. There is strong adoption in France and francophone regions.
*   DOIs until recently have mostly been known as reliable identifiers for scientific and scholarly literature, when in fact this applies to a subset of DOIs assigned via [Crossref](http://crossref.org). What it means to be a DOI is becoming harder to pin down because DOIs are being assigned to datasets, data management plans, field stations, etc. via [DataCite](http://datacite.org), as well as to movies (eg, "Kung Fu Panda") via [EIDR](http://eidr.org). Having said that, Crossref and DataCite DOIs have been successful in creating tools and services for scholarly publishers.
*   PURLs have seen lots of use in identifying metadata vocabulary and ontology terms.

### I've heard of ORCIDs, RORs, and UUIDs – where do they fit in?

Those are special kinds of persistent identifiers. ORCIDs (Open Researcher and Contributor Identifiers) only identify researchers, and they link to research works using ARKs, DOIs, etc. ORCIDs look like

     `[https://orcid.org/0000-0001-7604-8041](https://orcid.org/0000-0001-7604-8041)`

ROR (Research Organization Registry) identifiers designate organizations. For example, here's the California Digital Library:

     `[https://ror.org/03yrm5c26](https://ror.org/03yrm5c26)`

UUIDs are globally unique, 37-character strings that are easy for software to generate but only become usable as web addresses when made part of a URL, for example, in this ARK:

           `[https://somehost.example.com/3c2e39526-e0c3-41ae-be4f-07558a9458eb](https://somehost.example.com/3c2e39526-e0c3-41ae-be4f-07558a9458eb)`

While embedding a UUID in an ordinary URL makes it _actionable_ ("clickable"), you could expect more if it were embedded in an ARK such as

           `[https://n2t.net/ark:/65665/3c2e39526-e0c3-41ae-be4f-07558a9458eb](https://n2t.net/ark:/65665/3c2e39526-e0c3-41ae-be4f-07558a9458eb)`

As an ARK, for example, that UUID should return metadata (if available) and be insensitive to the hyphens, making this form equally viable:

     `[https://n2t.net/ark:/65665/3c2e39526e0c341aebe4f07558a9458eb](https://n2t.net/ark:/65665/3c2e39526e0c341aebe4f07558a9458eb)`

  

  

  

Attachments:
------------

![](images/icons/bullet_blue.gif) [n2t\_arch\_v5.jpg](attachments/123109431/123109432.jpg) (image/jpeg)