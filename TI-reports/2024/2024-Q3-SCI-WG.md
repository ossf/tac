# 2024 Q3 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**



*   [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)
*   [GitHub](https://github.com/ossf/wg-supply-chain-integrity); 24 contributors (=)
*   [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity); 181 members (**⇧3**)
*   [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K); 839 members (**⇧94**)
*   [Meeting Notes](ssci.io/sci-notes); 15 attendees average since last TAC briefing (**⇧4**)

**tl;dr:** Strong membership and attendance trends, and the formal addition of Zarf and Security Insights to SCI WG. With the retirement of FRSCA we now have SLSA, S2C2F, GUAC, gittuf, Zarf, and Security Insights; with interest expressed from the Trusted Repository Security Initiative (TRSI) and Clean Dependency Project in addition.

**We’re ready to graduate this WG when we have time for the paperwork.**

**Latest news**:



*   SLSA v1.1 readying for release (7 TODOs left)
*   S2C2F working with SLSA on Dependency Track
*   SLSA Source Track in draft
*   Funding approved for gittuf GitHub App
*   Zarf 1.0 anticipated by EoY


## SLSA


### Purpose

A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.


### Current Status

v1 (2023) focused on build integrity and provenance (“Build Track”).


### Up Next

v1.1 (soon!) with an updated threat model and minor clarifications

Source Track in draft

Hardware Attestations Track in development

Dependencies Track work beginning


### Questions/Issues for the TAC

None


## S2C2F


### Purpose

Standardizing secure consumption of open source software and dependency management into the developer’s workflow


### Current Status

Deprioritized standards submission work

Collaboration with SLSA on Dependencies Track


### Up Next

Desire to work with Scorecard to be a tool that also helps identify S2C2F compliance (i.e. future SLSA Dependencies Track compliance)

Exploring applicability to AI/ML domain


### Questions/Issues for the TAC

None


## GUAC


### Purpose

Observability for the software supply chain


### Current Status

Version 0.7 and 0.8 releases:



*   Clearly Defined integration completed
*   CycloneDX SBOM license parsing
*   Improved S3 collector


### Up Next

Planning 1.0 release


### Questions/Issues for the TAC

None


## gittuf


### Purpose

Verifiable security governance for git-based source repositories


### Current Status



*   Several releases with bug fixes and optimizations
*   Improved support for Sigstore (including private deployments)
*   Usability work
    *   Adding support for integrations with code review systems such as GitHub PRs
    *   Requested (and got approved) for funding for a gittuf GitHub App


### Up Next



*   Plan to reach beta status by end of year
*   Planning towards releasing v1.0 in the new year


### Questions/Issues for the TAC

None


## Zarf


### Purpose

Continuous software delivery on systems that are disconnected from the internet


### Current Status

Readying for 1.0 release by EoY


### Up Next

Release candidate at SOSS Fusion

v1.0 release at KubeCon NA (This might see a small delay depending on how things go over the next couple months)


### Questions/Issues for the TAC

None


## Security Insights


### Purpose

Standardized machine-readable metadata describing security properties and processes of open source projects


### Current Status

v1.0 launched in October 2023


### Up Next

Tidying up specification and auditing existing data

Aligning with the Baseline SIG and Best Practices Badge, to work on required values for SI specification


### Questions/Issues for the TAC

None
