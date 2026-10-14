# 2025 Q4 through 2026 Q3 OpenBao TAC update

OpenBao's last OpenSSF TAC update was about a year ago:
https://gist.github.com/cipherboy/4bb66fe9967fd103a44ea561baaaa4e9

(This update never seems to have landed [in the TAC repo](https://github.com/ossf/tac/pull/501#pullrequestreview-3019995464)
 though was shared with the Ryan in DMs with [him and Michael Hofer](https://openssf.slack.com/archives/C0963HC7R70/p1753197590786179)).

**TSC Chair**: Michael Hofer

**Dev WG Chair**: Alexander Scheel

## About

[OpenBao](https://openbao.org/) securely manages static and dynamic secrets,
certificates, and keys at scale, allowing greater auditing for compliance with
best practices. This is important because many other solutions don't allow for
centralized risk accounting and inventory.

## Overview

OpenBao's community has continued to grow and iterate on the project's
governance and functionality. We've made three new major release series
(13 total releases), seen adoption exceed 2M combined downloads, and managed
the increased load AI security findings have placed on the community. In the
next couple of releases, we'll likely reach reasonably full parity with Vault
Enterprise and continue innovating in novel directions.

Lack of a formal working group hasn't negatively affected us, as so far we've
mostly routed through OpenSSF staff when relevant discussions needed to occur.

On the whole, things are going very well for the project.

### Challenges

- Marketing and project visibility help is always appreciated.
- AI-assisted CVE deluge has continued, though OpenSSF staff has continued to
  try to enable the project to get access to either Alpha/Omega or newer
  replacement projects to help get ahead of this. The broader community has
  been able to keep up with volume just fine, though.

## Leadership

In the last year, the following project leadership changes have occurred:

 - Alex S. left GitLab in January 2026, causing him to step down his TSC Chair
   position so it continued to be held by an active TSC member. Michael H.
   volunteered and was accepted by the TSC as chair.
 - Alex S. acquired an individual TSC seat and subsequently rolled that into a
   seat for ControlPlane in May 2026, a new entity on the TSC.
 - The last IBM representative (Nathan P.) has fully left the project as of
   June 2026, though IBM stepped down as a TSC member in January 2026.
 - In September 2025, SAP (Klaus K., as member and Jonas K. from Reply as
   alternate) joined the TSC.
 - Four new voting members of the Dev WG (representing Reply and Adfinis) were
   accepted in June 2026 (Huy D., Wojciech S., Pascal R., and Philipp S.).
 - Jonas K. was promoted to org-wide maintainer (representing Reply) in March
   2026.
 - Three new subsystem committers were added, representing Adfinis and
   Securosys (Philipp S., Tomasz M., and Valentin W.)
 - Four new org-wide moderators were invited, representing Adfinis, SAP, and
   Ericsson (Philipp S., Klaus K., Tero S., and Valentin W.).
 - WALLIX (Dan G. and Julian C.) and IOTech Systems (James B. and Brad C.)
   renewed their TSC seat for another 2-year term in July 2026.

Current status of the TSC and Dev WG can be seen on our [`CONTRIBUTING.md`
file](https://github.com/openbao/openbao/blob/main/CONTRIBUTING.md#technical-steering-committee-tsc-members)
and state of our maintainers, committers, and moderators can be seen on our
[`MAINTAINERS.md` file](https://github.com/openbao/openbao/blob/main/MAINTAINERS.md).
The TSC continues to regularly meet and/or handle business asynchronously on
the mailing list or Zulip.

The TSC split our existing roadmap into [Project
Direction](https://docs.google.com/document/d/1oNqm4GXCsIZbcNHsIqft4kgciRcuwS9rrIRGXlMz1yg/edit?tab=t.j9lcyrvl3939#heading=h.9n1zwjabxqai)
and [Development Direction](https://docs.google.com/document/d/1oNqm4GXCsIZbcNHsIqft4kgciRcuwS9rrIRGXlMz1yg/edit?tab=t.j9lcyrvl3939#heading=h.f8brm190ymhh)
documents in March 2026 to set tangible and measurable yearly goals for the
project.

## Releases

OpenBao has made three major release series
([v2.4.x](https://openbao.org/community/release-notes/2-4-0/),
[v2.5.x](https://openbao.org/community/release-notes/2-5-0/), and
[v2.6.x](https://openbao.org/community/release-notes/2-6-0/)) since the last
update.

The direct repository has seen [over 600k
downloads](https://tooomm.github.io/github-release-stats/?username=openbao&repository=openbao),
[over 1M+ DockerHub container pulls](https://hub.docker.com/r/openbao/openbao)
on our main image, and another [500k on
GHCR](https://github.com/openbao/openbao/pkgs/container/openbao). Quay regularly
sees [40k+ daily downloads](https://quay.io/repository/openbao/openbao) but
does not provide total download statistics.

### v2.4.x

**Release date**: August 28, 2025

The v2.4.x series brought key improvements to operability: declarative
self-initialization and audit devices (enabling templated deployment of
new instances); inline authentication (with no storage requirements unlike
regular token authentication); and ACL filtering of LIST and SCAN responses.
These worked towards our [roadmap goals](https://github.com/openbao/openbao/issues/569)
of **Safer** and **Scalability**.

### v2.5.x

**Release date**: February 4, 2026

The v2.5.x series brought key improvements to scalability: horizontal read
scalability on the Raft storage backend and configuration-driven plugin
registration with distribution via OCI images. These worked towards our
[roadmap goals](https://github.com/openbao/openbao/issues/569) of
**Community** and **Scalability**.

### v2.6.x

**Release date**: July 22, 2026

The v2.6.x series brought key improvements to security: per-namespace seals
to allow strong, cryptographic separation of tenants; externally pluginizing
auto-unseal to decouple releases and allow consumption of third-party KMS
devices; and the new workflow engine for native governance and cross-plugin
communication. These worked towards our [roadmap
goals](https://github.com/openbao/openbao/issues/1974) of **Sustainability**
and **Operator Experience**.

Alex S. is working with the OpenSSF to land this release on the blog post.

### Future

v2.7.0 is already underway with PostgreSQL horizontal read scalability and
external HSM/KMS backed key material planned. Namespaces might see auto-unseal
support and other general improvements around multi-node consistency are also
underway.

v2.8.0 will likely see improvements around authorization (allowing tying into
OPA or CEL), post-quantum algorithm adoption now that Go will have support for
ML-DSA, better break-glass recovery, and other foundational stabilizations and
refactors.

Much of the rest of the roadmap will likely shift from 2026 into 2027+.

## Community

The community has continued to see growth the [number of contributors
YoY](https://insights.linuxfoundation.org/project/openbao/contributors?timeRange=past365days&start=2025-07-23&end=2026-07-23)
per LFX Insights:

- 456 contributors, up 85% YoY
- 135 organizations, up 62% YoY
- Three contributors for 57% of all contributions, down from two contributors
  for 53% of all contributions YoY.
- Three organizations for 65% of all contributions, down from two organizations
  for 57% of all contributions YoY.
- Overall contribution volume has also improved.

The community continues to see consistent participation in its regular working
group calls, though the broader community call's attendance has dropped. The
community has published 10 blog posts in the past year, down from 18 the year
before.

OpenBao now has an [ecosystem page](https://openbao.org/ecosystem/), where
we've begun soliciting supporters, integrators, adopters, and vendors to
include their logos and a description of their involvement and a [news
page](https://openbao.org/ecosystem/news/) highlighting OpenBao at
conferences, blogs, and other publications.

OpenBao contributors continue to work with other projects such as
[ESO](https://github.com/external-secrets/external-secrets/issues/6446)
and [FluxCD](https://fluxcd.io/blog/2026/07/flux-openbao-secrets-signatures/).

### Development WG

The Development WG is a top-level working group reporting to the OpenBao TSC,
focused on leading all day-to-day development actions. It directly handles
roadmap planning (subject to approval by the TSC), handles security incidents,
and has spun off a number of project-scoped sub-working groups discussed below:

- **Horizontal Scalability WG**, focused on improving scalability of OpenBao.
  When forked, OpenBao had no horizontal scalability and only had high
  availability based on Vault Community/Enterprise edition's open core
  feature differentiation.
- **Namespaces WG**, focused on bringing strong multi-tenancy to OpenBao.
- **UI WG**, focused on improvements to OpenBao's UI.
- **PKCS#11/KMS WG**, focused on using and integrating with various third-party
  hardware security modules or key management systems, such as in Transit, PKI,
  or for auto-unseal.
- **Supply Chain Security WG**, focused on meeting OpenSSF project
  requirements and improving OpenBao's security posture in our
  dependency tree.

#### Horizontal Scalability WG

The Horizontal Scalability WG saw the release of its flagship feature, Raft
horizontal scalability, and is working towards PostgreSQL horizontal
scalability. Designs for future write scalability are under discussion and
the community sees continued involvement and will continue for the foreseeable
future.

#### Namespaces WG

The Namespaces WG had previously underseen the release of the namespaces
feature and just shipped per-namespace sealing via Shamir's (manual
unseal). Up next will be auto-unseal support for namespace sealing followed
likely by assisting the Horizontal Scalability WG with write scaling based on
namespace sharding.

Designs from GitLab had initially been proposed for a broader extended roadmap
for this working group but unless there's broader community buy-in, the
namespaces WG may fold into the horizontal scalability WG or may find other
avenues to continue. This is expected as namespaces were a broad but
self-contained agenda.

#### UI WG

The UI WG initially was working on a rewrite of the UI in React. This effort
has largely stalled and will not be continued. The UI WG is effectively
discontinued and may be formally disbanded later.

#### PKCS#11/KMS WG

The PKCS#11/KMS WG continues to see broad participation from multiple
entities. Many new KMS libraries have been built especially as support for
external KMS plugins landed in v2.6.x. Support for external keys in v2.7.0 is
this WG's immediate focus but work on KMIP server support is also happening.
This working group will likely continue indefinitely and sponsor most of the
post-quantum adoption work in the future as well.

#### Supply Chain Security WG

The WG has seen varying levels of participation and interest but overall
achieved various improvements such as adopting `security-insights.yml`, the
creation of [dependency-vulnerabilities](https://github.com/openbao/dependency-vulnerabilities)
to scan for and triage vulnerabilities, and renewed activities to push the
adoption of OSPS over the finish line.

### Marketing WG

While the Marketing WG is in motion to become our second dedicated top-level WG,
the community was able to achieve several improvements. It established the
already mentioned [ecosystem page](https://openbao.org/ecosystem/) which grew
already to 20+ members through proactive outreach. In addition, the
[ecosystem news](https://openbao.org/ecosystem/news/) is its newest addition
to spotlight publications from the wider community. For social media, the
community has revived its LinkedIn account with overall good success. The
amount of follower grew to 939 (up 798) with over 40 posts in the past year.
In terms of events and talks, the community was activate at several events
with sponsored booths and various talks to promote the project.
