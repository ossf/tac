# 2024 Q3 Securing Critical Projects WG

## Overview

Sub projects continue to run and make progress. Little to no progress on main
initiative of enhancing Critical Project Set with more information. Attendance
is low.

## Identifying Critical Projects

Addition of Metadata to Set:
- Metadata fields roughly scoped and defined.
- Consensus is still hesitant
- Work to enhance set is stalled

## Criticality Score

- Continues to run and recalculate scores
- Updates 1 to 2 times a month
- Tracking 500,000 projects
- Small calculation fixes

## Package Analysis / Malicious Packages

- Ingesting data from Reversing Labs
  - Worked through issues with NPM namespacing
- Worked through broken RSS feed from NPM
- Working to OSV team about PURL casing issues
- Working on formal definition of "Malicious Package"
  - Example: Is a reputation farming package malicious?
  - PR: https://github.com/ossf/malicious-packages/pull/381
  - TAC Feedback appreciated, interested in doing a blog post
- Malicious Package counts ~25,000 packages
  - 2 crates-io
  - 15543 npm
  - 731 nuget
  - 8081 pypi
  - 802 rubygems

## Purpose

Open Source Software has long suffered from a "tragedy of the commons"
problem. Organizations large and small make use of OSS every day, but many
projects are struggling for the time, resources and attention they need.

This is a resource allocation problem - and we can help solve it together. We
need ways to connect critical projects we all rely on with organizations that
can provide them with support.

[MVSR Link](https://github.com/ossf/wg-securing-critical-projects/blob/main/MVSR.md)

## Current Status

See overview.

## Up Next

Continue to support sub projects.

### RE: [Proposal: Funding Critical Projects POC with commercial vendors](https://github.com/ossf/tac/issues/360)

> Once the TI has agreed to sponsor the effort

> There also appears to be little community/TI engagement on this. If this effort were ever to move forward, we would want to see broad discussion and collaboration from one of our Technical Initiatives. We suggest taking the idea to the Securing Critical Projects working group or perhaps Alpha-Omega

SCP WG is happy to serve as a forum for this initiative. We see a roadblock in being able to execute this due to not having a way to request staffing (in addition to funding). Essentially, we wish to be able to propose funding to staff the management to provide: "We are requesting X amount of funding to achieve Y result in Z timeline." 

## Questions/Issues for the TAC

Please provide feedback on Malicious Package definition.
See staffing ability request above.
