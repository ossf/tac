# 2025 Q2 Best Practices WG 

## Overview

The group continues to be active and is working on several simultaneous projects aligned with our Mission & Vision. There is continued strong demand for best practices and guidance on secure software development and supply chain security.

### Sub-groups

* Guides - [link](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)  
* EDU.SIG - [link](https://github.com/ossf/education/)  
* Memory Safety SIG - [link](https://github.com/ossf/Memory-Safety)  
* OpenSSF Best Practices Badge - [link](https://www.bestpractices.dev/)  
* OpenSSF Scorecard - [link](https://github.com/ossf/scorecard)  
* Best Practices Badge and Developing Secure Software (LFD121) course - [link](https://github.com/ossf/secure-sw-dev-fundamentals)  
* Security Baseline - [link](https://github.com/ossf/security-baseline)  
* Web (with SWAG) - [link](https://github.com/w3c-cg/swag/)


## Best Practices Badge

### Purpose

* The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

#### Current Status

* As of 2025-03-25 there were 8169 OSS projects pursuing an OpenSSF Best Practices badge, with 1674 projects achieving at least a passing level badge.  
* A vulnerability report was received and while it was determined not being a vulnerability per se, improvements were implemented.  
* Infrastructure improvements included dependency updates, such as Rails 8.0, and changes in staging where ActiveJob now uses a database backend to eliminate a rare race condition.  
* Continued processing of GDPR requests.

### Up Next

* Continued maintenance.

## Developing Secure Software Fundamentals Course (LFD121)

### Purpose

* Provide baseline security education for developers.

### Current Status

* As of 2025-03-25 our 2025 enrollments in all variations was 1,993. Enrollments in LFD121 was 1,649, LFD-121 (Japanese) was 32, LFD104x (edX first part) was 296, and LFD104x-JP (edX first part Japanese) was 16\.

### Up Next

* Continue to maintain content.

## Questions/Issues for the TAC

* Are there other ways we can get the word out for people to take the course and/or integrate it into organizations?

## EDU.SIG

### Purpose

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

### Current Status

* The "[Security for Software Development Managers](https://openssf.org/blog/2025/03/06/new-free-course-security-for-software-development-managers-lfd125/)" course is now available online. As of 2025-03-25 has 281 enrollments.  
* The final changes and scripting for LFEL1001, "[Understanding the EU CRA](https://docs.google.com/presentation/d/1j3OlNz2k5rk9KRD8ZZz8xvsM_hyxqOioK4UUkJTWee8/edit)" (aka “CRA 101”), have been completed. We are trying to get the free course released mid-April  
* An improved format of "[A Brief Introduction to Developing Secure Software](https://docs.google.com/presentation/d/12b7Wm6KRp9kd1oV3QVrJpiCWVDexxF8doYZOFOfLy2Y/edit)" (\< 1 hour summary) is available.  
* "What's in the SOSS" podcast on education has been recorded and will be released soon. Eight more guests are scheduled, with expected releases in February and March.

### Up Next

* Currently pressing to get release of LFEL 1001 \- please help us spread the word in mid-April\!

## Concise Guides

### Purpose

* Artifacts that consolidate BEST practices in OSS software development and management techniques

### Current Status

* Guides under active development:   
  * [C/C++ Compiler Option Hardening](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C%2B%2B.md)
  * [Python Secure Coding Guide](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs/Secure-Coding-Guide-for-Python)
* Completed Guides (under maintenance)
  * [Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)
  * [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)
  * [npm Best Practices Guide](https://github.com/ossf/package-manager-best-practices/blob/main/published/npm.md)
  * [Source Code Management Platform Configuration Best Practices Guide](https://best.openssf.org/SCM-BestPractices/)

### Up Next

* Kicking off an effort to translate some of the guides to Swedish  
* Potential new guide based on topics discussed in breakout sessions at DC Policy Summit (see Additional Information below)

## C/C++ Compiler Option Hardening Guide

### Purpose

* Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

### Current Status

* Receiving and discussing very valuable feedback from adopters and implementers of the guide (e.g., [blog post](https://www.chainguard.dev/unchained/mitigating-a-rsync-vulnerability-a-lesson-in-compiler-hardening) by Chainguard). Looking into arranging a dedicated feedback session.   
* Continued revision, updates, & enhancement, e.g., keeping the compiler options hardening guide up-to-date with upstream options additions and changes in GCC and Clang/LLVM and addressing feedback from Linux distribution communities.  
* Resumed work on [Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) which provides guidance on leveraging attributes to annotate C/C++ code with the goal of enabling a compiler to perform better code analysis.

### Up next

* Microsoft MSVC guidance planned for 2025 (tracked in [BEST Issue 150](https://github.com/ossf/wg-best-practices-os-developers/issues/150))  
* Plan outreach activities for 2025, possibly talks aimed at C++ conferences.

## Python Secure Coding Guide

### Purpose

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.  
* Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

### Current Status

* The group is working on adding more content for a broad range of CWE rules. The status is being tracked in issue [531](https://github.com/ossf/wg-best-practices-os-developers/issues/531).  
* Feedback from and discussion with Seth Larson on the content and community outreach.

### Up Next

* We invited people from MITRE for feedback and further collaboration. In particular, we are looking for feedback regarding our use of CWEs to structure the guide.

## Memory Safety SIG

### Purpose

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

### Current Status

* Released the [Memory Safety Continuum](https://github.com/ossf/Memory-Safety/blob/main/docs/memory-safety-continuum/memory-safety-continuum.md) document
* Scorecard release of memory safety check (unsafe block check)

### Up Next

* Focus on interoperability and interfacing between memory safe by default and non-memory safe by default languages in software.

## OpenSSF Scorecard

### Purpose

* Automate analysis and trust decisions on the security posture of open source projects.  
* Use this data to proactively improve the security posture of the critical projects the world depends on.

### Current Status

* Progress on implementing and testing experimental probes (e.g., memory safety).  
* Discussion on personas and roles of maintainers and consumers in relation to Scorecard.  
* Consideration of including sponsorship in determining maintenance level of a project.

### Up Next

* Make OpenSSF Scorecard (and its GitHub Action) easier to run on groups of repositories  
* Build contributor base  
* Work towards project graduation  
* Refine project release cadence  
* Align with forthcoming OpenSSF persona work

## Security Baseline

## Purpose

* The goal of this SIG is to evolve OpenSSF security baseline for Linux Foundation wide adoption.  
* For OpenSSF adoption of the security baseline, there needs to be a home for tracking the adoption, for maintainers to raise issues to refine the security baseline, merge the baseline back to TAC lifecycle, and for OpenSSF to develop the roadmap for the security baseline. It will provide a venue for early adopters to share their reusable code and findings with other maintainers. The pilot adoption builds the foundation for wider adoption of the security baseline in OpenSSF and in Linux Foundation.  
* This SIG creates a venue for other participating foundations to help evolve the OpenSSF security baseline into a security baseline that can be applied to a broad range of software-based projects. The group will define the right level of risks that the security baseline is applicable for, the effectiveness measurement of the security baseline, and the adoption path of the security baseline at the minimum.

### Current Status

* [Security Baseline](https://openssf.org/projects/osps-baseline/) has been [released](https://baseline.openssf.org/versions/2025-02-25) ([blog post](https://openssf.org/press-release/2025/02/25/openssf-announces-initial-release-of-the-open-source-project-security-baseline/)).
* Collaboration with pilot projects, e.g., OpenSSF and CNCF projects ([CNCF Security Slam](https://kccnceu2025.sched.com/type/Experiences/Security+Slam)), but more feedback from other projects always welcome.
* A (prototype) tool for scanning GitHub repositories against Baseline requirements has been implemented. The scanner will move to an OpenSSF repo soon. Discussion with Scorecard and all other tools related to Baseline regarding future evolution and collaboration is ongoing.

### Up Next

* Lots of presentations (e.g., Kubecon, VulnCon) about Baseline scheduled to create awareness and solicit feedback.
* Baseline will be part of the next [CNCF Security Slam](https://kccnceu2025.sched.com/type/Experiences/Security+Slam).

## Web Developer Security Guide

### Purpose

* Develop security best practice and guidelines specifically aimed at web developers.

### Current Status

* The W3C SWAG group is actively working on reviewing and creating material for web developers, including  
  * a [Security Guidelines](https://github.com/w3c-cg/swag/blob/main/docs/security_guidelines.md) document, and   
  * a [Libraries Guidelines](https://github.com/w3c-cg/swag/blob/main/docs/guidelines_for_libraries.md) document.  
* The group is holding weekly calls. The calls are minuted here: [https://github.com/w3c-cg/swag/tree/main/meetings](https://github.com/w3c-cg/swag/tree/main/meetings).  
* Call for participation by OpenSSF contributors and ongoing conversations on how to foster cross-collaboration.  
* Videos & Blog Post on XSS  
  * New blog posts on XSS : [https://www.w3.org/blog/2025/how-to-protect-your-web-applications-from-xss/](https://www.w3.org/blog/2025/how-to-protect-your-web-applications-from-xss/) protection including link to a YouTube playlist of the guest lectures from Google folks late last year on XSS and some tooling for developers: [https://www.youtube.com/playlist?list=PLNhYw8KaLq2Wr27HLfSTD4d6JpC3G0PVr](https://www.youtube.com/playlist?list=PLNhYw8KaLq2Wr27HLfSTD4d6JpC3G0PVr)   
* Working towards June “deadline” (presentation proposed at both SOSS community day NA and EU)  
* New members of the group include Bytedance, Capital One and Samsung

### Up Next

* We anticipate starting work on the libraries doc after the new year and as well continue to develop the web developer guide. Both documents will be at the level of detail of the "concise guide" document. We also held a special call where some Google security folks came to talk about tooling they are building around CSP and Trusted Types. Those talks will be posted shortly.

## Questions/Issues for the TAC

* none

## Additional Information

* New topics for collaboration were discussed at the [DC Policy Summit](https://events.linuxfoundation.org/openssf-policy-summit-dc/) in a [break-out session](https://docs.google.com/document/d/1XzlTmDBPBpUPzVEE2ftOOwcqNRV1hqIPaeJSJk__ksE/edit):  
  * Improving component updates  
  * A structured approach to declaring an open source project’s maintenance or production status  
  * Self-attest disagreements in security scans  
  * Ensuring that executables match their claimed source code  
* We expect close collaboration between the Best Practices WG and the newly created [Global Cyber Policy WG](https://github.com/ossf/wg-globalcyberpolicy).

## Previous Updates

* [Q4 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q4-BEST-WG.md)  
* [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)  
* [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)  
* [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)  
* [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)

