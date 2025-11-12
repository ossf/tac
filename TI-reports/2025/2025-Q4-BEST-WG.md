# 2025 Q4 Best Practices WG

## Overview

The group continues to be active and is working on several simultaneous projects aligned with our Mission & Vision. There is continued strong demand for best practices and guidance on secure software development and supply chain security.

### **Sub-groups**

* [Guides](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)  
* [EDU.SIG](https://github.com/ossf/education/)  
* [Memory Safety SIG](https://github.com/ossf/Memory-Safety)  
* [OpenSSF Best Practices Badge](https://www.bestpractices.dev/)  
* [OpenSSF Scorecard](https://github.com/ossf/scorecard)  
* [Best Practices Badge and Developing Secure Software (LFD121) course](https://github.com/ossf/secure-sw-dev-fundamentals)  
* [Web (with SWAG)](https://github.com/w3c-cg/swag/)

## **Activity**

### **Best Practices Badge**

#### **Purpose**

* The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

#### **Status Update**

* Continued maintenance (e.g., on 2025-08-25, 97.2% transitive gems up-to-date out of 208), including security updates
* Small feature improvements (e.g., transferring ownership of badges)
* Steady growth. As of 2025-09-28 we had 8,994 participating projects, compared to 2025-06-28’s 7,289.

#### **Up Next**

* Continued maintenance.

### **EDU.SIG**

#### **Purpose**

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

#### **Status Update**

* A new free course “Secure AI/ML-Driven Software Development (LFEL1012)” was co-developed with the AI/ML WG. The content is ready and has been submitted to LF Education.
  * We expect to release it October 16; sign up [here to get release notification](https://docs.google.com/forms/d/e/1FAIpQLSfWW8M6PwOM62VHgc-YyogzT-eK_scJVk21BtezFUnJmMx6DQ/viewform)
  * When it’s available it will be at [this location](https://training.linuxfoundation.org/express-learning/secure-ai-ml-driven-software-development-lfel1012)
* Under the umbrella of creating ["OSS Newbie" class & materials](https://github.com/ossf/education/issues/72), a [first blog](https://openssf.org/blog/2025/08/08/from-beginner-to-builder-understanding-openssf-community-and-working-groups/) post was published

#### **Up Next**

* Initial research into a course on [“Doing Risk Assessments per the ENISA framework”](https://github.com/ossf/education/issues/83) course #83

### **Concise Guides**

#### **Purpose**

* Artifacts that consolidate BEST practices in OSS software development and management techniques

#### **Status Update**

* A new [Security Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions) was released. This guide was jointly developed by the Best Practices WG and the AI/ML WG. The upcoming course (LFEL1012) refers to this guide.
* A [Cyber Resilience Act (CRA) Brief Guide for Open Source Software (OSS) Developers](https://best.openssf.org/CRA-Brief-Guide-for-OSS-Developers) was released

Overview of guides:

* Guides under active development:   
  * [C/C++ Compiler Option Hardening](https://github.com/ossf/tac/diffs/0?base_sha=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&branch=87769be64cb25d5808e856910370771544fbe4e6&commentable=true&head_user=gkunz&name=87769be64cb25d5808e856910370771544fbe4e6&pull_number=423&qualified_name=87769be64cb25d5808e856910370771544fbe4e6&sha1=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&sha2=87769be64cb25d5808e856910370771544fbe4e6&short_path=409950f&unchanged=expanded&w=false#cc-compiler-option-hardening-guide)  
  * [Python Secure Coding Guide](https://github.com/ossf/tac/diffs/0?base_sha=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&branch=87769be64cb25d5808e856910370771544fbe4e6&commentable=true&head_user=gkunz&name=87769be64cb25d5808e856910370771544fbe4e6&pull_number=423&qualified_name=87769be64cb25d5808e856910370771544fbe4e6&sha1=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&sha2=87769be64cb25d5808e856910370771544fbe4e6&short_path=409950f&unchanged=expanded&w=false#python-secure-coding-guide)  
* Completed Guides (under maintenance)  
  * [Security Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions)
  * [Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)
  * [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software)
  * [npm Best Practices Guide](https://github.com/ossf/package-manager-best-practices/blob/main/published/npm.md)
  * [Source Code Management Platform Configuration Best Practices Guide](https://best.openssf.org/SCM-BestPractices/)
  * [Correctly Using Regular Expressions for Secure Input Validation](https://best.openssf.org/Correctly-Using-Regular-Expressions)
  * [Simplifying Software Component Updates](https://best.openssf.org/Simplifying-Software-Component-Updates)
  * [The Memory Safety Continuum](https://memorysafety.openssf.org/memory-safety-continuum)
  * [Cyber Resilience Act (CRA) Brief Guide for Open Source Software (OSS) Developers](https://best.openssf.org/CRA-Brief-Guide-for-OSS-Developers)

#### **Up Next**

* Additional guides based on topics discussed in breakout sessions at DC Policy Summit. Ideas include (aka are in the backlog):
  * A way to formally declare maintenance/production level intent for OSS project
  * How to handle freshness of dependencies?
  * Guidance about testing for OSS projects.
  * Guidance on how to ensure that executables match their putative source code.

### **C/C++ Compiler Option Hardening Guide**

#### **Purpose**

* Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

#### **Status Update**

* Compiler Options Guide: Continued revision, updates, and enhancements. 
A complementary [Compiler Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) has been drafted and is nearing completion. A request for comments will be sent to the community (BEST WG) shortly.

#### **Up next**

* Release C/C++ [Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) after soliciting and incorporating feedback from the community.

### **Python Secure Coding Guide**

#### **Purpose**

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.  
* Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

#### **Status Update**

* Content-wise the team is ready to cut a first release.
Last action before cutting a release is to update the structure of the guide (e.g., naming of coding rules) and structuring in topic areas.

#### **Up Next**

* First release by the end of this year.

### **Memory Safety SIG**

#### **Purpose**

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

#### **Status Update**

* The group focuses on exploring interoperability and interfacing between memory safe by default and non-memory safe by default languages.
Meeting cadence reduced to monthly.

#### **Up Next**

* Publish a guide for best practices when interfacing between memory safe by default and non-memory safe by default languages.

### **OpenSSF Scorecard**

#### **Purpose**

* Automate analysis and trust decisions on the security posture of open source projects.  
* Use this data to proactively improve the security posture of the critical projects the world depends on.

#### **Status Update**

* Wrapping up addressing the items identified during a security audit. A report will follow after a new release the week of Oct 6.
Integration / collaboration with Minder is being explored.
An AdaLogics contributor is working their way up the contribution ladder to give the project an additional maintainer

#### **Up Next**

* Roadmap + funding proposal planning

### **Web Developer Security Guide**

#### **Purpose**

* Develop security best practice and guidelines specifically aimed at web developers.

#### **Status Update**

* Presentation about this work at Open Source Summit US (Amsterdam)
* We merged some proposed changes on updating the [policy & regulatory document](https://github.com/w3c-cg/swag/blob/main/docs/regulatory_policy.md) (proposed by David W.)
* The group has developed a developer survey and we are working on getting this launched and out there - the focus of the survey is to ask developers how they are using currently available web security features in their projects.


#### **Up Next**

* Still pending: publish a link to the guide on https://best.openssf.org/
* Progress with the developer survey and get the word out.

## Questions/Issues for the TAC

* none

## **Additional Information**

* none

## **Previous Updates**

* [Q3 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q3-BEST-WG.md)
* [Q2 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q2-BEST-WG.md)  
* [Q4 2024 (== Q1 2025\)](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q4-BEST-WG.md)
* [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)  
* [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)  
* [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)  
* [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)
