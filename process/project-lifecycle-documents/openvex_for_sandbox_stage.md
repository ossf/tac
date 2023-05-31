## Application for adopting the OpenVEX Project at Sandbox stage

### List of project maintainers
The requirement states that the project must have a minimum of two maintainers with different organizational affiliations.
OpenVEX has 5 maintainers across 4 organizations.
The canonical source for this list can be found here: https://github.com/openvex/go-vex/blob/main/MAINTAINERS.md

We have inlined the current list for convenience:

* Dan Luhring (@luhring), Chainguard
* Adolfo García Veytia (@puerco), Chainguard
* Brandon Lum (@lumjjb), Google
* Alex Goodman (@wagoodman), Anchore
* Rose Judge (@rnjudge), VMWare

#### Contribution Stats

While these are not required for a [Sandbox project](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md#sandbox), we've included them anyway here.

According to GitHub as of 3/22/2023:
* The specification itself has had [7 contributors](https://github.com/openvex/spec/graphs/contributors).
* The Go implementation has had [9 contributors](https://github.com/openvex/go-vex/graphs/contributors).
* The reference implementation cli (`vexctl`) has had [10 contributors](https://github.com/openvex/vexctl/graphs/contributors).

### Alignment to the OSSF Sandbox

The OSSF Sandbox has [four defined goals](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md#sandbox):

> Encourage experimentation and open collaboration that can add value to the OpenSSF mission and build the ingredients of a successful Incubation level Project.
> Facilitate alignment with existing Working Groups or Projects if this is desired (there may be cases where pursuit of different approaches is desirable).
> Nurture Projects.
> Remove possible legal and governance obstacles to adoption and contribution by ensuring all projects adhere to OpenSSF legal, code of conduct, and IP Policy requirements.

We believe OpenVEX is aligned with these goals.

* OpenVEX is a draft specification that seeks to collaborate in the open and add value to the OpenSSF mission (more below).
* OpenVEX is aligned with the Vulnerability Disclosures WG (more below).
* OpenVEX is an early-stage project that still needs some nurturing. This is why we've chosen to apply for Sandbox rather than incubation.
* A large goal of joining the OpenSSF is to reduce legal and governance obstacles that may impede the adoption of OpenVEX, including the use of the Community Specification process for a possible eventual standardization effort.

### Mission of the project

The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be initial code needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.

The full mission and principles of the project can be found here: https://github.com/openvex/spec#openvex-specification

In short:

> OpenVEX is a specification and set of reference tooling to implement the Minimum Requirements for VEX, as defined by CISA.
> OpenVEX is minimal and SBOM-format agnostic.
> The mission of OpenVEX is aligned with the mission of VEX itself, which is to improve transparency in the vulnerability disclosure and management process for the entire industry.
> OpenVEX complements SBOMs by making the data contained in them more actionable.

This is directly aligned with the OpenSSF's mission and [Technical Vision](https://openssf.org/about/), in particular these first three elements:

> * Developers can easily learn secure development practices and are proactively guided by their tools to apply those practices and automatically informed when action is needed to prevent, remediate, or mitigate security issues.
> * Developers, auditors, and regulators can create and easily distribute security policies that are enforced through tooling and automation, providing continuous assurance of the results.
> * Developers and researchers can identify security issues (including unintentional vulnerabilities and malicious software) and have this information swiftly flow backwards through the supply chain to someone who can rapidly address the issue.

* OpenVEX provides tooling to help developers automatically remediate and mitigate security issues.
* OpenVEX allows developers, auditors, and regulators to define more actionable security policies by providing better tooling and automation.
* OpenVEX enables developers and researchers to more easily identify security issues in software by providing a channel to communicate analysis information backwards throughout the supply chain, reducing false-positives and improving data quality.

OpenVEX is also directly aligned with the mission of the [Vulnerability Disclosures WG](https://github.com/ossf/wg-vulnerability-disclosures#objective):

> * Documenting and promoting reasonable vulnerability disclosure and coordination practices within the OSS ecosystem for component maintainers and community members by providing documented standards and educational materials.
> * Identifying vulnerability disclosure pain points for OSS maintainer, consumers, and security researchers and take steps to address them.
> * Facilitate the development and adoption of a standards-based OSS Vulnerability Exchange that uses existing industry formats and allows OSS projects of all sizes to be able to report, share, and learn about vulnerabilities within OSS components.

* OpenVEX aids in automation of vulnerability disclosure practices within OSS projects by documenting standards and formats.
* OpenVEX directly facilitates the development and adoption of a standards-based OSS Vulnerability Exchange that is SBOM agnostic and builds upon existing SBOM formats.

### IP policy and licensing due diligence
When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).
  * "yes / no / not applicable. If yes, provide a link to the corresponding GitHub issue."

OpenVEX is governed by the Community Specification process, required by the OpenSSF.
Full diligence is TODO.
  
### Project References
The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference          | URL |
|--------------------|-----|
| Repo               | https://github.com/openvex |
| Website            | https://openvex.dev |
| Contributing guide | https://github.com/openvex/spec/tree/main/governance |
| Roadmap            | https://github.com/openvex/spec#openvex-roadmap |
| Demos              | https://www.youtube.com/watch?v=MBn1Ph6aBxc |
| Other              |     |