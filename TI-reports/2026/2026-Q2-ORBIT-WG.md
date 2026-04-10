# 2026 Q2 ORBIT WG

## Overview

The ORBIT working group continues to grow, with the first major release of the Gemara project and the formalization of end-user engagement structures through the recently approved ORBIT Launchpad initiative.

## OSPS Baseline SIG

https://github.com/ossf/security-baseline

### Current Status of OSPS Baseline SIG

Published release 2026-02-19 in February with three new controls, three modified controls, and one removed control, plus two new regulatory mappings.

### Up Next for OSPS Baseline SIG

The SIG is currently working on the following:

- Expanded regulatory mappings
- Finalizing alignment with Gemara v1
- Professional tech writer (funding approved, onboarding delayed)

The SIG has identified a need for the following, but work is not yet underway:

- Specific examples of real-world implementations of certain control requirements (particularly on documentation/process)

### Funding requests

None at this time.

## ORBIT Launchpad SIG

https://github.com/ossf/orbit-launchpad

### Purpose of ORBIT Launchpad SIG

Engage with any community efforts that relate to the ORBIT resources, especially with regards to automation and adoption support for manufacturer end users.

### Current Status of ORBIT Launchpad SIG

- The SIG has been renamed from “Tooling” and new governance is in place
- A dedicated fortnightly session has been well attended by 10+ consistent manufacturer representatives
- Tooling is seeing adoption from an increasing volume of users
- Significant progress has been made to integrate OSPS Baseline with Best Practices Badge and increase awareness of the new features
- Launchpad’s partnership with the CNCF Security Slam resulted in increased adoption of ORBIT tools and specs

### Up Next for ORBIT Tooling SIG

An effort is underway to get OSPS Baseline + CRA insight from Legal contributors at Microsoft and Red Hat, after which a private review will be open to Launchpad participants prior to development of an extension catalog based on OSPS Baseline.

### Funding requests

None at this time.

## OSPS Assessments SIG

https://github.com/ossf/security-assessments

### Purpose of OSPS Assessments SIG

In response to a rising demand for standardized security review of open source projects, the Open Source Project Security (OSPS) Assessments project provides a tiered model for assessing the security state of open source software.

### Current Status of OSPS Assessments SIG

The SIG is currently not meeting due to other obligations from members. There is a known obligation to support OpenSSF Staff in the maintenance of *LFEL1005: Security Self-Assessments for Open Source Projects*

### Up Next for OSPS Assessments SIG

The WG is currently working on the following:

- Recruit more interested contributors (help wanted!)
- Continue refinement of the current content

The SIG has identified a need for the following, but work is not yet underway:

- Creation of regulatory compliance assessment recommendations
- Creation of third-party audit assessment recommendations

### Funding requests

None at this time.

## Security Insights SIG

[https://github.com/ossf/security-insights](https://github.com/ossf/security-insights) https://github.com/ossf/si-tooling

### Purpose of Security Insights SIG

This specification provides a mechanism for projects to report information about their security in a machine-processable way. It is formatted as a YAML file to make it easy to read and edit by humans.

The data tracked within this specification is intended to fill the gaps between simplified solutions such as SECURITY.md and comprehensive automated solutions such as SBOMs. In that gap lay elements that must be self-reported by projects to allow end-users to make informed security decisions.

Security Insights is a key component for automating the evaluation of many Baseline controls that cannot be inferred without a claim being made by the project maintainers. The `si-tooling` go library for Security Insights v2 is integrated into the Baseline evaluation tool recently adopted by LFX.

### Current Status of Security Insights SIG

ENISA directly recommends and links to Security Insights in the upcoming [Secure by Design and Default Playbook](https://www.enisa.europa.eu/sites/default/files/2026-03/ENISA_Secure_By_Design_and_Default_Playbook_v0.4_draft_for_consultation.pdf), along with Scorecard.

### Up Next for Security Insights SIG

- Business as usual, responding to community feedback on GitHub issues and in ORBIT community calls

### Funding requests

None at this time.

## Gemara

https://github.com/gemaraproj/gemara

### Purpose of Gemara

The Gemara model is a logical model that describes automated governance, risk, and compliance activities. It outlines a series of categorical layers and their interactions to facilitate automated interoperability and communication between different functions across organizations.

A concrete example is the Open Source Project Security Baseline (OSPS Baseline), which is expressed in Gemara's Layer 2 Control Catalog schema.

### Current Status of Gemara

The Gemara project released v1 of the Gemara spec (model implementation) on April 10th.

To support this milestone, we have completed the following actions:

- Published an official whitepaper that explains the Gemara model's origin, philosophy and architectural goals.
- Support alignment efforts with consumers like the OSPS Baseline and FINOS CCC
- Created a v1.0.0 release to define a complete set of schemas and stabilize Layer 2 (Controls) and Layer 5 (Evaluation) schemas.
- Updated the Go SDK and MCP Tooling to facilitate testing and validation of the spec

### Up Next for Gemara

Responding to community feedback through GitHub issues, ORBIT calls, and ORBIT Launchpad calls and continue to mature the schemas still in the experimental stage. 

Specific targets currently being worked on are the following:

- Adding Gemara definitions to the OpenSSF glossary to enable shared terms
- Creating a comprehensive set of project tutorials in the Gemara website
- Expanding supported conversions in the Gemara Go SDK with Markdown generation
- Improvements to the Gemara MCP Server and tooling to include an evaluation suite

The project has identified a need for the following, but work is not yet underway:

- Improve and centralize community documentation including creating an official Contributor Ladder
- Expanded support for OSCAL conversions in the Gemara Go SDK
- Expanded Artifact Type support in the Gemara MCP Server

### Funding requests

None at this time.  