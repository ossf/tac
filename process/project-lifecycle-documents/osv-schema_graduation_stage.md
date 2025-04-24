## Project graduation application

### Project has met all Incubating requirements
  * n/a

### List of project maintainers
The project must have maintainers with a minimum of five different contributors from three different organizational affiliations.
  * Oliver Chang, Google, @oliverchang
  * Andrew Pollock, Independent, @andrewpollock
  * Madison Oliver, GitHub, @taladrane
  * Jason Shepherd, Red Hat, @jasinner
  * Christopher 'CRob' Robinson, OpenSSF, @SecurityCRob 

OSV Schema has had 62 contributors from 18 different organizations.

### Mission of the project
The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be code needed to deliver OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.
  * The mission of OSV is to develop a standard interchange format for describing vulnerabilities in open source packages.
  * The OSV schema provides a human and machine readable data format to describe vulnerabilities in a way that precisely maps to open source package versions or commit hashes.

### Project adoption
The project must be able to show adoption by multiple parties, which could be production deployments or substantial use by established open source communities, and demonstrate the value of that adoption to either the end users or the open source community.

The OSV Schema is currently exported by:
- [AlmaLinux](https://github.com/AlmaLinux/osv-database)
- [Bitnami Vulnerability Database](https://github.com/bitnami/vulndb)
- [Chainguard](https://packages.cgr.dev/chainguard/osv/all.json)
- [Curl](https://curl.se/docs/vuln.json)
- [GitHub Security Advisories](https://github.com/github/advisory-database)
- [Global Security Database](https://github.com/cloudsecurityalliance/gsd-database)
- [Go Vulnerability Database](https://github.com/golang/vulndb)
- [Haskell Security Advisories](https://github.com/haskell/security-advisories)
- [LoopBack Advisory Database](https://github.com/loopbackio/security/tree/main/advisories)
- [Malicious Packages Repository](https://github.com/ossf/malicious-packages)
- [Mageia Advisories](https://advisories.mageia.org/)
- [OSS-Fuzz](https://github.com/google/oss-fuzz-vulns)
- [OSV.dev maintained converters](https://google.github.io/osv.dev/data/#converted-data) (Debian, Alpine, NVD)
- [PyPI Advisory Database](https://github.com/pypa/advisory-database)
- [Python Software Foundation Database](https://github.com/psf/advisory-database)
- [RConsortium Advisory Database](https://github.com/RConsortium/r-advisory-database)
- [Red Hat](https://security.access.redhat.com/data)
- [Rocky Linux](https://distro-tools.rocky.page/apollo/openapi/#osv)
- [Rust Advisory Database](https://github.com/RustSec/advisory-db)
- [SUSE](https://www.suse.com/support/security/)
- [Ubuntu](https://github.com/canonical/ubuntu-security-notices/)
- [VMWare Photon OS](https://github.com/vmware/photon/wiki/Security-Advisories) (unofficial)

### Release cadence
The project must be able to show a consistent release cadence.
  * https://github.com/ossf/osv-schema/releases

### Governance
Projects must have documented project governance and be able to demonstrate that governance in action.
  * https://github.com/ossf/osv-schema/blob/main/CHARTER.md

Have a defined and documented roadmap and annual goals for the project
  * "link to roadmap and goals"

Project has met at least 4 times over a period of at least 2 months since becoming incubating
  * The project has a standing agenda item in the Vulnerability Disclosures Working Group meetings. [Meeting Notes](https://docs.google.com/document/d/1TdxiFofLOfpHUEQILlKq7qkjSsRXVab0uApSDJ8c5rI/edit?tab=t.0)

Implements, practices, and refines mature software development and release practices, such as adherence to semantic versioning, and having a declared policy for stable releases and backported fixes.
  * "link to policy for (or describe here) software development and release practices"

Projects should harden their build systems in accordance with the SLSA Framework
  * "link to policy for (or describe here) hardened build system"

### Security audit
When applicable, projects must have completed a security audit through a third party and addressed audit findings and recommendations.
  * "link to results of security audit"

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
| Repo                  | https://github.com/ossf/osv-schema |
| Website               | https://ossf.github.io/osv-schema/ |
| Contributing guide    |     |
| Security.md           | https://github.com/ossf/osv-schema?tab=security-ov-file#readme |
| Roadmap               |     |
| Demos                 |     |
| Best Practices Badge  |     |
| Scorecard integration |     |
| Other                 | [Tools (converters)](https://github.com/ossf/osv-schema/tree/main/tools) |
