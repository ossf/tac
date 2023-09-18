## Application for creating a new project at Sandbox stage

### List of project maintainers

  * Justin Cappos, NYU, justincappos
  * Ian Dunbar-Hall, Lockheed Martin, idunbarh
  * Cole Kennedy, TestifySec, colek42
  * Marina Moore, NYU, mnm678
  * Trishank Kuppusamy, Datadog, trishankatdatadog

### Mission of the project

SBOMit's goal is to provide SBOMs to end users with minimal effort that provide cryptographic validation of the steps performed in the software 
supply chain.  This differs from other SBOM efforts in that the data in the SBOM is validated cryptographically using [in-toto](in-toto.io) 
link metadata and layouts, which provides a strong threat model while providing a robust set of guarantees about the SBOM's accuracy.  

Specific goals include:

 * Maintain compatibility with existing SBOM formats (could generate existing SBOMs), and ideally operable with SPDX, CycloneDX, and similar efforts
 * Define use cases and outcomes (end user ux) including machine readable
 * Emphasize usability / on-boarding for users.  Acknowledged as critical by many stakeholders.
 * Cryptographic verification that exactly the steps in the verifiable SBOM were performed
 * Threat model of an attacker that can compromise any part of the software supply chain (e.g., Section 2.2 of https://www.usenix.org/system/files/sec19-torres-arias.pdf )
 * Define which pieces of the Verifiable SBOM are cryptographically verifiable
 * Be applicable anywhere (not just cloud native)!
 * Utilize in-toto delivered bundle for distribution of a single file
 * Optionally enabling the capture of reasonable information about the runtime environment of the supply chain steps including pre-build, post-build, and all other portions
 * Optionally enabling the capture of the output of scanning tools, etc. that may make inferences.  Note that these may be based upon incomplete and / or incorrect information, but surfacing this information may be useful.
 * Provide a clear specification that other groups can implement for Verifiable SBOMs
 * Provide exemplars of the tooling needed to generate and process Verifiable SBOMs
 * Enable users of Verifiable SBOMs to be able to understand clearly what steps were performed, possibly via plug-ins through things like Testify, SLSA, FRSCA, etc.
 * Multi-language tooling

Non-Goals:
 * Picking a winning SBOM format (SPDX, CycloneDX, etc.)
 * Recursing into components like the packages inside of a container image when the build process does not otherwise do so.
 * Knowing that an individual action is actually a good security practice  
 * Assertions about the quality of the implementation of the tool / security processes describing how the SBOM or artifact came to exist




### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).

  * See [#191](https://github.com/ossf/tac/issues/191) for LF IP Review
  * Our reference implementations will use the Apache 2.0 license
  * Our specification uses [Community Specification License 1.0](https://github.com/SBOMit/specification/blob/main/LICENSE.md)
  * Our website uses [Creative Commons Attribution 4.0 International](https://github.com/SBOMit/website/blob/main/LICENSE.md)
  
### Project References

| Reference          | URL  |
|--------------------|------|
| Repo               | https://github.com/SBOMit |
| Website            | https://sbomit.dev/       |
| Contributing guide | TODO |
| Roadmap            | TODO |
| Demos              | N/A  |
