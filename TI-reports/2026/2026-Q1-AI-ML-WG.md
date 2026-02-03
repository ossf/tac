# 2026 Q1 AI/ML WG and model signing project

## Overview

We are situated at the intersection of security and AI/ML and we continue in
our mission to support both using AI to improve security of software, and
adding security practices to AI development processes.

There are similar AI related groups, both under Linux Foundation and other
groups, with new ones starting up and old ones ramping down. The other mission
this working group has is to be the central place to get updates from all
other relevant AI related groups.

In the last quarter we:

- created a course on secure development with AI
- launched two new releases of `model-signing`
- ramped up 2 new SIGs for AI/ML supply chain security
- created a SIG for securing the agentic workflow
- created a SIG to adopt the AIxCC competition software, working for a unified
  plaftorm to use AI to secure the OSS ecosystem
- adapted an existing SIG to the realities of using AI for vulnerability
  research and needs of OSS maintainers
- restarted the model signing project meetings

## WG and SIG updates

### Purpose

We work both in the "security for AI" and "AI for security" directions, having
SIGs for both of them.

### Current Status

On the 16th of October 2025 the
["Secure AI/ML-Driven Software development" (LFEL 1012)](https://training.linuxfoundation.org/express-learning/secure-ai-ml-driven-software-development-lfel1012/)
course was launched, developed collaboratively between the Best Practices WG
and the AI/ML WG. The course was launched before PyTorch Conference and we
have talked about it and the AI/ML WG on a Birds of a Feather session at the
conference.

We launched `model-signing` 1.1.0 and 1.1.1. Together, these releases:

- added signing with PKCS #11 as an optional path
- added support for private Sigstore instances
- added support for OIDC authentication with custom OAuth clients
- added support for hashing models with BLAKE3
- as well as a few bug fixes and usability improvements

Over the quarter model signing was adopted by IBM and Cohere, as part of the
work with [Coallition for Secure AI](https://www.coalitionforsecureai.org/) to
publish
[a whitepaper on model signing](https://github.com/cosai-oasis/ws1-supply-chain/blob/main/signing-ml-artifacts.md).
The whitepaper tackles the differences between signing traditional software
artifacts and signing ML artifacts, discusses industry concerns, and
recommends the `model-signing` approach based on Sigstore as the best
alternative.

After publishing the whitepaper, CoSAI members started working on an upgraded
version that introduces maturity levels for adoption of supply chain security
tooling and concepts for ML. This would be an extension of SLSA levels, across
both the source and the build tracks, but also with an eye for future
integrations with AI-BOMs. We are planning to continue the collaboration with
CoSAI in this year.

We restarted the model signing project meetings, on a monthly basis. We have a
[roadmap](https://docs.google.com/document/d/1NkkQh0-60cY8giCtNh2bcZON8tCDQDDAOVz7dztOKT8/edit)
for future development of the project and integration into model hubs and ML
frameworks. We also tarted looking beyond just signing and discussed the
[synergies between model signing and other attestations](https://github.com/sigstore/model-transparency/issues/586),
to [correctly represent model lineage](https://github.com/sigstore/model-transparency/issues/588).
As part of this, we also considered the number of attestations that would be
generated throughout an usual model development cycle. To prevent the issue
where we'd have more metadata files than the model components, we
[proposed](https://github.com/sigstore/model-transparency/issues/587)
migrating the model signature format to an extensible JSONL format.

We started two new SIGs related to model signing. One is focused on
[GPU-based model integrity](https://github.com/ossf/ai-ml-security/issues/41),
as a collaboration between Intel and Purdue. The other one focuses on
[End to end model provenance](https://github.com/ossf/ai-ml-security/issues/40)
and aims to extend Intel's Project Atlas and integrate with the OMS
specification. The project also looks at how SLSA framework can be applied to
ML, which tend to have longer development chains. It looks at how the VSA and
SVR summarization formats can help with identifying how far in the chain a
verifier should go.

Together, these two SIGs and the model signing project should
cover the entire supply chain for training and releasing ML models, in an
efficient and usable manner.

Moving to agentic development, we had a demo on signing agent cards with
Sigstore as a prototype using `sigstore-python` directly. The code
[was donated to Sigstore](https://github.com/sigstore/sigstore-a2a) and it
aims to tackle the risk of maliciously spoofed agent cards in the A2A protocol.

We also had a presentation on [SAFE MCP](https://github.com/fkautz/safe-mcp),
after which we ramped up a new [SIG](https://github.com/ossf/tac/pull/561)
to secure the agentic deployment and usages of MCP tools with participation
from [OpenID Foundation](https://openid.net/), [OWASP](https://owasp.org/),
and the [AGNTCY framework](https://agntcy.org/). One of the ideas of the SIG
is to provide identity to agents talking with each other, in a secure way.

Continuing the topic of agentic security, we also had a short presentation on
a secure version of the A2A protocol, [A2AS](https://www.a2as.org/). The group
proposed a security model for agentic AI runtime security and provided a demo
on how this would be applied in practice.

Finally, we also had a presentation about using
[AI System Cards](https://docs.google.com/presentation/d/1iLJjFzPJV5l3adlR7XnV6Sh_iLiLmOuS44MYdAgX4m8/edit?slide=id.g39d8ccd8806_2_818#slide=id.g39d8ccd8806_2_818)
to add more security to ML runtimes, going beyond just supply chain protection
for models and agents.

On the "AI for security" front, after a presentation on the AIxCC finals, the
group decided unanimously to create a new SIG,
[Cyber Reasoning Systems](https://github.com/ossf/ai-ml-security/issues/32).
The initial purpose of the SIG is to collect the projects from AIxCC and
develop them towards building systems that can automatically find and fix
vulnerabilities, to build a sustainable OSS ecosystem in the AI era, while
also presenting empathy for OSS maintainers and now swamping them in too many
PRs and issues: the focus of these tools is to produce high-quality reports
and fixes that maintainers can trust. As part of this SIG, we have proposed
two sandbox applications for projects to be adopted within OpenSSF:

- [OSS-CRS](https://github.com/ossf/tac/pull/559) -- in progress
- [FuzzingBrain](https://github.com/ossf/tac/pull/555) -- accepted

A few more AIxCC projects are working towards adoption under OpenSSF, towards
integrating into a unified system that can be used by any OSS security
researcher or OSS maintainer. This is also being done in collaboration with
the Academic Connections SIG that got created last year.

For the OSS Economics SIG, we had a presentation on
[CVE Bench](https://arxiv.org/abs/2503.17332), a framework to benchmark
agentic systems on how they discover and fix OSS vulnerabilities. Following
the experiences (both positive and negative) that curl had with
vulnerability reports generated by AI, the OSS Economics SIG is
[switching direction](https://github.com/ossf/ai-ml-security/issues/37) on
benchmarking economic value of AI/ML security agents.

Finally, a theme that has been running across multiple meetings is that we are
not the only group that works on securing AI development. Thus, we started a
[biweekly meeting](https://docs.google.com/document/d/1w8d08HStfi9LKbz2VVWxH-wZ5BOsDSnFpwzwHjwb3sg/edit?tab=t.0)
to collaborate more closely between the OpenSSF AI/ML WG, CoSAI, SPDX AI BOM,
and multiple other similar groups.

### Up Next

The OpenSSF strategy for Q1 2026 is centered around AI/ML, so we plan to build
on the momentum from the last year. We now have 5 different SIGs, working on
the entire spectrum of security for AI but also providing AI for securing
traditional software.

We have a roadmap for model signing that involves integrations with more model
hubs and model frameworks, as well as wider industry adoption. This also
entails work within CoSAI, and is well complemented by the roadmaps for the
GPU integrity and the E2E provenance SIGs.

We will need to consider how SAFE MCP and Sigstore-A2A interact with the newer
[Agentic AI Foundation (AAIF)](https://aaif.io/) which is also an LF project.
We have not yet interacted with the group, but this is an important action
item for 2026.

A similar need to work together across multiple forums arises with respect to
the CoSAI work. The whitepaper on model signing helped with the industry
adoption, and we're planning to use the existing synergies to get more results
in the AI supply chain space.

On the agentic front, the SAFE MCP group
[is rebranding](https://github.com/ossf/ai-ml-security/issues/45) to cover all
the new developments in the agentic space, including A2A, MCP, and all new
AI-centric IDEs that have been released last year.

The Cyber Reasoning Systems SIG is also continuing to adopt all the AIxCC
projects and unifying them into an OSS framework that can be used to
strengthen the security of OSS systems.

A similar theme is covered by the OSS Economics SIG, with their new focus on
benchmarking the economic value of AI/ML security agents and how thee can be
used to build a more secure OSS, with empathy towards maintainers.

Finally, we will be working on a new course on developing software to securely
include AI, extending the current course with techniques that are proven to
work.

### Funding requests

None planned at the time

## Questions/Issues for the TAC

None

## Additional Information

None
