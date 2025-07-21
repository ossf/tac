# 2025 Q3 Securing Critical Projects Working Group

## Overview

Sub-projects continue to run. Malicious Packages continues to
attract interest, and is splitting from Package Analysis. Attendance is low.

[2025-Q2 Update](2025-Q2-SCP-WG.md)

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

- Leveraging new, more comprehensive data sets
    - [Census III](https://www.linuxfoundation.org/research/census-iii)
    - [Ecosyste.ms](https://ecosyste.ms/) data

### Up Next

- Now that we have a good idea of critical projects, OSTIF is proposing a Managed Audit Program to go out and do the following to projects identified as critical:
    - Establish contact with maintainer(s)/community.
    - Collaborate with them to determine their security posture and needs.
    - Commission security experts to assess the project, do threat modeling and perform third party review, build/augment security tooling, and review the project for supply chain security risks.
    - Commission security experts to work with the project on bug and vulnerability fixes, tooling and supply chain security improvements. 
    - Document and publish the work done in a report. 
    - Publish annual impact reports of the work done (bugs/vulns fixed, tooling implemented, etc) 

## Criticality Score

### Purpose

1. Generate a criticality score for every open source project.

1. Create a list of critical projects that the open source community depends
   on.

1. Use this data to proactively improve the security posture of these critical
   projects.

### Current Status

- Run not working regularly, but get a successful run here and there
- Working through quota issues

### Up Next

- Improve reliability

## Package Analysis

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

### Current Status

- No major updates

## Malicious Packages

### Purpose

Malicious Packages is a collection of reports of malicious packages identified in
Open Source package repositories, consumable via the Open Source Vulnerability
(OSV) format.

The aim of this project and repository is to be a comprehensive, high quality, open source database of reports of malicious packages published on open source package repositories.

These public reports help protect the open source community, and provide a data source for the security community to improve their ability to find and detect new open source malware.

### Current Status

- Regular submissions and activity
- Was under Package Analysis
- Splitting to separate project
- https://github.com/ossf/tac/pull/500

### Up Next

- Work on lifecycle process

## OSTIF Managed Audit Program

### Current Status

- Multiple security audit results released
    - Ruby on Rails (made it to front page of hacker news) 
    - RSTUF (in case it wasn’t mentioned last time) 
    - Security Scorecard (in post-audit remediation phase) 

### Up Next

- Critical Open Source Software Managed Audit Program
