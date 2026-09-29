# 2026 Q3 ORBIT WG

## Overview

The ORBIT working group spent this quarter restructuring to absorb growth. Three new control catalogs have been proposed for contribution to ORBIT, and rather than chartering a SIG for each, the WG has evolved the OSPS Baseline SIG into a parent ORBIT Definitions SIG that will govern all catalogs under a shared lifecycle. Minder was recognized as an ORBIT Technical Initiative, and the Baseline Scanner harness, Privateer, was approved by the TAC as a sandbox project.

Gemara shipped a Python SDK and several Go SDK releases, Security Insights gained a web-based editor, and the Launchpad SIG's CRA work has progressed from legal review into a draft catalog (CRAB-FOSC).

## ORBIT Definitions SIG

https://github.com/ossf/orbit-definitions

### Purpose of ORBIT Definitions SIG

The Definitions SIG develops and maintains a portfolio of definition artifacts (specifications, criteria sets, and supporting vocabularies) that open source projects and their consumers can adopt to describe and improve security posture. It evolves from the OSPS Baseline SIG, and maintainership is assigned per artifact, with the SIG coordinating shared tooling, release processes, mappings, and Gemara-compliant representations across all of them.

### Current Status of ORBIT Definitions SIG

- Following a WG vote on [ossf/wg-orbit#44](https://github.com/ossf/wg-orbit/issues/44), the Baseline SIG is being expanded into a parent initiative for all ORBIT catalogs rather than adding a new SIG (and TSC seat) per catalog
- The [parent charter](https://github.com/ossf/wg-orbit/blob/main/technical-initiatives/sigs/definitions-sig-charter.md) is in place, and the SIG repository now holds the SIG's policies and procedures; artifacts live in their own repositories with their own maintainers and local governance
- The SIG publishes a register of all development efforts with a lifecycle status (Proposed, Draft, Released, Retired). Anything not Released is a draft and must not be presented as final. The register currently lists:
  - **OSPS Baseline** ([ossf/security-baseline](https://github.com/ossf/security-baseline)), Released
  - **OSPS Templates** ([ossf/osps-templates](https://github.com/ossf/osps-templates)), Draft
  - **CRA Baseline for Open Source Consumption (CRABFOSC)** ([ossf/crabfosc](https://github.com/ossf/crabfosc)), Draft
  - **AI Project Security Baseline**, Proposed, no repository yet
- IBM's AI Governance and Security Baseline, built on the Baseline infrastructure and generators and expressed in Gemara controls format, has been presented to the WG as the basis for the proposed AI Project Security Baseline and has attracted an outside academic contributor
- The Common Mitigation Enumeration (CME) project from Red Hat presented to the WG as a potential collaborator, proposing a taxonomy of defensive controls mapped to CVSS vectors to complement CWE and CVE

**OSPS Baseline** (https://github.com/ossf/security-baseline)

- TAC approved a top-up of technical writer funding; the tech writing effort is complete with some final PRs pending resolution
- A release is being prepared covering all proposed changes since February; proposed changes to the legal control details ([#536](https://github.com/ossf/security-baseline/issues/536)) remain open and are excluded
- Mapping documents have been split out into separate documents for individual publication
- Baseline is participating in the Linux Foundation standardization process through the Software Supply Chain Security Project, which is driving the ongoing standardization discussion ([#511](https://github.com/ossf/security-baseline/issues/511))
- The Best Practices Badge site (bestpractices.dev) now serves the current Baseline release in all nine supported languages, and its repository has moved into the `ossf` GitHub org

### Up Next for ORBIT Definitions SIG

The SIG is currently working on the following:

- Scheduling a regular Definitions SIG meeting
- Writing the policies the parent charter obligates the SIG to maintain, none of which exist yet: acceptance criteria for new efforts, a publication process for drafts to become releases, shared release tooling, artifact status and retirement labeling, a contributor ladder with terms of at most one year, and a decision-making process
- Completing the Baseline-to-Gemara mapping (initial AI-assisted draft exists)
- A standardization guide and role definitions for Baseline to support the LF standardization process

The SIG has identified a need for the following, but work is not yet underway:

- A repository and maintainers for the AI Project Security Baseline
- Resolution of the legal requirements discussion in Baseline

### Funding requests

None at this time.

## ORBIT Launchpad SIG

https://github.com/ossf/orbit-launchpad

### Current Status of ORBIT Launchpad SIG

- Following the legal review reported last quarter, the SIG has held a series of working sessions on **CRAB-FOSC** (CRA Baseline For Open Source Consumption), a Baseline-derived catalog for consumers and manufacturers
- 13 requirements have been agreed upon and objectives are defined; an initial PR to a new catalog repository is open at [ossf/crabfosc#1](https://github.com/ossf/crabfosc/pull/1)
- A communications plan is in flight in coordination with the CRA Awareness SIG, the Cyberpolicy SIG, and OpenSSF Marketing
- The Supply Chain Integrity WG has expressed interest in coordinating with Launchpad, given SCI's new focus on maintainers versus Launchpad's focus on consumers and manufacturers
- A joint Tech Talk with the Gemara project is being planned

### Up Next for ORBIT Launchpad SIG

The SIG is currently working on the following:

- Organizing CRAB-FOSC requirements into categories and objectives, followed by a v1 release
- Discussing measurement capabilities in lockstep with Baseline Scanner development
- Mappings from CRAB-FOSC to other efforts
- Planning for 2027 and the Prague event

The SIG has identified a need for the following, but work is not yet underway:

- A Minder demo for the `ossf` GitHub org during a Launchpad call

### Funding requests

None at this time.

## OSPS Assessments SIG

https://github.com/ossf/security-assessments

### Current Status of OSPS Assessments SIG

The SIG remains inactive. OpenSSF staff have flagged that *LFEL1005: Security Self-Assessments for Open Source Projects* needs an update, with a deadline of end of December 2026; if no progress is made, the course is expected to be unpublished until it can be refreshed.

### Up Next for OSPS Assessments SIG

The WG is currently working on the following:

- Coordinating a content review with CNCF TAG Security
- Standing up a GitHub Pages website for the self-assessment content as a prerequisite to the course update

The SIG has identified a need for the following, but work is not yet underway:

- Recruit more interested contributors (help wanted!)
- Creation of regulatory compliance assessment recommendations
- Creation of third-party audit assessment recommendations

### Funding requests

None at this time.

## Security Insights SIG

[https://github.com/ossf/security-insights](https://github.com/ossf/security-insights) https://github.com/ossf/si-tooling

### Current Status of Security Insights SIG

- A form-and-wizard editor for creating new insights files is live at [security-insights.openssf.org/editor](https://security-insights.openssf.org/editor/), contributed by Michael Scovetta
- Website and documentation updates were merged in July
- Minder can now generate a `SECURITY-INSIGHTS.yml` for an enrolled repository (first exercised on [ossf/community#49](https://github.com/ossf/community/pull/49))
- OpenSSF leadership is planning an initiative to roll out Security Insights across the remaining OpenSSF projects

### Up Next for Security Insights SIG

- A proposal is underway for improved AI support in insights file creation
- Review the strictness of the project linter, which currently rejects some tool-generated files over trailing newlines
- Business as usual, responding to community feedback on GitHub issues and in ORBIT community calls

### Funding requests

None at this time.

## Gemara

https://github.com/gemaraproj/gemara

### Current Status of Gemara

Releases this quarter:

- Gemara spec v1.3.0, adding an optional type to EvaluationLogs to capture details about raw inputs
- go-gemara v0.6.0 through v0.10.0
- `gemara-python`, a Python SDK now available on PyPI

Other completed work:

- Joint work with the CNCF to publish the Cloud Native Security Controls Catalog (CNSCC) in Gemara was completed; a follow-on collaboration with CloudNativePG uses the CNSCC guidance catalog to produce a hardening guide
- Evidence Model expansion merged
- New repositories: `grcli`, `grc-store-clientkit`, `gemara-ai` (initial content), a relocated website repository, and a community repository to track engagement
- Gemara definitions submitted to the OpenSSF glossary ([#88](https://github.com/ossf/glossary/pull/88), [#103](https://github.com/ossf/glossary/pull/103))
- Project guidance added for AI attribution on PRs and comments
- Community structure formalized into a scheduled community call (office hours) and a separate maintainer call
- Alignment conversations underway with FINOS CALM and the GRC Engineering Community
- Several new contributors and issue reporters

### Up Next for Gemara

The project is currently working on the following:

- A formal release process for publishing Gemara artifacts, including a standard flow for upload to the GRC Store
- Bundling and distribution tooling
- A tutorial on extending and constraining Gemara schemas with CUE
- Reaching 100% Baseline scanning coverage on `gemaraproj` repositories (currently around 80%)
- Integration with other OpenSSF community tools

The project has identified a need for the following, but work is not yet underway:

- Aligning the Risk Catalog with FAIR for risk quantification
- Determining whether in-toto's Simplified Verification Record (SVR) can serve as input to audit logs

### Funding requests

None at this time.

## Minder

https://github.com/mindersec/minder

### Purpose of Minder

Minder is a policy engine for software supply chain security that lets users define and enforce security policy across repositories and artifacts, including automated evaluation of OSPS Baseline controls and remediation of findings.

### Current Status of Minder

- Minder was recognized as an ORBIT Technical Initiative in July
- Client releases v0.2.2, v0.3.0, and v0.3.1; the last fixes several reported security vulnerabilities (GHSA-9c2x-rm59-4335)
- 18 new contributors since v0.1.0, and two new maintainers onboarded via the mentorship program
- Mentorship project on rule testing reached rollout: `mindev test` for integration testing, Starlark-based tests, and coverage tracking; existing rules are being migrated
- Initial GitLab support, including OSPS Baseline rules for GitLab repositories, and a Quay.io provider for OCI repository policies
- Rego-formatted rules, Rego v1 dialect enforcement, interactive profile editing, generic entity commands, and an "issue" remediation type to tie into LLM-driven remediation flows
- Most community rules now declare their required provider
- Published and updated GitHub Actions (`minder-client-installer`, `minder-action`, `minder-action/test`), removing the need for Go toolchain setup in workflows

### Up Next for Minder

The project is currently working on the following:

- A proposal for adoption of Minder across the OpenSSF GitHub org, supporting the "Practicing What We Preach" initiative
- An exceptions API
- Specifying entity lifecycle remediation
- Additional Minder features to smoothly support repositories that span both GitHub and GitLab APIs

The project has identified a need for the following, but work is not yet underway:

- Diagrams and images for documentation

### Funding requests

None at this time.

## Privateer

https://github.com/privateerproj/pvtr

### Purpose of Privateer

Privateer is a plugin-based evaluation framework that runs assessments against a target and produces Gemara-formatted evaluation results. Assessment logic lives in plugins, so the same runner can evaluate different targets against different catalogs.

### Current Status of Privateer

- The TAC approved Privateer's sandbox application ([ossf/tac#630](https://github.com/ossf/tac/pull/630)); the required signatures have been completed and integration into OpenSSF is ongoing

### Funding requests

None at this time.

## Baseline Scanner

https://github.com/privateerproj/pvtr-github-repo-scanner

### Purpose of Baseline Scanner

The Baseline Scanner is a Privateer plugin that evaluates repositories against OSPS Baseline controls. It is the evaluation tool adopted by LFX Insights and consumes Security Insights data via `si-tooling`.

### Current Status of Baseline Scanner

- Test quality and precision have been substantially improved through a series of small fixes
- Some contributions were paused pending the go-gemara evidence collection merge, which has since landed

### Up Next for Baseline Scanner

The project is currently working on the following:

- Implementing AI-generated evidence on top of the new evidence model
- Roadmap for increasing test quality to cover Baseline levels 2 and 3

### Funding requests

None at this time.
