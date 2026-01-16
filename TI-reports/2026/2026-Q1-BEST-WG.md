# 2026 Q1 Best Practices

## **Overview**

The group continues to be active and is working on several simultaneous projects aligned with our Mission & Vision. There is continued strong demand for best practices and guidance on secure software development and supply chain security.

### **Sub-groups**

* [Educational Guides](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)
  * [C/C++ Compiler Option Hardening](https://github.com/ossf/tac/diffs/0?base_sha=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&branch=87769be64cb25d5808e856910370771544fbe4e6&commentable=true&head_user=gkunz&name=87769be64cb25d5808e856910370771544fbe4e6&pull_number=423&qualified_name=87769be64cb25d5808e856910370771544fbe4e6&sha1=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&sha2=87769be64cb25d5808e856910370771544fbe4e6&short_path=409950f&unchanged=expanded&w=false#cc-compiler-option-hardening-guide)
  * [Python Secure Coding Guide](https://github.com/ossf/tac/diffs/0?base_sha=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&branch=87769be64cb25d5808e856910370771544fbe4e6&commentable=true&head_user=gkunz&name=87769be64cb25d5808e856910370771544fbe4e6&pull_number=423&qualified_name=87769be64cb25d5808e856910370771544fbe4e6&sha1=eed2ae23a0d8a2e5b18d9bcdeeb7fa40b75ac241&sha2=87769be64cb25d5808e856910370771544fbe4e6&short_path=409950f&unchanged=expanded&w=false#python-secure-coding-guide)
* [EDU.SIG](https://github.com/ossf/education/)
* [Memory Safety SIG](https://github.com/ossf/Memory-Safety)
* [OpenSSF Best Practices Badge](https://www.bestpractices.dev/)
* [OpenSSF Scorecard](https://github.com/ossf/scorecard) & [OpenSSF Allstar](https://github.com/ossf/allstar)
* [Web Developer Security Guide (in collaboration with W3C)](https://github.com/w3c-cg/swag/)
* [Academic Connections SIG](https://github.com/ossf/education/)

## **Activity**

### **Best Practices Badge**

#### **Purpose**

* The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

#### **Status Update**

* Working to integrate Baseline criteria into best practices badge. Phase 1-3 implemented, phase 4 ongoing. BP badge itself implements baseline-1
* Made some changes to better handle massive endless downloads, which are likely used for training ML systems: e.g., reduce rate limits, fewer items per page, to spread out the load. We are glad to share data, but we just don’t want to be overwhelmed. Some specifics are here: [https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/optimize-2025-12.md](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/optimize-2025-12.md)

**Up Next**

* Continued implementation of Baseline criteria.

### **EDU.SIG**

#### **Purpose**

* Deliver Baseline Secure Software Development Education and Certification to All. Provide access to open and widely available education materials to all learners. Materials will be maximally accessible and easy to consume for all learners.

#### **Status Update**

* Released Secure [AI/ML-Driven Software Development (LFEL1012)](https://training.linuxfoundation.org/express-learning/secure-ai-ml-driven-software-development-lfel1012/)
* Mapping of Cybersecurity Skills Framework to courses: We believe we can improve existing courses to improve support of framework without too much effort, probably will work early 2026
* Courses have been added to the US Government’s NICCS [catalog](https://niccs.cisa.gov/training/catalog/tlf): Security for Software Development Managers (LFD125); Understanding the EU Cyber Resilience Act (CRA) (LFEL1001); Secure AI/ML-Driven Software Development (LFEL1012). LFD121 was already there.
* A new Academic Connections SIG has been established

#### **Up Next**

* ENISA Risk Framework course in progress.
* OpenSSF CyberSecurity certification planning \- look for more details next year as we develop a certification based on the works of the foundation

### **Concise Guides**

#### **Purpose**

* Artifacts that consolidate BEST practices in OSS software development and management techniques

#### **Status Update**

* A [Compiler Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) for C/C++ compilers has been released.
* Added a Swedish translation of the [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/sv/Concise-Guide-for-Evaluating-Open-Source-Software)

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

* Additional guides are being discussed, in particular in the context of addressing needs arising from regulation such as the Cyber Resilience Act. Such guides would be created in collaboration with the Global Cyber Policy Working Group.
* Example: * How to contribute upstream security improvements to open source projects.

### **C/C++ Compiler Guides**

#### **Purpose**

* Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

#### **Status Update**

* Compiler Options Guide: Continued revision, updates, and enhancements.
* A complementary [Compiler Annotation Guide](https://github.com/ossf/wg-best-practices-os-developers/blob/main/docs/Compiler-Hardening-Guides/Compiler-Annotations-for-C-and-C%2B%2B.md) has been released.

#### **Up next**

* Compiler Hardening Guides sub-initiative is looking for individuals interested in taking a leadership role in the initiative and the Compiler Hardening BP calls with fresh ideas for how to develop the initiative in 2026

### **Python Secure Coding Guide**

#### **Purpose**

* Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.
* Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

#### **Status Update**

* The team has reworked the structure of the guide based on conversations with MITRE. Originally, the guide was structured around CWEs. To avoid misunderstandings, the guide now uses an independent structure and maps CWEs to this.
* Talk proposal submitted to security track of PyCon US

#### **Up Next**

* The rules of the guide are being rephrased from DON’T DO to DOs
* First release

### **Memory Safety SIG**

#### **Purpose**

* The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

#### **Status Update**

* Java Memory Safety scorecard probe is in PR
* Starting to gather data for the interfacing between memory safe and non memory safe by default languages.

#### **Up Next**

* Raised potential TI with Rust Foundation on tooling/guides for integrating between rust and C++
* Potential new collaboration with the AI/ML WG about Agents Memory Safety

### **OpenSSF Scorecard**

#### **Purpose**

* Automate analysis and trust decisions on the security posture of open source projects.
* Use this data to proactively improve the security posture of the critical projects the world depends on.

#### **Status Update**

* Discussions with the TAC and OpenSSF staff ongoing regarding funding of hosted services.
* Scorecard audit completed: [https://openssf.org/blog/2025/10/10/openssf-scorecard-audit-is-complete/](https://openssf.org/blog/2025/10/10/openssf-scorecard-audit-is-complete/)
* Work on new checks is ongoing
  * maintainer responses on security bugs ([PR link](https://github.com/ossf/scorecard/pull/4867))
  * releases with vulns at time of release ([PR link](https://github.com/ossf/scorecard/pull/4876))
  * mean time to update ([PR link](https://github.com/ossf/scorecard/pull/4868))
  * Java memory safety ([PR link](https://github.com/ossf/scorecard/pull/4849))
* Multi-repo support added

#### **Up Next**

* Continue working on roadmap \+ funding situation

### **Web Developer Security Guide**

#### **Purpose**

* Develop security best practice and guidelines specifically aimed at web developers.

#### **Status Update**

* Collecting feedback about web security features through a [survey](https://docs.google.com/forms/d/e/1FAIpQLScbKJL2Q8XABAHVystmqGU2lQoE0tAJSL_dwhvwPwBcJ-M4fQ/viewform?pli=1&pli=1). Planning to further spread awareness of the survey in front of more web developers.
* Adding content about passkeys
* Breakout session at W3C TPAC meeting in Kobe to promote the work
* The SAWG group participated in reviewing [MDN article on supply chain attacks](https://developer.mozilla.org/en-US/docs/Web/Security/Attacks/Supply_chain_attacks)

#### **Up Next**

* Analyzing the results of the survey, publishing them and applying this to further work.
* Publish a link to the guide on [https://best.openssf.org/](https://best.openssf.org/)

## Funding requests

Are you considering applying for any [funding requests](https://github.com/ossf/tac/blob/main/process/TI%20Funding%20Request%20Process.md)?

* No concrete proposal in the pipeline right now. Once potential funding request covers support of a technical writer for the Python Secure Coding Guide.

## Questions/Issues for the TAC

* none

## **Previous Updates**

* [Q4 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q4-BEST-WG.md)
* [Q3 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q3-BEST-WG.md)
* [Q2 2025](https://github.com/ossf/tac/blob/main/TI-reports/2025/2025-Q2-BEST-WG.md)
* [Q4 2024 (== Q1 2025\)](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q4-BEST-WG.md)
* [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)
* [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)
* [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)
* [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)
