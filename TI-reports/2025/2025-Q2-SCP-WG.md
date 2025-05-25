# 2025 Q2 Securing Critical Projects WG

## Overview

Sub-projects continue to run and make progress. Malicious Packages project is
attracting interest. Continue discussion on ideas for helping top
projects. Attendance is low.

[2025-Q1 Update](2025-Q1-SCP-WG.md)

## Identifying Critical Projects

### Purpose

Open Source Software has long suffered from a "tragedy of the commons"
problem. Organizations large and small make use of OSS every day, but many
projects are struggling for the time, resources and attention they need.

This is a resource allocation problem - and we can help solve it together. We
need ways to connect critical projects we all rely on with organizations that
can provide them with support.

[MVSR Link](https://github.com/ossf/wg-securing-critical-projects/blob/main/MVSR.md)

### Current Status

- Investigation of [Census 3](https://www.linuxfoundation.org/research/census-iii) data

### Up Next

- Investigating what a "light" review/audit would look like.
- An experiment would be 2 person-week (2 eng 1 week) to see if that works,
  expect this to be minimum time for any valuable findings

### Questions/Issues for the TAC

None

## Criticality Score

### Purpose

1. Generate a criticality score for every open source project.

1. Create a list of critical projects that the open source community depends
   on.

1. Use this data to proactively improve the security posture of these critical
   projects.

### Current Status

- Github enumerator has stopped working. Investigating
- Scoring running with a manual list
- Updates 1 to 2 times a month
- Tracking 500,000 projects

### Up Next

Fix enumerator

### Questions/Issues for the TAC

None


## Package Analysis / Malicious Packages

### Purpose

The Package Analysis project analyses the capabilities of packages available on
open source repositories. The project looks for behaviors that indicate
malicious software:

- What files do they access?
- What addresses do they connect to?
- What commands do they run?

The project also tracks changes in how packages behave over time, to identify
when previously safe software begins acting suspiciously.

This effort is meant to improve the security of open source software by
detecting malicious behavior, informing consumers selecting packages, and
providing researchers with data about the ecosystem.

Malicious Packages is a collection of reports of malicious packages identified in
Open Source package repositories, consumable via the Open Source Vulnerability
(OSV) format.

### Current Status

- New contributors helping with routine maintenance
- Working on documenting dependency confusion
- Scanning tooling needs to differentiate internal packages/namespaces when generating reports
- Package Analysis big query is not updating, working on bug

### Up Next

- Dependency confusion documentation is top priority

### Questions/Issues for the TAC

None
