# 2025 Q3 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**

* [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)  
* [GitHub](https://github.com/ossf/wg-supply-chain-integrity); 23 contributors (**–**)  
* [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity); 182 members (**–**)  
* [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K); 980 members (**▲53**)  
* [Meeting Notes](http://ssci.io/sci-notes); 9 attendees average since last TAC briefing (**–**)

**tl;dr**: SLSA v1.2 Release Candidate 1 features the new Source track. GUAC is incorporating Red Hat's Trustify project to create a unified effort around managing supply chain metadata at scale.

**We’re ready to graduate this WG when we have time for the paperwork.**

**Headlines**:

* SLSA:  
  * Source Track: released in SLSA v1.2 RC1 in late June.   
  * Dependency Track: released in draft in late June.  
* GUAC:   
  * Red Hat contributing Trustify under the GUAC umbrella to create a unified effort around managing software supply chain security metadata at scale

## **SLSA**

### Purpose

A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.

### Current Status

* **Core Specification**:  
  * [SLSA 1.2 Release Candidate (RC) 1](https://slsa.dev/spec/v1.2-rc1/) was published on June 20th 2025 in time for LF OS Summit NA in Denver. It introduced the new Source Track and a new structure which presents the existing Build Track on the same level as the Source Track.  
  * Received substantial comments that are being worked out.  
* **Dependency Track**:  
  * Draft [SLSA Dependency Track](https://slsa.dev/spec/draft/dependency-track) published to slsa.dev on June 25th and presented in OpenSSF Community Day in Denver, CO  
* **Build Environment Track:**  
  * No update this period

### Up Next

* **Core Specification:**  
  * Finalising the few remaining issues to publish SLSA 1.2 RC2.  
* **Dependencies** Track  
  * Preparing Dependency Track for inclusion in an upcoming Release Candidate version of SLSA by defining detailed requirements for Producing Artifacts and Verifying Artifacts    
* **Attested Build Environment** Track  
  *  No update this period  
* Once SLSA 1.2 is finalized, we are planning to change the repository structure and build pipeline of the slsa.dev website to be able to leverage git branches to manage the different versions of the specification.

### Questions/Issues for the TAC

None

## **GUAC**

### Purpose

Observability for the software supply chain

### Current Status

* Red Hat is contributing the Trustify project, which focuses on security and compliance aspects of SBOMs, to the GUAC project.  
* Aiming to create a single, central hub within the OpenSSF for initiatives centered around building and using software supply chain knowledge graphs.  
* Operationally, a new GUAC Steering Committee will now oversee both the original GUAC project and Trustify

### Up Next

* No update this period

### Questions/Issues for the TAC

None

## **Zarf**

### Purpose

Continuous software delivery on systems that are disconnected from the internet

### Current Status

* Working on a separate registry bootstrap mechanism to support Kubernetes distributions more broadly  
* Introducing feature flags for more granular promotion of alpha features to GA  
* Working to improve project governance and introduce contributor ladder / new organization roles

### Up Next

* Refining scope for v1.0.0 release and roadmap  
  * Planning for deprecations and removals  
* Enhanced configuration options with a values passthrough capability

### Questions/Issues for the TAC

None

## **S2C2F**

From now on we’ll be following along with S2C2F under its guise of the SLSA Dependencies Track.

## **gittuf**

### Purpose

Verifiable security governance for git-based source repositories

### Current Status

* No update this period

## **Security Insights**

### Purpose

Standardized machine-readable metadata describing security properties and processes of open source projects

### Current Status

* No update this period
