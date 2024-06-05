## Project incubation application

### Project has met all Sandbox requirement
  * https://github.com/ossf/tac/pull/137

### List of project maintainers

  * Kairo Araujo, TestifySec, kairoaraujo
  * Radoslav Dimitrov, Stacklok, rdimitrov
  * Martin Vrachev, VMware by Broadcom, mvrachev
  * Lukas Pühringer, NYU, lukpueh
  * Konstantinos Papadopoulos, Channable, KAUTH

### Mission of the project
The Repository Service for TUF's mission is to make it easier for repositories to integrate the features of [The Update Framework (TUF)] without requiring TUF expertise or deep changes to the repository service implementation.

The project provides repository signing functionality with a simple REST API for integration into any repository offering. The system's architecture enables scalability for high-traffic repositories.

The project was born out of experience developing changes for Warehouse (PyPI) to deliver [PEP 458] and, for the initial roadmap, focuses on providing PEP 458-like repository signing functionality. In future, the Repository Service for TUF will develop to support other TUF architecture patterns including [PEP 480]-like developer signing and more.

[The Update Framework (TUF)]: https://theupdateframework.io
[PEP 458]: https://peps.python.org/pep-0458/
[PEP 480]: https://peps.python.org/pep-0480/


### Project adoption
The project has early adoption (beta version) by the following organizations:
  * [PyPI](https://github.com/pypi/warehouse/pulls?q=is%3Apr+PEP458+is%3Aclosed)
  * [RubyGems](https://github.com/rubygems/rubygems.org/pull/4167)

### Governance
We have a monthly meeting on the first Wednesday of the month.
  * The meeting agenda is available [here](https://repository-service-tuf.readthedocs.io/en/stable/devel/contributing.html#meetings)

Governance
  * RSTUF TAC (https://repository-service-tuf.readthedocs.io/en/stable/devel/tac.html)

Contributor Guide
  * https://repository-service-tuf.readthedocs.io/en/stable/devel/contributing.html

Project has attained an OpenSSF Best Practice Badge at "passing" level
  * https://www.bestpractices.dev/en/projects/6587

Project is integrated into the OpenSSF Scorecard
  * https://scorecard.dev/viewer/?uri=github.com/repository-service-tuf/repository-service-tuf-cli
  * https://scorecard.dev/viewer/?uri=github.com/repository-service-tuf/repository-service-tuf-worker
  * https://scorecard.dev/viewer/?uri=github.com/repository-service-tuf/repository-service-tuf-api

### IP policy and licensing due diligence
  * This has been completed as per https://github.com/ossf/tac/issues/136.

### Project References
The project should provide a list of existing resources with links to the repository, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

 Reference              | URL |
|-----------------------|-----|
| Repo                  | github.com/repository-service-tuf     |
| Meeting Agenda        | https://hackmd.io/sSB1pwpDR5Seag0YB-vYMA   |
| OSSF Calendar Entry   | https://zoom-lfx.platform.linuxfoundation.org/meetings/repository-service-tuf    |
| Website               | https://repository-service-tuf.readthedocs.io    |
| Contributing guide    | https://repository-service-tuf.readthedocs.io/en/stable/devel/contributing.html    |
| Roadmap               | https://repository-service-tuf.readthedocs.io/en/stable/devel/roadmap.html   |
| Demos                 | https://repository-service-tuf.readthedocs.io/en/stable/index.html#mentions    |

