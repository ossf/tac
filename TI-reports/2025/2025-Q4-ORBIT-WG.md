# 2025 Q4 ORBIT WG

## Overview

The ORBIT Working Group is solidifying its foundational specifications while actively expanding its focus to tooling, adoption, and community engagement to meet rising ecosystem demands.

The OSPS Baseline and Security Insights are both preparing for a upcoming major releases, while the newly formalized Tooling SIG is driving adoption through automation. The OSPS Assessments SIG is still actively recruiting contributors to advance its foundational work which, alongside the Baseline, forms a necessary response to regulations like the CRA.

Across all SIGs, common needs have been identified for contributor recruitment, improved end-user documentation with real-world examples, and a stronger web presence to guide adopters.

## OSPS Baseline SIG

### Current Status of OSPS Baseline SIG

Development on a second release of the control catalog is currently underway, proposed for Q4 2025. See "Up Next" for more details.

### Up Next for OSPS Baseline SIG

The SIG is currently working on the following:

- Expanded regulatory mappings
- Final edits for a new release
- Improving text consistency and clarity
- Professional tech writer (funding approved, onboarding in process)

The SIG has identified a need for the following, but work is not yet underway:

- Specific examples of real-world implementations of certain control requirements (particularly on documentation/process)

## ORBIT Tooling SIG

### Purpose of ORBIT Tooling SIG

Engage with any community efforts that relate to the OSPS Baseline, especially with regards to automation and adoption support.

### Current Status of ORBIT Tooling SIG

Formerly logged as 'Baseline Tooling Support', the WG has elected to form an official SIG under the leadership of Travis Truman (@trumant).

### Up Next for ORBIT Tooling SIG

The WG is currently working on the following:

- Compiling an authoritative list of user-ready tools that accelerate OSPS Baseline adoption
- Supporting integration of Baseline controls into Best Practices Badge interface
- Supporting integration of Baseline controls into Minder

The SIG has identified a need for the following, but work is not yet underway:

- ORBIT Website with guidance for Baseline adopters
- Integration of Baseline controls into OpenSSF Scorecard

## OSPS Assessments SIG

https://github.com/ossf/security-assessments

### Purpose of OSPS Assessments SIG

In response to a rising demand for standardized security review of open source projects, the Open Source Project Security (OSPS) Assessments project provides a tiered model for assessing the security state of open source software.

### Current Status of OSPS Assessments SIG

The SIG has made a call for more contributors to extend the foundational work that was initially contributed by CNCF's TAG Security.

### Up Next for OSPS Assessments SIG

The WG is currently working on the following:

- Recruiting interested contributors

The SIG has identified a need for the following, but work is not yet underway:

- Refinement of the current content
- Creation of regulatory compiance assessment recommendations
- Creation of third-party audit assessment recommendations


## Security Insights SIG

https://github.com/ossf/security-insights
https://github.com/ossf/si-tooling

### Purpose of Security Insights SIG

This specification provides a mechanism for projects to report information about their security in a machine-processable way. It is formatted as a YAML file to make it easy to read and edit by humans.

The data tracked within this specification is intended to fill the gaps between simplified solutions such as SECURITY.md and comprehensive automated solutions such as SBOMs. In that gap lay elements that must be self-reported by projects to allow end-users to make informed security decisions.

Security Insights is a key component for automating the evaluation of many Baseline controls that cannot be inferred without a claim being made by the project maintainers. The `si-tooling` go library for Security Insights v2 is integrated into the Baseline evaluation tool recently adopted by LFX.

### Current Status of Security Insights SIG

Security Insights is intended to be stable, with minimal changes on a year-over-year basis. In order to support OSPS Baseline, a non-breaking change to add new fields was released in v2.1.0 on May 9th. This was the first update since the last major release on Jan 1st 2025.

### Up Next for Security Insights SIG

The SIG is currently soliciting proposals ahead of the January 1st major version update. Proposals must be open in the form of an enhancement proposal for no less than 30 days before they may be approved.

The SIG has identified a need for the following, but work is not yet underway:

- Improved end user documentation, especially as it pertains to supporting OSPS Baseline automated checks.
- Increased awareness of Security Insights, and how it helps projects demonstrate conformance with Baseline

## Gemara

https://github.com/ossf/gemara

### Purpose of Gemara

The Gemara model is a logical model that describes automated governance, risk, and compliance activities.
It outlines a series of categorical layers and their interactions to facilitate automated interoperability 
and communication between different functions across organizations.

A concrete example is the Open Source Project Security Baseline (OSPS Baseline), which is expressed in Gemara's Layer 2.

### Current Status of Gemara

The Gemara project is actively refining its existing schemas with a focus on Layer 2 (Controls) and Layer 4 (Evaluation).
To increase community collaboration, the project has established a dedicated Slack [channel](https://openssf.slack.com/archives/C09A9PP765Q) and plans to hold regular community meetings starting in October.

### Up Next for Gemara

The project is currently working on the following:

- Expansion of Layer 4 (Evaluation) schema to support reusable evaluation plans and human-led assessments  
- Translating the Gemara model to existing standards like OSCAL and SARIF to support interoperability within the wider security and compliance ecosystem  

The project has identified a need for the following, but work is not yet underway:

- Completion of schemas for the last two layers - Layer 5 (Enforcement) and Layer 6 (Audit)
- Refinement of the existing cue package to reduce schema duplication and increase usability