\---

confluence-id: 187179373

confluence-space: %%CONFLUENCE-SPACE%%

\---

2020-08-10 NAAN Registry WG Agenda and Notes
============================================

Created by John Kunze, last modified on Aug 10, 2020

Date
----

10 Aug 2020

Attendees
---------

*   John Kunze
    

Goals
-----

*   Updates on "shoulder" definition and registry

Discussion items
----------------

|     |     |     |     |
| --- | --- | --- | --- |
| Time | Item | Who | Notes |
|     | announcements |     |     |
|     | Expand FAQ shoulder explanation (see new text below table)<br><br>*   Clarify and add documentation pertaining to the "reserved" status of 99999 NAAN |     |     |
|     | Create document as stub registry of current test shoulders under 99999 NAAN<br><br>*   see [https://n2t.net/e/pub/shoulder\_registry.txt](https://n2t.net/e/pub/shoulder_registry.txt)<br>*   Document the test shoulders assigned to the 99999 NAAN and how to use it to avoid conflicts |     |     |

  

NEW FAQ TEXT FOR SHOULDERS

### What is the purpose of the NAAN?

By obtaining a NAAN, an organization gets the exclusive right to create ARKs "under" that NAAN. Your NAAN is part of a prefix in front of all your ARKs. The set of ARKs you can create is infinite and is known as your NAAN's namespace, and your NAAN namespace is a sub-namespace (subset) of the ARK namespace (the set of all possible ARKs). For example, the Internet Archive's NAAN namespace is all ARKs starting with "ark:/13960/". NAANs effectively subdivide the ARK namespace into non-overlapping sub-namespaces, each one holding an infinite number of possible ARKs. Since organizations can only create ARKs in their own namespaces, it is impossible for ARK assignments between organizations to conflict.

NAANs play a key role in resolution. For example, if a resolver cannot find an incoming ARK in its database, it looks at the incoming NAAN and redirects the ARK to the local resolver registered with the NAAN. This is precisely what the N2T.net resolver does. Any local resolver could be configured to return the favor for any incoming ARKs with NAANs that it doesn't know about, simply by redirecting them to N2T.

Namespaces and sub-namespaces work on the principle that every time a prefix defines a namespace, it only needs to be "extended" (adding characters to the end of the prefix) to create a new sub-namespace containing an infinite number of possible ARKs. There is potentially a sub-namespace associated with every prefix.

| Set of all ARKs starting | Namespace defined | Example ARK in that namespace |
| --- | --- | --- |
| ark:/ | All ARKs | ark:/99999/fk4gt2m |
| ark:/12345/ | ARKs under the NAAN 12345 | ark:/12345/p987654 |
| `ark:/12345/x5` | ARKs under the 12345/x5 _shoulder_ | ark:/12345/x5wf6789 |
| ark:/12345/x5wf6789/ | ARKs under the 12345/x5wf6789 _object_ | ark:/12345/x5wf6789/c2/s4.pdf |

Examples like those in the above table are quite common. The first is for all ARKs and the second is for all ARKs under ark:12345. The third is the shoulder concept, described below, which is the next subdivision under the NAAN; note that it has no "/" after it. The fourth, a complete ARK-as-prefix example, shows that an object ARK itself is a namespace, with potentially an infinite number of "sub-ARKs" that descend from it to name object parts and variants. The practice of creating new namespaces by adding information to an existing namespace is very widely used and pre-dates the Internet (eg, a neighbor, who lives at flat #3B, receives mail at 1234 Main Street, #3B, Springfield, IL, USA).

### What is a shoulder?

A _shoulder_ is a sub-NAAN namespace. It is the set all ARKs starting with a short, fixed extension to the NAAN. For example, in

ark:/12345/x5wf6789/c2/s4.pdf

the shoulder, can be designated by /x5 if the context is clear, but it is often best to use its fully qualified, globally unique designation of ark:/12345/x5. In the classic namespace tradition, the shoulder is the set of all possible ARKs starting with the longer shoulder name. Note that while the shorter shoulder name (the extension to the NAAN) is set off from the NAAN by a "/", it is _not_ followed by any separator character that marks the end of the shoulder. Our use of the term is borrowed from the locksmith profession, which understands sets of keys to be defined by fixed (unvarying) "shoulders" that precede the varying shapes ("blades") that end at the tip of the key.

### What is the purpose of a shoulder?

Shoulders help organize ARKs in a NAAN namespace. A shoulder is analogous to a guest room in your house. Imagine a colleague, Sam, who took in a long-term lodger, Larry. Sam's home is very spacious, but Sam complains that Larry leaves things permanently lying about all over the house: coat on the kitchen chair, glasses on the dining table, book on Sam's desk, slippers next to the sofa, coffee cup on the bathroom sink, etc. By special terms of his lodging agreement, once placed, Larry's things cannot be moved. Needing to find new places (ARKs, in the analogy) for things, Sam is stuck forever noticing and trying not to disturb Larry's stuff. You shake your head in sympathy and quietly decide that if you ever took in a long-term lodger, the lodging agreement would set aside a guest room (shoulder) with the requirement that the lodger's things could only be placed in the guest room.

So shoulders allow ARK assignment operations under a NAAN to be delegated to autonomous projects or divisions, just as NAANs do under the overall ARK namespace. Even if an organization initially only wants to use ARKs for one project, plans may change. If other needs for ARKs arise later, setting aside a new shoulder for each new project or division makes it easy to ensure that autonomous assignment streams – present, past, or future – won't conflict with each other, thanks to non-overlapping namespaces. (Shoulders can also ease the [namespace splitting problem](https://n2t.net/e/n2t_vision.html).)

### Why is there no "/" to mark the end of a shoulder?

In other words, in an ARK such as ark:/12345/x5wf6789, why is the shoulder "/x5" not followed by a "/"? According to ARK rules, if you had published

(please don't do this)     ark:/12345/x5/wf6789/c2/s4.pdf

the "/" after "/x5" implies

*   that ark:/12345/x5 is also an object and
*   that the object named ark:/12345/x5/wf6789/c2/s4.pdf is contained in it.

Both are likely untrue, at least in any way that can be easily explained to a user. It may seem natural to add a "/" because it makes the shoulder boundary obvious to in-house ARK administrators, but they are specialists who can be inconvenienced by the non-obvious. It doesn't help the end user who is either uninterested and confused by your internal operational boundaries, or so very interested that they may try to hold you to account for their inferences (eg, about consistent support levels across objects sharing the apparent containing object). Less transparency about administrative structure hides messy details and can save user-support time in the end.

In fact ARK administrators always know where the shoulder ends, provided it was chosen using the "first-digit convention". A _primordinal shoulder_ is a sequence of one or more [betanumeric](https://wiki.lyrasis.org/display/ARKs/ARK+Identifiers+FAQ#ARKIdentifiersFAQ-betanumeric) letters ending in a digit. This means the shoulder is all letters (often just one) after the NAAN up to and including the first digit encountered after the NAAN. Another advantage of primordinal shoulders is that there is an infinite number of them possible under any NAAN.

### How do I implement a shoulder?

There are different ways to implement a shoulder. Fundamentally, a shoulder is a deliberate practice that is created from a decision you make to assign ARKs that start with a particular extension to your NAAN. A shoulder can then emerge from ARK assignment practices that have consciously reserved and use that extension.

Having said that, there are a couple of cases where shoulder creation can involve another step. A system such as ezid.cdlib.org supports these kinds of "user-based" shoulders (that emerge from user practice, eg, Smithsonian), but also supports the creation of system-recognized shoulders with accompanying minter services and registered API access points. To implement a user-based shoulder requires no separate shoulder creation step, but does involve the creation of one or more ARKs under that shoulder.

In another case, to implement a shoulder under one of a handful of shared NAANs (below), your organization must first register to reserve a shoulder under a shared NAAN.

### Are there restrictions on the use of NAANs and shoulders?

Yes. First, it is important never to invent or use a NAAN that is not listed in the public NAAN registry. There are, however, four special NAANs that are for shared use:

*   99999, for "test", "development", or experimental ARKs,
*   12345, for ARKs appearing in documentation,
*   99152, for controlled vocabulary (metadata) terms, and
*   99166, for people, groups, and institutions as agents.

For people with enough training, it is easy to recognize and exploit ARKs with the immutable attributes or connotations of these NAANs. For example, broken link reports for 99999 and 12345 ARKs can safely be ignored. Despite providers' best efforts, test ARKs frequently "escape into the wild", so the fixed semantics of these NAANs can mitigate their potential to end up confusing users and link checkers.

To create ARKs that use these shared NAAN-based semantics without conflict, there needs to be a way to reserve namespaces (shoulders) under the NAANs, and that requires a public shoulder registry. To register a shoulder under a shared NAAN requires filling out the same online form used to request a NAAN.

### Can I make changes to a NAAN or a shared shoulder?

You can change the registry entry for a NAAN by filling out the same online form used for requesting a new NAAN. For security purposes requests are processed manually. Example reasons for a change may include

*   notifying [N2T](https://wiki.lyrasis.org/pages/viewpage.action?pageId=131533174#ARKIdentifiersFAQ-n2t) of a change in your organization's contact person or resolver URL,
*   updating your organization's name assignment policy (sample policy),
*   requesting an additional NAAN, eg, to support a significant new body of ARKs or new organizational division, and
*   transitioning your NAAN to another organization that will carry on your work and future use of your NAAN.

NAANs are portable. If your organization transitions into or out of a vendor relationship, there is no impediment to taking your NAAN with you.

Action items
------------

Attachments:
------------

![](images/icons/bullet_blue.gif) [image2020-6-7\_22-38-18.png](attachments/187179373/187179393.png) (image/png)