# 2026 Q3 TAC Report for Global Cyber Policy Working Group

## Overview

* GitHub repo: https://github.com/ossf/wg-globalcyberpolicy/
* Minutes doc: https://docs.google.com/document/d/1iAplSQheMgemdMnEw74uPj3oi_6rLLbFFXhg4svqIDo/edit
* Charter: https://github.com/ossf/wg-globalcyberpolicy/blob/main/CHARTER.md

This has been running since January 2025, after the Linux Foundation workshop on "Stewards and Manufacturers" in Amsterdam in December 2024. The scope of the group is to provide a forum for our members and the broader community to collaborate on Global Cybersecurity-related legislation, frameworks, and standards which facilitate conformance to regulatory requirements by open source projects and their consumers. We have been holding bi-weekly calls. We have 2 active SIGs - Awareness and Standards. The group is focusing most of its attention on the European Cyber Resilience Act (CRA) and its first September 2026 enforcement with some time put aside to monitor activities in other jurisdictions. Recognizing the growth of AI regulations (like AI Act) and standardization activities (like CEN/CLC 7 AI standards or COSAI work), AI Policy x Security is an agenda item for the WG as well. We also have drafted a [liaisons list](https://github.com/ossf/wg-globalcyberpolicy/blob/main/governance/external-liaisons.md) which is a list of external organizations we feel we need to liaise with, with a special emphasis on the [Eclipse ORC working group](https://github.com/orcwg/), to minimize overlap. 

At Open Source Summit North America, the group ran a "hybrid" f2f meeting where community members raised concerns about manufacturer awareness and the regulatory burden on open source projects, which we need to address more actively. Since then, some members from our Japanese chapter have become more active in the group, highlighting the global nature of this effort. This group of Japanese organizations produced a list of questions concerning the distinction between stewards and manufacturers under the CRA, for which a first set of draft answers has been provided. GCP WG views this as an opportunity to facilitate and document international CRA use-cases as part of our playbooks.

At the upcoming Open Source Summit Europe in Prague, we intend to run an extended CRA workshop for enterprise engineers, security officers, stewards, open source developers to stress-test real-world CRA challenges, including CRA personas across varying PDE classifications, due diligence, SBOMs, vulnerability management and reporting obligations.

We also hope to spread more awareness of our efforts at OpenSSF Community Day Europe and Open Source Summit Europe via outreach from the OpenSSF booth, including leveraging the awesome CRAfish mascot plushie. Members of GCP WG will give talks throughout entire week.

<img width="300" height="300" alt="Image" src="https://github.com/user-attachments/assets/82dc5c79-78e6-4e80-9403-139d5e473fbc" alt="The ultra-cute CRAfish plushie."/>

We have two working group co-leads: [Daniel Appelquist | Samsung](https://github.com/torgo) and [Roman Zhukov | Red Hat](https://github.com/rozhukov). [Megan Knight | Arm](https://github.com/businesscasualkesha) chairs the Awareness SIG and [Madalin Neag](https://github.com/madalinnneag) from OpenSSF staff chairs the Standards SIG. In addition, we have support from [Jeff Diecks](https://github.com/GeauxJD), [Crob](https://github.com/SecurityCRob) and [David A. Wheeler](https://github.com/david-a-wheeler).

We have a regular schedule of calls for our main working group as well as for our Awareness and Standards SIGs and take minutes in the following minutes docs:
* Main WG/Awareness SIG: https://docs.google.com/document/d/1iAplSQheMgemdMnEw74uPj3oi_6rLLbFFXhg4svqIDo/edit?tab=t.0
* Standards SIG: https://docs.google.com/document/d/1XjE5VYdyIdH32T94ZQIj0Hf5btRiKG58z3jSInY77wA/edit?tab=t.0

Our general working group call, besides being a place where SIGs report, also serves as a venue to work on general deliverables and to drive awareness with group members of related activities. 

This quarter, we have continued to work with the [ORBIT Launchpad](https://github.com/ossf/orbit-launchpad) effort, including facilitating a "CRA Monthly Tech Talk" covering ORBIT Launchpad, its progress and its future plans. As noted in their charter, Cyber Policy working group is a key stakeholder and partner for ORBIT Launchpad. This work has subsumed the work that we initially conceived of as a "Tooling" SIG in our own working group.

Since our last report:

- we continue to do a "CRA Roadshow" for communities to help navigating CRA
- we held 2 CRA Tech Talks, one dedicated to Launchpad SIG, and one dedicated to the upstream contributors and their role under the CRA building on our recently published [Guidelines for Maintainers and Developers](https://policy.openssf.org/CRA/maintainers.html)
- The new 2026 CRA Awareness and Readiness Report is out highlighting unfamiliarity (still) with the CRA with only 41% of manufacturers expect to be fully compliant by December 2027 as well as the $250k cost of maintaining private forks.
- we do comprehensive bi-weekly update on CRA standards, policy developments, collect and submit community feedback for open consultations (https://openssf.org/category/policy/cra/), thanks to Madalin
- we maintain and constantly update our pages: https://openssf.org/public-policy/eu-cyber-resilience-act/ & https://policy.openssf.org/CRA/ as a one-stop-shop to learn what's hapenning around the CRA
- we supported and contributed to [OpenChain CRA Guidance and Checklist](https://openchainproject.org/cracompliance) and continue collaborating with other communities to help navigating CRA
- promotion and citation of the [2026 CRA Awareness and Readiness Report with a foreword from us](https://www.linuxfoundation.org/research/cra-readiness-2026?hsLang=en) highlighting only 41% of manufacturers expect to be fully compliant by December 2027 as well as the $250k cost of maintaining private forks for, and other shocking numbers
- our members were guests at the 3 recent [What's in the SOSS Podcast](https://openssf.org/podcast/) talking about CRA practicalities (+more coming soon)
- we help to publish [the Understanding the European Cyber Resilience Act (CRA) e-book](https://openssf.org/cra-ebook/) authored by Sal Kimmich
- GCP WG and ORBIT Launchpad SIG members were invited to the OpenSSF Tech Talk Webinar [CRA Readiness: A Practitioner’s Guide to Compliance](https://openssf.org/resources/tech-talks/cra-readiness-a-practitioners-guide-to-compliance/)
- 2 more CRA Blogs are out:[ Case Study: Conquering the EU Cyber Resilience Act (CRA) with 1,400 Upstream Security Fixes](https://openssf.org/blog/2026/08/26/case-study-conquering-the-eu-cyber-resilience-act-cra-with-1400-upstream-security-fixes/) and [CRA Readiness: A Practitioner’s Guide to Compliance](https://openssf.org/policy/cra/2026/08/14/cra-monthly-tech-talk-orbit-launchpad-sig-updates/)
- We organized the European Open Source Security Forum in Brussels, bringing together policymakers, industry representatives, and the open source community to discuss how to translate the requirements of the CRA into practical implementation."

## Awareness SIG

The awareness SIG is led by [Megan Knight](https://github.com/businesscasualkesha) of Arm. The scope is activities that drive awareness of the work of this group and of the regulatory landscape in general. The SIG has been marshalling blog posts and the upcoming conference schedule and other outreach described above.

The main objective of the SIG is continue to be around increasing our collaboration with other WGs and broader LF community on publications, producing materials and PR plans. This is based on the feedback that we hear from our members and in other communities on (still) lack of understanding how to approach CRA by different stakeholders.

## Standards SIG

The Standards SIG is led by [Madalin Neag](https://github.com/madalinnneag).

The mission of the Standardization SIG has been to coordinate stakeholder engagement on cybersecurity standards related to policy, with a focus on raising awareness of standards development activities connected to the CRA. The SIG has also monitored complementary standards initiatives and policy developments to ensure members maintain visibility into the evolving regulatory and standardization landscape.

The group has supported the involvement of OpenSSF members and staff in standards activities by serving as a coordination forum to guide engagement strategies across European Standards Organizations (ESOs) and other SDOs, particularly where confidentiality practices differ from those typically used in open source communities. Through this coordination, OpenSSF representatives have enabled participation by sharing knowledge and updates, advocating for open source values, and coordinating community-level feedback on key deliverables, including the [CEN](https://www.cencenelec.eu/about-cen/) horizontal standards (such as PT1 and PT3 - see [standards map](https://policy.openssf.org/CRA/standards.html) for detail).

Here we store the Standardization SIG presentations: https://github.com/ossf/wg-globalcyberpolicy/tree/main/docs/CRA/presentations/standardization-sig/

As an OpenSSF community, we responded to the following public consultations: 

- AI act standards
- ENISA's public consultation on their Secure Update Mechanisms Technical Advisory
- European Interoperability Framework (EIF), complementing the Linux Foundation Europe (LFEU) submission
- [Public Consultation on the NIS 2 Directive](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/14578-The-EU-Cybersecurity-Act/F33400854_en)
- [Public Consultation on the EU Cybersecurity Act](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/14578-The-EU-Cybersecurity-Act/F33400612_en)
- [Draft Commission guidance on the Cyber Resilience Act](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/16959-Draft-Commission-guidance-on-the-Cyber-Resilience-Act/F33390215_en)
- [European Open Digital Ecosystem Strategy](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/16213-European-Open-Digital-Ecosystems/F33370575_en)
- [Public Procurement Directive revision](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/15492-EU-public-procurement-rules-revision/F33368454_en)
- [Public Consultation on the proposal for a revision of Regulation (EU) No 1025/2012](https://drive.google.com/file/d/107UfUKJJ3lhT0n-GoK2cbYUNsnEQtkGx/view?usp=sharing)
- [ENISA Technical Advisory for Secure Use of Package Managers](https://drive.google.com/file/d/1kaU470ZqtXxbXU4BRdbVwakMSCCd9hQy/view?usp=sharing)
- [SBOM Landscape Analysis – Towards an Implementation Guide](https://drive.google.com/file/d/1jRrT7iw3irIm1tuQvDfyWj9tedc3U0b4/view?usp=sharing)
- [RED DA Repeal](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/14766-Cybersecurity-repeal-of-Delegated-Regulation-supplementing-the-Radio-Equipment-Directive/F33363045_en)
- [ENISA Survey on SBOM State of the Art](https://drive.google.com/file/d/1OXxdngIc8Rtys4BhP8kgO8aAsJFihhCH/view?usp=sharing)
- [Call for evidence for Digital Omnibus](https://ec.europa.eu/info/law/better-regulation/have-your-say/initiatives/14855-Simplification-digital-package-and-omnibus/F33088470_en)

A core component of the SIG’s work has been facilitating community’s participation in public consultations related to cybersecurity standards and policy. The group has raised awareness of consultation opportunities, shared relevant information, and coordinated the consolidation of feedback so that responses reflect the collective expertise of the OpenSSF community.

The SIG has also acted as an information-sharing platform on related policy developments, standards initiatives, funding opportunities, and key steps for CRA implementation, including updates on delegated and implementing acts, guidance materials, roadmaps, and developments from relevant European institutions and authorities.

The SIG's mission has been to coordinate between stakeholders regarding engagement in Standards work related to cybersecurity policy. This is complicated by the fact that many of these standards organizations have a different approach to confidentiality than the OpenSSF. The discussions of this group have helped to guide the engagement of OpenSSF staff within some of these efforts.

The SIG's main work this year has been on raising awareness of relevant standards efforts, disseminating information to members about these efforts, and highligting when public consultations are open / helping members participate in these consultations.

## Questions/Issues for the TAC

We see growing interest to our WG from manufacturers and other community members based in APAC (Japan, Korea, etc.) to the CRA but also beyond. As well as emerging cyber- and AI- standards and regulations attempts around open source. We'd like to understand if broader OpenSSF and LF can help us with international collaborations and connections to experts and bodies in different countries beyond US and EU (like regional CIRTs, Cyber Agencies, etc.).

## Additional Information

Upcoming deliverables include:

* [Manufacturer guidelines](https://docs.google.com/document/d/10wZFyWMt97-3rCd-cMBWW0KvXnOyOEPCYnen1fBvNXE/edit?tab=t.0)
* Playbook/guideline for downstream on how to engage with upstream contributors
* White paper on OpenChain-OpenSSF interplay/alignment

And more listed [here](https://docs.google.com/document/d/1dPIUfGTzzS0IQ1BYrlQSDUX0fMu-shREIFI-wMLgQ4Q/edit?tab=t.0).

The progress of this group has been tracked by the governing board. Madalin has presented at GB policy committee meetings to ensure alignment with our group and the policy committee. Megan has also presented to the GB.
