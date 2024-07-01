\---

confluence-id: 230818201

confluence-space: %%CONFLUENCE-SPACE%%

\---

2021-12-14 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Dec 22, 2021

Date
----

14 Dec 2021

Attendees
---------

*   John Kunze 
*   Amir Alwash 
*   Curtis Mirci 
*   Karen Hanson 
*   Dave Vieglais 

Goals
-----

    new spec, new github repo for spec maintenance, proposed tweaks for impersistence and developer assistance

Discussion items
----------------

|     |     |     |
| --- | --- | --- |
| Item | Who | Notes |
| Announcements |     |     |
| Calls for papers, submission deadlines, upcoming meetings: [Calendar of events](Calendar-of-events_208341505.html) |     |     |
| Any news items we should blog about? |     | jk: some suggestion in Outreach we should blog about new spec versions, but some of our new spec versions are often only of minor interest; the total departure (in sum) from version 18 will be of interest when we're done |
| New [ARK spec (v30)](https://www.ietf.org/archive/id/draft-kunze-ark-30.txt)<br><br>[Diffs from v29->v30](https://www.ietf.org/rfcdiff?url2=draft-kunze-ark-30) |     | jk: minor changes in this version, mostly to test new github actions in its new home (first git version)  <br>dv: what should we focus on overall in the spec?  <br>jk: are we ok leaving the metadata defined (for this spec) by example?  <br>jk: current repo is probably going to have to be redone to get it correct |
| This new (v30) spec is the first draft with raw XML stored in a github repo: [jkunze/arkspec](https://github.com/jkunze/arkspec)<br><br>*   built from [template designed for managing Internet Drafts](https://github.com/martinthomson/i-d-template/blob/main/doc/TEMPLATE.md) (TY Mark for forwarding)<br>*   it's a first attempt, probably will need to redo it got messy making it work for draft in XML (not markdown)<br>*   volunteer to help make sure it's right technically<br>*   please test the sociology: **can you do a pull request to fix typos**? do we need more committers? what's missing? |     | dv: PRs is right; two ways to do it: either fork or add additional participants to the repo; there's usually a social contract, eg, that one designated person approves  <br>jk: how to set up privileges? do we need additional committers?jk: is forking cumbersome?  <br>kh: on software my projects, even main committers will create a fork and request a review of their changes  <br>kh: might be good to have an "ARKA" github account, and establish review requesting as part of the PR protocol that we agree to; that way anyone outside ARKA could contribute  <br>all: agreed  <br>ACTION: set up ARKA account and repo  <br>dv: some people get confused until head gets wrapped  <br>ACTION: kh and jk will meet to walk through some PR scenarios |
| Support (non-normative) for building ARK services using N2T's convention – should the ARK spec describe this as one known tool for resolver implementors?<br><br>*   **Prefix extension.** N2T supports a "prefix extension" feature that permits developers to extend a scheme or an ARK NAAN (both of which "prefix" an identifier) with -dev in order to forward to an alternate destination. For example, if the NAAN 12345 forwards to domain [a.b.org](http://a.b.org), then ark:/12345-dev/678 forwards to a-dev.b.org/678. It works similarly for schemes, for example, if scheme xyzzy forwards to a.b.org/$id, then xyzzy-dev:foo forwards to a-dev.b.org/foo. |     | dv: prefix extension could go into an implementors guidelines dockh: agreed  <br>dv: "ark or identifier resolver implementor guidelines" |
| Are there best practices in how to do short term ARKs? All the ARK services, features, metadata, inflections can be used for ARKs that expire (persistent within a defined ending term, eg, link expires after first access, object access expires in 12 months per agreement with rights holder). How best to avoid confusion if ARKs can be used for both persistent and persistent-but-expiring identifiers?<br><br>One approach is a NAAN-based convention, similar to how four particular NAANs (eg, 99999 and 12345) instantly (in the string itself, not requiring lookup) reveal something important to the recipient.<br><br>Strawdog "Zero NAAN" proposal: every org that receives a NAAN, say 98765, also implicitly receives a second NAAN with a '0' (zero) prepended. We can promise that no org will _ever_ be assigned a NAAN beginning with zero, so if you see a NAAN starting with a zero, published in an ARK, say "ark:098765/t7gh, you can assume that it is expiring and not suitable for long-term reference. Implementors would be encouraged to publish with a leading zero if and only if they know they are publishing an expiring ARK. |     | dv: maybe instead of ark:0 use "tark:"<br><br>cm: don't see any reason to say that there's an expiration date up front when it can be in the metadata |
| [New comments](https://docs.google.com/document/d/1NhjaUymkcZD444_TtQx7CpFuttInJkti2Ot_yiguxuM/edit) (from TC) on the [ARKs in URLs](https://hpad.dataone.org/arks_in_urls?view#comparison-of-urls-containing-arks) document<br><br>Please review for next time |     | dv: I responded to comments in the doc |

Action items
------------

- [ ] John Kunze set up ARKA account and repo
- [x] John Kunze and Karen Hanson will meet to walk through some PR scenarios