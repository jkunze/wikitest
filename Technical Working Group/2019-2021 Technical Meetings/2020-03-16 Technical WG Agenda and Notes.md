\---

confluence-id: 183076760

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-03-16 Technical WG Agenda and Notes
========================================

Created by John Kunze, last modified on Apr 19, 2020

Date
----

16 Mar 2020

Attendees
---------

*   John Kunze
    
*   Bertrand Caron
*   Karen Hanson
*   Roxana Maurer

Goals
-----

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | [Revised Networked Entity Model (and ?info) spec](https://docs.google.com/document/d/1Kv3HEopw7PphZtHkOuf3gJVT1jKgNX8Um5rQ0lHVcek/edit)<br><br>Open issues from last time<br><br>*   alternative spellings for the new Networked Entity model terms<br>*   model overlap with things like OAI, IIIF, signposting, Portland common data model |     | K: lowest level building blocks should familiar proper terms; synthetic objects; can have synthetic terms; compound things like Slugcar; FRBR example [https://sparontologies.github.io/fabio/current/fabio.html](https://sparontologies.github.io/fabio/current/fabio.html)  <br>B: "representation" physical or digital; PREMIS doesn't distinguish born  <br>digital  <br>K: the doc could be split into a NE model and a ?info spec  <br>K: could possibly use Dot and Mug as types  <br>R: ?info Jan 6 call would use ERC, which is good idea; don't want to implement new model because it complicates and is hard to explain  <br>R: agree with splitting the document  <br>R: people will understand "digital object" better than "Dot"  <br>R: btw, we do persistence statements  <br>K: use Dot (digital object) as a type; better to describe the components as "type"  <br>ACTION: terminology needs to be way more intuitive  <br>B: the categories have some utility; like being able to adjust expectations based on the type of object  <br>B: should the ARK go to the plunging page?  <br>K: we have no physical object, but do have Slug type object |
|     | copy editing tech spec |     |     |
|     | deferred topic<br><br>**arks-forum issue: upper case normalization of % encoding**<br><br>Hello Mario, you bring up an issue that has not been noticed before.  Section 6.2.2.1 of RFC 3986 is talking about case normalization for the purpose of determining equivalence, but section 2.1 of the same gives a more general recommendation for using uppercase: "For consistency, URI producers and normalizers should use uppercase hexadecimal digits for all percent-encodings."  <br>  <br>The ARKs In The Open project has a technical working group that is looking at changes to the ARK specification, and we will take up your suggestion as a topic.  <br>  <br>I'm afraid I don't quite follow your suggestion that, e.g., "/" can be transformed to "\_" to avoid encoding issues.  The premise of encoding is that the ARK producer desires or needs to use certain characters.  If the producer were forced to change the characters they use, there would be no need for an encoding mechanism at all.  <br>  <br>\-Greg<br><br>  <br>\> On Feb 3, 2020, at 8:13 AM, John Kunze <[jak@ucop.edu](mailto:jak@ucop.edu)\> wrote:  <br>\>  <br>\> Did you all get this? If not please make sure you're subscribed and its not going to spam.  <br>\>  <br>\> ---------- Forwarded message ---------  <br>\> From: Mario Xerxes Castelán Castro <[marioxcc.MT@yandex.com](mailto:marioxcc.MT@yandex.com)\>  <br>\> Date: Sat, Feb 1, 2020 at 5:27 PM  <br>\> Subject: \[arks\] Case of percent-encoded character  <br>\> To: ARKs <[arks-forum@googlegroups.com](mailto:arks-forum@googlegroups.com)\>  <br>\>  <br>\>  <br>\> There exist a soft conflict between the ARK specification where lowercase percent-encoded characters and the URI specification (RFC 3986 §6.2.2.1) where uppercase percent-encoded characters are preferred. This is not a strict contradiction because both documents allow both lowercase and uppercase. However it leaves users that generates ARKs with percent-encoded characters and authors of software that generates them having to chose between contradictory recommendations.  <br>\>  <br>\> My personal suggestion is to change the ARK document to state that uppercase percent-coded characters are preferred to be consistent with the URI specification. The currently rationale for lowercase characters “Lower case hex digits are preferred to reduce the chances of false acronym recognition;” applies only when generating ARKs based on previously existing identifiers where some reserved characters appear in the previously existing identifier; in that case, another option is to encode the previously existing identifiers into the alphabet of unreserved ARK characters using some specific scheme that avoid percent-encoded chanters at all. For example, if the previously existing identifier is known to use the alphabet “0-9a-zA-Z/”, the character “/” can be transformed into “\_”, thus avoiding %2f or %2F. |     |     |

Action items
------------