# 2025 Q3 AI/ML WG and model signing project

## Overview

We are still working at the interesection of security and AI, working on both
enabling security for AI and using AI for security of OSS. While there are
similar AI related groups in other places, this group is still the central place
where we get updates from interlocking with these other TIs.

For the past quarter we have achieved significant milestones on model signing
and mapping AI/ML workflows to the DevSecOps diagram and we started a new SIG
for applying AI to understand the security economics of OSS projects. We will
continue working on all these initiatives, but we are also looking at
[new long term plan](https://docs.google.com/document/d/1I-GDKV3rL3jPwPK3xO5hKh8feGBouTwTUY3aqj0-0IY/edit?pli=1&tab=t.0)
to make the group even more useful.


## General WG updates

### Purpose

We aim for the WG to be the central place to collect all information regarding
ML and security. At the same time, we are delivering technical products (model
signing) and whitepapers (AIDevSecOps paper). We are also looking at how AI
could be used to understand the economic impact of vulnerabilities and
compromises in OSS repositories.

The goal is that the groups serves as a central place to collate any
recommendation for using AI securely ("security for AI") and using AI to improve
security of other products ("AI for security").

### Current Status

The AI/ML working group now has incubating status.

We have finalized the work on
[mapping AI development lifecycle on the MLSecOps diagram from Ericsson](https://github.com/ossf/ai-ml-security/issues/16).
This resulted in a
[whitepaper draft](https://docs.google.com/document/d/1w0Gcw3rfD0XDEyMMRmPjXcoFX9NNqzjHILEo_92CGXU/edit?tab=t.0#heading=h.rxbdc9zg5x7u)
which is now submitted to the design team to prepare for publication.

The work on the AIDevSecOps has also generated a list of
[AI-related security toolbet personas](https://github.com/ossf/toolbelt/tree/main/personas).

[The AI economics SIG](https://github.com/ossf/ai-ml-security/issues/27) just
started working, looking at tools to generate SBOMs and AI SBOMs, analyzing the
FAIR framework, trying to quantify the risk of OSS compromises. The SIG briefly
touched on past experience from Alpha-Omega work: the main issue identified was
that _there is not enough skilled developer time for deep security work_. In
particular, for dependencies of OSS projects, this results in the need to have a
team of "firefighters"/"fire prevention squad". These cannot be part-time.

Next, the AI economics SIG also looked at the impact of AI slop on vulnerability
management and how this can result in bogus security reports being sent to
maintainers, adding to their stress.

The AI economics SIG and the AI/ML working group at large will continue working
on these issues.

The AI/ML working group has also been involved in the DARPA AIxCC challenge, but
at a minimal level. However, after the finals this year, when all materials will
be made open source, the working group should get even more involved.

Finally, the model signing project has launched the 1.0 release with stable API,
clear documentation and standardized signature format. The project provides both
a CLI that can be used independently and an API to integrate in other libraries.

In fact, we already released a 1.0.1 patch release and are currently working on
a 1.1 release to incorporate more support. Whereas the 1.0 release only supports
Sigstore, certificate and key signing, we are now looking at support for PKCS11
and private Sigstore instances.

We have also extracted the model signature format into a separate specification
under OpenSSF as the "OpenSSF Model Signing" format (OMS). This has two goals:

- it creates a forum where the OMS format can evolve in forwards and backwards
  compatible ways, taking into account the needs of the OSS ML ecosystem but
  also working for industry partners needs. This should allow extensions to
  dataset signing and to ensure tamper-proof model cards, as just two examples.
- it allows extending the model signing tooling to other languages and
  ecosystems, in a way that is not tied to just the main repository.

Signatures generated from the model signing project are already present for
models on NVIDIA's model hub. We are also experimenting with signing models on
Kaggle -- this is 90% done, currently under a feature flag, but demo-able.

Regarding model signing, we also had a presentation from Purdue about generating
model signatures directly on GPU and validating them on GPU at the user's site.

### Up Next

We started with
[an issue to ask the community for ideas to work on in 2025](https://github.com/ossf/ai-ml-security/issues/26),
and now we also have a
[new long term plan](https://docs.google.com/document/d/1I-GDKV3rL3jPwPK3xO5hKh8feGBouTwTUY3aqj0-0IY/edit?pli=1&tab=t.0).
The group will start alignment to this plan, to produce new artifacts for the
rest of the year.

The model signing project will move from sandbox stage to incubating. We will
need to work on the documentation PRs for this, as well as on the documentation
PRs for formalizing the sandbox stage for the AI Economics SIG.

For model signing, we are looking at more integrations and demos. We are talking
with various companies (HuggingFace, Cohere, Dell, RedHat), directly or via
CoSAI. We have given demos at OSS NA, devconf.cz and academic conferences.

The model signing project is also looking at incorporating signatures generated
on GPUs. We are also looking at merging with the work from the [Atlas project](https://sched.co/21A0r)
from Intel.

## Questions/Issues for the TAC

None

## Additional Information

None
