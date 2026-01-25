## Project graduation application for SLSA

It is the shared view of the SLSA Steering Committee that SLSA meets the requirements of a **Graduated** project within the OpenSSF.

Below are the details of the project's readiness for graduation.

### Project has met all Incubating requirements

SLSA was adopted by OpenSSF before the current TAC lifecycle process was established. SLSA is currently in incubating status but there is no prior incubating application to cite. This application is to formalize SLSA's graduation based on its maturity and widespread adoption.

### List of project maintainers

SLSA has maintainers across many different companies (Bloomberg, GitHub, Google, IBM, Intel, Kusari, Red Hat).

| Name | Email | OpenSSF Slack | GitHub | Affiliation
| --- | --- | --- | --- | ---
| Aditya Sirish A Yelgundhalli | ayelgundhall@bloomberg.net | @Aditya Sirish A Yelgundhalli | [adityasaky](https://github.com/adityasaky) | Bloomberg
| Andrew McNamara | arewm@redhat.com | @arewm | [arewm](https://github.com/arewm) | Red Hat
| Arnaud Le Hors | lehors@us.ibm.com | @Arnaud Le Hors | [lehors](https://github.com/lehors) | IBM
| Marcela Melara | marcela.melara@intel.com | @Marcela Melara | [marcelamelara](https://github.com/marcelamelara) | Intel
| Mark Lodato | lodato@google.com | @Mark Lodato | [MarkLodato](https://github.com/MarkLodato) | Google
| Michael Lieberman | mlieberman85@gmail.com | @Michael Lieberman | [mlieberman85](https://github.com/mlieberman85) | Kusari
| Pavel Iakovenko | paveliak@github.com | @Pavel Iakovenko | [paveliak](https://github.com/paveliak) | GitHub
| Tom Bedford | tbedford9@bloomberg.net | @Tom Bedford | [tombedfordgit](https://github.com/tombedfordgit) | Bloomberg
| Tom Hennen | tomhennen@google.com | @Tom Hennen | [TomHennen](https://github.com/TomHennen) | Google

The project also has a formal Steering Committee with members from 5 different organizations:
- Adrian Diglio (Microsoft)
- Andrew McNamara (Red Hat)
- Mike Lieberman (Kusari)
- Michael Winser (Eclipse Foundation)
- Tom Hennen (Google)

### Mission of the project

SLSA (Supply chain Levels for Software Artifacts) is a security framework providing a checklist of standards and controls to prevent tampering, improve integrity, and secure packages and infrastructure. The framework serves as:

- A common language to talk about how secure software, supply chains and their component parts really are
- A guide for **producers** implementing secure supply chains
- A tool for **consumers** evaluating package trustworthiness via its supply chain

SLSA directly supports the OpenSSF mission to secure the open source software supply chain by providing a practical, incrementally adoptable framework that the industry has rallied around.

### Project adoption

SLSA has become a de facto industry-standard framework for supply chain security with broad adoption across major platforms, package ecosystems, and projects.

**Major Platform Integrations:**
- **GitHub**: npm package provenance using SLSA attestations
- **Google Cloud Build**: Native SLSA provenance generation support
- **IBM Cloud DevSecOps**: SLSA integration in their secure software supply chain
- **Konflux CI**: Open source cloud native software factory designed to meet or exceed all SLSA Build L3
- **Tekton Chains**: SLSA provenance generation for Kubernetes-native CI/CD
- **Sigstore**: SLSA attestation signing and verification support

**Package Ecosystem Adoption:**
- **Homebrew**: Adopting SLSA for macOS package provenance
- **Python/PyPI**: [PEP 740](https://peps.python.org/pep-0740/) makes SLSA adoption easier for Python packages; PyPI supports and distributes digital attestations including SLSA provenance

**CNCF and Other Projects:**
- ArgoCD
- Flux
- Numerous other projects that either provide SLSA provenance attestations or providing tooling for implementing SLSA

### Release cadence

SLSA follows semantic versioning with a release candidate process for major versions (besides the initial version.):

| Version | Date | Notes |
|---------|------|-------|
| v2021-04-21 | Apr 21, 2021 | Initial release |
| v0.1 | Sep 16, 2021 | Early version |
| v1.0 | Apr 18, 2023 | First stable release |
| v1.1 | Apr 21, 2025 | Added Source Track |
| v1.2 | Nov 24, 2025 | Current version |

- [GitHub Tags](https://github.com/slsa-framework/slsa/tags)

### Governance

[Project governance is documented](https://github.com/slsa-framework/governance) following the Community Specification License 1.0 model from the Joint Development Foundation (JDF).

- [Governance Repository](https://github.com/slsa-framework/governance)
- [MAINTAINERS.md](https://github.com/slsa-framework/slsa/blob/main/MAINTAINERS.md)

The Steering Committee can be reached at:
- GitHub: @slsa-framework/slsa-steering-committee
- Email: slsa-steering-committee@googlegroups.com

**Roadmap and Goals:**

- [Current Activities](https://slsa.dev/current-activities)

**Meeting Cadence:**

The project holds weekly specification meetings since 2022.

- [Meeting Notes](https://slsa.dev/community)
- [#slsa on OpenSSF Slack](https://slack.openssf.org)
- [Mailing List](https://groups.google.com/g/slsa-discussion)

**Software Development Practices:**

As a specification project, SLSA follows mature development practices:
- Semantic versioning for specification releases
- Community Specification Development Process for changes
- Release candidate process (rc1, rc2) before stable releases
- Clear version management policies documented in governance

**SLSA Build System Hardening:**

N/A - SLSA is a specification and does not need build hardening.

### Security audit

N/A - SLSA is a specification project. Traditional security audits apply to software implementations, not specifications. The specification itself undergoes extensive community review and consensus processes through the Community Specification model.

### Security Baseline

SLSA is a **specification project**, not software. Many Security Baseline requirements designed for software projects do not directly apply.

The project implements controls relevant to a specification project while marking software-specific controls as N/A. A detailed mapping of OSPS controls is available:

- [SLSA OSPS Controls Mapping](https://docs.google.com/spreadsheets/d/1_oQfcod-zB4DuKucExmtMmz16eec4USdt0I1e-VJGxM/edit?gid=490880952#gid=490880952)

**Summary:**
- [x] [Security Baseline - Once Sandbox](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-sandbox) (applicable items)
- [x] [Security Baseline - To Become Incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-incubating) (applicable items)
- [x] [Security Baseline - Once Incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-incubating) (applicable items)
- [x] [Security Baseline - To Become Graduated](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-graduated) (applicable items)

*Note: Items like SAST scanning, SBOM generation, signed release artifacts, etc. are N/A for this specification that produces no software artifacts.*

### Project References

| Reference | URL |
|-----------|-----|
| Repo | https://github.com/slsa-framework/slsa |
| Website | https://slsa.dev |
| Contributing guide | https://github.com/slsa-framework/slsa/blob/main/CONTRIBUTING.md |
| Security.md | N/A (specification project - see note below) |
| Roadmap | https://slsa.dev/current-activities |
| Governance | https://github.com/slsa-framework/governance |
| Specification | https://slsa.dev/spec/v1.2 |
| Slack | https://slack.openssf.org (#slsa) |
| Mailing List | https://groups.google.com/g/slsa-discussion |

**Note on Security.md**: As a specification project, SLSA does not produce software that could have security vulnerabilities in the traditional sense. Issues with the specification itself are reported and discussed through the standard GitHub issues process and community channels.