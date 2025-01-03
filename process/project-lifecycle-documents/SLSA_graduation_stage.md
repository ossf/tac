## Project graduation application

### Project has met all Incubating requirements
  * Yes, all relevant information is included below.

### List of project maintainers
The project must have maintainers with a minimum of five different contributors from three different organizational affiliations.

  * SLSA has active maintainers across many different organizations including Datadog, GitHub, Google, IBM, Intel, Kusari, New York University, Red Hat.
    See https://github.com/slsa-framework/slsa/blob/main/MAINTAINERS.md

### Sponsor
Most projects will report to an existing OpenSSF Working Group, although in some cases a project may report directly to the TAC. The project commits to providing quarterly updates on progress to the group they report to.
  * [Supply Chain Integrity WG](https://github.com/ossf/wg-supply-chain-integrity/tree/main)

### Mission of the project
The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be code needed to deliver OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.
  * SLSA (pronounced "salsa") is a security framework, a checklist of standards and controls to prevent tampering, improve integrity, and secure packages and infrastructure. It’s how you get from "safe enough" to being as resilient as possible, at any link in the software supply chain.
  * The SLSA specification is useful for both software producers and consumers: producers can follow SLSA’s guidelines to make their software supply chain more secure, and consumers can use SLSA to make decisions about whether to trust a software package.

### Project adoption
The project must be able to show adoption by multiple parties, which could be production deployments or substantial use by established open source communities, and demonstrate the value of that adoption to either the end users or the open source community.
  * Since the release of SLSA 1.0 in April 2023, evidence of its adoption keeps growing. This includes support in build platform offerings from companies like [Google](https://cloud.google.com/build/docs/overview), [IBM](https://cloud.ibm.com/docs/devsecops?topic=devsecops-cd-devsecops-slsa), and [Red Hat](https://developers.redhat.com/products/trusted-software-supply-chain/overview), as well as support for [npm package provenance in GitHub](https://github.blog/security/supply-chain-security/introducing-npm-package-provenance/) and the [build provenance artifact attestation GitHub action](https://docs.github.com/en/actions/security-for-github-actions/using-artifact-attestations/using-artifact-attestations-to-establish-provenance-for-builds), support in [Tekton Chains](https://tekton.dev/docs/chains/slsa-provenance/#how-to-configure-tekton-chains), and integration with [Sigstore](https://www.sigstore.dev) among others.

### Release cadence
The project must be able to show a consistent release cadence.
  * https://github.com/slsa-framework/slsa/tags

### Governance
Projects must have documented project governance and be able to demonstrate that governance in action.
  * https://github.com/slsa-framework/governance

Have a defined and documented roadmap and annual goals for the project
  * https://github.com/slsa-framework/slsa/projects?query=is%3Aopen

Project has met at least 4 times over a period of at least 2 months since becoming incubating
  * The SLSA project has basically been meeting every Monday since 2022! See https://slsa.dev/notes/community

Implements, practices, and refines mature software development and release practices, such as adherence to semantic versioning, and having a declared policy for stable releases and backported fixes.
  * The SLSA project follows the Community Specification Development Process and has a clearly documented policy about version management:
    * https://github.com/slsa-framework/governance/blob/main/5._Governance.md
    * https://github.com/slsa-framework/slsa/blob/main/CONTRIBUTING.md#slsa-versions-management

Projects should harden their build systems in accordance with the SLSA Framework
  * Not Applicable but we do use features such as branch protection, Dependabot, and Mend Renovate bot.

### Security audit
When applicable, projects must have completed a security audit through a third party and addressed audit findings and recommendations.
  * Not Applicable.

### Security Baseline

The project meets all applicable Security Baseline requirements:
 * [ ] [Security Baseline - Once Sandbox](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-sandbox)
 * [ ] [Security Baseline - To Become Incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-incubating)
 * [ ] [Security Baseline - Once incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-incubating)
 * [ ] [Security Baseline - To Become Graduated](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-graduated)

### Project References
The project must provide a list of existing resources with links to the repository, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

 Reference              | URL |
|-----------------------|-----|
| Repo                  |  https://github.com/slsa-framework/slsa   |
| Website               |  https://slsa.dev   |
| Contributing guide    |  https://github.com/slsa-framework/slsa/blob/main/CONTRIBUTING.md   |
| Security.md           |     |
| Roadmap               |     |
| Demos                 |     |
| Best Practices Badge  |     |
| Scorecard integration |     |
| Other                 |     |
