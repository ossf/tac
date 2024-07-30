## Application for creating a new project at Sandbox stage

### List of project maintainers

The project must have a minimum of three maintainers with a minimum of two different organizational affiliations.

* "Jonathan Howard", "Lockheed Martin", @jhoward-lm
* "Eddie Zaneski", "Defense Unicorns", @eddiezane
* "Allen Shearin", "Lockheed Martin", @ashearin
* "Ian Dunbar-Hall", "Lockheed Martin", @idunbarh

### Sponsor

Most projects will report to an existing OpenSSF Working Group, although in some cases a project may report directly to the TAC. The project commits to providing quarterly updates on progress to the group they report to.

* Security Tooling WG - This project was initial developed as an experiment under the Security Tooling WG.

### Mission of the project

The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be initial code needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.

* "__bomctl__ is format-agnostic Software Bill of Materials (SBOM) tooling, which is intended to bridge the gap between SBOM generation and SBOM analysis tools. It focuses on supporting more complex SBOM operations by being opinionated on only supporting the NTIA minimum fields or other fields supported by protobom."
* "__bomctl__ started as an action from Secure Open Source Summit 2023 in DC. The action item was to merge existing sbom tooling into a single source for sbom format agnostic tooling to manage relationships between SBOM files. No existing tooling beyond the [protobom](https://github.com/protobom/protobom) work existed that was format agnostic. This lead to __bomctl__ being developed by the Security Tooling WG."
* "__bomctl__ heavily builds on [protobom](https://github.com/protobom/protobom)."
  * "[Protobom](https://github.com/protobom/protobom) is a go library for manipulating SBOM data in an agnostic manner"
  * "__Bomctl__ is a CLI that handles movement, operations, and caching of SBOM files and will allow linkages between SBOM files"

### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).

* "TBD"
  
### Project References

The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference           | URL |
|---------------------|-----|
| Repo                | https://github.com/bomctl/bomctl |
| Website             | https://github.com/bomctl/bomctl |
| Contributing guide  | https://github.com/bomctl/bomctl/blob/main/CONTRIBUTING.md |
| Security.md         | https://github.com/bomctl/bomctl/blob/main/SECURITY.md |
| Scorecard Report    | https://securityscorecards.dev/viewer/?uri=github.com/bomctl/bomctl |
