# 2026 Q4 TAC Report for Global Cyber Policy Working Group

## Overview

* GitHub repo: https://github.com/ossf/wg-globalcyberpolicy/
* Minutes doc: https://docs.google.com/document/d/1iAplSQheMgemdMnEw74uPj3oi_6rLLbFFXhg4svqIDo/edit
* Charter: https://github.com/ossf/wg-globalcyberpolicy/blob/main/CHARTER.md

We're coming to the end of our 2nd year of this group, having been first chartered in January 2025. The group was started after the [Linux Foundation workshop on "Stewards and Manufacturers"](https://events.linuxfoundation.org/open-source-software-stewards-manufacturers-workshop/program/schedule/) in Amsterdam in December 2024. The scope of the group is to provide a forum for our members and the broader community to collaborate on Global Cybersecurity-related legislation, frameworks, and standards which facilitate conformance to regulatory requirements by open source projects and their consumers. We have been holding bi-weekly calls. We have 2 active SIGs - Awareness and Standards. The group is focusing most of its attention on the European Cyber Resilience Act (CRA) and its first September 2026 enforcement with some time put aside to monitor activities in other jurisdictions. Recognizing the growth of AI regulations (like AI Act) and standardization activities (like CEN/CLC 7 AI standards or COSAI work), AI Policy x Security is an agenda item for the WG as well. We keep an open line of communication with the [Eclipse ORC working group](https://github.com/orcwg/), to try to minimize overlap. 

Notably, since our last report, the [ENISA CRA single reporting platform](https://www.enisa.europa.eu/topics/product-security/vulnerability-services/eu-incident-response-and-cyber-crisis-management/single-reporting-platform-srp) has launched and we have been helping our community navigate this.

At Open Source Summit Europe, the group [ran a workshop](https://osselceu2026.sched.com/event/2WChc/workshop-operationalizing-the-cyber-resilience-act-boxed-lunch-included-dan-appelquist-samsung-roman-zhukov-red-hat-madalin-neag-the-linux-foundationopenssf-megan-knight-arm), and we are in the process of analyzing the outcomes. Part of the point of the workshop has been to help us refine our roadmap for next year by hearing from the wider community. The workshop split into 3 discussion groups, focusing on software dilligence, vulnerability reporting and working with and supporting maintainers. 

We also delivered a talk at OpenSSF Community Day Europe and we spread more awareness of our efforts at Open Source Summit Europe via outreach from the OpenSSF booth, including leveraging the awesome CRAfish mascot plushie (and locally made ginger cookies!). Members of GCP WG also gave talks throughout entire week.

We have also continued to engage with members from our Japanese and Korean chapters, who have become more active in the group, highlighting the global nature of this effort. This group of Japanese organizations produced a list of questions concerning the distinction between stewards and manufacturers under the CRA, which have helped to guide our work in the last quarter. We are holding a call with Korean chapter members this week.

We have two working group co-leads: [Daniel Appelquist | Samsung](https://github.com/torgo) and [Roman Zhukov | Red Hat](https://github.com/rozhukov). [Megan Knight | Arm](https://github.com/businesscasualkesha) chairs the Awareness SIG and [Madalin Neag](https://github.com/madalinnneag) from OpenSSF staff has been chairing the Standards SIG. In addition, we have support from [Jeff Diecks](https://github.com/GeauxJD), [Crob](https://github.com/SecurityCRob) and [David A. Wheeler](https://github.com/david-a-wheeler). 

We have a regular schedule of calls for our main working group as well as for our Awareness and Standards SIGs and take minutes in the following minutes docs:
* Main WG/Awareness SIG: https://docs.google.com/document/d/1iAplSQheMgemdMnEw74uPj3oi_6rLLbFFXhg4svqIDo/edit?tab=t.0
* Standards SIG: https://docs.google.com/document/d/1XjE5VYdyIdH32T94ZQIj0Hf5btRiKG58z3jSInY77wA/edit?tab=t.0

## New Working Group Structure

After some work between the above leadership team members, we have announced a new working group structure to the group:

* **Full Working Group** stays the same, keeping CRA as a standing topic, but dedicate more time for other global regulation / policy and SIGs report o to full working group
* **Awareness SIG** continues and expands scope beyond CRA
* **Standards SIG** will be deprecated CRA standards are almost in the done phase – we will preserve the value by adding updates as a standing agenda point to main WG
* New **CRA community Forum SIG** - starting in Standards SIG times-slot (and we may adjust time). This will focus more on open discussions and cross-support regarding CRA implementation issues. We are looking for a new chair to help with this SIG.
* New **GCP APAC SIG** - time tbd, and looking for facilitators ← looking for help to chair

The group would like to thank Madalin for his stellar work in chairing the Standards SIG calls.

## Main Working Group

Our general working group call, besides being a place where SIGs report, also serves as a venue to work on general deliverables and to drive awareness with group members of related activities. 

This quarter, we have continued to work with the [ORBIT Launchpad](https://github.com/ossf/orbit-launchpad) effort, including facilitating a "CRA Monthly Tech Talk" covering ORBIT Launchpad, its progress and its future plans. As noted in their charter, Cyber Policy working group is a key stakeholder and partner for ORBIT Launchpad. This work has subsumed the work that we initially conceived of as a "Tooling" SIG in our own working group.

Since our last report:

We organized 3 Tech Talks:
- [ORBIT Launchpad](https://openssf.org/policy/cra/2026/08/14/cra-monthly-tech-talk-orbit-launchpad-sig-updates/)
- [CRA Reporting Obligations](https://openssf.org/policy/cra/2026/09/29/cra-tech-talk-09-07-2026/)
- [A Practitioner's Guide to Compliance](https://openssf.org/blog/2026/08/11/cra-readiness-a-practitioners-guide-to-compliance/)

Also:
- talk at OpenSSF Day Europe and workshop at Open Source Summit Europe (as detailed above)
- we do comprehensive bi-weekly update on CRA standards, policy developments, collect and submit community feedback for open consultations (https://openssf.org/category/policy/cra/), and we hope we will keep receiving amazing presentations from Madalin.
- we maintain and constantly update our pages: https://openssf.org/public-policy/eu-cyber-resilience-act/ & https://policy.openssf.org/CRA/ as a one-stop-shop to learn what's hapenning around the CRA
- we worked with Open Chain on [a joint white paper](https://openssf.org/wp-content/uploads/2026/10/openssf_openchain_supplychainsecurity_100526a.pdf)
- Group chairs attended a Todo group Ospo meet-up to answer questions about the CRA
- [Manufacturer guidelines](https://policy.openssf.org/CRA/checklists/Manufacturers_September_Checklist.html)
- We developed and submitted a FOSDEM 2027 dev room proposal - and it was accepted!
- We published a member case study related to the CRA from [Ericsson](https://openssf.org/blog/2026/08/26/case-study-conquering-the-eu-cyber-resilience-act-cra-with-1400-upstream-security-fixes/), a community authored [e-book on understanding the CRA](https://openssf.org/resources/built-to-last-understanding-the-european-cyber-resilience-act-cra/) and a few other blogs relevant for CRA
- We published a member case study related to the CRA from [Ericsson](https://openssf.org/blog/2026/08/26/case-study-conquering-the-eu-cyber-resilience-act-cra-with-1400-upstream-security-fixes/), a community authored [e-book on understanding the CRA](https://openssf.org/resources/built-to-last-understanding-the-european-cyber-resilience-act-cra/) and a few other blogs relevant for CRA
- We published a member case study related to the CRA from [Ericsson](https://openssf.org/blog/2026/08/26/case-study-conquering-the-eu-cyber-resilience-act-cra-with-1400-upstream-security-fixes/), a community authored [e-book on understanding the CRA](https://openssf.org/resources/built-to-last-understanding-the-european-cyber-resilience-act-cra/) and a few other blogs relevant for CRA

- GCP WG and ORBIT Launchpad SIG members were invited to the OpenSSF Tech Talk Webinar [CRA Readiness: A Practitioner’s Guide to Compliance](https://openssf.org/resources/tech-talks/cra-readiness-a-practitioners-guide-to-compliance/) **[any more work with ORBIT Launchpad?]**
- Our WG discussions has already expanded beyond CRA. In Q3 we've seen updates from the UK, US and growing interest to explore intersection and alignments between Cyber and AI policies worldwide.
- [Blog: Grow CRA Readiness: Find Your Path Through the European Union Cyber Resilience Act](https://openssf.org/blog/2026/09/15/grow-cra-readiness-find-your-path-through-the-european-union-cyber-resilience-act/)
- [Blog: Who Checked It? Attestations, Gemara, and CRA Due Diligence](https://openssf.org/blog/2026/10/22/who-checked-it-attestations-gemara-and-cra-due-diligence/)

## Awareness SIG

The awareness SIG is led by [Megan Knight](https://github.com/businesscasualkesha) of Arm. The scope is activities that drive awareness of the work of this group and of the regulatory landscape in general. The SIG has been marshalling blog posts and the upcoming conference schedule and other outreach described above.

The main objective of the SIG is continue to be around increasing our collaboration with other WGs and broader LF community on publications, producing materials and PR plans. This is based on the feedback that we hear from our members and in other communities on (still) lack of understanding how to approach CRA by different stakeholders.

## Standards SIG

The Standards SIG has been led by [Madalin Neag](https://github.com/madalinnneag). As noted we have decided to deprecate as of this week.

The mission of the Standardization SIG has been to coordinate stakeholder engagement on cybersecurity standards related to policy, with a focus on raising awareness of standards development activities connected to the CRA. The SIG has also monitored complementary standards initiatives and policy developments to ensure members maintain visibility into the evolving regulatory and standardization landscape.

The group has supported the involvement of OpenSSF members and staff in standards activities by serving as a coordination forum to guide engagement strategies across European Standards Organizations (ESOs) and other SDOs, particularly where confidentiality practices differ from those typically used in open source communities. Through this coordination, OpenSSF representatives have enabled participation by sharing knowledge and updates, advocating for open source values, and coordinating community-level feedback on key deliverables, including the [CEN](https://www.cencenelec.eu/about-cen/) horizontal standards (such as PT1 and PT3 - see [standards map](https://policy.openssf.org/CRA/standards.html) for detail).

Here we store the Standardization SIG presentations: https://github.com/ossf/wg-globalcyberpolicy/tree/main/docs/CRA/presentations/standardization-sig/

## Questions/Issues for the TAC

Does the TAC see any issues in re-organizing our SIGs as we have indicated?

## Additional Information

Upcoming deliverables include:

* Blog post on Prague workshop
* Tech talk on November 16th focusing on "wearing multiple hats" (e.g. Manufacturer and Steward).

And more listed [here](https://docs.google.com/document/d/1dPIUfGTzzS0IQ1BYrlQSDUX0fMu-shREIFI-wMLgQ4Q/edit?tab=t.0).

The progress of this group has been tracked by the governing board. Madalin has presented at GB policy committee meetings to ensure alignment with our group and the policy committee. Megan has also presented to the GB.
