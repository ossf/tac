# 2025 Q3 Best Practices WG

## Overview

### **Sub-groups**

* [Guides](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)  
* [EDU.SIG](https://github.com/ossf/education/)  
* [Memory Safety SIG](https://github.com/ossf/Memory-Safety)  
* [OpenSSF Best Practices Badge](https://www.bestpractices.dev/)  
* [OpenSSF Scorecard](https://github.com/ossf/scorecard)  
* [Best Practices Badge and Developing Secure Software (LFD121) course](https://github.com/ossf/secure-sw-dev-fundamentals)  
* [Security Baseline](https://github.com/ossf/security-baseline)  
* [Web (with SWAG)](https://github.com/w3c-cg/swag/)

## **Activity**

### **Best Practices Badge**

#### **Purpose**

* The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

#### **Status Update**

* Continued maintenance and security updates.   
* Resolved subtle problem that was preventing ONAP from earning a gold badge.  
* Extremely high number of requests results in logs growing too large to store. The requests are likely caused by content collection for AI training.

**Up Next**

* Continued maintenance.

### **EDU.SIG**

#### **Purpose**

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

#### **Status Update**

* LFD121 labs are being translated into Japanese\!  
* LFD121 \- added warnings about AI-generated code (it can have vulnerabilities including slopsquatting)  
* CRA 101 course "[Understanding the EU CRA](https://training.linuxfoundation.org/express-learning/understanding-the-eu-cyber-resilience-act-cra-lfel1001/)" (LFEL1001) released. Enrollment is 3,111 as of 2025-05-27

#### **Up Next**

* Initial research into the c[reation of a  "OSS Newbie" class & materials](https://github.com/ossf/education/issues/72)  
* Initial research into a course on [“Doing Risk Assessments per the ENISA framework” course \#83](https://github.com/ossf/education/issues/83) 

### **Concise Guides**

#### **Purpose**

* Artifacts that consolidate BEST practices in OSS software development and management techniques

#### **Status Update**

* A new guide on [Simplifying Software Component Updates](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Simplifying-Software-Component-Updates.md) was drafted and published. This guide is based on topics discussed at the 2025 DC Policy Summit.
* A new [Security-Focused Guide for AI Code Assistant Instructions](https://github.com/ossf/wg-best-practices-os-developers/pull/936) is being developed to help developers write better instructions for AI code assistants, such as Copilot, to produce more secure code. The guide will be based on the existing foundation guides and courses and is a joint effort with the Memory Safety SIG, the AI/ML WG and the Best Practices WG. The guide will be available in the coming months.
* A Swedish translation of the Concise Guide for Evaluating Open Source Software is [ongoing](https://github.com/ossf/wg-best-practices-os-developers/pull/867).  
* A [Cyber Resilience Act (CRA) Brief Guide for Open Source Software (OSS) Developers](https://best.openssf.org/CRA-Brief-Guide-for-OSS-Developers) has been created jointly with the Global Cyber Policy Working Group.

Overview of guides:

* Guides under active development:   
  * [C/C++ Compiler Option Hardening](https://github.com/ossf/tac/diffs/0?base_sha=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&branch=87769be64cb25d5808e856910370771544fbe4e6&commentable=true&head_user=gkunz&name=87769be64cb25d5808e856910370771544fbe4e6&pull_number=423&qualified_name=87769be64cb25d5808e856910370771544fbe4e6&sha1=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&sha2=87769be64cb25d5808e856910370771544fbe4e6&short_path=409950f&unchanged=expanded&w=false#cc-compiler-option-hardening-guide)  
  * [Python Secure Coding Guide](https://github.com/ossf/tac/diffs/0?base_sha=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&branch=87769be64cb25d5808e856910370771544fbe4e6&commentable=true&head_user=gkunz&name=87769be64cb25d5808e856910370771544fbe4e6&pull_number=423&qualified_name=87769be64cb25d5808e856910370771544fbe4e6&sha1=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&sha2=87769be64cb25d5808e856910370771544fbe4e6&short_path=409950f&unchanged=expanded&w=false#python-secure-coding-guide)  
* Completed Guides (under maintenance)  
  * [Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)  
  * [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)  
  * [npm Best Practices Guide](https://github.com/ossf/package-manager-best-practices/blob/main/published/npm.md)  
  * [Source Code Management Platform Configuration Best Practices Guide](https://best.openssf.org/SCM-BestPractices/)

#### **Up Next**

* Additional guides based on topics discussed in breakout sessions at DC Policy Summit. Ideas include:  
  * A way to formally declare maintenance/production level intent for OSS project  
  * How to handle freshness of dependencies?   
  * Guidance about testing for OSS projects.  
  * Guidance on how to ensure that executables match their putative source code. 

### **C/C++ Compiler Option Hardening Guide**

#### **Purpose**

* Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

#### **Status Update**

* The guide was featured in a recently published [case study](https://openssf.org/blog/2025/05/15/case-study-ericssons-c-c-compiler-options-hardening-guide-and-openssf-collaboration/).  
* Continued revision, updates, & enhancement, e.g., keeping the compiler options hardening guide up-to-date with upstream options additions and changes in GCC and Clang/LLVM and addressing feedback from Linux distribution communities.  
* Continued work on an [Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) which provides guidance on leveraging attributes to annotate C/C++ code with the goal of enabling a compiler to perform better code analysis.

#### **Up next**

* Aiming to distribute [Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) for a wider audience (e.g., OpenSSF BEST WG mailing list) when full draft is available in the latter half of 2025\.

### **Python Secure Coding Guide**

#### **Purpose**

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.  
* Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

#### **Status Update**

* Discussions with the CWE team @ MITRE on our use of CWE in the guide. Additionally, there is an opportunity to contribute some of our code examples to the MITRE CWE corpus. The team is [planning to change the titles](https://github.com/ossf/wg-best-practices-os-developers/issues/894) of the rules to distinguish them from CWEs. In this context, the style of the language shall also change from “what not to do” (as in CWEs) to “what to do”.

#### **Up Next**

* Continued work on adding more content. Tracked in issue [531](https://github.com/ossf/wg-best-practices-os-developers/issues/531).

### **Memory Safety SIG**

#### **Purpose**

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

#### **Status Update**

* More Scorecard probes are being developed, including a probe for unsafe blocks in Java.
* The SIG is planning to update the Developing Secure Software Fundamentals course (LFD121) to include content from the recently released Memory Safety Continuum document.
* The SIG is collaborating with the AI/ML WG and the BEST WG to develop a Security-Focused Guide for AI Code Assistant Instructions (more info under Concise Guides section).
* Engaged with EU-focused memory safety efforts and shared updates from events such as RustNL workshops, considering how these might influence funding or modernization.

#### **Up Next**

* Focus on interoperability and interfacing between memory safe by default and non-memory safe by default languages in software.

### **OpenSSF Scorecard**

#### **Purpose**

* Automate analysis and trust decisions on the security posture of open source projects.  
* Use this data to proactively improve the security posture of the critical projects the world depends on.

#### **Status Update**

* Release of Scorecard v5.2.0  
* Release of Allstar v.4.4   
* Initial discussions with Baseline on how to add support to Scorecard  
* Migration to new container registry Artifact Registry

#### **Up Next**

* Further explore support for Baseline

### **Security Baseline**

* The Security Baseline work has migrated to the [ORBIT WG](https://github.com/ossf/wg-orbit)

### **Web Developer Security Guide**

#### **Purpose**

* Develop security best practice and guidelines specifically aimed at web developers.

#### **Status Update**

* The W3C SWAG group is actively working on reviewing and creating material for web developers, including  
  * a [Security Guidelines](https://github.com/w3c-cg/swag/blob/main/docs/security_guidelines.md) document, and   
  * a [Libraries Guidelines](https://github.com/w3c-cg/swag/pull/10) document.  
  * a [Policy & Regulatory](https://github.com/w3c-cg/swag/pull/25) document  
* The group is holding weekly calls. The calls are minuted here: [https://github.com/w3c-cg/swag/tree/main/meetings](https://github.com/w3c-cg/swag/tree/main/meetings).  
* Call for participation by OpenSSF contributors and ongoing conversations on how to foster cross-collaboration.  
* Working towards June “deadline” (presentation proposed at both SOSS community day NA and EU)  
  * Talks accepted at both OpenSSF Community days NA and EU \- Dan working on slides

#### **Up Next**

* Working on a survey of web developers on use of security-related specs \- to be released along with W3C WebDX group.

## Questions/Issues for the TAC

* none

## **Additional Information**

* Close collaboration between the Best Practices WG and the [Global Cyber Policy WG](https://github.com/ossf/wg-globalcyberpolicy) is continuing.

## **Previous Updates**

* [Q2 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q2-BEST-WG.md)  
* [Q4 2024 (== Q1 2025\)](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q4-BEST-WG.md)   
* [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)  
* [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)  
* [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)  
* [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)
