# 2026 Q2 AI/ML WG and model signing project

## Overview

We are still working at the intersection of security and AI/ML, continuing the
mission to support both using AI to improve security of software, and
adding security practices to AI development processes. With the focus on
agentic AI and the advent of AI driven contributions, this is vital.

There are similar AI related groups, both under The Linux
Foundation and elsewhere, some of which (e.g., OpenSSF, CoSAI, OWASP) are
umbrellas on their own with multiple working groups and meetings that are
relevant. Thus, one additional mission of this working group is to be the
central place to get updates from all other relevant AI related groups.

In the last quarter we:

- increased collaboration with different working groups, within OpenSSF and
  outside
- extended model signing by creating a separate Go implementation,
  experimenting with signing other AI artifacts, and working on a formalized
  spec
- worked on a standardization of lineage and provenance for the end-to-end ML
  provenance, with a vision to cover the entire lifecycle of any ML artifact
- used OSS CRS and similar automated tools to find vulnerabilities in OSS
  projects and the Linux kernel
- discussed AI slop and created a dashboard for vulnerabilities generated from
  vibe-coding
- evolved and extended the SAFE MCP project to the Safe Agentic Framework,
  which now has a subproject on MCP and one on K8s
- continued the engagement with CoSAI, SPDX, OWASP, and other working groups
- delivered an OpenSSF Welcome Call (hosted by the BEAR WG) on the AI/ML Security WG
  ([recording](https://youtu.be/GGEIoi6XHi0?si=yPhfH0_qwFbczp0S))
- continued engagement with CoSAI on the Model Signing Maturity Levels
  whitepaper

### The AI/ML working group

After the
["Secure AI/ML-Driven Software development" (LFEL 1012)](https://training.linuxfoundation.org/express-learning/secure-ai-ml-driven-software-development-lfel1012/)
course was published last year, we (mainly David) have started working on a
second course, this time focused on developing software that securely uses AI.

The working group was introduced to the BEAR working group at the end of
February. We presented an overview of how the group was created, what are the
areas we work on, what are the standing SIGs, and asked for more volunteers to
join the meetings.

Sarah started a discussion on ensuring that the OpenSSF tools can easily
integrate with agentic skills, MCP, and other agentic tools. This is in
collaboration with the ORBIT working group and has also resulted in the
[OpenSSF AI-readiness issue](https://github.com/ossf/tac/issues/601).

After the Trivy compromise resulted in a
[compromise of liteLLM](https://docs.litellm.ai/blog/security-update-march-2026)
a few members of the working groups have engaged with the LiteLLM developers
to help them secure their supply chain and their releases.

### The model signing project

The model signing project has started to look into
[Extending OMS to skills, artifacts, etc](https://docs.google.com/document/d/1ioRt23ow5Q0mEALkHU-toQBl76dLIMxTAsaiHmxc1qs/edit?usp=sharing)
given that many people started using OpenClaw and similar agents which use
agentic components from third-parties. In parallel, we had
[a demo of signing agent skills with OMS](https://docs.google.com/document/d/1Z4LIh3wyBPZYc_0Yfuj7bODO-NdYNkWEAMQUhF5NoBs/edit?tab=t.0).

With the extension in scope of what `model-signing` can sign, we are looking
at changing the format of the signature,so that it can cover more AI
artifacts.

In fact, given that there is now a Go version of the `model-signing` library,
we are actively working on fully formalizing the OMS specification in the
[OMS repository](https://github.com/ossf/model-signing-spec). The goal here is
to have a human readable specification of the supported signature formats,
paired with machine readable and validated JSON documents. We also intend to
add conformance tests to compare between the Python and Go libraries and to
ensure that models can be signed and verified across the tools and the
operating systems boundaries.

Given the extension in scope, we are looking at renaming, since we are moving
towards a world where we need to sign more than models.

### The end-to-end ML provenance SIG

In a similar vision, the end-to-end ML provenance SIG is working on a spec for
[the standard](https://docs.google.com/document/d/1S5UUKt91RvLoJUNXF0wYtcedzopoeOteyJ6L-7l7CsE/edit?pli=1&tab=t.0#heading=h.sxcmqopt7zqg)
on how to generate provenance and lineage for all ML artifacts, across the
entire lifecycle of ML development. The goal is to adopt as much as possible
from the existing supply chain pieces that have been developed (e.g., SLSA,
in-toto, GUAC), and only extend them to ML use cases. For this, we also need
to properly identify use cases and ML-specific risks.

There is a collaboration opportunity between the end-to-end ML provenance SIG
and cyberpolicy groups (OpenSSF Global Cyberpolicy and ORBIT), given EU CRA
and other pieces of legislation that cover AI.

Another goal of the SIG is to integrate the Atlas CLI with the wider ML supply
chain security efforts. The CLI is already compatible with OMS v1.0 and the
SIG plans to donate the project to OpenSSF.

### The OSS Cyber Reasoning Systems (CRS) SIG and project

Moving to the OSS Cyber Reasoning Systems, working group, the main update is
that the OSS-CRS project [was approved](https://github.com/ossf/tac/pull/559)
and is now being onboarded. The team behind the project also published a
[paper on ArXiV](https://arxiv.org/abs/2603.08566), which pairs with two other
papers ([1](https://arxiv.org/abs/2604.01645),
[2](https://arxiv.org/abs/2602.07666)) on using AI to find vulnerabilities
at scale. There is also a blog post,
["More CPUs won't find more bugs"](https://team-atlanta.github.io/blog/post-sinkfuzz-glm/),
on the same topic. Similarly, there is a
[blog post](https://team-atlanta.github.io/blog/post-patch-2026-ensemble/) on
ensembled patch techniques that are already integrated with OSS-CRS project.

The OSS-CRS working group also proposed an
[RFC](https://github.com/ossf/oss-crs/pull/59) for a standardized CRS
interface that any cyber reasoning system can use, regardless of the
underlying agent (model and harness).

The team has run the CRS implementation against OSS projects and identified
some bugs which got patched. The plan is to integrate OSS-CRS within CI, to
strengthen OSS projects.

The OSS-CRS SIG has also worked with the vulnerabilities disclosure working
group on ways to handle
[AI slop](https://github.com/ossf/wg-vulnerability-disclosures/issues/178).
There is now
[a dashboard for vulnerabilities introduced by vibe-coding](https://vibe-radar-ten.vercel.app/).

The OSS-CRS-SIG has also worked on using AI and fuzzing to identify
vulnerabilities in the Linux Kernel.

Tackling maintainer anxiety (from e.g., 100 new vulnerability reports that
they have to fix in 90 days), is the main priority of the working group. So,
the group has looked at the large number of opinions on how to better engage
with maintainers, to identify the most sensible approach. With help from OSTIF
and maintainers of the OSS-Fuzz project, we can focus on the huge positive
gain from OSS-CRS: removing the big inertia in solving vulnerabilities by
surfacing them as soon as possible. There is some collaboration with
Alpha-Omega to pilot building these tools on GitHub

### The SAFE MCP SIG and project

On the SAFE MCP front, the
[Sandbox application for the SAFE Framework](https://github.com/ossf/tac/pull/561)
was accepted. The project is rebranding as SAFE Agentic Framework, with
SAFE-MCP and (the new) SAFE-K8s as sub-projects.

There have been several whitepapers written by members of the SIG and people
from the industry that build on top of SAFE MCP.

The SIG collaborates with MITRE and NIST and aims to also cover A2A and other
agentic AI projects.

## Up Next

This quarter there was an announcement of the
[LF grant funding to advance OSS Security](https://openssf.org/press-release/2026/03/17/linux-foundation-announces-12-5-million-in-grant-funding-from-leading-organizations-to-advance-open-source-security/)
which brings together AI and traditional software companies to advance the
security of OSS projects, using a mix of both AI and traditional practices.
This will create more opportunities for the working group and the SIGs to get
involved.

Given the large number of working groups, we are continuing the
[biweekly meeting](https://docs.google.com/document/d/1w8d08HStfi9LKbz2VVWxH-wZ5BOsDSnFpwzwHjwb3sg/edit?tab=t.0)
to collaborate more closely between the OpenSSF AI/ML WG, CoSAI, SPDX AI BOM,
and other similar groups. The general purpose of the meeting is to align
between these working groups and spread the knowledge of what each one is
working on. For the future, we are looking into a place where interested
parties can work on an OSV-like schema for AI vulnerabilities, with a goal to
have some updates ready by DEFCON.

## Funding requests

None planned at the time

## Questions/Issues for the TAC

None

## Additional Information

None
