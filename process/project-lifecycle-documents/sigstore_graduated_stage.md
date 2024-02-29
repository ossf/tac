## Project graduation application for Sigstore

It is the shared view of the Sigstore Technical Steering Committee that
Sigstore meets the requirements of a **Graduated** project within the OpenSSF

Below are the details of the project's readiness for graduation.

### List of project maintainers

Sigstore has maintainers across many different companies and academic institutions (Examples include Purdue, NYU, Google, Chainguard, GitHub, RedHat, Stacklok, VMware, IBM, Trail of Bits, Yahoo)

- We maintain a diversified contributor base with an active flow of contributions

  - [58 repositories](https://github.com/orgs/sigstore/repositories?q=\&type=all\&language=\&sort=stargazers) spanning polyglot client SDKs, servers (transparency logs, certificate authorities, policy controllers), supporting automation (e.g. Helm charts and Terraform templates)

  - Examples of contributor/maintainer diversity:

    - Cosign: [Contributor data](https://github.com/sigstore/cosign/graphs/contributors)

      - Maintainers from: Chainguard, Google, Trendyol 

    - Sigstore-python: [Contributor data](https://github.com/sigstore/sigstore-python/graphs/contributors) 

      - Maintainers from: Google, Trail of Bits, Stacklok

    - Sigstore-rs: [Contributor data](https://github.com/sigstore/sigstore-rs/graphs/contributors)

      - Maintainers from: Alibaba, Google, Red Hat, Stacklok, SUSE

    - Sigstore-go: [Contributor data](https://github.com/sigstore/sigstore-go/graphs/contributors)

        - Maintainers from: GitHub, Google Stacklok 

- We have two formalized sub-groups:

    - [SIG-Clients](https://github.com/sigstore/sig-clients)

    - [SIG-Public-Good-Operations](https://github.com/sigstore/sig-public-good-operations)


### Mission of the project

Sigstore represents a novel approach to digital signing, removing the need for signing key management and providing an auditable record of signatures. Sigstore provides a trust foundation for other OpenSSF projects (SLSA, Scorecard, OpenVex).

### Project adoption

Sigstore has become the de-facto approach to code signing for open source projects. 
As seen on [Sigstore's Landscape](https://landscape.openssf.org/sigstore), major 
adopters include Kubernetes, Helm, Python and Kyverno. In 2024 and beyond,
package repositories are the focus for adoption, to improve supply chain
security for package ecosystems. 

NPM leverages Sigstore to sign SLSA provenance statements, a feature which went
into general availability last year. 

Homebrew, PyPI and Maven Central Sigstore integration is actively underway for each ecosystem.

### Release cadence

Clients and services receive regular updates and release frequently (approximately
a monthly cadence, or as needed for bug fixes)

### Governance

]Project governance is documented](https://github.com/sigstore/community/blob/main/MEMBERSHIP.md)
and seen through updates to the community repository to update maintainers.

Technical Steering Committee (TSC) Meeting minutes are available at [Sigstore TSC Agenda and Minutes](https://docs.google.com/document/d/1rN_tn2Jf1hd_e6XDLlKg0vmQog3LIxEHfulG50WzgKQ/)

- An [up-to-date charter](https://github.com/sigstore/TSC/blob/main/docs/CHARTER.MD) is located under the [sigstore/tsc repo](https://github.com/sigstore/tsc)

We provided updates to OpenSSF TAC on _8/9/22, 10/4/22, 8/8/23, 11/14/23_

  - [OpenSSF TAC Meeting Notes (2022-04-05..2023-12-12)](https://docs.google.com/document/d/1706vJpuyq4NpHpVYsOTeU90j5RpoJREX7MRlhAo-CW4/edit#heading=h.d8z1b876r79s)

### Security audit

OSTIF completed [a security audit](https://openssf.org/blog/2022/07/18/results-of-sigstore-and-slf4j-security-audits/) for Sigstore, with all findings addressed.

### Project References

| Reference          | URL |
|--------------------|-----|
| Repo               |  https://github.com/sigstore  |
| Website            |  https://sigstore.dev   |
| Contributing guide |  https://github.com/sigstore/.github/blob/main/CONTRIBUTING.md   |
| Roadmap            | https://github.com/sigstore/community/blob/main/ROADMAP.md   |
| Mailing List       |  https://groups.google.com/g/sigstore-dev   |
| YouTube            |  https://www.youtube.com/channel/UCWPVc8glVGOODxsA_ep0VVw  |
| Slack              |  https://sigstore.slack.com/   |
| X                  |  @projectsigtore   |
| LinkedIn           | https://www.linkedin.com/company/71558774/  |

#### Other

- We follow security best practices (Scorecard, AllStar, Dependabot & CodeQL support, build pipelines automated through CI/CD, branch protection). For the services we operate, infrastructure is hardened, access for oncall engineers is on-demand with review, and we use the latest cloud technologies to manage infrastructure (GKE, Helm, Terraform)

  - Writeup available here: [Sigstore Best Practices Badge Application](best_practices_badge.md)

- We maintain a point of contact for vulnerability reports as documented in [security.MD](https://github.com/sigstore/.github/blob/main/SECURITY.md) and follow coordinated vulnerability disclosure practices.

- We implement and practice mature development & release processes. We leverage automated CI/CD for testing and releases, with releases built on Google Cloud Build and GitHub Actions. Releases are signed with Sigstore. We adhere to semantic versioning for the clients and services, and have a declared policy documenting this. Clients must meet a minimum bar for a GA/1.0 release ([example with Rust](https://github.com/sigstore/sigstore-rs/issues/274)).

- We receive guidance from the OpenSSF TAC while providing updates to the TAC.

- Sigstore is represented in OpenSSF conferences through the supply chain security track.

- Each Sigstore repository includes a [code of conduct](https://github.com/sigstore/sigstore/blob/main/CODE_OF_CONDUCT.md).

- Follows [vulnerability disclosure practices](https://github.com/sigstore/.github/blob/main/SECURITY.md) as documented in the Vulnerability Disclosure WG.

- Our GitHub-organization-wide [security.MD](https://github.com/sigstore/.github/blob/main/SECURITY.md) file covers our disclosure reporting process

  - 4-member security response team responsible for triaging reported issues

- Project updates are regularly posted to [blog.sigstore.dev](https://blog.sigstore.dev/) and to the OpenSSF blog. The Linux Foundation offers a [training course](https://training.linuxfoundation.org/training/securing-your-software-supply-chain-with-sigstore-lfs182x/) for Sigstore.
