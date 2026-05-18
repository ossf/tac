## Project graduation application

### Project has met all Incubating requirements

The project was transferred to OpenSSF upon its formation and has successfully met all incubating goals. It has established a diverse Technical Steering Committee (TSC), maintained a robust security posture, and achieved widespread adoption within the open source ecosystem.

For more information see:

* [PR 609](https://github.com/ossf/tac/pull/609)

### List of project maintainers

*The project must have maintainers with a minimum of five different contributors from three different organizational affiliations.*

Maintainers include the Technical Steering Committee (TSC) and key contributors with commit rights:

  * David A. Wheeler, The Linux Foundation, @david-a-wheeler (TSC)
  * Christopher "CRob" Robinson, The Linux Foundation, @SecurityCRob (TSC)
  * Tony Hansen, AT&T, @TonyLHansen (TSC)
  * Toine Siebelink, Ericsson, @toine-at-est (TSC)
  * Andrew Fader, Yagni Corporation, @andrewfader
  * Jason Dossett, Institute for Defense Analyses, @jdossett

This list represents 6 contributors from 5 distinct organizational affiliations, exceeding the graduation requirement.

### Mission of the project

*The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be code needed to deliver OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.*

  * The mission of the project is to identify best practices for Free/Libre and Open Source Software (FLOSS) and implement a badging system for those best practices. This encourages projects to apply best practices and helps users determine which FLOSS projects do so, thereby improving the overall security and quality of the open source ecosystem. It serves as a foundational "Catalyst for Change" within the OpenSSF mission.

### Project adoption

*The project must be able to show adoption by multiple parties, which could be production deployments or substantial use by established open source communities, and demonstrate the value of that adoption to either the end users or the open source community.*

  * [Over 10,000 projects participate in the OpenSSF Best Practices Badge](https://www.bestpractices.dev/en/project_stats). These include many high-profile projects such as the Linux kernel, Node.js, Kubernetes, and Curl. It serves as the industry standard for projects to demonstrate their commitment to security best practices. Approximately 20% of projects pursuing the badge reach the "passing" level, establishing it as a meaningful and rigorous benchmark for the open source community.

### Release cadence

*The project must be able to show a consistent release cadence.*

  * The project follows a continuous delivery (CD) model for the live application at [bestpractices.dev](https://www.bestpractices.dev).
  * For this project a release is a commit to the production branch. Commits are made to the protected main, staging, and production branches in that order, and each time the CI/CD verification is run. A commit to the production branch that passes all CI/CD tests automatically triggers deployment to the production site.
  * The product demonstrates a consistent and mature release cadence that shows it is active. This is demonstrated through CircleCI history; there were 14 production releases recorded between mid-February and mid-May 2026 (a 3-month window). This is an average of 4.6 releases per month. This includes updates for dependencies; we generally immediately update dependencies with known vulnerabilities, and occasionally update dependencies so that they are not too obsolete.

### Governance

*Projects must have documented project governance and be able to demonstrate that governance in action.*

  * Governance is documented in [docs/governance.md](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/governance.md) and the [Technical Charter](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/Best-Practices-Badge-Technical-Charter-Final-2024-04-30.pdf). The TSC provides oversight and manages the project asynchronously via email and pull requests.

*Have a defined and documented roadmap and annual goals for the project*

  * The roadmap is maintained in [docs/roadmap.md](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/roadmap.md).

*Project has met at least 4 times over a period of at least 2 months since becoming incubating*

  * The project is an integral part of the OpenSSF Best Practices Working Group (WG) and participates in its regular public meetings. Meeting notes are documented in the [OpenSSF Best Practices WG repository](https://github.com/ossf/wg-best-practices-os-developers).

*Implements, practices, and refines mature software development and release practices, such as adherence to semantic versioning, and having a declared policy for stable releases and backported fixes.*

  * The best practices badge project implements mature software development processes. It has earned the [OpenSSF best practices gold badge](https://www.bestpractices.dev/en/projects/1/gold) and the [OpenSSF baseline-3 badge](https://www.bestpractices.dev/en/projects/1/baseline-3).
  * The project enforces strict code quality through its automated test suite and linting tools. These practices are detailed in [CONTRIBUTING.md](https://github.com/coreinfrastructure/best-practices-badge/blob/main/CONTRIBUTING.md) and [docs/testing.md](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/testing.md). Its CI/CD pipeline includes many tools to detect problems. The project identifies specific releases using git commit IDs. At one time the project used semantic versioning, but since it's software intended for deployment to a single site that we also maintain, this specific practice was dropped as irrelevant; we now use git commit IDs to unique identify each release. All releases are stable releases (by definition) and there are never backported fixes (as that makes no sense for this context). We *do* perform all database changes through migrations; this prevents data loss when changing database schema structures. SBOMs are automatically generated for releases to the staging and production branches.

*Projects should harden their build systems in accordance with the SLSA Framework*

  * The project utilizes hardened build systems when executing testing through CircleCI and GitHub Actions. These incorporate static and dynamic analysis. Evidence of SLSA-aligned practices during testing can be found in the automated test suite and [security-related documentation (specifically our assurance case)](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/assurance-case.md). Test results are saved for analysis but are not directly used for deployment.
  * For *production* use there is no separate "build" process. When a commit to production branch occurs, the production site is alerted and directly retrieves the source code using git and https. The Ruby source code is then run, and it does not require compilation. Dependencies are brought in as pinned dependencies. There is an asset regeneration process but that is done on program startup (as there is no build process). This unusual approach completely eliminates the possibility of subverted builds being a possible vector of attack.

### Security audit

*When applicable, projects must have completed a security audit through a third party and addressed audit findings and recommendations.*

  * While the project has not undergone a traditional "paid" third-party audit, it has implemented an exceptionally rigorous security evaluation process that exceeds standard requirements:
    * **Comprehensive Assurance Case**: The project maintains a deep, publicly available [Assurance Case](https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/assurance-case.md) that argues why the project is adequately secure.
    * **Automated Security Tooling**: The CI/CD pipeline includes a variety of industry-standard security tools including `rubocop` (linter), `rails-best-practices` (linter), `brakeman` (SAST), GitHub Code Scanning (SAST), `bundle-audit` (SCA), and GitHub dependabot (SCA).
    * **Automated Test Suite**: The automated test suite covers 100% statement coverage (as measured by CodeCov) and includes negative tests for security (that is, tests to specifically verify that what should not be allowed is in fact not allowed).
    * **AI-Powered Security Evaluations**: In 2026 the project underwent specialized security evaluations by AI using both **Claude Code** and **Gemini**. These evaluations involved deep codebase analysis to identify and remediate potential vulnerabilities, providing a "third-party" perspective on the project's security posture.

### Security Baseline

*The project meets all applicable Security Baseline requirements:*

 * [x] [Security Baseline - Once Sandbox](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-sandbox)
 * [x] [Security Baseline - To Become Incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-incubating)
 * [x] [Security Baseline - Once incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-incubating)
 * [x] [Security Baseline - To Become Graduated](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-graduated)

### Project References

*The project must provide a list of existing resources with links to the repository, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.*

| Reference              | URL |
|-----------------------|-----|
| Repo                  | https://github.com/coreinfrastructure/best-practices-badge |
| Website               | https://www.bestpractices.dev |
| Contributing guide    | https://github.com/coreinfrastructure/best-practices-badge/blob/main/CONTRIBUTING.md |
| Security.md           | https://github.com/coreinfrastructure/best-practices-badge/blob/main/SECURITY.md |
| Roadmap               | https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/roadmap.md |
| Demos                 | https://www.bestpractices.dev |
| Best Practices Badge  | https://bestpractices.coreinfrastructure.org/projects/1 |
| Scorecard integration | https://scorecard.dev/viewer/?uri=github.com/coreinfrastructure/best-practices-badge |
| Assurance Case        | https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/assurance-case.md |
| Testing Documentation | https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/testing.md |
| API Documentation     | https://github.com/coreinfrastructure/best-practices-badge/blob/main/docs/api.md |
