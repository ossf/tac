## Application for creating a new project at Sandbox stage

### List of project maintainers

The project has 9 maintainers from 6 different organizations:

*  Ori Avraham, Manifest, @manifestori
*  Daniel Bardenstein, Manifest, @bardenstein 
*  Adolfo García Veytia, Chainguard, @puerco
*  Xunchao Hu, Deepbits, @smarabbit
*  Frederick Kautz, TestifySec, @fkautz
*  John Speed Meyers, Chainguard, @jspeed-meyers
*  Danny Nebenzahl, Scribe, @dn-scribe
*  Jonathan Ness, Veramine, @veramine
*  Mikhail Swift, TestifySec, @mikhailswift

### Mission of the project

The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be initial code needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.

> The protobom project strives to become a foundational library and associated
> command line tools to create, read, modify, and write Software Bill of
> Materials (SBOM) data. The project values the richness and innovation of the
> leading SBOM formats and aims to build a common set of abstractions on top of
> them to enable projects to easily add SBOM capabilities without worrying
> about the details of parsing or rendering.

#### Specific Goals Include:

* Building an I/O layer for Software Bill of Materials data with support for the
major SBOM formats (CycloneDX/SPDX) in their most common versions and encodings.
* Lossless ingestion of SBOM information.
* Ensuring a predictable and documented degradation path in case of fidelity loss
when writing SBOMs.
* Exposing data querying and manipulation primitives to let users access the
SBOM data efficiently.

#### Non-Goals Include:

* Handling other capabilities of the formats outside of the "bill of materials"
use case. This means that features like vulnerabilities, provenance, VEX, etc
are out of the scope of the protobom project.
* Defining a new SBOM format.

### OpenSSF Mission Alignment

We believe our mission aligns with the OpenSSF mission in the following ways:

> make it easier to sustainably secure the development, maintenance, and
> consumption of the open source software

The protobom project aims to cancel the complexity of reading and writing SBOM
data. It also makes it easier to secure the consumption of open source software
by providing prebuilt abstractions that make it easier to create applications
that verify it.

> fostering collaboration

The library was developed by a cohort of independent companies working together
to solve common SBOM problems under the auspices of the 
[Department of Homeland Security Science and Technology Directorate](https://www.dhs.gov/science-and-technology).

> establishing best practices

Protobom is strongly tested and ensures SBOM data consistency across formats.
Uniform data makes it simpler to establish a quality baseline and check
requirements independently of their origin.

### Security Tooling WG Alignment

The project maintainers believe the project aligns with the Security Tooling WG's
objective to Improve and Develop tools:

> Improve - Some tools need just a little bit of help to offer the best solution.
> We need to, where possible, contribute to improve those tools.
> 
> Develop - Despite the large number of tools available, there are still large
> areas of the security problem space that do not have tools to help developers
> find issues. We will develop those tools where there is interest and bandwidth.

As an independent library, protobom reduces the complexity to improve any tool
that reads, writes or manipulates software bills of materials. By offloading 
the document read and write operations to protobom, SBOM tooling can focus on
its core functionality. 

### IP policy and licensing due diligence

When contributing an existing Project to the OpenSSF, the contribution must
undergo license and IP due diligence by the Linux Foundation (LF).

* Yes __(License due diligence TBD)__
  
### Project References

The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference          | URL |
|--------------------|-----|
| Main Repository    | http://github.com/bom-squad/protobom |
| Contributing guide | https://github.com/bom-squad/protobom/blob/main/CONTRIBUTING.md |
| Roadmap            | https://github.com/bom-squad/protobom/milestone/1 |
| Demos              | **Introduction to Protobom** <br>  https://www.youtube.com/watch?v=Q8XkMVORorI <br> **OpenSSF Security Tooling WG Presentation** <br> (waiting for the recording) |
| Other              |  **Blog Posts** <br> [Working with government and industry to put open source security tooling into practice](https://www.chainguard.dev/unchained/working-with-government-and-industry-to-put-open-source-security-tooling-into-practice) <br> [Can Protobom end the SBOM format wars?](https://www.chainguard.dev/unchained/can-protobom-end-the-sbom-format-wars)   |
