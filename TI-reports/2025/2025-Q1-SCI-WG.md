# 2025 Q1 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**
* [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)
* [GitHub](https://github.com/ossf/wg-supply-chain-integrity); 23 contributors (▼**1**)
* [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity); 183 members (**▲2**)
* [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K); 890 members (**▲51**)
* [Meeting Notes](ssci.io/sci-notes); 10 attendees average since last TAC briefing (▼**5**)

**tl;dr:** Strong membership and engagement continues, despite a slight softening of core WG attendance over the holiday period. Notable ✨internal synergies✨ include s2c2f powering the upcoming SLSA Dependencies track, and gittuf powering a proof-of-concept for SLSA Source attestations.

**We’re ready to graduate this WG when we have time for the paperwork.**

**Latest news**:
* Three new SLSA tracks in development, including a Dependencies Track based on s2c2f
* GUAC, gittuf, and Zarf each working steadily towards 1.0 releases
* gittuf established proof-of-concept enablement of SLSA Source attestation


## SLSA

### Purpose
A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.

### Current Status
v1 (2023) focused on build integrity and provenance (“Build Track”).

### Up Next
* **Dependencies** Track
    * Dependency Track OpenSSF working group was formed and is meeting fortnightly.
    * Working group has been making progress towards the first draft of the Dependency Track based on s2c2f.
    * The group is currently aligning on the properties of different controls in s2c2f to enable clustering and generalization into objective outcomes.
* **Source** Track
    * The source track is approaching completion. All high level concepts have been agreed upon, and draft requirements are in place. The next steps are to complete at least one  [proof-of-concept](https://github.com/slsa-framework/slsa-source-poc) implementation of the track and use the lessons learned from the process to refine our requirements and language.
* **Attested Build Environment** Track
    * The initial set of BuildEnv track levels are [in draft](https://slsa.dev/spec/draft/attested-build-env-levels), with a more detailed threat model and implementation guidance upcoming in Q1.
    * The demo for the track is [available on GitHub](https://github.com/slsa-framework/attested-build-environments-demo), showcasing L1 and L2 provenance generation with vTPMs for VM-based build environment
* Other:
    * Navigation improvements on the website are underway to better highlight current activities and different spec versions
    * [Investigating splitting the spec into multiple documents](https://github.com/slsa-framework/slsa/discussions/1285) so that each track can mature at its own pace.

### Questions/Issues for the TAC
None

## S2C2F

### Purpose
Standardizing secure consumption of open source software and dependency management into the developer’s workflow

### Current Status
* Adapting S2C2F into a SLSA Dependencies Track 🙌
* Our work in progress is [here](https://docs.google.com/document/d/1JLDi2-IqLqemQ4QqRgFdMsYiMWUTqIjwji38FJw0Bmc/edit?usp=sharing): 
    * It is expected that not all original S2C2F requirements will be converted into the first version of SLSA Dependency Track

### Up Next
Once the initial version of SLSA Dependency Track is published, it has been agreed upon by the SLSA community that the OpenSSF S2C2F repo will persist, but be rebranded as a supplement to the SLSA Dependency Track to provide a more holistic framework to mitigating risk

### Questions/Issues for the TAC
None

## GUAC

### Purpose
Observability for the software supply chain

### Current Status
* Recent releases include new support for endoflife.date, reading from OCI-compatible container registries, and publishing OpenTelemetry data
    * Latest release is v0.13.2 on January 24
* Three separate mentions in KubeCon NA keynotes
* Published [2024 in review blog post](https://guac.sh/blog/2025-01-31-2024_in_review/)

### Up Next
* Continuing to work toward 1.0 release
* Discussing a new architecture to shorten the time-to-value for new users

### Questions/Issues for the TAC
None

## gittuf

### Purpose
Verifiable security governance for git-based source repositories

### Current Status
* Next release will be beta release, we have a milestone for 1.0
* GitHub app is ready for deployment, sorting out issues with Google Cloud billing with Riaan Kleinhans
* Developing features for enforcing gittuf policies across multiple repositories (e.g., for enterprise use)
* PoC of gittuf for current SLSA source track draft is ready

### Up Next
* Complete development of multi-repository features
* Address issues with Google Cloud billing and deploy GitHub app
* Move towards 1.0 by addressing relevant issues
* Make SLSA source track specific features ready for general use, in combination with GitHub app

### Questions/Issues for the TAC
None

## Zarf

### Purpose
Continuous software delivery on systems that are disconnected from the internet

### Current Status
* Focus on Zarf SDK utilization
* Pausing 1.0 in favor of new feature development that may include breaking changes 

### Up Next
* UX and runtime improvements
* Governance and Community Engagement Support
* Stability and Performance towards a future 1.0 release

### Questions/Issues for the TAC
None

## Security Insights

### Purpose
Standardized machine-readable metadata describing security properties and processes of open source projects

### Current Status
* v2.0 launched in January 2025
* si-tooling updated with go library for external integrations, currently being used by Baseline validator

### Up Next
Infrequent / iterative maintenance based on user feedback

### Questions/Issues for the TAC
None
