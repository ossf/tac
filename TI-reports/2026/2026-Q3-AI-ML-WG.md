# 2026 Q3 AI/ML WG and model signing project

## Overview

We are still working at the intersection of security and AI/ML, continuing the
mission to support both using AI to improve security of software, and
adding security practices to AI development processes. The recent developments
in using AI for cybersecurity means that we have to prioritize using AI for
security, but we still also continue to have working groups and projects
focused on the security for AI pillar.

There are similar AI related groups, both under The Linux
Foundation and elsewhere, some of which (e.g., OpenSSF, CoSAI, OWASP) are
umbrellas on their own with multiple working groups and meetings that are
relevant. Thus, one additional mission of this working group is to be the
central place to get updates from all other relevant AI related groups.

In the last quarter we:

- increased collaboration with different working groups, within OpenSSF and
  outside, adding new collaborations with 2 new working groups and having
  significant discussions with AI-BOM groups.
- significantly progressed the OSS-CRS project, both in technical direction
  and in engagements with open source projects
- extended model signing by creating a separate Go implementation,
  experimenting with signing other AI artifacts, and working on a formalized
  spec
- had a set of presentations related to AI and security, across the multiple
  meetings we had.

### The AI/ML working group

This quarter, the working group was in the post-Mythos, post-Glasswing
releases world. A bigger focus was being put on using AI for security.

Members of the working group are involved in discussions regarding OpenSSF
Priority 2, AI. We want to prioritize building secure AI tools, providing
guidance for secure AI governance and AI tools for maintainers. We will be
focusing more on the AI for security pillar.

We had a rework of the plan for the new AI course. Following the
["Secure AI/ML-Driven Software development" (LFEL 1012)](https://training.linuxfoundation.org/express-learning/secure-ai-ml-driven-software-development-lfel1012/)
course published last year, this year we were planning on working on a course
for securely embedding AI in software systems. With the launches in the AI
world, we are now looking at a course on using AI to find, fix, and triage
vulnerabilities, in collaboration with the Best Practices Working Group and
the OSS-CRS project. It is possible to pair the course with a potential
training course on OSS-CRS.

David gave a [talk](https://www.youtube.com/watch?v=8DzOV-yArRE) on how we can
use AI to enhance governance for software dependencies, managing supply chain
vulnerabilities, adding and updating new dependencies. It is a mix of using AI
and traditional measures together and the working group might be starting a
SIG to further work on this.

Last quarter, Sarah started a discussion on ensuring that the OpenSSF tools
can easily integrate with agentic skills and MCP. There is an
[OpenSSF AI-readiness issue](https://github.com/ossf/tac/issues/601) and we
also started looking at proposing a new SIG called
[Embracing AI Securely SIG](https://github.com/ossf/ai-ml-security/issues/48).
The goal is to both migrate OpenSSF projects to make them available to agentic
tooling systems, but also help volunteer OSS projects to build around AI in a
secure way. This is still in discussions, the roadmap might change.

The group is also looking at the IBM proposal to build an AI security
baseline. The goal is to make a new SIG that will build upon
[the IBM project](https://github.com/IBM/ai-security-baseline), which starts
from the OpenSSF Security Baseline and creates a similar framework for the AI
ecosystem. This would be a collaboration between the working group, Orbit and
Gemara.

On the academic front, Teodora Baluta and Zedian Shao from Georgia Tech gave a
[presentation](https://drive.google.com/file/d/1JclDHEVzO2q_piEiYMWtqcXhXrm4UGrW/view)
on "Cordyceps: Covert Control Attacks on LLMs via Data Poisoning", showing how
LLMs are still vulnerable to data poisoning attacks.

The meeting time for the working group got move to Thursdays at 11am Pacific,
but we might need to move it again to eliminate a new overlap.

The group was present at Open Source Summit North America. We had a panel on
AI, where we talked about model signing, OSS-CRS, and the end-to-end
provenance SIG. We had a session to demo the tooling at CdCon. And we had a
keynote on OSS-CRS at OpenSSF Community Day collocated event.

The group built new relationships with the Confidential Computing Consortium
and the Trusted Computing Group for issues related with confidential AI,
trusted datasets, trusted model inference.

### The OSS Cyber Reasoning Systems (OSS-CRS) project

The OSS Cyber Reasoning Systems project was presented in the OpenSSF Community
Day Keynote and got significant updates. The frameworks for bug-finding and
for bug-fixing are merging in a new design. There is a partneship with MIT
Lincoln Labs to help with engineering support, in particular with modularizing
the project to scalably support more tools and more agents. There is also work
on adding support for deploying the project in offline environments,
potentially using Nix to achieve this goal.

Thanks to Puerco, there is now an OSS-CRS reusable GitHub action
([example run](https://github.com/puerco/ampel/actions/runs/29232598664)).

The group is collaborating with Alpha - Omega to strategically find open
source projects to apply OSS-CRS to. In partnership with OSTIF, the group had
a bug reporting campaign. Out of 200 reported bugs, only 6 were deemed to be
invalid after triage, showing that the project is able to find high-quality
vulnerabilities.

The OSS-CRS team (Team Atlanta) is also working on
[CRSBench](https://oss-crs.openssf.org/crsbench), as an environment to
evaluate AI agents on bug finding and fixing. The accompanying paper has been
submitted to ACM CCS. Team 42 also has a similar environment, SSEBench. Both
teams presented on their environments and the results they got.

Jeff gave a talk on how AI changes the vulnerability handling processes,
[The Vulniverse: Hold the Slop Please](https://docs.google.com/presentation/d/1eVDcZDhUiI9kdhrb0DfrxcFRJIZT6irtpEobt_54moQ/edit?slide=id.g3ba3cc1bb03_2_112#slide=id.g3ba3cc1bb03_2_112).
This also discussed the CNCF blogpost,
[AI-driven shift in vuln discovery](https://www.cncf.io/blog/2026/04/16/the-ai-driven-shift-in-vulnerability-discovery-what-maintainers-and-bug-finders-need-to-know/),
in the context of a sharp reduction of time to active exploit of
vulnerabilities. This is relevant for OSS-CRS, as the goal is to provide a
solution to discover vulnerabilities that is not tied to one orchestration
framework or the models from one single provider.

Another presentation was on [GONDAR](https://arxiv.org/abs/2604.01645), a
sink-centric fuzzing framework to
[scale LLM agent based bug finding beyond just adding more CPUs](https://team-atlanta.github.io/blog/post-sinkfuzz-glm/).

Next, the FuzzingBrain team presented a methodology for preventing false
positives, based on two blog posts that they wrote
([1](https://fuzzingbrain.github.io/posts/spring-2026-campaign-update.html)
and
[2](https://fuzzingbrain.github.io/posts/how-we-verify-fuzzer-crashes.html)).
This also got linked with
[OpenSSF Coordinated Vulnerability Disclosure Guide](https://github.com/ossf/oss-vulnerability-guide/blob/main/finder-guide.md).

### The Secure Agentic Framework project

The Secure Agentic Framework project got its new name and rebranding (from the
formerly known SAFE-MCP). It has expansions as "SAF for MCP" and "SAF for
Kubernetes".

The goal of the project is to combat shadow AI, make sure that all MCP servers
and agents that are deployed in an organisation are secure by default. There
is strong synergy with Gemara and the ORBIT working group.

Jay proposed a new repository,
[Security Analysis Skill for SAF for MCP](https://github.com/camaleon2016/SAFE-MCP-skill/tree/main),
to be donated to the SAF group. We might need a new GitHub organisation to
coordinate between various projects in the Secure Agentic Framework project.

The group had a
[presentation](https://docs.google.com/presentation/d/1m6h-LaZeOisUPViknXH8S-Jkiq84NuYMi054BbA5kfw/edit?slide=id.p1#slide=id.p1)
about [Nono](https://nono.sh/), a solution to securely use AI agents,
[cooler than a sandbox](https://docs.google.com/document/d/1d48jvmBiQSR0HbPdiwmdanihnh77aI4qOc8-5Rn3DSI/edit?tab=t.0).
The aim is to integrate Nono into the "Isolation and Containment Strategy"
workstream of the project.

The group is also looking at the AI attacks designed to trigger safeguards, to
prevent automated AI analyses. For example, malware that explicitly includes
texts that would trigger AI refusals so that analysts are not able to use AI
to increase their efficiency.

### The model signing project

The model signing project is evolving the OMS standard by formalizing the
[OMS specification](https://github.com/ossf/model-signing-spec)
and adding a conformance test suite. This is to ensure that the Python and Go
version of the tooling work without any gaps.

We are now supporting
[signing agent skills with OMS](https://docs.google.com/document/d/1Z4LIh3wyBPZYc_0Yfuj7bODO-NdYNkWEAMQUhF5NoBs/edit?tab=t.0)
and are looking into extending the OMS specification to support
signing and verification of AI artifacts deployed in OCI containers.

We are also looking at enhancing the signature format to allow multiple
signatures from different identities, or to support multiple predicates (e.g.,
a signature at the moment of publication to HuggingFace and another signature
after a different actor scanned the model for vulnerabilities).

As part of formalizing the OMS specification, we are also looking at defining
stricter policies for verification of signatures.

There is a strong synergy with the End-To-End ML Provenance SIG and with
the Supply Chain Workstream in CoSAI.

We would need to rename the repository to signal the expansion to more ML
artifacts and we are looking into using a separate GitHub organisation to have
all ML supply chain projects in a single place.

### The End-To-End ML Provenance SIG

The End-To-End ML Provenance SIG is looking at integrating with the model
signing project, donating Atlas to be an OpenSSF project. As part of this, we
are looking at migrating everything to the same GitHub organisation.

The SIG is the technical side in a pair with CoSAI's Supply Chain Workstream.
The group has been helping write the ML Supply Chain Maturity Levels
whitepaper in CoSAI.

There is a collaboration opportunity between the end-to-end ML provenance SIG
and cyberpolicy groups (OpenSSF Global Cyberpolicy and ORBIT), given EU CRA
and other pieces of legislation that cover AI.

## Up Next

Given the large number of working groups, we are continuing the
[biweekly meeting](https://docs.google.com/document/d/1w8d08HStfi9LKbz2VVWxH-wZ5BOsDSnFpwzwHjwb3sg/edit?tab=t.0)
to collaborate more closely between the OpenSSF AI/ML WG, CoSAI, SPDX AI BOM,
and other similar groups. The general purpose of the meeting is to align
between these working groups and spread the knowledge of what each one is
working on.

We had a few sessions of the meeting where we discussed synergies with the
AI-BOM communities. We expect collaboration to continue here.

## Funding requests

None planned at the time

## Questions/Issues for the TAC

None

## Additional Information

None
