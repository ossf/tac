# 2026 Q1 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**

* [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) (Not updated in a while) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)
* [GitHub](https://github.com/ossf/wg-supply-chain-integrity); 
* [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity)
* [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K)
* [Meeting Notes](http://ssci.io/sci-notes)-  attendees average since last TAC briefing - 8

**tl;dr**: <!-- TODO: 1-2 sentence summary of the quarter's highlights -->

<!-- TODO: Update graduation status. Q3 noted: "We're ready to graduate this WG when we have time for the paperwork." -->

**Headlines**:

* WG:
    * New co-chairs (Nicole Bates, Justin Cappos, Michael Lieberman)
    * Looking to refresh the scope/chart of the group in the coming months.
* SLSA:
  * SLSA has graduated!

## **SLSA**

### Purpose

A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.

### Current Status

* **Core Specification**:
    * SLSA v1.2 has been released
* **Dependency Track**:
  * Still being worked on.
  * There have been some shifts in 
* **Build Environment Track:**
* * Paused rework of threat model during technical writer contract, but plan to resume
  * Started development of L3 demo on Azure, and early stages of L2/L3 demo on GCP
  * New co-developer from Google joined the track
* **Tooling Improvement Projects**
  * Both projects had a delayed start due to christmas break
  * SLSA Source Tools
      * Finished the planning phase
      * Started refactor preparing for SLSA 1.2
      * Started work to integrate with gittuf
  * SLSA Build Tools
      * Beginning planning phase this week (week of Feb 16th '25) 

### Up Next

* <!-- TODO -->

### Funding Requests

* None

### Questions/Issues for the TAC

<!-- TODO: or "None" -->

## **GUAC**

### Purpose

Observability for the software supply chain

### Current Status

* Trustify development active, with 6 Q4 2025 releases in the Trustify 0.4.x series
* One security release of GUAC Visualizer

### Up Next

* Ongoing Trustify development, targeting a biweekly release cadence
* Several GUAC fixes and improvements in flight

### Funding Requests

* None

### Questions/Issues for the TAC

* None

## **Zarf**

### Purpose

Secure Software Delivery for connected and disconnected systems

### Current Status

* Registry Proxy feature is released in alpha and available for testing
* Package Sign and Package Verify are now explicit commands
* Zarf agent now supports OCI image volumes during kubernetes mutation
* Native documentation storage has been added to the manifest/package structure
* Feature Flags are implemented and accessible with the CLI and SDK

### Up Next

* mTLS improvements for the Init Infrastructure
* v1.0.0 Planning
    * Updated schema definition & migration planning
* Package Signing and Verification with the Sigstore Bundle Format
* Package values are under active development

### Funding Requests

* No funding requests at this time

### Questions/Issues for the TAC

* No questions or issues for the TAC at this time

## **gittuf**

### Purpose

Verifiable security governance for git-based source repositories

### Current Status

* v0.12.0 released.
* Creation of documentation library for gittuf, hosted on gittuf.dev.

### Up Next

* v0.13.0 release upcoming pending migration from legacy Sigstore dependencies.
* v1.0.0 and promotion to full release/stable from beta pending discussion on backwards compatibility.
* Further deployment of gittuf GitHub app and gittuf itself across more repositories.
* Major UI/UX overhaul with focus on a TUI for the default user experience (as opposed to the current CLI-driven workflow).
* New quickstart/setup utility to get projects started quickly with gittuf (i.e. "three commands to get gittuf up and running").

### Funding Requests

* None at this time.

### Questions/Issues for the TAC

* None at this time.

## **Security Insights**

### Purpose

Standardized machine-readable metadata describing security properties and processes of open source projects

### Current Status

* Has officially moved over to the ORBIT working group!