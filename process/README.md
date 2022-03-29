# I. Overview

This policy describes the Open Source Security Foundation (OpenSSF) project life cycle process, from sandbox to archival and more. It describes the stages a project may be admitted under and what the criteria and expectations are for a given stage, as well as the acceptance criteria for a project to move from one stage to another. It also describes the Annual Review Process through which those changes will be evaluated and made.

Project progression, movement from one stage to another, allows projects to participate at the level that is most appropriate for them given where they are in their lifecycle.


# II. Stages - Definitions & Expectations

OpenSSF projects have a maturity level of sandbox, incubating, or graduated. Archived is for projects no longer in active development. The maturity level is a signal by OpenSSF as to what sorts of enterprises should be adopting different projects. Projects increase their maturity by demonstrating their sustainability to OpenSSF’s Technical Advisory Committee(TAC): that they have adoption, a healthy rate of changes, committers from multiple organizations, have adopted the OpenSSF Code of Conduct, and have achieved and maintained the Core Infrastructure Initiative Best Practices Badge.

![Project Stages](https://github.com/ossf/tac/blob/main/process/project-stages.png)

## Sandbox:

The OpenSSF Sandbox is the entry point for early stage projects and has four goals:

* Encourage public visibility of experiments or other early work that can add value to the OpenSSF mission and build the ingredients of a successful Incubation level project
* Facilitate alignment with existing projects if (and only if) this is desired
* Nurture projects (e.g. via OpenSSF Service Desk requests)
* Remove possible legal and governance obstacles to adoption and contribution by ensuring all projects adhere to OpenSSF legal, code of conduct and IP Policy requirements


## Incubating:
~~Incubating projects have access to all resources listed at https://cncf.io/services-for-projects, and have a presence at CloudNativeCon.~~
*** Needs new text ***


## Graduated:
Graduated projects signal the highest level of maturity for a OpenSSF project.


## Archived:
Archived projects are no longer in active development and are only archived after a TAC vote.

# III. Project Proposal Process

Introduction:
This governance policy sets forth the proposal process for projects to be accepted into the OpenSSF.
The process is the same for both existing projects which seek to move into the Foundation, and new projects to be formed within the OpenSSF.

## Project Proposal Requirements:

## Sandbox Projects:

Projects being submitted to the OpenSSF at the sandbox level are intended to be the entry point for early stage projects and are not required to undergo due diligence.

Sandbox projects should be early-stage projects that the OpenSSF TAC believes warrant experimentation.

* New projects that are designed to extend one or more OpenSSF projects with functionality or interoperability libraries. In the case of Kubernetes, the Sandbox is intended as a home for projects that would previously have started in the Kubernetes Incubator.
* Independent projects that fit the OpenSSF mission and provide potential for a novel approach to existing functional areas (or are an attempt to meet an unfulfilled need)
* Projects commissioned or sanctioned by the OpenSSF, including initial code for OpenSSF WG collaborations, and "experimental" projects
* Any project that realistically intends to join OpenSSF Incubation in future and wishes to lay the foundations for that

To apply for inclusion into the Sandbox, projects should use [this form](https://docs.google.com/forms/d/1bJhG1MuM981uQXcnBMv4Mj9yfV5_q5Kwk3qhBCLa_5A/edit).
The TAC will review on a rotating basis, currently every two months as of June 2020.

## Project Graduation Process: Sandbox to Incubating

Incubating projects are required to undergo due diligence as a part of the process to move from Sandbox to Incubation. Due Diligence is driven by a TAC sponsor, with two weeks for public comment before a vote is called.

Criteria:
To be accepted to incubating stage, a project must meet the sandbox stage requirements plus:

* Document that it is being used successfully in production by at least three independent end users which, in the TAC’s judgement, are of adequate quality and scope.
* Have a healthy number of committers. A committer is defined as someone with the commit bit; i.e., someone who can accept contributions to some or all of the project.
* Demonstrate a substantial ongoing flow of commits and merged contributions.
* Since these metrics can vary significantly depending on the type, scope and size of a project, the TAC has final judgement over the level of activity that is adequate to meet these criteria
* A clear versioning scheme.
* Specifications must have at least one public reference implementation.

![Incubating](https://github.com/ossf/tac/blob/main/process/incubation-process.png)

~~Projects currently in progress for consideration at the Incubating stage are tracked: https://github.com/ossf/tac/projects/7~~
*** Need new text ***

## (3) Project Graduation Process: Incubating to Graduation
Projects that wish to move from Incubating to Graduation should open a PR confirming the following criteria:
* Have committers from at least two organizations.
* Have achieved and maintained a [Core Infrastructure Initiative Best Practices Badge](https://bestpractices.coreinfrastructure.org/).
* Have completed an independent and third party security audit with results published of similar scope and quality as [this example](https://github.com/envoyproxy/envoy#security-audit) which includes all critical vulnerabilities and all critical vulnerabilities need to be addressed before graduation.
* Explicitly define a project governance and committer process. This preferably is laid out in a GOVERNANCE.md file and references an OWNERS.md file showing the current and emeritus committers.
* Have a public list of project adopters for at least the primary repo (e.g., ADOPTERS.md or logos on the project website). For a specification, have a list of adopters for the implementation(s) of the spec.
* Please include a short one-page narrative based off the Graduation template, no more than 500 words.

Projects moving from incubation to graduation are tracked here: *** Needs new link ***

## (4) Archiving Projects

Open source projects have a lifecycle and there are times that projects become inactive due to a variety of reasons. There are also cases where a project may no longer want to be supported by the TAC, or the TAC may no longer wish to recommend the use of a project.
Archiving Criteria
When voting on a proposal to archive a project, TAC members may wish to consider whether the project continues to meet the criteria for OpenSSF acceptance. The TAC may also look at activity levels in the project (https://all.devstats.cncf.io/d/53/projects-health-table?orgId=1), although it is important to note that there is a difference between a mature project that doesn't get much attention any more but is stable, versus a project that is inactive.

### Voting Process

To archive a project:
* A proposal must be put forth to the TAC repo
* The TAC will inform the project maintainers, OpenSSF end user community and wider community of all archiving proposals
* The proposal must remain open for at least 2 weeks of discussion after the maintainers are informed.
* A vote must be finalized with 2/3 approval from the TAC

### Archiving Process

What does archiving for a OpenSSF project mean?
* OpenSSF will no longer provide support for the project via service desk
* OpenSSF will list archived projects online
* Trademarks and domain names of archived projects are still hosted by the OpenSSF and the Linux Foundation
* OpenSSF can provide services such as documentation updates to help transition users.
* Other OpenSSF marketing activities will no longer be provided for the project

# IV. Annual Review Process

Sandbox projects are subject to an annual review by the TAC. This is intended to be a lightweight process to ensure that projects are on track, and getting the support they need.

Your annual review should answer the following questions:

* Include a link to your project’s devstats page. We will be looking for signs of consistent or increasing contribution activity. Please feel free to add commentary to add colour to the numbers and graphs we will see on devstats.
* How many maintainers do you have, and which organisations are they from? (Feel free to link to an existing MAINTAINERS file if appropriate.)
* What do you know about adoption, and how has this changed since your last review / since you joined Sandbox? If you can list companies that are end users of your project, please do so. (Feel free to link to an existing ADOPTERS file if appropriate.)
* How has the project performed against its goals since the last review? (We won't penalize you if your goals changed for good reasons.)
* What are the current goals of the project? For example, are you working on major new features? Or are you concentrating on adoption or documentation?
* How can the OpenSSF help you achieve your upcoming goals?
* Do you think that your project meets the criteria for incubation?

Based on this review the TAC will vote on whether to continue to sponsor the project in Sandbox. If the vote does not reach a simple majority, we will discuss archiving or other next steps with you.

Additionally, the TAC might recommend that you apply for Incubation stage. This requires extra work and due diligence so it’s not a possible outcome to move directly to Incubation from this lightweight annual review.

It is fine for a project to stay in the Sandbox indefinitely while it is still active, but if a project has genuinely stalled we can save everyone’s effort by archiving it.



