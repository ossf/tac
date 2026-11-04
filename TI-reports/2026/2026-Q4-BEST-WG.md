# 2026 Q4 Best Practices WG

## Overview

The group continues to be active and is working on several simultaneous projects aligned with our Mission & Vision. There is continued strong demand for best practices and guidance on secure software development and supply chain security.

### Sub-groups

* [OpenSSF Best Practices Badge](https://www.bestpractices.dev/)
* [EDU.SIG](https://github.com/ossf/education/) and [Academic Connections SIG](https://github.com/ossf/education/)
* [Educational Guides](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)
* [Memory Safety SIG](https://github.com/ossf/Memory-Safety)  
* [OpenSSF Scorecard](https://github.com/ossf/scorecard) and [OpenSSF Allstar](https://github.com/ossf/allstar)
* [Web Developer Security Guide (in collaboration with W3C)](https://github.com/w3c-cg/swag/)

## Best Practices Badge

### Purpose

* The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

### Current Status

* Infrastructure: upgraded to PostgreSQL 18 and Ubuntu 26, with updates automated so vulnerability fixes can be deployed quickly.
* Translations: machine translation now reuses common phrases (1–3-word sequences) from existing human translations, so terminology stays consistent.
* Baseline: the criteria are up to date with the latest OSPS Baseline.
* Session hardening against AI-enabled attackers:
  * Users now get random session IDs, and the database stores only a hash of each ID linked to the user.
  * Even an attacker who has both the server secret and database access can't spoof a user or take over a session.
  * The key is rotated daily.
  * Write-up: LinkedIn post "Harden your software".

### Up Next

* TODO: TBD

## EDU.SIG

### Purpose

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

### Current Status

* Release the new [Finding and Fixing Vulnerabilities Using AI](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Finding-and-Fixing-Vulnerabilities-Using-AI) guide
  * Yannick Moy has since contributed improvements, and France's cybersecurity agency ANSSI is expected to use it.
* SCORED 2026 (October 6, Prague, co-located with OpenSSF Community Day):
  * 15 papers accepted out of 74 submissions; the event drew strong attendance and good industry–academia interaction.
  * Best paper: "Software Dark Matter" (Purdue/Bloomberg), which found three confirmed high-severity CVEs.
  * Open issue: sponsorship was hard to find

### Up Next

* The guide becomes a course with quizzes and a final exam. LF Education is speeding this up and has asked for the final exam as soon as possible.

## Concise Guides

### Purpose

* Artifacts that consolidate BEST practices in OSS software development and management techniques

### Status Update

* Released the new [Concise Guide for Collaborating with Open Source Projects](https://best.openssf.org/Concise-Guide-for-Collaborating-with-Open-Source-Projects)

Overview of guides:

* Guides under active development:
  * [Python Secure Coding Guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Secure-Coding-Guide-for-Python)
* Completed Guides (under maintenance)  
  * [C/C++ Compiler Annotation Guide](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C++.html)  
  * [C/C++ Compiler Option Hardening](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++)  
  * [Security Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions)  
  * [Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)  
  * [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)
  * [Concise Guide for Collaborating with Open Source Projects](https://best.openssf.org/Concise-Guide-for-Collaborating-with-Open-Source-Projects)
  * [npm Best Practices Guide](https://github.com/ossf/package-manager-best-practices/blob/main/published/npm.md)  
  * [Source Code Management Platform Configuration Best Practices Guide](https://best.openssf.org/SCM-BestPractices/)  
  * [Correctly Using Regular Expressions for Secure Input Validation](https://best.openssf.org/Correctly-Using-Regular-Expressions)  
  * [Simplifying Software Component Updates](https://best.openssf.org/Simplifying-Software-Component-Updates)  
  * [The Memory Safety Continuum](https://memorysafety.openssf.org/memory-safety-continuum)  
  * [Cyber Resilience Act (CRA) Brief Guide for Open Source Software (OSS) Developers](https://best.openssf.org/CRA-Brief-Guide-for-OSS-Developers)

## C/C++ Compiler Guides

### Purpose

* Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

### Status Update

* Continued maintenance of the compiler options and compiler annotations guides.
* MSVC compiler options guide was released under Creative Commons on GitHub.

### Up next

* Adding Microsoft MSVC compiler options guide to the overall corpus as a separate document.

## Python Secure Coding Guide

### Purpose

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.  
* Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

### Status Update

* Moved to new dedicated [repository](https://github.com/ossf/python-secure-coding-guide). Open issues and PRs have been migrated.
* Talk accepted at PyCon Ireland 2026 (November 21).
* Building out the cryptography section (09), checking each candidate rule against CVE, EPSS and CWE data.
* Discussing versioning so new content can be added step by step.

### Up Next

* TODO

## Memory Safety SIG

### Purpose

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

### Status Update

* No updates.

### Up Next

* Roadmap for 2027

## OpenSSF Scorecard

### Purpose

* Automate analysis and trust decisions on the security posture of open source projects.  
* Use this data to proactively improve the security posture of the critical projects the world depends on.

### Status Update

TBD

### Up Next

TBD

## Web Developer Security Guide

### Purpose

* Develop security best practice and guidelines specifically aimed at web developers.

### Status Update

* The last additions to the [guidelines document](https://w3c-cg.github.io/swag/docs/swag.html) were finished.
* The W3C Community Group issued its final report, and the guidelines are now in maintenance mode.

### Up Next

* The guideline will receive a dedicated URL shortly
* The guideline will be placed in maintenace

## Funding requests and updates

Are you considering applying for any [funding requests](https://github.com/ossf/tac/blob/main/process/TI%20Funding%20Request%20Process.md)?

* none

## Questions/Issues for the TAC

* none

## Previous Updates

* [Q3 2026](https://github.com/ossf/tac/blob/main/TI-reports/2026/2026-Q3-BEST-WG.md)
* [Q2 2026](https://github.com/ossf/tac/blob/main/TI-reports/2026/2026-Q2-BEST-WG.md)
* [Q1 2026](https://github.com/ossf/tac/blob/main/TI-reports/2026/2026-Q1-BEST-WG.md)
* [Q4 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q4-BEST-WG.md)
* [Q3 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q3-BEST-WG.md)
* [Q2 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q2-BEST-WG.md)
* [Q4 2024 (== Q1 2025\)](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q4-BEST-WG.md)
* [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)
* [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)
* [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)
* [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)
