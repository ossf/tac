## Application for creating a new project at Sandbox stage

### List of project maintainers

The project must have a minimum of three maintainers with a minimum of two different organizational affiliations.

* Eddie Knight, Revanite, [@eddie-knight](https://github.com/eddie-knight)
* Jason Meridth, Revanite, [@jmeridth](https://github.com/jmeridth)
* Vinaya Damle, Microsoft, [@vinayada1](https://github.com/vinayada1)

### Sponsor

Most projects will report to an existing OpenSSF Working Group, although in some cases a project may report directly to the TAC. The project commits to providing quarterly updates on progress to the group they report to.

* ORBIT Working Group

### Mission of the project

The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be initial code needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.

Privateer is a plugin-based framework for security and compliance validation of deployed systems. Its CLI, `pvtr`, actively interacts with software resources to verify that systems behave as expected, testing from both normal user and attacker perspectives to identify security vulnerabilities and misconfigurations that static analysis might miss.

Privateer orchestrates plugin-based tests and provides consistent, machine-readable output according to the [Gemara](https://gemara.openssf.org) specification. This structure allows any number of resources to be subject to any number of assessment requirements, enabling community-driven and organization-specific compliance validation at scale.

The project provides a novel approach to accelerate the development of security and compliance evaluators. It provides a neutral, extensible validation framework that can execute security and compliance checks against deployed software or configurations using community-maintained plugin catalogs. Existing users include the FINOS Common Cloud Controls project, the OpenSSF ORBIT initiative (via the [GitHub repo scanner plugin](https://github.com/ossf/pvtr-github-repo-scanner)), and LFX Insights for scanning CNCF projects against the OpenSSF Baseline.

### Alignment with the OpenSSF MVSSR

The mission of the Project must be aligned with the [Mission, Vision, Values, Strategy, and Roadmap (MVVSR)](https://openssf.org/about/) of the OpenSSF. Please indicate to which of the three strategies and four pillars of the OpenSSF the Project contributes to.

**Strategies:**

* *Catalyst for Change* - Privateer provides a concrete, actionable tool for organizations to validate their security posture against published control catalogs (such as the OpenSSF Baseline and FINOS Common Cloud Controls). By making compliance validation automated and accessible, it lowers the barrier for projects to adopt security best practices.

* *Ecosystem Leader* - Privateer's plugin architecture enables the OpenSSF and broader community to define, publish, and execute security validation tools in a consistent format. It serves as the runtime engine behind the OpenSSF ORBIT Working Group's GitHub repository scanner and the Baseline initiative, directly advancing the OpenSSF's leadership in defining and operationalizing software supply chain security standards.

**Pillars:**

* *Programs & Projects* - Privateer is already actively used within OpenSSF programs (ORBIT, Baseline) and Linux Foundation projects (FINOS CCC, LFX Insights). Bringing it under OpenSSF governance formalizes this relationship and ensures continuity.

### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).

Yes - IP and license due diligence will be required. The project is currently licensed under Apache 2.0. The contribution will need to go through LF Legal for IP transfer as outlined in the [contribution plan](https://github.com/privateerproj/privateer/issues/271). Tracking issue: https://github.com/ossf/tac/issues/629

### Project References

The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference | URL |
|-----------|-----|
| Repo | https://github.com/privateerproj/privateer |
| Website | https://privateerproj.com |
| Contributing guide | https://github.com/privateerproj/privateer/blob/main/CONTRIBUTING.md |
| Security.md | https://github.com/privateerproj/.github/blob/main/.github/SECURITY.md |
| SDK | https://github.com/privateerproj/privateer-sdk |
| Plugin Example | https://github.com/privateerproj/plugin-example |
| ORBIT Scanner | https://github.com/ossf/pvtr-github-repo-scanner |
| Gemara Spec | https://gemara.openssf.org |
| Contribution Proposal | https://github.com/privateerproj/privateer/issues/271 |
