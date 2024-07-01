\---

confluence-id: 112525432

confluence-space: %%CONFLUENCE-SPACE%%

\---

Notes from ARK "Experts" meetings, March 22 and June 11, 2018
=============================================================

Created by John Kunze, last modified on Mar 06, 2019

  

**ARK Experts Day** **@ National Library of France (BnF),****March 22nd 2018**
==============================================================================

\[ Discussions are noted in italics to distinguish them from the original agenda. Notes are mostly unedited. \]

*   Emmanuelle Bermès (BnF) (points 4 & 5)
*   Bertrand Caron (BnF) (all day)
*   Angela Dappert (digital preservation consultant) (all day)
*   John Deck (University of California, Berkeley) (points 1 & 2)
*   Adrien Di Mascio (Logilab) (all day)
*   Greg Janée (CDL) (points 1 & 2)
*   Frédérique Joannic-Seta (BnF) (points 4 & 5)
*   John Kunze (CDL) (all day)
*   Amy Kirchoff (Portico) (all day)
*   Thomas Ledoux (BnF) (all day)
*   Roxana Maurer-Popistasu (Bibliothèque nationale de Luxembourg) (all day)
*   Pascale Montmartin (Bibliothèque et Archives nationales du Québec) (points 3, 4 & 5)
*   Sheila Morrissey (Portico) (all day)
*   Sébastien Peyrard (BnF) (all day)
*   Mark Phillips (University of North Texas) (all day)
*   Claire Sibille de Grimoüard (Service interministériel des archives de France) (points 3, 4 & 5)
*   Jean-Philippe Tramoni (BnF) (all day)
*   Hélène Zettel (Service interministériel des archives de France) (all day)

  

1\. ARK specification change proposals
======================================

(present IETF draft at [{+}](https://tools.ietf.org/html/draft-kunze-ark-18)[https://tools.ietf.org/html/draft-kunze-ark-18+](https://tools.ietf.org/html/draft-kunze-ark-18+))

1.  1.  Goals of changes to the spec
        1.  fix what's broken, if anything
        2.  remove barriers to acceptance
        3.  move from Draft to RFC

  
**5+1 proposed changes:**

1.  Literal character repertoire changes: allow '~', but disallow '#' (which is is reserved in URIs fragments and LOD).
    *   _'~' is filesystem friendly and will not cause problems in current situation_
    *   _The number of characters in the repertoire will not change; just these 2 characters will change_
    *   _BnF: use the W3C recommendations for coolURIs:_ [{\_}{+}](https://www.w3.org/TR/cooluris/)[https://www.w3.org/TR/cooluris/+\_](https://www.w3.org/TR/cooluris/+_) _especially for hash URIs. Goal: distinguish the URI of a real-world object's description from the URI for the RWO itself._
    *   _Logilab is also in favour of disallowing the hash_
    *   **_No opinions against => the group approves the change_**

  

1.  Make the first '/' optional, so that ark:/12345/678 is equivalent to ark:12345/678. This would match a near universal practice in other id schemes, and is a commonplace and understandable mistake that currently penalizes ARK users and potential adopters.
    *   _Allows to reduce the length of the URL and users like the compactness of URLs_
    *   _It's optional in the sense that the parsers should still accept it and not break any old ARKs_
    *   _Going forward, the canonical form would be the shorter form, but the documentation should always mention that the / is still accepted_
    *   _Would it make sense to accept ark:12148:cb12345689 → no_
    *   _The colons should be encoded according to the URI spec, but people are using it anyway -> colons are even a bigger problem_
    *   **_This is passed, with a note about the hierarchical computation_**
2.  Parsers (resolvers) should check for inflections (final punctuation character combinations) before normalization of final structural characters ('/' and '.'), for example, given "ark:/12345/678./", parsers should check if "./" is an inflection and only normalize to "ark:/12345/678" if no inflection is matched
    *   _When a resolver is checking an ARK in order to decide what to do, resolvers are sensitive to inflections and they normalize ARKs first and usually final . or / are left outside_
    *   _The idea is to keep the possibility to use those / and . for reserved used. E.g. direct consumption vs. landing page: would be great to leave the possibility open to use the final / for a landing page for the object_
    *   _When registering an ARK in a database, leave the inflections out and store the normalized form, but for resolving ARKs we should use these final characters and check if they are in the list of inflections_
    *   _For those final characters, instead of recommending to toss them out, recommend to "set them aside" because they might have a special meaning;_
    *   _A ? at the end of the id is not considered part of the identifier. Proposal to tell in the spec that reserved characters (with a list of inflections) at the end are not part of the identifier. This would be a set of rules for resolvers_
    *   _Some concerns about overloading the ARK specification with REST API type requests_
    *   _This change would not affect current ARKs. Inflections should only be used when you are using a resolver, checking what was at the end and whether it has an associated feature or not in the context_
    *   _Inflections are a situational use of the ARK_
    *   _A / at the end of an ARK is a violation of the current specification_
    *   _Software doesn't want a landing page, but users do want to make a choice_
    *   _People want access to previous versions or the history of the object; this kind of use would be possible with this change in the specification_
    *   _This is about implementing a resolver, and not so much about the ARK proper_
    *   _Proposal: leave new inflections out from the ARK spec, and elaborate the use cases in a separate specification that could also be used for other types of identifiers. Qualifiers would remain built in the ARK spec_
    *   _Question: should we leave all inflections out of the ARK spec and define them for all kinds of Identifiers? -> but very disruptive to the current spec._
    *   _How do inflections and suffix pass-through work? Can we put an inflection at the end of a suffix? -> It should be subject to the same rules we were talking about, but not add this to the ARK specs_
    *   **_OK from the group, but will still look at the final wording_**

  

1.  Make the NAAN more flexible – instead of just 5 digits or 9 digits, allow any "beta-numeric" string (defined to be the same as noid repertoire: bcdfghjkmnpqrstvwxz0-9) with no runs of adjacent letters longer than two, eg, ark:/bc8/… but not ark:/bcd8/….
    *   _Leave lots of room for lots of name assigning authorities_
    *   _Original idea: 5 digits can not be mistaken for a date, same for 9 digit._
    *   _People now want shorter addresses, so using a 9 digit NAAN would not be that desirable. So we might want to densify the NAAN namespace (allow letters in that mixture but make everything possible to disallow a brand)_
    *   _Use the same opaque naming and character set as NOID, same rules (not more than 2 letters in a row)._
    *   _Proposal: do not block this in the spec, but suggest very strongly absolutely no changes to the way we currently assign NAANs_
    *   _Have a separate policy that defines who gets which type of NAANs (NAANs other than the 5 digits the CDL currently assigns)_
    *   _Minimum length: the NAAN could be a single character. With this change we could also have NAANs for namespaces marked by special starting character (for example "x" for UUIDs or "p" for physical objects), not just organisations._
    *   _With this change is it still a "Number"? We could keep the "NAAN", but call it a "Name"._
    *   _In terms of the registry indexing might be an issue if switching from integer to text_
    *   _The policy could be decided within the project "ARKs in the Open"_
    *   **_Everyone agrees with this change_**

  

1.  Update our understanding of what it means for metadata returned by inflections ('?' and '??') in 2018 to be both human- and machine-readable. In 2003, a simple email-header format (eg, ANVL) served both purposes, but now it is common to see a human-readable HTML landing page with machine-readable metadata embedded in it (where it doesn't interfere with the user experience).
    *   _Now we have new norms for this: enter this in a browser and get an HTML page that would be human readable, underneath: Javascript, JSON, Metadata tags, number of ways metadata can be embedded in HTML_
    *   _The spec should recommend providing human- and machine-readable metadata, but not specifying its form (in particular, keep silent about content negotiation), just providing examples._
    *   _Resolvers would have a choice in what format they would return upon the inflections_
    *   _Keep the resolving (including content negotiation and inflections) for a separate specification_
    *   _All of these changes are subject to reviewing the final wording of the draft_
    *   _Simple rewording: provide an example ("e.g., HTML page with embedded JSON-LD"...)_
    *   **_OK with the group_**

  

1.  Max link length for the ARKs : now 128 digit limit
    *   _Should we raise it? Leave it alone_
    *   _Whenever you are running a database, you have to set a limit for your column. However this is implementation-specific._
    *   _The idea is to remove obstacles, but the current trend is to have_
    *   _Qualifiers are included in this limit (the BnF has already longer links when considering the qualifiers)_
    *   _Current limits for databases shouldn't be the reason for limiting something in the specification_
    *   _2 sentences would be struck from the spec and not mention the limit_
    *   _Would dropping the limit have any impact on the suffix pass-through? -> No_
    *   _The spec could just make a recommendation, but specific implementations could have a higher limit_
    *   **_We will change the spec to eliminate the limit, but we will make a recommendation for a minimum of 255 characters supported in implementations_**

  

2\. Counting ARKs project
=========================

It is a feature of ARKs that there's no centralized maintenance authority, but that makes it difficult to count how many ARKs there are in the world. We propose an easy way for registered ARK implementers – those who are willing – to post a small JSON or YAML file (eg, at a well-known URL path) containing a date and an estimated number of ARKs published. Such files would be harvested to obtain a base total.

*   _Good for advocacy: how big is the number of ARKs that exist in the world? Not a one-time measure, but something that is updated on a regular basis_
*   _Machine-readable assertion with a date and a number (very rough estimate of ARKs created at this date). Should be kept very simple._
*   _Updates: once a day or once a year - up to each institution._
*   _A bit complex for BnF, which manages several independent subnaming authorities - other institutions could be in this case._
*   _Maybe add semantics about ARKs that were deleted, ARKs that are not public_
*   _Question: what we count are qualified or unqualified ARKs?_
    *   _This should maybe be decided by the name assigning authority, because they should know this rough estimate_
    *   _Maybe we need to differentiate between: all ARKs generated, all ARKs that might be seen in the wild/public, and ARKs on artifacts?_
    *   _4 options : ARKs that you assigned, ARKs that are in the wild, ARKs that the NAA considers to be an intellectual unit_
    *   _It would be hard to give an estimate number with variants if each variant has to be counted as one ARK_
    *   _DOIs are increasingly assigned as arbitrary levels of granularity_
*   _We could also have links to each NAA's naming policy_
*   _We could also have something similar to Thor Project's minting dashboard_
*   _We all agree that variants form of the same object need not be counted separately; where it gets tricky is the hierarchy. Let's think not in terms of a tree, but a graph._
*   _We want to provide numbers that are comparable to those using other identifiers_
*   _We should leave out things when things would get wild with answers to dynamic queries (potential infinite number of possibilities)_
*   _\=> strong encouragement to link to the naming policy_
*   _We could start with a first version of the count by asking the institutions participating in the ARK experts day to send in their numbers and analyse that first and only afterwards ask the 500 other institutions: "Let's get some numbers and define what the heck they mean and only after that decide which are the useful numbers"_
*   _Question for the survey: what is the thing you are assigning an ARK to?_
*   _We may even need some new terminology for what an ARK is, we don't have language to distinguish between "mother ARK" from "child ARK" or between variants. It's useful to distinguish between resolvable and citable, but both are really important._
*   _We should be raising awareness about naming policies that could inform future adopters on their own policies._
*   _What numbers are easy to produce ?_
    *   _Counting ARK names, not include qualifiers_
    *   _Counting ARK names that are kept / active / published / viable / "in the wild", "out there somehow", "meant to persist"_
*   _Do not add up the counts for bananas and apples: for different sub-naming authorities give separate numbers_

  

3\. Persistence statements
==========================

It has long been said that ARKs should provide a commitment or policy statement on demand from the current archival institution (object provider, name mapping authority). The day when this becomes true is closer with publication of "Persistence Statements: Describing Digital Stickiness" ([{+}](https://datascience.codata.org/articles/10.5334/dsj-2017-039/)[https://datascience.codata.org/articles/10.5334/dsj-2017-039/+](https://datascience.codata.org/articles/10.5334/dsj-2017-039/+)). The paper proposes certain controlled vocabulary terms as building blocks for exactly this purpose. All that is lacking is to select, review, and revise the terms (which we can evolve ourselves in a crowdsourced metadata dictionary), and finally test and propose as a community consensus.

*   _Idea that the service provider (NMA) can provide its own persistence policy_
*   _Persistence is not a binary things, there are many nuances of it_
*   _Explain what is supposed to change in the content behind the ARK_
    *   _"Frozen": no bit will change: pretty unusual case_
    *   _"Keeping": bits will change but it will look identical: format migration, compression change_
    *   _"Fixing": we will fix errors if we come upon them: corrections to content._
    *   _Growing content: latest issue / version_
    *   _The content will change: the homepage of an institution_
*   _How long would you keep this object:_
    *   _"Indefinite" commitment: we're not committing to anything, we don't know_
    *   _"Lifetime": it will be around as long as we are around_
    *   _"Subinfinite": we have successional arrangements with other organizations. Content will still be there even though we are not around anymore._
*   _What does the unqualified identifier lead you to by default? Landing page? Stable/Latest version?_
*   _If something happens to this object, what is your priority for replacing it?_
    *   _No particular priority_
    *   _High priority: we will do whatever it costs to restore access to it_
*   _Hyperlinked terms in the document are part of a vocabulary, but are still in a draft form. Controlled terms accessible, temporary definitions._
*   _Define persistence by the nature of the organisation: what are your missions? are you for profit, not for profit?_
*   _It would help to get a group of motivated testers and sketch up a testing plan_
    *   _Do we think this is a priority?_
    *   _Is there another approach?_
    *   _Is the vocabulary rich enough to describe your situation? Is it too elaborated?_
*   _Vision of the future: machine-readable, but for the time being keep it in natural language (paragraphs), but with hyperlinks to the definitions so that people talk about the same things_
    *   _A paragraph for each ARK, but with different paragraphs for "mother ARK" and "child ARK" (an ARK with qualifiers)_
    *   _Round-trip test with prose, test it with some institutions, redefine the vocabulary and at the end "translate" it into machine-readable statements_
*   _How do we set expectations upfront about things that could happen? -> Some terminology. This is different from things that happened: some provenance trail_
*   _PREMIS proposes semantic units to express "significant properties" (what the repository considers to be preserved along migrations) and "preservation level" (bit-level preservation / functional preservation). Have been practically implemented at Danish Royal Library_
*   _There are 2 types of persistence statements: specific for the institution or for the object -> Some of the vocabulary has to do with the nature of the institution_
*   _The user: the recipient of the identifier to make an informed judgement about whether it trusts the service: does reality comply with the persistence policy? What premise can we have_
*   _Such vocabularies could be used by all persistent identifier systems. Handle has a way of providing such a service_
*   _The paper uses a crowd-sourced "metadictionary" (_[{\_}{+}](http://www.yamz.net/)[http://www.yamz.net/+\_](http://www.yamz.net/+_)_), where people can upvote or downvote a term; each term has an identifier_
*   _How does this metadata dictionary manage multilingualism? Wikidata has several labels in different languages for each item._
*   _BnL will have persistence statements in three or four languages and also machine-readable ones._
*   _First stage: human-readable English statements. Each of our institutions tries to define them on one or two resource categories?_
*   _Be prepared to find out that those terms are not working and need to be enhanced, in which case you can suggest changes in YAMZ.net, start new terms..._
*   _Institutions doing the tests_
    *   _Portico_
    *   _CDL_
    *   _BnF_
    *   _BnL_
    *   _UNT_
*   _Each institution will do the exercise individually and send the first versions to John and only afterwards we will start working collaboratively_
*   **_Deadline for the first version of the statements & first conference call: Tuesday, 22nd of May at 8:00 PDT / 11:00 EDT / 17:00 CEST_**
    *   NOTE: this call was postponed pending establishment of the ARKs-in-the-Open working groups
        

  

4\. Towards ARK sustainability
==============================

Any persistent identifier system maintained solely by one organization is vulnerable, and ARK is no exception. CDL is seeking guidance on sustainability of the ARK "infrastructure" and on building a coalition of organizations with shared responsibility and governance. The ARK infrastructure includes the specification, the NAAN registry, the arks-forum googlegroup, and the N2T.net resolver (code, admin scripts, and primary and secondary servers).

*   _We don't want a persistent identifier system to depend on a single organisation_
*   _Take the ARK infrastructure and make it shared (the specs and the registry of NAANs, then the perimeter of the pilot could extend to the N2T resolver, policies, monitoring, testing, source code)_
*   _Formal discussions with DuraSpace_
    *   _DuraSpace could help with promotion, awareness, membership_
    *   _They could set up a non-profit association in the US (they have the legal means)_
    *   _Would the fact that we're talking about an US-based association would be a problem for non-US organisations? -> According to the BnF, probably not. We could work with a memorandum of understanding or form a consortium (that works for IIPC or, in a similar form, for IIIF). A consortium does not have a legal entity though and having an organisation that can take care of the legal aspects, like DuraSpace, could help, by hiring a maintainer / developer for example._
    *   _Duraspace has a model where all the contributors can decide which projects they use their money for_
*   _THOR has delivered a report on sustainability models for PID service providers - Angela will send out the document - it is not yet online (interim version online, but interim)_
*   _Organization Identifier Project:_ [{\_}{+}](https://figshare.com/articles/ORG_ID_WG_Governance_Principles_and_Recommendations/5402002)[https://figshare.com/articles/ORG\_ID\_WG\_Governance\_Principles\_and\_Recommendations/5402002+\_](https://figshare.com/articles/ORG_ID_WG_Governance_Principles_and_Recommendations/5402002+_)_. A Way Forward -_ [Web](https://orcid.org/blog/2016/10/31/organization-identifier-project-way-forward) _|_ [PDF](https://orcid.org/sites/default/files/ckfinder/userfiles/files/20161031%20OrgIDGovernance.pdf)
*   _DuraSpace summit in early April, good time to discuss a proposal and make an announcement_
*   _Brainstorming about the expected benefits:_
    *   _continuity plan for N2T_
    *   _shared roadmap for community development, priorities, tools_
    *   _creating a website for ARKs. The domain arks.org has been registered and currently redirects to N2T but should have content on its own, as a community-owned thing. Documentation, tools, registry of NAANs, map of users etc. Could have_
    *   _funding opportunities_
    *   _advocacy for ARK (Duraspace: "ambassador training" for people to advocate for their solution)_
    *   _conferences & meetings around ARK_

  

5\. ARK survey: joint BnF-CDL proposal
======================================

BnF and CDL would like to feedback on a proposed online survey to get a better understanding of the different ARK implementations.

*   _The survey idea came after a discussion between BnF and CDL_
*   _Would an online survey be helpful? If yes, what questions could we ask ARK users?_
*   _Sample questions include:_
    *   _Why did you choose ARKs?_
    *   _For what kinds of objects?_
    *   _Do you mint and/or resolve ARKs?_
    *   _Are there challenges that you encountered using ARKs?_
    *   _Would you consider contributing (at any level) to ARK community sustainability?_
*   _The results of the community survey could be used as well for the IETF specs and showing there is support for this standard_
*   _The survey could also include:_
    *   _Some examples of resolvable ARKs_
    *   _Examples of persistence statements, if they use them_
    *   _Iteration of major ARK features to see what groups support (qualifiers, inflection, 'wear their identifiers')_
*   _Beware of not having a survey that is too long!_
*   _CDL is interested in designing the survey, BnF could take the lead_
*   _Because the French speaking community is not always comfortable with English, we could have the survey in English and French, but reduce drastically the number of open questions_
*   _How can we advertise for that survey? Which channels can we use to promote it?_
    *   _Google group_
    *   _Mailing lists_
    *   _Twitter_
*   _Ithaka could review the survey before sending it out_
*   _We should create a first draft by the 22nd of May_

  

6\. Wrap-up
===========

*   How can we communicate with each other as a group?
    *   _Emails for the beginning_

**_ACTIONS By May 22, 2018_**
-----------------------------

*   _ACTION: John will propose wording changes for the ARK spec and send with diffs for review by May 2, 2018_
*   _ACTION: Each institution will send a snapshot set of numbers and naming policy links for the Counting ARKs project_
*   _ACTION: Portico, CDL, BnF, BnL, UNT - persistence statements test_
*   _ACTION: John asks Duraspace for a debriefing call with BnF regarding ARK Summit outcomes_
*   _ACTION: John asks Duraspace and CDL for input on the survey_
*   _ACTION: Sebastien will talk to BnF survey department_

  
  

**Follow up telecon 2018 June 16**
==================================

  
— 2018.06.11 Notes from ARK experts group meeting —

// Attending

Sébastien Peyrard  
Bertrand Caron  
Jean-Philippe Tramoni  
Adrien Di Mascio  
Sheila Morrissey  
Amy Kirchhoff  
Pascale Montmartin  
John Deck  
Mark Phillips

  
// Agenda + notes

1\. ARKs-in-the-Open (AitO) project update  
Advisory Group to meet in next 4-7 weeks  
Working groups to be launched: technical, outreach, financial/sustainability 

2\. Keeping momentum for the ARK Experts Day ad hoc group  
\- collaboration pros and cons (eg, is there something urgent we need  
done soon?)  
\- should we offer outcomes to seed AitO working groups?  
\- should we offer ourselves to seed AitO working groups?  

ARKsInTheOpen.org has all the info  
Great deal of overlap between this group and the expected working groups from AitO.  
The Experts Group is fine using our outcomes to feed into the working groups, and volunteer to carry our work forward in the context of the AitO project.

3\. ARK usage survey review – next steps  

SP: Thanks to all for the draft survey comments. BnF is ok letting this survey be carried forward in a future outreach working group. Survey specialists have had a chance to review it as well. There will also be a French version of the survey.  
JK: If the working groups don't form in a way that's to our liking we can always resume our Experts Group meetings. I don't expect that outcome, but there are elements that we cannot control.  
SP: We will have to consider where the survey will be hosted.  
BC: Meanwhile, BnF will move forward in setting up the French-speaking forum.  

4\. Other items

SM: It seems like a good idea to do a brief talk at iPres about some of our activities. I could to draft something in response to a recent call and send it to this group for review.  
JK: +1!  
JD: It would be great to have a single place to go for information about ARKs.  
JK: I hope the outreach group can direct the building out of [arks.org](http://arks.org/) (currently pointing to [n2t.net](http://n2t.net/)).  
5\. Around the room:  
Confirmed that everyone is ok to wait for the AitO working groups and merge our efforts with theirs.