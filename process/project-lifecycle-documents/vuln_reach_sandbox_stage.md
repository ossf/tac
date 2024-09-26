## Application for creating a new project at Sandbox stage

### List of project maintainers
The project must have a minimum of three maintainers with a minimum of two different organizational affiliations.
  * Andrea Venuta, Phylum, @andreaphylum
  * Louis Lang, Phylum, @louislang
  * Craig McLuckie, Stacklock, @craigmcl

### Sponsor
  * wg-security-tooling

### Mission of the project
A large number of vulnerabilities reported by software component analysis (SCA) tooling are false positives. The vulnerable functions are never called, and as a result the reported CVE is not applicable.

The goal of "vuln reach" is to help answer the question "Am I _truly_ impacted by a given CVE?"

This project aims to minimize alert fatigue for vulnerabilities by commoditizing the technology for determining whether or not a code base is making use of known vulnerable functions. We acomplish this by building access graphs from a package and its transitive dependencies, and are then able to determine paths from a user's code to known vulnerable identifiers (i.e., function calls exported by the vulnerable package).

Currently the project exists as a library with support for Javascript. The broad goals of this project are to:

* Simplify determining if CVEs are actually impacting a given codebase
* Implement broad support for other languages and ecosystems (e.g., Python, Ruby, etc.)
* Make vulnerability reachability technology broadly available to the community

### IP policy and licensing due diligence
  * See [387](https://github.com/ossf/tac/issues/387) for LF IP Review

### Project References
| Reference           | URL |
|---------------------|-----|
| Repo                | https://github.com/phylum-dev/vuln-reach?tab=readme-ov-file |
| Website             | TODO |
| Contributing guide  | https://github.com/phylum-dev/vuln-reach?tab=readme-ov-file#contributing |
| Security.md         | TODO |
| Roadmap             | TODO |
| Demos               | Included in `README.md` |
