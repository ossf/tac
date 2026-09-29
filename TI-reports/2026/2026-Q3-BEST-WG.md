# 2026 Q3 Best Practices WG

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

* Best Practices Badge project (belatedly) earned "[graduated](https://github.com/ossf/tac/blob/main/process/project-lifecycle-documents/best_practices_badge_graduation_stage.md)" stage.
* Repo migrated from `coreinfrastructure` to the `ossf` organization
* Mitigations against email subscription bombing (attackers using activation / password-reset emails to harass users): purged 34,413 never-activated accounts and 217 "suspicious" activated accounts; unactivated accounts now auto-delete after 7 days; password resets are blocked on unactivated accounts; account activation now requires an authenticated POST (not a plain GET).
* Dramatically increased Fastly CDN caching for non-personalized pages to handle heavy load from AI/web crawlers.
* Published "[The Road to Gold: How CPS Set a New Standard for Security and Quality in Open Source](https://openssf.org/blog/2026/05/07/the-road-to-gold-how-cps-set-a-new-standard-for-security-and-quality-in-open-source/)" (2026-05-07).

### Up Next

* Continued work with LF IT to enable inbound email so a permanent fix for subscription-bombing is possible.  
* Continued maintenance and hardening (including AI-assisted vulnerability review).

## EDU.SIG

### Purpose

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

### Current Status

* New EDU.SIG co-leads: David A. Wheeler and Justin Cappos. Dave Russo is stepping back due to a change in role.
* Change of scope for the planned AI course: originally "Securely embedding AI in systems", now "Finding and Fixing Software Vulnerabilities with AI" (aligned with AI/ML WG). Target audience is developers and maintainers of their own projects. Draft content has been compiled, feedback is welcome before the final course will be created.
* Academic Connections SIG: [SCORED](https://scored.dev/) (academic conference on OSS security) is confirmed for 2026-10-06 as a second track of OpenSSF Community Day in Prague. An "in-cooperation with ACM" agreement has been secured, with paperwork underway so accepted papers can be indexed in the ACM Digital Library. Sponsorships still available and wanted.
* Met with Governing Board representatives on yearly progress / plan; work is on track.

### Up Next

* Continue drafting the "Finding and Fixing Vulnerabilities with AI" guide and derive the course from it.
* Continue to drive SCORED 2026.

## Concise Guides

### Purpose

* Artifacts that consolidate BEST practices in OSS software development and management techniques

### Status Update

* Continued work on the new [Concise Guide for Collaborating with Open Source Projects](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Concise-Guide-for-Collaborating-with-Open-Source-Projects.md)

Overview of guides:

* Guides under active development:
  * [Python Secure Coding Guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Secure-Coding-Guide-for-Python)
  * [Concise guide for upstream collaboration](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Concise-Guide-for-Collaborating-with-Open-Source-Projects.md)  
* Completed Guides (under maintenance)  
  * [C/C++ Compiler Annotation Guide](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C++.html)  
  * [C/C++ Compiler Option Hardening](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++)  
  * [Security Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions)  
  * [Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)  
  * [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)  
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

* Continued maintenance of both guides (compiler options and compiler annotations)
* Adding example code for C and C++ compiler annotations

### Up next

* Continued asynchronous maintenance of both guides on GitHub.
* Conversation about adoption of compiler options guide for Microsoft MSVC compiler

## Python Secure Coding Guide

### Purpose

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.  
* Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

### Status Update

* Continued development of the Python Secure Coding guide
* Ongoing collaboration with Python community in Ireland: presented in-person at the Irish Python User Group meetup in Dublin
* Talk submitted to PyCon Ireland 2026 (Dublin, November)
* Release blog post "[Secure Coding Guide for Python (pySCG) First Release](https://openssf.org/blog/2026/05/12/secure-coding-guide-for-python-pyscg-first-release/)" was published

### Up Next

* The team intends to move the guide out to a separate repository to faciliate automation, rendering, and management of the content

## Memory Safety SIG

### Purpose

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

### Status Update

* Given lower-than-expected participation over the past months, the SIG is considering folding its activities back into the broader Best Practices WG; a community discussion has been initiated over the WG calls.

### Up Next

* Complete the community discussion and decide on the SIG's future structure.

## OpenSSF Scorecard

### Purpose

* Automate analysis and trust decisions on the security posture of open source projects.  
* Use this data to proactively improve the security posture of the critical projects the world depends on.

### Status Update

[Scorecard infrastructure migration](https://github.com/ossf/scorecard-infra) from GCP to AWS —
in partnership with [AboutCode Foundation](https://aboutcode.org) — initial cutover on 2026-08-31.

[Funding was winding down](https://github.com/ossf/tac/issues/552); rather than interrupt a service
the ecosystem depends on, the Steering Committee secured a durable, community-run home for it.

See the announcement in [scorecard#5208](https://github.com/ossf/scorecard/issues/5208) and the
tracking issue at [scorecard-infra#77](https://github.com/ossf/scorecard-infra/issues/77).

Breaking changes users should be aware of:

* BigQuery public dataset discontinued
* Container images moved from `gcr.io/openssf/scorecard` to `ghcr.io/ossf/scorecard`
* Scorecard Action users must upgrade to [v2.4.4+](https://github.com/ossf/scorecard-action/releases/tag/v2.4.4)
* Allstar's hosted GitHub App was retired as part of the same cutover — it remains under active
  development — it just requires [self-hosting](https://github.com/ossf/allstar/issues/881) moving forward

Community response has been strong:

* Renovate shipped an [auto-migration PR](https://github.com/renovatebot/renovate/pull/45597) for
users still on the old registry, and reported breakages e.g., `urllib3` were resolved within hours.

### Up Next

* Chartering a dedicated Scorecard Infrastructure group to build sustainable infra for the project
* Issue backlog pruning
* Scorecard v6 / OSPS Baseline work
* [Scorecard MCP server](https://github.com/uwu-tools/scorecard-mcp) is available for early testing.
  Feedback welcome!

## Web Developer Security Guide

### Purpose

* Develop security best practice and guidelines specifically aimed at web developers.

### Status Update

* Re-published the SWAG guidelines at a stable URL: [https://w3c-cg.github.io/swag/docs/swag.html](https://w3c-cg.github.io/swag/docs/swag.html); the group has agreed to fold the separate "libraries" guidelines document into the main guide.
* Contributed a Fetch Metadata guide to MDN ([mdn/content \#43424](https://github.com/mdn/content/pull/43424))
* Presented "[What are web developers doing about security?](https://openssfcdna2026.sched.com/event/2I45f/what-are-web-developers-doing-about-security-daniel-appelquist-samsung)" at OpenSSF Community Day North America.
* Held a joint session on package managers with Andrew Nesbit

### Up Next

* Aiming to land 2 minor changes before declaring 1.0: [dependency cooldowns](https://cooldowns.dev/) and [trusted publishing](https://github.com/w3c-cg/swag/issues/58)

## Additional activities

* Two new experimental AI "skills" incubating with the WG that may become future BEST WG projects: David A. Wheeler's [secure-dependencies](https://github.com/david-a-wheeler/secure-dependencies) (due diligence for dependencies using AI) and Jordan Conway's [package-manager-hardening](https://github.com/jordanconway/package-manager-hardening) (hardening the *use* of package managers, informed by the Axios compromise).

## Funding requests and updates

Are you considering applying for any [funding requests](https://github.com/ossf/tac/blob/main/process/TI%20Funding%20Request%20Process.md)?

* none

## Questions/Issues for the TAC

* none

## Previous Updates

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
