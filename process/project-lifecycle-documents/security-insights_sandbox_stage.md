# Security Insights Sandbox Application

While Security Insights has been an OpenSSF project since 2022, a lifecycle document was never logged. This seeks to rectify that oversight.

## Application for creating a new project at Sandbox stage

### List of project maintainers

The project currently has 2 maintainers:

* Eddie Knight, Sonatype, @eddie-knight
* Jason Meridth, GitHub, @jmeridth

### Sponsor

Most projects will report to an existing OpenSSF Working Group, although in some cases a project may report directly to the TAC. The project commits to providing quarterly updates on progress to the group they report to.

* [ORBIT WG](https://github.com/ossf/wg-orbit)

### Mission of the project

The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be initial code needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.

* Security Insights provides a mechanism for projects to report information about their security in a machine-processable way. It is formatted as a YAML file to make it easy to read and edit by humans. The data tracked within this specification is intended to fill the gaps between simplified solutions such as SECURITY.md and comprehensive automated solutions such as SBOMs. In that gap lay elements that must be self-reported by projects to allow end-users to make informed security decisions.

### Alignment with the OpenSSF MVSSR
The mission of the Project must be aligned with the [Mission, Vision, Values, Strategy, and Roadmap (MVVSR)](https://openssf.org/about/) of the OpenSSF. Please indicate to which of the three strategies and four pillars of the OpenSSF the Project contributes to.

Strategies: *i) Catalyst for Change*, *ii) Educate and Empower the Modern Developer*, *iii) Ecosystem Leader*
  * **Catalyst for Change**: Security Insights enables "secure by default" adoption by giving projects a standardized, machine-processable format to self-report their security practices, making it easier for the ecosystem to identify and act on security-relevant data.
  * **Educate and Empower the Modern Developer**: The specification helps developers and maintainers understand what security information matters and provides a structured way to communicate it, bridging the gap between lightweight SECURITY.md files and comprehensive automated solutions like SBOMs.
  * **Ecosystem Leader**: By defining a common YAML-based standard for security reporting across open source projects, Security Insights positions the OpenSSF as a leader in cross-project security interoperability and transparency.

Pillars: *i) Programs & Projects, ii) Education, iii) Public Policy, iv) Community & Events*
  * **Programs & Projects**: Security Insights is an active technical project producing a versioned specification, tooling, and a companion website, providing practical resources for projects to adopt standardized security reporting.
  * **Education**: The specification and its documentation serve as educational resources, helping project maintainers understand what security-relevant information end-users need to make informed decisions.

### IP policy and licensing due diligence
When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).
  * Not applicable.

### Project References

The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference           | URL |
|---------------------|-----|
| Repo                | https://github.com/ossf/security-insights |
| Website             | https://security-insights.openssf.org |
| Contributing guide  | https://github.com/ossf/security-insights?tab=readme-ov-file#contributing |
| Security.md         | https://github.com/ossf/security-insights/blob/main/.github/SECURITY.md |
