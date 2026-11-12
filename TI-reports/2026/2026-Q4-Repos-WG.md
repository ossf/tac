# 2026 Q4 Securing Software Repositories Working Group

## Overview

While the direct attacks on package repositories from the first half of this year have died down, a number of security incidents involving language ecosystems are continuing to keep us on our toes.

## Securing Software Repositories Working Group 

### Purpose

Improve security of software repositories by providing a forum for discussion, a maturity model for security roadmaps, and guidance for individual security capabilities. These conversations, roadmaps, and guidance help ecosystems learn from each other, which accelerates the deployment of security capabilities.

### Current Status

The security incidents mentioned above include:

- [eMudhra CA mismanagement](https://emudhra.we-have-a-problem.com/): while not directly a problem with package repositories, many [ecosystem CLIs and libraries have embedded trust stores](https://discuss.python.org/t/information-for-python-users-regarding-emudhra-emsign-ca-certificate-security-incident/109576).

- [Node's October security release](https://nodejs.org/en/blog/vulnerability/october-2026-security-releases) contained several high and medium severity issues

- [php2shell](https://www.cisa.gov/news-events/alerts/2026/10/21/critical-vulnerabilities-php-require-immediate-patching) requires upgrading all versions of PHP that are not end-of-life

On a more proactive note, we participated in the [IAB Workshop on Accelerating the Deployment of Post-Quantum Authentication](https://intarchboard.github.io/iab-pq-ws.github.io/) including [npm's plans on package signing with post-quantum cryptography](https://coffeehousecoders.org/blog/iab_pq_workshop.html). We are still working out details of npm's PQC transition, but as we finalize plans we will share with other package repositories.

### Up Next

- Really for real update [Recent Package Repository Security Capabilities](https://docs.google.com/spreadsheets/d/1JydRQSJ2jTHREmWXXlzlFdhKJ_sY7cORKp_6AI6mRNw/edit?usp=sharing).

- In addition to signing build provenance with PQC, package repositories also have to solve the problem of authoritatively assert what packages correspond to a given release name and version string, in a tamper-resistant way. Golang famously solves this with a transparency log, and npm addresses this with a delegate in the Sigstore public good trusted root.

### Funding requests and updates

There are no outstanding funding requests, or planned funding request in the near future.

### Questions/Issues for the TAC

None at this time.

## Additional Information

There are a number of projects that report to the Securing Package Repositories Working Group that are continuing to operate but do not have major updates this quarter, including:

- [Repository Service for TUF](https://github.com/repository-service-tuf/repository-service-tuf)
- [Package Analysis](https://github.com/ossf/package-analysis)
- [Malicious Packages](https://github.com/ossf/malicious-packages)
  - GitHub is now consuming and distributing malicious package information additionally from PyPI, Maven Central, RubyGems, NuGet, Go, crates.io, and PHP Composer, as noted in the [OpenSSF blog post](https://openssf.org/blog/2026/10/16/case-study-github-expands-malware-advisories-across-eight-ecosystems-with-openssf/) 
