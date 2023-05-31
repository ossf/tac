# Becoming an OpenSSF Project

The OpenSSF's mission is to inspire and enable the community to secure the open source software we all depend on. OpenSSF's top priority is the security of existing open source projects however, there are missing pieces in the tooling needed to improve the security of these projects. The development of these pieces are what OpenSSF aims to steward and support.

## Project Life Cycle

New [Projects](../organizational-structure-overview.md#definitions) to the OpenSSF, and progression through the project lifecycle, are approved by the Technical Advisory Council (TAC). Projects follow the Sandbox, Incubating, Graduated, and Archived lifecycle stages defined below. Projects that seek widespread adoption and end user use are expected to progress through the stages. Projects coming to OpenSSF that already meet the entry requirements may enter the Incubating stage directly.

## Project Oversight

Projects report either directly to the Technical Advisory Council (TAC) or to a specific Working Group (WG). When a Project reports into a specific WG, that WG can support the Project's progression and provide recommendations to the TAC. The overseeing group provides Projects advice on technical direction, and is a point of escalation or dispute resolution in technical disagreements. The overseeing group does not set the charter or operations for Projects, but ensures Projects operate in line with the [OpenSSF values.](https://openssf.org/about/values/) 

<!-- TOC -->

  - [Stages - Definitions & Expectations](#stages---definitions--expectations)
      - [Sandbox](#sandbox)
      - [Incubating](#incubating)
      - [Graduated](#graduated)
      - [Archived](#archived)
  - [Submission Process](#submission-process)

<!-- /TOC -->


## Stages - Definitions & Expectations

A project's lifecycle stage is a signal of maturity level. Projects progress through the lifecycle by demonstrating their maturity in technical vision, impact to the open source community (such as adoption), and sustainability in governance and contributors. All projects, at all stages, are expected to abide by the [OpenSSF Code of Conduct](https://openssf.org/community/code-of-conduct/).

![Project Stages](/process/project-stages.png)

### Sandbox

The OpenSSF Sandbox is the entry point for early stage Projects and has four goals:

* Encourage experimentation and open collaboration that can add value to the OpenSSF mission and build the ingredients of a successful Incubation level Project.
* Facilitate alignment with existing Working Groups or Projects if this is desired (there may be cases where pursuit of different approaches is desirable).
* Nurture Projects.
* Remove possible legal and governance obstacles to adoption and contribution by ensuring all projects adhere to OpenSSF legal, code of conduct, and IP Policy requirements.

#### Project Responsibilities
* Provides bi-annual updates to the TAC on technical vision and progress on vision.
* Maintains a diversified contributor base (i.e. not a single-vendor project).
* Follows security best practices (as recommended by the OpenSSF and others), including passing the [OpenSSF Best Practices criteria](https://bestpractices.coreinfrastructure.org/en/criteria/0).
* Provides project updates to OpenSSF Marketing Committee as requested.

#### Project Support
* Receives guidance on technical direction from TAC.
* Receives consideration as in-scope for any submission to an OpenSSF-managed conference or event.
* Receives OpenSSF Code of Conduct Committee support.
* Reserved space for project updates in OpenSSF newsletters.
* May request infrastructure support from the OpenSSF.
* Projects, sponsors, and contributors may not promote the project with the OpenSSF logo or be referred to as an "OpenSSF Project" or "OpenSSF $ProjectName." Projects may say they are, "A sandbox project in the OpenSSF" or "An experimental project in the OpenSSF."

#### Sandbox Entry Requirements and Considerations

* Projects must have a minimum of two maintainers with different organization affiliations.
* Projects must be aligned with the OpenSSF mission _and_ either be a novel approach for existing areas or address an unfulfilled need. It is expected that the initial code needed for an OpenSSF WG to work be kept within their repository and will not function as a project in its own right. Should initial WG code grow and mature that it warrants its own Project status, then it is subject to Sandbox entry requirements. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.
* If contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).

See [Submission Process](#submission-process) below and [Sandbox application](templates/PROJECT_NAME_sandbox_stage.md).


### Incubating

Incubating projects represent maturing but not fully realized projects. Incubating projects have an established technical vision and working project, but are still refining implementation, discovering (and adapting to) new use cases, and operating as an open source team.

#### Project Responsibilities
* Provides bi-annual updates to the TAC on technical vision and progress on vision.
* Maintains a diversified contributor base (i.e. not a single-vendor project) with an active flow of contributions.
* Follows security best practices (as recommended by the OpenSSF and others), including achieving a [Silver OpenSSF Best Practices badge](https://bestpractices.coreinfrastructure.org/en/criteria).
* Maintains a point of contact for vulnerability reports.
* Implements, practices, and refines mature software development and release practices such as following a version schema.
* Begins to establish the appropriate governance that enables its sustainment for potential graduation.

#### Project Support
* Receives guidance on technical direction from TAC.
* Receives a TAC or WG sponsor for guidance as an Incubation project.
* Receives consideration as in-scope for any submission to an OpenSSF-managed conference or event.
* Receives OpenSSF Code of Conduct Committee support.
* Receives infrastructure support (details determined by project leads and OpenSSF Budget Committee).
* Receives support with vulnerability disclosure from the OpenSSF (Vulnerability Disclosure WG).
* May post project updates and tutorials to the OpenSSF blog.
* May request OpenSSF budget for project improvements such as security audits or time-bound contracting needs.
* With additional TAC or WG approval, may fundraise for dedicated project funds, coordinated by the OpenSSF.
* Projects may use the OpenSSF logo to promote their project (in accordance with the trademark guidelines). Projects may not be referred to as an "OpenSSF Project" or "OpenSSF $ProjectName." Projects may say they are an "OpenSSF Incubating Project."

#### Incubation Entry Requirements and Considerations

* Projects must have a minimum of three maintainers with a minimum of two different organization affiliations.
* Projects should be able to show adoption by multiple parties and adoption's value to the open source community and/or end users (may include adoption of beta/early versions) with the intent to showcase wide adoption by the project's consumers.
* Projects must be aligned with the OpenSSF mission _and_ either be a novel approach for existing areas or address an unfulfilled need. It is expected that the initial code needed for an OpenSSF WG to work be kept within their repository and will not function as a project in its own right. Should initial WG code grow and mature that it warrants its own Project status, then it is subject to Sandbox entry requirements. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.
* Projects must have documented, initial project governance.

#### Project Process: Sandbox to Incubation and direct entry to Incubation

Projects are required to undergo technical due diligence as a part of the process of entering Incubation, whether as a move from Sandbox to Incubation or entering Incubation directly. Technical Due Diligence is driven by a TAC or parent WG sponsor with close collaboration of the project. Once the diligence is complete and the proposal made, the Due Diligence document is made available to the community for two weeks to solicit public comment before a TAC vote is called.

See [Submission Process](#submission-process) below and [Incubation application](templates/PROJECT_NAME_incubation_stage.md).


### Graduated

Graduated projects signal the highest level of maturity for an OpenSSF project. Graduated projects have consistent, mature open source development practices with sustained contribution and activity. 

#### Project Responsibilities

* Provides bi-annual updates to the TAC on technical vision and progress on vision.
* Maintains a diversified contributor base (i.e. not a single-vendor project) with an active flow of contributions.
* Follows security best practices, including achieving a [Gold OpenSSF Best Practices badge](https://bestpractices.coreinfrastructure.org/en/criteria).
* Maintains a point of contact for vulnerability reports and follow coordinated vulnerability disclosure practices.
* Implements, practices, and refines mature software development and release practices, such as adherence to semantic versioning, and having a declared policy for stable releases and backported fixes.

#### Project Support
* Receives guidance on technical direction from TAC.
* Receives consideration as in-scope for any submission to an OpenSSF-managed conference or event.
* Receives OpenSSF Code of Conduct Committee support.
* Receives infrastructure support (details determined by project leads and OpenSSF Budget Committee).
* Receives support with vulnerability disclosure from the OpenSSF (Vulnerability Disclosure WG).
* May post project updates and tutorials to the OpenSSF blog.
* May request OpenSSF budget for project improvements such as security audits or time-bound contracting needs.
* May request OpenSSF budget for sustained maintainer stipends (details determined by OpenSSF and project leads).
* With additional TAC or WG approval, may fundraise for dedicated project funds, coordinated by the OpenSSF.
* Projects may use the OpenSSF logo to promote their project (in accordance with the trademark guidelines). Projects may be referred to as an "OpenSSF Project" or "OpenSSF $ProjectName."

#### Graduated Project Entry Requirements and Considerations

* Projects must have maintainers with a minimum of three different organizational affiliations.
* Projects must be aligned with the OpenSSF mission and be a novel approach for existing areas or address an unfulfilled need. Projects with duplicate, similar or competing functionality to an existing OpenSSF project may be denied Graduation status if the TAC does not see technical justification for overlapping projects.
* Projects must be able to show adoption by multiple parties, which could be production deployments or substantial use by established open source communities, and demonstrate the value of that adoption to either the end users or the open source community —  effectively wide adoption by the project's consumers.
* Projects must be able to show a consistent release cadence.
* Projects must have documented project governance and be able to demonstrate that governance in action.
* When applicable, projects must have completed a security audit through a third party and addressed audit findings and recommendations.

#### Project Graduation Process: Incubating to Graduation

Graduation requires undergoing due diligence as a part of the process to move from Incubation to Graduation. Due diligence is driven by a TAC or parent WG sponsor. For projects seeking Graduation, this may be a light refresh of the existing due diligence to cover the additional criteria, or a more in depth due diligence depending on the level of change the project has incurred since the original due diligence of Incubation was performed. Once the diligence is confirmed by the Sponsor to be complete and the proposal made, the Due Diligence document is made available to the community for two weeks to solicit public comment before a TAC vote is called.

See [Submission Process](#submission-process) below and [Graduation application](templates/PROJECT_NAME_graduation_stage.md).

### Archived

Open source projects have a lifecycle and there are times when projects become inactive due to a variety of reasons. There are also cases where a project may no longer want to be supported by the OpenSSF, or the OpenSSF TAC may no longer wish to recommend the use of a project. Archiving happens through a vote of the TAC, and can be requested by the corresponding project's lead(s) or a TAC member.

#### Archiving Considerations

When voting on a proposal to archive a project, TAC members may consider:
* If the project has consistently met the Project Requirements.
* If the project still supports the OpenSSF mission.
* If the project's inactivity or inconsistent maintenance presents a user security risk.
* If the project's design or approach is no longer a recommended best practice.

#### Archive Process

Archived projects are no longer in active development and are only archived after a TAC vote.

What does archiving for an OpenSSF project mean?
* OpenSSF will no longer provide budgetary, event, or marketing support for the project.
* Trademarks and domain names of archived projects are still hosted by the OpenSSF and the Linux Foundation.
* Project maintainers may request trademark transfers from the OpenSSF and the Linux Foundation.
* OpenSSF can provide services such as documentation updates to help transition users.

To archive a project:
* A proposal must be made to the TAC or WG repo.
* The TAC or parent WG will inform the project maintainers, OpenSSF end user community and wider community of all archiving proposals.
* The proposal must remain open for at least 2 weeks of discussion after the maintainers are informed.
* A vote must be finalized with 2/3 approval from the TAC or parent WG.

See [Submission Process](#submission-process) below and the [Archive application](templates/PROJECT_NAME_archived_stage.md).


## Submission Process

### Project creation or change of lifecycle stage

For initiating the creation of a new project or for requesting a change of a project's lifecycle stage, an application must be submitted to the TAC. To this end, a maintainer of the project (or anyone in the case of Archived projects) creates a PR in this repository with the following changes:

* A new file in the `project-lifecycle-documents` directory containing all information requested for a project creation or a lifecycle change review. This file must be based on the template for the respective lifecycle stage in the `templates` directory. The `PROJECT_NAME_` prefix of the template must be replaced by the project name.

* Modification of the table listing all projects in the [README](../README.md) of this repository by either updating the status field of the project in the table to the intended new lifecycle stage or by adding the project to the table in case of a project creation request.

The TAC members review the PR and upon approval according to voting criteria defined in the [OpenSSF charter](https://cdn.platform.linuxfoundation.org/agreements/openssf.pdf), the PR can be merged. The new project has been created and the new lifecycle stage is in effect after the PR is merged.


### IP policy and license review

Contributing an existing project to the OpenSSF requires a one-time IP policy and license review with The Linux Foundation. To enable tracking of the IP policy and license review process, an issue in the TAC repo must be created. The results of the review as well as all relevant data (e.g., results of license scans) must be attached to this issue. Finally, the issue must be mentioned in the project creation PR and the latter can only be merged once the issue tracking the IP policy and license review has been closed.
