# 2025 Q4 AI/ML WG and model signing project

## Overview

We continue our mission of being at the intersection of security and AI,
supporting both using AI to improve security of software, and adding security
practices to AI development processes. While there are similar AI related groups
in many other places -- with new ones starting and old ones ramping down --, we
still try to make this group as the central place to get updates from all other
TIs.

For the past quarter we continued to provide value via model signing, and the
MLSecOps whitepaper. We also ramped up 2 additional SIGs:

- Safe-MCP: to secure the MCP, A2A, and similar agentic related workflows
- CRS: to introduce AI tools into discovering and patching vulnerabilities
  workflows, as a continuation of the DARPA AIxCC.

Together with the existing SIGs (one on model signing and one on applying AI to
understand the security economics of OSS projects), we are still performing work
in both the "security for AI" and "AI for security" domains.

Finally, we continued working on a
[new long term plan](https://docs.google.com/document/d/1I-GDKV3rL3jPwPK3xO5hKh8feGBouTwTUY3aqj0-0IY/edit?pli=1&tab=t.0)
to make the group even more useful, interlocking within more OpenSSF and similar
communities. We have bi-weekly strategy meetings on this to deliver a more
cohesive vision in the new year.

## General WG updates

### Purpose

We aim for the WG to be the central place to collect all information regarding
ML and security. The goal is that the groups serves as a central place to
collate any recommendation for using AI securely ("security for AI") and using
AI to improve security of other products ("AI for security").

### Current Status

We have published the
["Visualizing Secure MLOps"](https://openssf.org/wp-content/uploads/2025/08/OpenSSF_MLSecOps_Whitepaper.pdf)
whitepaper (MLSecOps), as a practical guide for building robust and secure AI/ML
pipelines. The whitepaper goes over OpenSSF and other open source tooling that
can help with security in every stage of the ML development cycle. It also
introduced 10 new personas for the
[AI-related security toolbelt](https://github.com/ossf/toolbelt/tree/main/personas).

We also collaborated with the Best Practices WG to release a
[Security Focused Guide for AI Code Assistant Solutions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions).
This also pairs with the launch on 16th of October of the
["Secure AI/ML-Driven Software development" (LFEL 1012)](https://training.linuxfoundation.org/express-learning/secure-ai-ml-driven-software-development-lfel1012/)
course.

We also held an OpenSSF Tech Talk on "Securing the AI Lifecycle" which covered
the MLSecOps whitepaper, the `model-signing` project, Intel's project ATLAS and
how the latter two can be merged together for a shared vision on trusted AI/ML
supply chain.

During the WG meetings we had talks on:
- secure A2A (A2As)
- CVE Bench -- a benchmark of AI Agents for Vulnerability patching in OSS
- GPU-based model signing with confidential computing support
- Project ATLAS for AI/ML supply chain security with confidential support
- AIxCC finals recap
- Safe-MCP
- Signing agent cards with Sigstore
- Project VAIL -- runtime fingerprinting of models to build lineage graphs
- Kusari inspector -- AI-driven PR reviews with a security focus

We had a successful TI funding engagement where AdaLogics added fuzzing support
to the `model-signing` library. No bugs have been reported yet!

We are going to talk about the work done by this group at PyTorch conference,
where we have a BoF on everything AI and security.

Moving on to the SIGs, the `model-signing` SIG is starting monthly meeting from
22nd of October, after putting these on a break with the launch of
`model-signing-1.0` in April.  We have just released `model-signing-1.1` on 10th
of October, adding support for new features such as supporting hashing via
BLAKE3, signing via PKCS 11, and supporting private Sigstore instances. The new
release also incorporates new features to simplify usage of the CLI and the API,
while also fixing bugs that have been discovered since April.

Coalition for Secure AI also published a
[whitepaper on model signing](https://github.com/cosai-oasis/ws1-supply-chain/blob/main/signing-ml-artifacts.md)
which promotes the `model-signing` project as the recommended approach to secure
the ML supply chain.

The AI economics SIG focuses on determining which OSS packages risk creating
huge financial losses for Fortune 500 companies if compromised in a supply chain
attack. The group identified that AI slop is a latent black swan event in
vulnerability management. The SIG also worked on benchmarking several AI agents
on how they can patch security vulnerabilities -- as patching these is an
expensive job.

After the AIxCC challenge, we started a "Cyber Reasoning System" SIG aimed to
surface the work done by the teams during AIxCC. This means both working with
the upstream projects to add code fixes and use the AIxCC tools to discover
additional vulnerabilities. But, it also entails developing these tools further
to create a suite of systems that are able to improve the security of OSS
software.

We also started a "SAFE MCP" SIG after the SAFE MCP presentation. The purpose of
this SIG is both to provide a home to SAFE MCP project, but, more importantly,
to serve as the place where we work towards securing the agentic development
workflows. It should allow closer collaboration with OIDF and OWASP for agent
identity, and, respectively, agent toolkit application security.

### Up Next

We will continue enhancing the
[long term plan](https://docs.google.com/document/d/1I-GDKV3rL3jPwPK3xO5hKh8feGBouTwTUY3aqj0-0IY/edit?pli=1&tab=t.0)
to increase synergies with the rest of OpenSSF and create a roadmap of
deliverables for the next year.

Although 2 of the SIGs are new and one is just starting, we hope to get
significant results from all of them in this quarter and the next year.

Tactically, we need to work on the PRs formalizing the sandbox stages for 3 of
the SIGs (all but the model signing one).

For model signing, we are looking at more integrations, after giving demos about
the project at various conferences, both for academia and for industry.

All of our SIGs are ramping up significantly, hoping for more updates in the
next year.

## Questions/Issues for the TAC

None

## Additional Information

None
