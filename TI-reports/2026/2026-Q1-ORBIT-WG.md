# 2025 Q4 ORBIT WG

## Overview

The ORBIT working group continues to grow, with an upcoming major release of the Gemara project and the formalization of end-user engagement structures through the recently approved ORBIT Launchpad initiative.

## OSPS Baseline SIG

### Current Status of OSPS Baseline SIG

Development on a new release of the control catalog is currently underway, proposed for Q1 2026.

### Up Next for OSPS Baseline SIG

The SIG is currently working on the following:

- Expanded regulatory mappings
- Increased alignment with Gemara specifications
- Professional tech writer (funding approved, onboarding delayed)

The SIG has identified a need for the following, but work is not yet underway:

- Specific examples of real-world implementations of certain control requirements (particularly on documentation/process)

### Funding requests

None at this time.

## ORBIT Tooling SIG

### Purpose of ORBIT Tooling SIG

Engage with any community efforts that relate to the OSPS Baseline, especially with regards to automation and adoption support.

### Current Status of ORBIT Tooling SIG

- The SIG has continued to operate through independent workstreams with check-ins on the main WG meeting
- Tooling has seen high-intensity adoption from a low volume of users
- Significant progress has been made to integrate OSPS Baseline with Best Practices Badge 

### Up Next for ORBIT Tooling SIG

The WG steering committee has approved a comprehensive proposal to restructure this SIG into "ORBIT Launchpad," charter pending, with a focus on coordinating end-user feedback to WG maintainers.

### Funding requests

None at this time.

## OSPS Assessments SIG

https://github.com/ossf/security-assessments

### Purpose of OSPS Assessments SIG

In response to a rising demand for standardized security review of open source projects, the Open Source Project Security (OSPS) Assessments project provides a tiered model for assessing the security state of open source software.

### Current Status of OSPS Assessments SIG

The SIG is currently supporting OpenSSF Staff in the maintenance of LFEL1005: Security Self-Assessments for Open Source Projects

### Up Next for OSPS Assessments SIG

The WG is currently working on the following:

- Recruiting interested contributors

The SIG has identified a need for the following, but work is not yet underway:

- Refinement of the current content
- Creation of regulatory compiance assessment recommendations
- Creation of third-party audit assessment recommendations

### Funding requests

None at this time.

## Security Insights SIG

https://github.com/ossf/security-insights
https://github.com/ossf/si-tooling

### Purpose of Security Insights SIG

This specification provides a mechanism for projects to report information about their security in a machine-processable way. It is formatted as a YAML file to make it easy to read and edit by humans.

The data tracked within this specification is intended to fill the gaps between simplified solutions such as SECURITY.md and comprehensive automated solutions such as SBOMs. In that gap lay elements that must be self-reported by projects to allow end-users to make informed security decisions.

Security Insights is a key component for automating the evaluation of many Baseline controls that cannot be inferred without a claim being made by the project maintainers. The `si-tooling` go library for Security Insights v2 is integrated into the Baseline evaluation tool recently adopted by LFX.

### Current Status of Security Insights SIG

Numbers of files seen in public repos has approximately doubled since mid-2025, following the adoption of ORBIT tools by the LFX Insights Security & Best Practices dasboard.

A major version was not released this year. `v2.2.0` was released in January to apply feedback from 2025, improve documentation, and add a new website at [security-insights.openssf.org]

### Up Next for Security Insights SIG

- Business as usual, responding to community feedback on GitHub issues and in ORBIT community calls

### Funding requests

None at this time.

## Gemara

https://github.com/gemaraproj/gemara

### Purpose of Gemara

The Gemara model is a logical model that describes automated governance, risk, and compliance activities.
It outlines a series of categorical layers and their interactions to facilitate automated interoperability 
and communication between different functions across organizations.

A concrete example is the Open Source Project Security Baseline (OSPS Baseline), which is expressed in Gemara's Layer 2.

### Current Status of Gemara

The Gemara project is actively preparing for the first stable release of the project components.

To support these activities, we have completed the following actions:
- Migrated the project to its own GitHub organization to support scaling
- Developed release strategies for each project component
- Created a website at `gemara.openssf.org` to house our project documentation and implementation guides

### Up Next for Gemara

The project is currently working on the following:

- Publishing an official whitepaper that explains the Gemara model's origin, philosophy and architectural goals.
- Adding Gemara definitions to the OpenSSF glossary to enable shared terms
- Stabilizing schemas for Layers 1 (Guidance) and 2 (Controls)
- Creation of initial MCP tooling

The project has identified a need for the following, but work is not yet underway:

- Stabilization of schemas for Layer 3 (Policy) and Layer 5 (Evaluation).
- Completion of schemas for the last two layers - Layer 6 (Enforcement) and Layer 7 (Audit)
- A comprehensive set of project tutorials

### Funding requests

None at this time.
