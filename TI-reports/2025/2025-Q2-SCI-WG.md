# 2025 Q2 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**

* [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)
* [GitHub](https://github.com/ossf/wg-supply-chain-integrity); 23 contributors (**–**)
* [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity); 182 members (▼**1**))
* [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K); 927 members (**▲37**)
* [Meeting Notes](ssci.io/sci-notes); 9 attendees average since last TAC briefing (▼**1**)

**tl;dr**: SLSA releases v1.1; GUAC readies v1.0; gittuf reaches beta v0.10.0.

**We’re ready to graduate this WG when we have time for the paperwork.**

**Latest news**:

* SLSA advances: new governance structure, core specification v1.1 released, headed to v1.2 including Source Track at [OSS NA](https://events.linuxfoundation.org/open-source-summit-north-america/)
* GUAC headed to 1.0 in mid-May
* gittuf reaches beta status with v0.10.0 release.



## SLSA

### Purpose
A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.

### Current Status
* **Governance**
    * In February, the SLSA Steering Committee voted on an [update to its governance policy](https://github.com/slsa-framework/governance/blob/main/5._Governance.md), which included revising the Steering Committee and its responsibilities
    * The Steering Committee is now 5 members each with a year-long term, with responsibilities including managing the lifecycle of SLSA workstreams and the overall success of the project
    * The [first election](https://github.com/slsa-framework/slsa/issues/1295) just concluded, and the new SC members are: Tom Hennen (Google), Adrian Diglio (Microsoft), Andrew McNamara (Red Hat), Mike Lieberman (Kusari), and Michael Winser (Eclipse Foundation)
* **Core Specification**:
    * [SLSA v1.1](https://slsa.dev/spec/v1.1/) is out
        * This release brings several changes aimed at enhancing the clarity and usability of the v1.0 specification. It also introduces backwards-compatible clarifications to the SLSA threat model, attestation model and verification procedure. This includes the addition of verifier metadata to the Verification Summary Attestation (VSA) format. See [announcement](https://slsa.dev/blog/2025/04/slsa-v1.1) for further details.
* **Source Track**:
    * We held an in-person sprint week of 4/21 where three maintainers worked to address various outstanding issues
        * Clarified and condensed multiple requirements
        * Added a ‘tag hygiene’ requirement
        * Proposal to add a “two party review” requirement at a new Level 4

### Up Next
* **Dependencies** Track
    * No updates
* **Source** Track
    * Hoping to release with SLSA 1.2 prior to OSS NA
* **Attested Build Environment** Track
    * The [threat model](https://github.com/slsa-framework/slsa/pull/1287) and [detailed implementation requirements](https://github.com/slsa-framework/slsa/pull/1323) for the track are in draft PRs awaiting some finishing touches, and will be ready for review in the coming weeks.

### Questions/Issues for the TAC
None

## S2C2F

From now on we’ll be following along with S2C2F under its guise as the SLSA Dependencies Track.

## GUAC

### Purpose
Observability for the software supply chain

### Current Status
* Finalizing plans for a 1.0 release in mid-to-late May
* Working on a plan to absorb the Trustification project into the guacsec organization
* Version 0.14.0 released in March to add support for collecting runtime SBOMs from Kubescape
* Two GUAC-related talks at KubeCon EU
    * “[Why Don’t We Have Both? Track Build- and Run-time Information for Security With Kubescape and GUAC](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” by Jeff Mendoza and Ben Hirschberg
    * “[Bridging Supply Chain Policy with Git-less GitOps and GUAC](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/program/schedule/?_hsenc=p2ANqtz-_Bt8t9ThHyK9D8zm1KUzjEnVYWcPGCpISaP1EHMlSegDNDwV8iA2WoOJTaCEvoL0Dow0Ss9VJEyvzt9owaFbwOHW_oGQ&_hsmi=342547164&utm_campaign=KubeCon-EU-2025&utm_medium=email&utm_content=342547164&utm_source=hs_email)” by Michael Lieberman and Andrew Martin

### Up Next
* Completing 1.0 release plans and Trustification merger

### Questions/Issues for the TAC
None

## gittuf

### Purpose
Verifiable security governance for git-based source repositories

### Current Status
* gittuf has advanced to beta with the v0.10.0 release
* Deployed funded gittuf GitHub app using LF cloud credits
* Adding support for gittuf over multiple repositories
* Adding support for upcoming SLSA Source Track

### Up Next
* Incubation at the OSSF

### Questions/Issues for the TAC
None

## Zarf

### Purpose
Continuous software delivery on systems that are disconnected from the internet

### Current Status
* Continuation of Zarf SDK utilization improvements
* Community and Engagement efforts

### Up Next
* Package Lifecycle, configuration, and operational improvements
* Enhancing observability & user experience


### Questions/Issues for the TAC
None

## Security Insights

### Purpose
Standardized machine-readable metadata describing security properties and processes of open source projects

### Current Status
* v2.0 launched in January 2025
* si-tooling updated with go library for external integrations, currently being used by Baseline validator
* Currently proposed for migration to the emerging ORBIT WG to better coordinate alignment with Baseline

### Up Next
Infrequent / iterative maintenance based on user feedback

### Questions/Issues for the TAC
None
