# 2024 Q2 Alpha-Omega

## Overview

The Alpha-Omega Directed Fund continues our mission, to catalyze sustainable security improvements to the world's most critical open source projects and ecosystems. We do this by applying funding and influence in four key areas:

* Staffing dedicated security roles within critical ecosystems/foundations
* Funding work to improve security for artifact repositories / package registries
* Funding security audits and remediation, often as a precusor to additional work
* Experimentation

### Recent Updates

We published our June 2024 report at <https://alpha-omega.dev/resources/reports>.

A few new/renewed engagments:

* **AI Library Reviews**: We've agreed to fund security audits for the top 100 open source AI libraries, the first set of 25 via the Open Source Technology Improvement Fund (OSTIF). Open source AI libraries are of particular interest due to their inherent nature and the speed at which the space is moving. OSTIF will be conducting these reviews through the end of 2024 after which we'll take what we learn and apply it to the next set of open source AI libraries.

* **OpenRefactory**: We've renewed our engagement with OpenRefactory to continue scanning important open source projects for serious security vulnerabilities, including full transitive dependency scans of Apache Airflow, Kubernetes, and Jenkins, as well as an initial scan of the top 300 Rust crates.

* **Apache Airflow**: We've agreed to fund work in 2024 on a security audit of Apache Airflow and a "light" audit it's entire (700+) dependencies. We expect to learn a lot for this experience and will use it to inform our strategy moving forward.

* **Rust for Linux**: We've agreed to renew funding (through Prossimo / ISRG) to support advancing Rust in the Linux Kernel.

In addition, we receive monthly inbound updates from each of our engagements - we urge TAC to read through some of the recent updates in [our repository](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024) to learn more about the depth and breadth of the work that's going on:

* [Eclipse Foundation](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/Eclipse%20Foundation)
* [FreeBSD](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/FreeBSD)
* [Homebrew](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/Homebrew)
* [jQuery](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/jQuery)
* [Node.js](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/NodeJS)
* [OpenRefactory](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/OpenRefactory)
* [OpenSSL](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/OpenSSL)
* [Prossimo](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/Prossimo)
* [Python Software Foundation](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/Python%20Software%20Foundation)
* [Ruby Central](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/RubyCentral)
* [Rust Foundation](https://github.com/ossf/alpha-omega/tree/main/alpha/engagements/2024/Rust%20Foundation)

Below is a very small sampling of recent updates from our existing engagements:

* **Homebrew**: Homebrew now supports build provenance for practically all bottles and opt-in client-side validation. Read more on the [Trail of Bits blog](https://blog.trailofbits.com/2024/05/14/a-peek-into-build-provenance-for-homebrew/).
* **Eclipse Kuksa**: This project provides shared building blocks for Software Defined Vehicles, and the audit covered the data broker and the Python client, conducted by
  Quarkslab and managed by the Open Source Technology Improvement Fund. There were two high severity findings and about a dozen lower severity findings, all
  addressed in the latest version. [Download the full report](https://ostif.org/wp-content/uploads/2024/05/Kuksaaudit1.2.pdf).
* **OpenSSL**: This security audit focused on the libcrypto component of OpenSSL 3.1, and was conducted by Trail of Bits and managed by the Open Source Technology
  Improvement Fund. There were four medium and six low severity findings. [Download the full report](https://github.com/trailofbits/publications/blob/master/reviews/2023-09-openssl-securityreview.pdf).

## Objectives & Key Results

|Key Result|Status|
|-|-|
|**O1: Catalyze trustworthy and secure software, runtimes, and infrastructure for all the major open source ecosystems through staffing**||
|KR 1.1: Fund security improvements and initiatives for at least ten critical open source organizations by the end of 2024. |On target|
|KR 1.2: For each engagement, confirm progress toward improved security outcomes, evidenced through initial and/or follow-on assessments, monthly reporting, and periodic check-ins.|On target|
|KR 1.3: Drive the organizations we work with to obtain security funding from at least one organization other than Alpha-Omega, targeting 33% by the end of 2024.|On target|
|KR 1.4: Organize quarterly roundtables for at least 5 major ecosystems  to share information, build connections, and collaborate, resulting in at least one new project or joint publication started in 2024.|On target|
|**O2: The top 10,000 open source projects are free of critical security vulnerabilities**||
|KR 2.1: Drive adoption of key security processes, including static analysis, credential scanning, the use of private vulnerability disclosures, structured metadata (Security Insights) and the use of multi-factor authentication by maintainers of 500 critical projects from the top 10,000 by the end of 2024.|Planning|
|KR 2.2: Independently scan, triage, and notify maintainers when critical vulnerabilities are found in 2,000 projects, chosen from the top 10,000 by the end of June 2024, with emphasis on clearing a "section of the beach" by focusing on the top PyPI packages.|On target|
|KR 2.3: Publish in a machine readable format the attestations for all packages from 2.2 that returned no vulnerabilities and those that found vulnerabilities which were subsequently fixed and verified.|On target|
|**O3: Enhance Alpha-Omega's effectiveness in driving security improvements through deliberate innovation and experimentation**||
|KR 3.1: By the end of 2024, run three experiments to explore new strategies for reducing security risk within the open source ecosystems, share the results/learnings, using them to refine our overall strategy and objectives for 2025.|Not started|
|**O4: Run an operationally efficient and effective program**||
|KR 4.1: Allocate at least 85% of our yearly spend to activities directly in support of our mission.|On Target|
|KR 4.2: Receive at least $5 million in renewed funding in 2024.|Completed|
|KR 4.3: For each partner engagement, at least 70% of the objectives defined within the respective agreement are met within the defined time period.|On target|

### Purpose

To catalyze sustainable security improvements to the world's most critical open source projects and ecosystems.

### Current Status

We're active and healthy. Our team consists of Michael Scovetta (Microsoft), Henri Yandell (Amazon Web Services), Bob Callaway (Google), supported by Michael Winser (contractor) and Michelle Martineau and Tracy Li from the Linux Foundation. We've received $5M in funding so far in 2024 and are actively meeting with new potential engagement partners. We've spent $4M so far in 2024 and plan to spend more. We meet at least weekly as a team and most weeks, meet with our partners (existing and potential) regularly.

### Up Next

Some key opportunities to engage:

* Our next monthly report is due out around July 5th.
* Our next roundtable (for grant recipients and selected guests) will be held on July 25th.
* Our next public meeting will be held on August 7th.
* We'll have a roundtable at Open Source Summit EU in September and are planning to attend the LF Member Summit.

### Questions/Issues for the TAC

No, but as always, we're eager for substantive discussion with TAC and others.

## Additional Information

We provide [monthly public reports](https://alpha-omega.dev/resources/reports), including to TAC and the OpenSSF Governing Board:
  * [June 2024](https://alpha-omega.dev/wp-content/uploads/sites/22/2024/07/June-Monthly-2024-Report.pdf)
  * [May 2024](https://alpha-omega.dev/wp-content/uploads/sites/22/2024/06/May-Monthly-2024-Report.pdf)
  * [March/April 2024](https://alpha-omega.dev/wp-content/uploads/sites/22/2024/05/AO-March-April-Monthly-2024-Report.pdf)
  * [February 2024](https://alpha-omega.dev/wp-content/uploads/sites/22/2024/03/AO-February-Monthly-2024-Report.pdf)
  * [January 2024](https://alpha-omega.dev/wp-content/uploads/sites/22/2024/02/AO-January-Monthly-2024-Report.pdf)
  * [2023 Annual Report](https://alpha-omega.dev/wp-content/uploads/sites/22/2024/02/Alpha-Omega-Annual-Report-2023.pdf)

You can always reach us at [#alpha_omega](https://openssf.slack.com/archives/C02LUUWQZNK) or by e-mail directly.
