# OpenSSF Technical Vision (v1), left for reference

We envision a future where participants in the open source ecosystem use and share high quality software, with security handled proactively, by default, and as a matter of course:
- Developers can easily learn secure development practices and are proactively guided by their tools to apply those practices and automatically informed when action is needed to prevent, remediate, or mitigate security issues.
- Developers, auditors, and regulators can create and easily distribute security policies that are enforced through tooling and automation, providing continuous assurance of the results.
- Developers and researchers can identify security issues (including unintentional vulnerabilities and malicious software) and have this information swiftly flow backwards through the supply chain to someone who can rapidly address the issue.
- Community members can provide information and notifications about product defects, mitigations, quality, and supportability and have this information rapidly flow forward across the ecosystem system to all users, and users can rapidly update their software or implement mitigations as appropriate.

The Open Source Security Foundation (OpenSSF) provides tools, services, training, infrastructure, and resources to achieve this vision.

---

# OpenSSF Values (pulled from [https://openssf.org/about/values/](https://openssf.org/about/values/))
- **Public good**: We believe the security of open source is a public good and as an industry we have an obligation to address it for the commonwealth of the community.

- **Openness and Transparency**: We commit to encouraging all interested stakeholders to participate in the foundation and its working groups. The foundation’s work will be made publicly available.

- **Maintainers** First: We approach the work of contributing to improving the security of open source software with a strong respect for open source maintainers and developers, with an intent to create resources and tooling to help scale security improvements to benefit the open source ecosystem as a whole.

- **Diversity, Inclusion, and Representation**: We work to actively invite and include people from a range of backgrounds, locations, identities, and perspectives, and promote a culture of mutual respect and inclusiveness as a requirement for participation

- **Agility and Delivery**: We work to deliver concrete and useful outputs and tools to help make open source more secure. We do so in a manner that enables us to learn from experience and experiment, and improve our outputs accordingly.

- **Credit where credit is due**: We commit to a culture where people’s contributions are recognized and acknowledged fairly.

- **Neutrality**: We don’t bias toward any ecosystem, vendor or platforms.

- **Empathy**: We recognize and understand each other’s challenges, perspective and circumstances. We commit to a culture of listening and caring for multiple opinions.

# OpenSSF Technical Vision (v2 proposed)

> _Note: the bullet points that are included below in block quotes would not be included in the final version of the vision, but are listed for reference/discussion._

An aspirational view of the future we seek to create in 2-5 years:

### OpenSSF is a well-respected strategic partner to both large OSS foundations and individual OSS projects
- Clearly positioned within broader ecosystem with a clear charter
- Catalyst for change and improving “secure by default”
- Trusted voice to consumers, producers, and market

> Approaches to achieve the above statement:
> - (proposed) Update OpenSSF website to reflect updated positioning
> - (proposed) Ensure we have specific segmentation strategies for targeted audiences
> - (proposed) Regular TAC / GB interlock with other OSS foundations with regular feedback into (annual?) planning cycles
> - (proposed) Content / marketing plan with measurements on reach and impact
> - Alpha/Omega: how to position?
> - Securing Software Repositories WG
> - Operator or financial sponsor of common centralized services (e.g. OSS-SIRT, MFA help desk, OpenSSF office hours)

### OpenSSF is an influential advocate for efforts that are aligned with its mission
- Support development and use of meaningful, actionable standards (e.g. SBOM formats, MFA?)
- Catalyze improvements / action through targeted investment
- ...

> Approaches to achieve the above statement:
> - Oversees time-bound projects to advocate for specific outcomes, e.g.
>     - Great MFA distribution project
>     - Sponsor of audits (via OSTIF & others) for critical projects
> - TAC endorsement of specific standards-track efforts, to be incorporated across other OpenSSF foundation workstreams
>     - Direct funding / staffing on tooling and adoption efforts (e.g. SPDX-Python)?
>     - _question_: would it make sense to mandate use of the standard within foundation-hosted projects?
> - (proposed) Engagement across platforms where developers already are (meetups, conferences, StackOverflow, etc)
>     - _idea_: should OpenSSF hire dev-rel resources to staff this?

### Consumers of OSS can leverage clear & consistent trusted signals to better understand the security profile of open source content:
- Provenance of source code & artifacts
- Security posture of projects and artifacts
- Community health
- Maintainer intent (e.g. project archived, not responsive to PRs, etc)
- Consumer demand / criticality score(?)
- ...

> Approaches to achieve the above statement:
> - OpenSSF hosts projects that produce these signals and/or make them trustworthy and actionable
>     - OpenSSF funds the adoption of its projects (via SOS)
> - OpenSSF hosts working groups that provide guidance on how to make use these signals
> - Badging programs for projects
> - End Users WG

### Producers of OSS (at all skill levels; also explicitly are consumers of OSS through dependencies) have access to:
- Best practices guides, education, etc
- Extremely low-friction tooling to make security processes less onerous, more accurate, and trusted (burden of maintenance offloaded through opt-in automation)
- Ability to start new projects from a more secure default position
- Ensure sufficient staffing, auditing, pen testing, rigor for critical projects
- ...

> Approaches to achieve the above statement:
> - OpenSSF hosts projects that produce tools that minimizes burden on project maintainers
> - OpenSSF hosts working groups that publish & maintain recommendations on how to produce secure OSS, interface with consumers, etc