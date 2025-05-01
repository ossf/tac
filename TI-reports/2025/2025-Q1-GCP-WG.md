# 2025 Q1 TAC Report for Global Cybersecurity Policy Working Group

## Overview

* GitHub repo: https://github.com/ossf/wg-globalcyberpolicy/
* Minutes doc: https://docs.google.com/document/d/1iAplSQheMgemdMnEw74uPj3oi_6rLLbFFXhg4svqIDo/edit?tab=t.0#heading=h.9m0zi4b0wnne 

This group has been formed in January 2025, after the Linux Foundation workshop on "Stewards and Manufacturers" in Amsterdam in December 2024. The shape of this group is very much based on consensus of that workshop. The scope of the group is to provide a forum for our members and the broader community to collaborate on Global Cybersecurity-related legislation, frameworks, and standards which facilitate conformance to regulatory requirements by open source projects and their consumers. We have been holding bi-weekly calls. We have agreed [our charter](https://github.com/ossf/wg-globalcyberpolicy/blob/main/CHARTER.md) and formed 3 SIGs - Awareness, Tooling and Standards. The group is focusing most of its attention on the European Cyber Resilience Act (CRA). We also have drafted a [liaisons list](https://github.com/ossf/wg-globalcyberpolicy/blob/main/governance/external-liaisons.md) which is a list of external organizations we feel we need to liaise with.

We have two working group co-leads: [Daniel Appelquist | Samsung](https://github.com/torgo) and [Mike Bursell | Confidential Compute Consortium](https://github.com/MikeCamel) with support from [Crob](https://github.com/SecurityCRob), [Jeff Diecks](https://github.com/GeauxJD) and [Fukami](https://github.com/fukami) from OpenSSF staff.

We are also exploring folding in the "CRA tech bi-weekly" call into the remit of this group.

Since forming, we have spent a fair amount of time refining the charter, in particular the wording around how we open up the group as much as possible while also making it clear who gets to vote when and if a vote is required.

We now have a schedule of calls for our SIGs and have started to take minutes in our main minutes doc. We are operating in a similar mode to the Best Practices Working group, with our SIGs reporting into the main working group call. 

We held a special session at LF Member Summit which is also minuted in our minutes doc.

## Awareness SIG

The awareness SIG is the furthest along. It's led by [Megan Knight](https://github.com/businesscasualkesha), Arm. The scope is activities that drive awareness of the work of this group and of the regulatory landscape in general. The SIG has been marshalling blog posts, upcoming conference schedule, as well as the CRA introductory course.

Blog Posts:
* [Linux Foundation Europe and OpenSSF Launch Initiative to Prepare Maintainers, Manufacturers, and Open Source Stewards for Global Cybersecurity Legislation
](https://openssf.org/press-release/2025/01/31/linux-foundation-europe-and-openssf-launch-initiative-to-prepare-maintainers-manufacturers-and-open-source-stewards-for-global-cybersecurity-legislation/)
* [What Will My Business Need to do for the CRA?](https://openssf.org/blog/2025/03/24/what-will-my-business-need-to-do-for-the-eu-cra/)
* [Does the EU CRA affect my business?](https://openssf.org/blog/2025/02/20/does-the-eu-cra-affect-my-business/)
* [OpenSSF Policy Summit DC 2025 Recap](https://openssf.org/blog/2025/03/14/openssf-policy-summit-dc-2025-recap/)

## Tooling SIG

The Tooling SIG has is still in start-up mode. However we have one lead, [Puerco](https://github.com/puerco), and we're looking for a co-lead. The scope is to coordinate work on relevant tooling and processes. What tools already exist out there that can help maintainers, stewards and manufacturers? What additional features do we need from existing tools?

## Standards SIG

The Standards work stream is progressing. Currently we have one lead [Tobias](https://github.com/0xAverageUser), we are actively seeking a co-lead.
The SIGs mission was defined as: 

> The OpenSSF Global Cyber Policy WG - Standardisation SIG’s mission is to align regulatory (e.g., the EU CRA) compliance strategies & standards across open-source participants to ensure clarity, consistency, and industry-wide adoption and coordination.

To meet that objective, we will likely start developing an index of curated Minutes, Resources, and References from OpenSSF, Eclipse, and OpenJS, as a building, deploying maintaining and a database ("index") for the EU CRA. 

Initially, the SIG will promote "Baseline" as a potential standard for CRA compliance. CRob, Jory Burson and Wheeler will present recommended OpenSSF and LF specifications for ETSI and CEN/CENELEC consideration during the April 1, 2025 call.

Minutes available here: [SIG Minutes Document](https://docs.google.com/document/d/1XjE5VYdyIdH32T94ZQIj0Hf5btRiKG58z3jSInY77wA/view?tab=t.0).

## Questions/Issues for the TAC

None at this time.

## Additional Information

Security Insights spec recently [incorporated](https://github.com/ossf/security-insights-spec/pull/117#pullrequestreview-2728878937) `steward` as a field in their schema. This is in response to an [issue](https://github.com/ossf/security-insights-spec/issues/106) we raised about how a project can specify its steward, which in turn came out of a [discussion](https://github.com/ossf/wg-globalcyberpolicy/issues/43) in this working group about whether we need a `steward.md` file so that projects can indicate what organization is playing a "stewardship" role for them, which has a specific meaning under the CRA. This also showcases how this group seeks to work with other groups.


