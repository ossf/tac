# 2026 Q2 Best Practices WG

## Overview

The group continues to be active and is working on several simultaneous projects aligned with our Mission & Vision. There is continued strong demand for best practices and guidance on secure software development and supply chain security.

### Sub-groups

* Guides - [link](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)
  * C/C++ Compiler Option Hardening Guide - [link](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++.html)
  * Python Secure Coding Guide - [link](https://best.openssf.org/Secure-Coding-Guide-for-Python/)
* EDU.SIG - [link](https://github.com/ossf/education/)  
* Academic Connections SIG - [link](https://github.com/ossf/education/)
* Memory Safety SIG - [link](https://github.com/ossf/Memory-Safety)  
* OpenSSF Best Practices Badge - [link](https://www.bestpractices.dev/)  
* OpenSSF Scorecard - [link](https://github.com/ossf/scorecard)  
* Best Practices Badge and Developing Secure Software (LFD121) course - [link](https://github.com/ossf/secure-sw-dev-fundamentals)  
* Web Developer Security Guide (in collaboration with W3C) - [link](https://github.com/w3c-cg/swag/)

## Best Practices Badge

### Purpose

* The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

#### Current Status

* Integrated baseline criteria (levels 1–3) into the badge system. Projects can now complete forms and earn baseline badges, with a transition period ending 2026-06-01 for enforcing new criteria.
* Major performance optimization effort to handle increased load from ML crawlers - switched markdown processor (to Commonmarker/Rust), switched memory allocator to mimalloc, and reduced unnecessary object creation.
* Improved automation so external tools can propose badge fill-ins with user-visible highlights.
* Best practices badge meets baseline-3 itself: added SPDX SBOM generation, secrets policy, and escalated permissions policy.

### Up Next

* Support security-insights.yml. Some early discussion about making this format a new Gemara spec.

## EDU.SIG

### Purpose

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

### Current Status

* Completed modifications to LFD121 ("Developing Secure Software") to cover 12 areas of the Cybersecurity Skills Framework (CSF) by end of Q1 - tracked via a mapping spreadsheet and submitted as PR #201.
* Top contenders for new courses identified: (1) Embedding AI securely in systems, (2) simplified security architecture course; plan for BEST WG + AI/ML WG collaboration on an AI security guide

### Up Next

* ENISA Risk Framework course in progress (Harald Fischer); Dave Russo stepping back from Edu SIG, looking for new participants.

## Concise Guides

### Purpose

* Artifacts that consolidate BEST practices in OSS software development and management techniques

### Current Status

* The Python Secure Coding Guide has achieved its first release.
* A new concise guide covering upstream collaboration between corporate developers and open source maintainers has kicked off.
* Review and suggest plans for maintenance and alignment to AI-assisted practices for existing guides.

#### Overview of guides

**Guides under active development:**
* Python Secure Coding Guide (finalizing)
* Concise guide for upstream collaboration

**Completed Guides (under maintenance)**
* C/C++ Compiler Annotation Guide
* C/C++ Compiler Option Hardening
* Security Focused Guide for AI Code Assistant Instructions
* Concise Guide for Developing More Secure Software
* Concise Guide for Evaluating Open Source Software
* npm Best Practices Guide
* Source Code Management Platform Configuration Best Practices Guide
* Correctly Using Regular Expressions for Secure Input Validation
* Simplifying Software Component Updates
* The Memory Safety Continuum
* Cyber Resilience Act (CRA) Brief Guide for Open Source Software (OSS) Developers

## C/C++ Compiler Option Hardening Guide

### Purpose

* Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

### Current Status

* Compiler Annotations Guide for C and C++ approved for publication. Announcement blogpost went live on 2026-02-12
* After completing the Compiler Annotation Guide in addition to the Compiler Option Hardening Guide, the team has decided to put the monthly calls on hold and continue the maintenance of the guides asynchronously on GitHub only.

### Up next

* Continued maintenance on both guides.

## Python Secure Coding Guide

### Purpose

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.
Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

### Current Status

* First release achieved and approved. Currently applying the last finishing touches.

### Up Next

* Announcing the first release via a blog post.

## Memory Safety SIG

### Purpose

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

### Current Status

* The group decided that it was time to fold the activity back to the Best Practices Working Group and to continue the existing collaboration through the WG's channels and will not have a separate meetings or a separate mailing list.

### Up Next

* Continue the ongoing scorecard and guides work through the Best Practices Working Group.

## OpenSSF Scorecard

### Purpose

* Automate analysis and trust decisions on the security posture of open source projects.  
* Use this data to proactively improve the security posture of the critical projects the world depends on.

### Current Status

* 2026 roadmap defined (PR #4952)

### Up Next

* Roadmap implementation.

## Web Developer Security Guide

### Purpose

* Develop security best practice and guidelines specifically aimed at web developers.

### Current Status

* Published the SWAG security guidelines as a W3C Community Group draft report. Working on getting it at a stable URL.
Closed the web developer survey and drafted a blog post with findings. Key insight: web devs are generalists with surprisingly high security feature adoption. Also contributed a fetch Metadata guide to MDN and reviewed session management docs.
Reviewing the 400+ page ETSI draft on browser standards related to CRA; working on a threat modelling guide for web developers (MDN PR #42980).

### Up Next

* Continue working on a threat modelling [guide for web developers](https://github.com/mdn/content/pull/42980).

## Questions/Issues for the TAC

* none

## Additional Information

* none

## Previous Updates

* [Q1 2026](https://github.com/ossf/tac/blob/main/TI-reports/2026/2026-Q1-BEST-WG.md)
* [Q4 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q4-BEST-WG.md)
* [Q3 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q3-BEST-WG.md)
* [Q2 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q2-BEST-WG.md)
* [Q4 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q4-BEST-WG.md)  
* [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)  
* [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)  
* [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)  
* [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)
