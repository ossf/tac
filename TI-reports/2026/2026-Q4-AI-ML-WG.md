# 2026 Q4 AI/ML WG, SIGs, and projects

## Overview

We are working at the intersection of security and AI/ML, supporting both
using AI to improve security of software, and adding security practices to AI
development processes. We are currently prioritizing using AI for security,
while till having working groups and projects on the security for AI pillar.

There are similar AI related groups, both under The Linux Foundation and
elsewhere, some of which (e.g., OpenSSF, CoSAI, OWASP) are umbrellas on their
own with multiple working groups and meetings that are relevant. Thus, one
additional mission of this working group is to be the central place to get
updates from all other relevant AI related groups.

For this quarter there are fewer updates, as activity was lower due to summer
holidays, conferences (DEFCON, OSS EU, SCORED) and some meetings being on
break. We still had a few achievements though:

- We helped publish a course on finding and fixing vulnerabilities using AI
- We contributed to the LF certification/exam for AI security best practices
- We created a reusable OSS-CRS GitHub Action and docker container
- There is a new competition aimed at students, which aims to create a
  mini-AIxCC competition developed around OSS-CRS
- We built a skill that would scan MCP servers for vulnerabilities and provide
  documentation and remediation guidance
- We now have a model signing conformance test suite, to pair with the OMS
  spec
- We contributed in editing and publication of CoSAI's ML Supply Chain
  Maturity Levels whitepaper
- Talks from OSS-CRS at OSS EU and OpenSSF Community Day, and a SAF workshop
  at AgntCon + MCPCon North America in San Jose

### The AI/ML working group

Members of the working group are involved in discussions regarding OpenSSF
Priority 2, AI. We want to prioritize building secure AI tools, providing
guidance for secure AI governance and AI tools for maintainers. We will be
focusing more on the AI for security pillar.

Members of the working group are also working on an LF certification/exam for
AI security best practices.

The working group contributed to the
[course on finding and fixing vulnerabilities with AI](https://best.openssf.org/Finding-and-Fixing-Vulnerabilities-Using-AI/),
a collaboration with the Best Practices Working Group. The course might be
paired in the future with a potential training on using OSS-CRS, but the main
material aims to be vendor neutral.

Yuval Kainan and Camit Hershman, both from JFrog, presented an initiative for
a [community protocol](https://github.com/jfrog/agentic-process-evidence) for
SDLC agentic processes provenance. This entails governance for the agent
outputs (behavior, logs, monitoring systems, dependencies), as a gate through
which humans in the loop can control swarm of agents. This is similar to
[nono](https://nono.sh), but is approaching the problem from the logging side,
instead of following a sandboxing and allowlisting approach.

In the future, we will have to handle the anti-AI sentiment that is growing in
the OSS ecosystem and might impact the adoption of the "AI for security" tools
that we are working on.

### The OSS Cyber Reasoning Systems (OSS-CRS) project

The OSS-CRS project continued development and engagements via the partnerships
with MIT Lincoln Labs and other similar organizations. There was a talk about
OSS-CRS at OpenAI, with participation from other participants in the AIxCC
competition.

The OSS-CRS project is looking at a possible collaboration with the Akrites
work, in order to bootstrap existing activities (Akrites, Glasswing, etc.)
into a cohesive system. In the last few months, there have been a plethora of
models released, making it a moving target to determine which one of them is
best for a particular task.

Thanks to Puerco, there is now an OSS-CRS reusable GitHub action
([example run](https://github.com/puerco/ampel/actions/runs/29232598664)).
Work continues here too, and the group published a
[reusable container](https://github.com/ossf/oss-crs-actions/pkgs/container/oss-crs-runner)
that is now available to the public.

Laura proposed documentation for setting up OSS-CRS on Apple Silicon devices.

There is a new [CRC competition](https://csaw.io/competition/cyber-reasoning-challenge)
during a CSAW event. This is similar to a mini AIxCC event and aims to
leverage OSS-CRS and CRS-Bench. It is open for students, with finals scheduled
to occur in November.

OSS-CRS was also included in talks given at OSS EU and OpenSSF Community Day
Europe.

### The Secure Agentic Framework project

There is a new [charter for the framework](https://docs.google.com/document/d/1PuUsxS9Zj9BXKZNZfxMEHpMV-scE-B00EMpmej8VIwE/edit?tab=t.0),
currently under review. The group also relicensed the framework to CSL.

There will be a workshop at AgntCon + MCPCon North America in San Jose. It
aims to create an AI skill and teach participants to use it. The skill scans a
vulnerable reference environment, surfaces what is exploitable and why, and
maps each finding to a concrete mitigation that attendees apply and re-scan to
confirm it clears. This will cover both SAF core implementation (SAF for MCP
and SAF for k8s).

The working group is also looking at defining metrics for model logging, for
building a control plane for AI. There is a potential for alignment with
Compliance Automation Revolution (CAR WG) from Cloud Security Alliance.

Jay proposed a [skill] (https://github.com/camaleon2016/SAFE-MCP-skill/tree/main)
which takes a JSON description a tool, server, or agent architecture, and it
runs an engine that checks 32 different rules looking at potential prompt
injections, credential theft attacks, data exfiltration possibilities, etc.
The user gets a report with risk ratings and cross-references to STRIDE, MITRE
ATLAS, OWASP LLM Top 10, and NIST AI RMF, plus actionable mitigations.

### The model signing project

The [conformance suite PR](https://github.com/ossf/model-signing-spec/pull/12)
merged, opening a way for having both a Python and Go implementation (and many
others, as needed) without compatibility issues. The group is also planning to
write a blog post about this, as well as the new support for
[signing agent skills with OMS](https://docs.google.com/document/d/1Z4LIh3wyBPZYc_0Yfuj7bODO-NdYNkWEAMQUhF5NoBs/edit?tab=t.0).

There is a [proposal](https://docs.google.com/document/d/10LIvnDz_4Tl2E8a5FAWM0xEmFfbtN-OgL8bWRPxJIlQ/edit?usp=sharing)
to sign ML specific OCI artifacts directly. This depends on pending work to
migrate to a `claims.jsonl` signature format which allows multiple signatures
from different identities, and/or supports multiple predicates (e.g., a
signature at the moment of publication to HuggingFace and another signature
after a different actor scanned the model for vulnerabilities).

As part of formalizing the OMS specification, we are also looking at defining
stricter policies for verification of signatures.

We would need to rename the repository to signal the expansion to more ML
artifacts and we are looking into using a separate GitHub organisation to have
all ML supply chain projects in a single place.

### The End-To-End ML Provenance SIG

The End-To-End ML Provenance SIG is looking at integrating with the model
signing project, and donating Atlas to be an OpenSSF project. Since restarting
the meetings in September, this has been the main focus of the SIG.

In order to achieve cohesion between model signing and End-To-End ML
Provenance SIG we are looking at having a single GitHub organisation as the
home for all projects related to ML supply chain security.

The SIG is the technical side in a pair with CoSAI's Supply Chain Workstream.
The group has been helping write the ML Supply Chain Maturity Levels
whitepaper in CoSAI, which has just
[been published](https://github.com/cosai-oasis/ws1-supply-chain/blob/main/whitepapers/aimm-artifact-integrity-maturity-model.md).

There is a collaboration opportunity between the end-to-end ML provenance SIG
and cyberpolicy groups (OpenSSF Global Cyberpolicy and ORBIT), given EU CRA
and other pieces of legislation that cover AI.

## Up Next

We have revived the [biweekly
meeting](https://docs.google.com/document/d/1w8d08HStfi9LKbz2VVWxH-wZ5BOsDSnFpwzwHjwb3sg/edit?tab=t.0)
to collaborate more closely between the OpenSSF AI/ML WG, CoSAI, SPDX AI BOM,
and other similar groups, across a variety of the OSS ecosystems. The meeting
was on-hold during the summer and we are now restarting it to provide
opportunities to align between these working groups and spread the knowledge
of what each one is working on.

## Funding requests

None planned at the time

## Questions/Issues for the TAC

None

## Additional Information

None
