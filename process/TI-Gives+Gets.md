# "Gives and Gets" for OpenSSF Technical Initiatives (TI)
_v1.0 approved and merged by the TAC on December 11, 2023_

The OpenSSF has a large community of contributors and efforts that span the broad spectrum of open source security interests.  The Technical Initiatives (TIs) of the foundation are where community members collaborate and help craft unique solutions to address improving the security of the open source ecosystem.
In exchange for meeting certain requirements, the TIs are eligible to receive an assortment of benefits and have access to the capabilities of the Foundation's resources.  The specific requirements and benefits (aka "Gives and Gets") for each level of maturity are documented below. Note that this about the maturity of the TI itself - basically about how it operates - rather than of its product. A TI can be at an advanced level of maturity even though its product is still immature and vice versa.

Based on the specific type of work the TI is focused on (e.g., software, specification, or documentation development) the requirements and benefits may slightly differ as applicable.

Also note that benefits may actually vary based on resources and funds availability, or lack thereof.

## Sandbox level Gives & Gets

### Gives/Requirements

 * TI must be aligned with the OpenSSF mission and either be a novel approach for existing areas or address an unfulfilled need. It is expected that the initial code needed for an OpenSSF WG to work be kept within their repository and will not function as a project in its own right. Should initial WG code grow and mature that it warrants its own Project status, then it is subject to Sandbox entry requirements. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.
 * TI must maintain a diversified contributor base (i.e. not a single-vendor project).  TI must have a minimum of two maintainers with different organization affiliations.
 * WG must find a TAC sponsor that can help guide the WG through its sandbox stage.
 * Project and or SIG must find an aligned WG to host the TI or must have a TAC sponsor that can help guide the TI through the sandbox stage.
 * TI agrees to follow the [Secure Software Development Guiding Principles](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/SecureSoftwareGuidingPrinciples.md) and the [Open Source Consumption Manifesto](https://github.com/ossf/wg-endusers/tree/main/MANIFESTO).
 * If contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).
 * Provides quarterly updates to the TAC on technical vision and progress on vision.
 * TI will have a [SECURITY.md](https://github.com/ossf/project-template/blob/main/SECURITY.md) that describes how the Project manages vulnerabilities, or more broadly how the OSSF handles vulnerability reports.

### Gets/Benefits

 * TI can get assistance with Architecture & Roadmap Alignment.
 * Receives consideration as in-scope for any submission to an OpenSSF-managed conference or event.
 * TI receives guidance on technical direction from its TAC sponsor or hosting WG.
 * Reserved space for project updates in OpenSSF newsletters.
 * May request basic infrastructure support from the OpenSSF (e.g., mailing list and github repo).
 * Projects may say they are, "A sandbox project in the OpenSSF" or "An experimental project in the OpenSSF."  Gets a "sandbox" logo that is shared amongst all OpenSSF sandbox TIs.
 * Communication & Collaboration - OpenSSF mailing list, OpenSSF Slack channel, OpenSSF GitHub, OpenSSF Calendaring / Recording,  OpenSSF Social Media & External Engagement Support
 * Governance & Administration - TI Charter Development & Review, TI Technical Steering Committee Setup, TI IP & License Review, TI Operations & Maintenance, Technical Support


## Incubating level Gives & Gets

### Gives/Requirements

 All requirements of Sandbox must be fulfilled. PR filed to promote group to Incubating stage.
 * Group has met no less than 5 times within the last calendar quarter
 * Maintains a diversified contributor base (i.e. not a single-vendor project) with an active flow of contributions.  Projects must have a minimum of three maintainers with a minimum of two different organization affiliations, and document the current list of maintainers.
 * Projects must have defined a contributor guide, which makes it clear how and when contributors should be given increasing responsibilities towards maintainership of the project. (Example guides: Sigstore, AllStar)
 * Projects should be able to show adoption by multiple parties and adoption's value to the open source community and/or end users (may include adoption of beta/early versions) with the intent to showcase wide adoption by the project's consumers.
 * TI must have documented, initial group governance.
 * Maintains a point of contact for vulnerability reports in the security.md
 * Implements, practices, and refines mature software development and release practices such as following a version schema.
 * TI follows security best practices (as recommended by the OpenSSF and others), including passing the OpenSSF Best Practices criteria, secret scanning, and code scanning.
 * TIs that include code use Scorecards
 * Begins to establish the appropriate governance that enables its sustainment for potential graduation.

### Gets/Benefits

 TI eligible to receive all Gets from Sandbox plus:
 * Receives more infrastructure support from the OpenSSF (e.g., website support)
 * Receives consideration as in-scope for any submission to an OpenSSF-managed conference or event.
 * Project may request custom OpenSSF Logo for group
 * Projects may use the OpenSSF logo to promote their project (in accordance with the trademark guidelines). Projects may not be referred to as an "OpenSSF Project" or "OpenSSF $ProjectName." Projects may say they are an "OpenSSF Incubating Project."
 * With additional TAC or WG approval, may fundraise for dedicated project funds, coordinated by the OpenSSF.
 * Receives support with vulnerability disclosure from the OpenSSF (Vulnerability Disclosure WG).
 * May post project updates and tutorials to the OpenSSF blog.

## Graduated level Gives & Gets

### Gives/Requirements
All requirements of Incubating must be fulfilled and additionally:
 * TI must have documented governance and be able to demonstrate that governance in action.
 * WG and Project has a defined and documented roadmap and annual goals.
 * WG and Project has met at least 4 times over a period of at least 2 months since becoming Incubating.
 * SIG has completed a major deliverable.
 * Project must have a minimum of five participants with a minimum of three different organization affiliations.
 * TI that develops code:
   * Implements, practices, and refines mature software development and release practices, such as adherence to semantic versioning, and having a declared policy for stable releases and backported fixes.
   * TI must be able to show a consistent release cadence.
   * Maintains a point of contact for vulnerability reports and follow coordinated vulnerability disclosure practices.
   * TI should harden its build systems in accordance with the SLSA Framework
 * When applicable, Project must have completed a security audit through a third party and addressed audit findings and recommendations.

### Gets/Benefits

 TI eligible to receive all Gets from Incubating plus:
 * Receives consideration as in-scope for any submission to an OpenSSF-managed conference or event.  This includes consideration for booth space at the conference and/or the OpenSSF booth.
 * Receives advanced infrastructure support from the OpenSSF (e.g., cloud hosting, to be determined by project leads and OpenSSF Budget Committee).
 * May post project updates and tutorials to the OpenSSF blog.
 * May request OpenSSF budget for project improvements such as security audits or time-bound contracting needs.
 * May request OpenSSF budget for sustained maintainer stipends (details determined by OpenSSF and project leads).
 * With additional TAC or WG approval, may fundraise for dedicated project funds, coordinated by the OpenSSF.
 * Projects may use the OpenSSF logo to promote their project (in accordance with the trademark guidelines). Projects may be referred to as an "OpenSSF Project" or "OpenSSF $ProjectName."
 * May request considered for Grants
 * May request consideration to get Contract Developers
 * Requests for one time funding needs to include: Tech writer, Graphic designer, Security audit, Event support, Outreach, Dashboard/reports, Recognition awards, Infrastructure support for software projects (like special build, QA) (will have ongoing operational expense),  Cloud hosting (will have ongoing operational expense)
