# 2024 Q3 BEST WG

## Overview

The BEST Working group is officially a [Graduated-level](https://github.com/ossf/tac/blob/main/process/working-group-lifecycle.md) working group within the OpenSSF <img align="right" src="https://github.com/ossf/tac/blob/main/files/images/OpenSSF_StagesBadges_graduated.png" width="100" height="100">
Our Mission is to provide open source developers with security best practices recommendations and easy ways to learn and apply them.

We seek to fortify the open-source ecosystem by championing and embedding best security practices, thereby creating a digital environment where both developers and users can trust and rely on open-source solutions without hesitation.

The BEST Working Group continues to curate and create artifacts tailored towards (open source) developers and open source software consumers illustrating secure development best practices.  This is done through the combination of training collateral, best practices guides, and educational awareness.

- We envision a world where software developers can easily IDENTIFY good practices, requirements and tools that help them create and maintain secure world-class software, helping foster a community where security knowledge is shared and amplified.
- We seek to provide means to LEARN techniques of writing and identifying secure software using methods best suited to learners of all types.
- We desire to provide tools to help developers ADOPT these good practices seamlessly into their daily work.

<img align="top" src="https://github.com/ossf/wg-best-practices-os-developers/blob/main/img/OpenSSF%20Dev%20Best%20Practices%20Projects%20Relations.png">

The group continues to be active and is working on several simultaneous projects aligned with our Mission & Vision.  Attendance generally is down, and several former key contributors no longer attend meetings.


### Key Resources

- Best Practices for OSS For Software Developers [link](https://best.openssf.org/developers)
- Best Practices Guides [link](https://openssf.org/resources/guides/)
- Secure Software Development Fundamentals Course [LFD121](https://training.linuxfoundation.org/training/developing-secure-software-lfd121/)
- Security Toolbelt - ARCHIVED - [link](https://github.com/ossf/toolbelt)


### Sub-groups

- Guides - [link](https://github.com/ossf/wg-best-practices-os-developers/tree/main/docs)
- EDU.SIG - [link](https://github.com/ossf/education/)
- Memory Safety SIG - [link](https://github.com/ossf/Memory-Safety)
- OpenSSF Best Practices Badge - [link](https://www.bestpractices.dev/)
- OpenSSF Scorecard - [link](https://github.com/ossf/scorecard)
- Best Practices Badge and Developing Secure Software (LFD121) course - [link](https://github.com/ossf/secure-sw-dev-fundamentals)
- Security Baseline - [link](https://github.com/ossf/security-baseline)
- Web (with SWAG) - [link](https://github.com/w3c-cg/swag/)

### Leads

- WG - Avishay Balter & Georg Kunz  
- OpenSSF Best Practices Badge and Developing Secure Software (LFD121) course - David A. Wheeler
- Compiler Hardening Guides - Thomas Nyman & Georg Kunz
- EDU SIG - CRob & Dave Russo
- Memory Safety SIG - Nell Shamrell-Harrignton & Avishay Balter
- Python Hardening Guide - Helge Wehder & Georg Kunz
- OpenSSF Scorecard - Stephen Augustus, Raghav Kaul, Jeff Mendoza, Spencer Schrock
- Security Baseline - Eddie Knight
- WebDev Sec BP - Daniel Appelquist


## Activity

### Best Practices Badge

#### Purpose

- The Open Source Security Foundation (OpenSSF) Best Practices badge is a way for Free/Libre and Open Source Software (FLOSS) projects to show that they follow best practices. Projects can voluntarily self-certify, at no cost, by using this web application to explain how they follow each best practice.

#### Current Status

- As of 2024-12-31 there were 7,851 OSS projects pursuing an OpenSSF Best Practices badge, with 1,585 projects achieving at least a passing level badge.
- Many housekeeping updates were done, including updating Rails 7.0 -> 7.1 -> 7.2 -> 8.0, Font Awesome, papertrail. These required code changes, such as how secrets and icons are managed. It also required unexpected changes such as switching past papertrail records from YAML to the jsonb PostgreSQL data format. We added the use of Solid Queue to use a database for jobs, so that when the system is restarted the jobs for cleaning the CDN cache are retained and eventually completed.

- #### Up Next

- Investigate potential use of the best practices badge with baseline. Both have a set of leveled criteria for OSS projects. However, baseline has a different set of requirements, and at the time of writing tends to assume OSS projects have many developers (most OSS projects have 1 developer), so exactly how this will work is to be determined.


### Developing Secure Software Fundamentals Course (LFD121)

#### Purpose

- Provide baseline security education for developers.

#### Current Status

- Our total 2024 enrollments for our "Developing Secure Software" course (LFD121) is 9,361. That was a dramatic increase from 2023 enrollments in LFD121, which was 6,658, and far exceeded our goal of 7,990.
- Added labs for *all* of the "top tier" sections. These labs require no software installation; users just use their browsers. They also provide hints for those who are stuck.
- Made various improvements, e.g., explained what open source software is, added various "story time" real-world examples from CrowdStrike and Meta, 

#### Up Next

- Continue to maintain content.


### EDU.SIG

#### Purpose

- Deliver Baseline Secure Software Development Education and Certification to All.  Provide access to open and widely available education materials to all learners.
Materials will be maximally accessible and easy to consume for all learners.

#### Current Status

- As noted above, LFD121 enrollment in 2024 was 9,361 and we completed all top-tier labs for it.
- Draft course for managers developed, reviewed by LF Education, and their comments have been incorporated.

#### Up Next

- Complete the manager's course and have it posted.


### Concise Guides

#### Purpose

- Artifacts that consolidate BEST practices in OSS software development and management techniques

#### Current Status

- Guides under active development:
  - [C/C++ Compiler Option Hardening](#cc-compiler-option-hardening-guide)
  - [Python Secure Coding Guide](#python-secure-coding-guide)

#### Up Next

- See status updates of respective guides


### C/C++ Compiler Option Hardening Guide

#### Purpose

- Help C and C++ developers and those who compile C/C++ code, e.g., package maintainers, ensure that produced application binaries (libraries and executables) are equipped with security mechanisms provided by compilers against potential attacks and/or misbehavior.

#### Current Status

- Continued revision, updates, & enhancement, e.g., keeping the compiler options hardening guide up-to-date with upstream options additions and changes in GCC and Clang/LLVM and addressing feedback from Linux distribution communities.

#### Up next

- Microsoft MSVC guidance planned for 2025 (tracked in [BEST Issue 150](https://github.com/ossf/wg-best-practices-os-developers/issues/150))
- Plan outreach activities for 2025, possibly talks aimed at C++ conferences.  


### Python Secure Coding Guide

#### Purpose

- Help Python developers to create more secure code by explaining vulnerable and non-vulnerable coding patterns based on the CWE framework and rules.
- Besides a description of each coding pattern, the guide includes executable code examples for each rule, which allow for an in-depth understanding of each pattern.

#### Current Status

- The group is working on adding more content for a broad range of CWE rules. The status is being tracked in issue [531](https://github.com/ossf/wg-best-practices-os-developers/issues/531).
- Dave and Bart gave a lightning talk at SOSS Community Day EU and demoed the ongoing work at the OpenSSF booth at Open Source Summit EU 2024.

#### Up Next

- We want to further grow the community by raising more awareness, for instance by publishing a blog post.
- We are inviting all interested Python coders to review the current content and/or pick a new CWE rule from [531](https://github.com/ossf/wg-best-practices-os-developers/issues/531) and contribute content.





### Memory Safety SIG

#### Purpose

- The Memory Safety SIG is a group working within the OpenSSF's Best Practices Working Group formed to understand and reduce memory safety vulnerabilities in OSS.

#### Current Status

- Defined the SIG's focus and terminology.
- Collaborated with ecosystem SMEs to compile tailored memory safety best practices for both memory-safe-by-default and non-memory-safe-by-default languages.
- Drafted the The Memory Safety Continuum document that aims to guide developers to becoming more memory safe through iterative process.

#### Up Next

- Release the Memory Safety Continuum document
- Focus on interoperability and interfacing between memory safe by default and non-memory safe by default languages in software.





### OpenSSF Scorecard

#### Purpose

- Automate analysis and trust decisions on the security posture of open source projects.
- Use this data to proactively improve the security posture of the critical projects the world depends on.

#### Current Status

- Became an OpenSSF Incubating project
- Community-led contributions for NuGet, Erlang, and Azure DevOps support

#### Up Next

- Make OpenSSF Scorecard (and its GitHub Action) easier to run on groups of repositories
- Build contributor base
- Work towards project graduation
- Request TI funding for security audit
- Refine project release cadence
- Align with forthcoming OpenSSF persona work


### Security Baseline

#### Purpose

- The goal of this SIG is to evolve OpenSSF security baseline for Linux Foundation wide adoption.
- For OpenSSF adoption of the security baseline, there needs to be a home for tracking the adoption, for maintainers to raise issues to refine the security baseline, merge the baseline back to TAC lifecycle, and for OpenSSF to develop the roadmap for the security baseline. It will provide a venue for early adopters to share their reusable code and findings with other maintainers. The pilot adoption builds the foundation for wider adoption of the security baseline in OpenSSF and in Linux Foundation.
- This SIG creates a venue for other participating foundations to help evolve the OpenSSF security baseline into a security baseline that can be applied to a broad range of software-based projects. The group will define the right level of risks that the security baseline is applicable for, the effectiveness measurement of the security baseline, and the adoption path of the security baseline at the minimum.

#### Current Status

- Wrapping up the final review/polish process for the 2025 release

#### Up Next

- A few open PRs on the baseline criteria definitions are currently pending prior to release of the 2025 version
- Integration into automated validation tools has already begun, in preparation for the official release

### Web Developer Security Guide

#### Purpose

- Develop security best practice and guidelines specifically aimed at web developers.

#### Current Status

- We started the W3C SWAG group earlier this year and we've been holding weekly calls. The calls are minuted here: https://github.com/w3c-cg/swag/tree/main/meetings. We've so far produced an early draft security guidelines doc for web developers https://github.com/w3c-cg/swag/blob/main/docs/security_guidelines.md and we have another work item which is a guidelines doc for library developers. I've presented this work to the OpenJS Foundation security coord group as well to socialize it widely.

#### Up Next

- We anticipate starting work on the libraries doc after the new year and as well continue to develop the web developer guide. Both documents will be at the level of detail of the "concise guide" document. We also held a special call where some Google security folks came to talk about tooling they are building around CSP and Trusted Types. Those talks will be posted shortly.
  

### Questions/Issues for the TAC

- none (for the moment)

## Additional Information

- We expect close collaboration between the Best Practices WG and the newly created [Global Cyber Policy WG](https://github.com/ossf/wg-globalcyberpolicy).


## Previous Updates

- [Q3 2024](https://github.com/ossf/tac/blob/main/TI-reports/2024/2024-Q3-BEST-WG.md)
- [April 2024](https://docs.google.com/presentation/d/1XjaJa2yxWgRmXhpv0N1_oPG23JPpJY_9zpSOMvqccUM/)
- [Dec 2023](https://docs.google.com/presentation/d/1A8Sxm1L3_GcWZqaXepqT1Pj-1sULzUG7fRkCP5tTr24/)
- [Sept 2023](https://docs.google.com/presentation/d/1BPSYzk9J33Xl08uekuDBlgJjhiJIMt5B_eBvZ9PetIo/)
