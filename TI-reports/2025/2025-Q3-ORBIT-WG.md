# 2025 Q3 ORBIT WG

## Overview

The ORBIT Working Group continues to mature, with active contributor participation across each group and a growing ecosystem of tools and adopters. Adoption of each workstream is growing, but some gaps remain in documentation, contributor recruitment, and web presence.

## OSPS Baseline SIG

https://github.com/ossf/security-baseline

### Purpose of OSPS Baseline

The Open Source Project Security Baseline (OSPS Baseline) is designed to act as a minimum definition of requirements for a project relative to its maturity level.

### Current Status of OSPS Baseline SIG

Development on a second release of the control catalog is currently underway, proposed for Q4 2025. See "Up Next" for more details.

The SIG has elected to refuse proposal of any tooling, including tool configuration files. These are to be maintained separately from the control catalog, in a wider collaboration under the ORBIT umbrella.

### Up Next for OSPS Baseline SIG

The SIG is currently working on the following:

- Expanded regulatory mappings
- Refinement of remediation recommendations
- Refinement of lexicon definitions

The SIG has identified a need for the following, but work is not yet underway:

- Website improvements

### Questions/Issues for the TAC regarding OSPS Baseline SIG

The SIG has highlighted a need for technical writing polish and website support. If any organizations intend to accelerate the adoption of Baseline through efforts such as organizational mandates, this last-mile refinement must be completed first.

## Baseline Tooling Support

### Purpose of Baseline Tooling Support

Engage with any community efforts that relate to the OSPS Baseline, especially with regards to automation and adoption support.

### Current Status of Baseline Tooling Support

Several tooling efforts are currently underway, including one community tool currently deployed into production by LFX Insights.

The ORBIT WG has issued a call for proposals to anyone who would like their integrations to be highlighted on a web page that is anticipated to be created soon with the support of OpenSSF staff.

### Up Next for Baseline Tooling Support

The WG is currently working on the following:

- Compiling an authoritative list of user-ready tools that accelerate OSPS Baseline adoption
- Supporting integration of Baseline controls into Best Practices Badge interface
- Supporting integration of Baseline controls into Minder

The SIG has identified a need for the following, but work is not yet underway:

- ORBIT Website with guidance for Baseline adopters
- Integration of Baseline controls into OpenSSF Scorecard

### Questions/Issues for the TAC regarding Baseline Tooling Support

It should be noted that the ORBIT WG is not currently prepared to do any direct software development activities to integrate Baseline controls into other tools, though attempts were made in the past. Any effort to upgrade other OpenSSF tools to feature Baseline controls should be led by the TAC or by the respective maintainers with support from ORBIT.

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

### Questions/Issues for the TAC regarding OSPS Assessments SIG

The ORBIT WG would like to highlight that a complete CRA response **must** include both a Baseline guidance for how software projects are run, and Assessment guidance to help projects improve how they design their systems and write their code. Prior to the full enforcement of the CRA, both OSPS-A and OSPS-B will need to be generally available for projects overseen by stewards.

## Security Insights SIG

https://github.com/ossf/security-insights
https://github.com/ossf/si-tooling

### Purpose of Security Insights SIG

This specification provides a mechanism for projects to report information about their security in a machine-processable way. It is formatted as a YAML file to make it easy to read and edit by humans.

The data tracked within this specification is intended to fill the gaps between simplified solutions such as SECURITY.md and comprehensive automated solutions such as SBOMs. In that gap lay elements that must be self-reported by projects to allow end-users to make informed security decisions.

### Current Status of Security Insights SIG

Security Insights is intended to be stable, with minimal changes on a year-over-year basis. In order to support OSPS Baseline, a non-breaking change to add new fields was released in v2.1.0 on May 9th. This was the first update since the last major release on Jan 1st 2025.

### Up Next for Security Insights SIG

The SIG is not currently working on any action items.

The SIG has identified a need for the following, but work is not yet underway:

- Improved end user documentation, especially as it pertains to supporting OSPS Baseline automated checks.
- Increased awareness of Security Insights, and how it helps projects demonstrate conformance with Baseline

### Questions/Issues for the TAC regarding Security Insights SIG

Security Insights is a key component for automating the evaluation of many Baseline controls that cannot be inferred without a claim being made by the project maintainers. The `si-tooling` go library for Security Insights v2 is integrated into the Baseline evaluation tool recently adopted by LFX.

## Additional Information

_Gemara_ is currently pending full adoption into the WG as necessary paperwork is being completed with the LF.
