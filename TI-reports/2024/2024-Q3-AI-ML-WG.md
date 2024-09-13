# 2024 Q3 AI/ML WG and model signing project

## Overview

We continue our mission to enable security for AI and use AI for security of open source. The community is healthy, but we are seeing multiple similar groups ramping up, so we need to always dedicate time to create interlocks between the groups, share the knowledge and developments, and make sure work is not duplicated. Future launches for model signing and documentation are planned for Q4. We still have a focus on experimentation too.

### Recent Updates

- Some members involved in ASIC (AI Safety Institute Consortium) workstreams
- Discussed [AI supply chain whitepaper](https://research.google/pubs/securing-the-ai-software-supply-chain/)
- Presentation on Scalibr and Tsunami as tool to scan for vulnerabilities
  - Seeding discussion on donating Tsunami to the OpenSSF -- decision pending
- Discussion on NIST SP 800-218A standard for GenAI and Dual-Use foundation models and how OpenSSF technologies can be used
- CoSAI, "What's in the SOSS" podcast

#### Model signing

- Several demos as the library/CLI progressed
- C2PA presentation from Adobe, with a focus on potential application for model signing

### Purpose

Serve as a central place to collate any recommendation for using AI securely ("security for AI") and using AI to improve security of other products ("AI for security").

The model signing project aims to create a cryptographic signing specification for AI models, taking into account difficulties that arise when trying to protect the integrity of large blobs.

### Current Status

We're active and healthy, both in the parent working group and the model signing project. The field evolves fast and we are keeping up to date.

### Up Next

- Document detailing how OpenSSF products can be used to strengthen the AI supply-chain.
- Potentially start a SIG on AI vulnerability disclosure. Need to make sure we have enough specificity to warrant creating the SIG vs merging with the vulnerability disclosure WG.
- Demo model signing library and CLI at the next model signing project meeting.  Then, start integrating these with model producers to extract feedback before a release of the model signing library.
  - Publication of wheel, followed by playbook to integrate it with ML frameworks and ML model hubs
  - Sign with Sigstore or own PKI
- Exploring deeper integrations of model signing with in-toto, witness, C2PA.

### Challenges

- New groups in AI/ML are constantly springing up. We are trying to create tentacles in each of them, and then report back to the working group meetings so that everyone is aware. A constant issue is to make sure we don't duplicate the same work in two separate groups.
- Meeting slot on Monday means several meetings have to be skipped due to US holidays. Might consider moving to another slot if this becomes an issue.

### Questions/Issues for the TAC

We have one TAC member as co-chair and several other TAC members are frequent participants in both the working group and the model signing project.

We're eager for substantive discussion with TAC and others.

## Additional Information

We are currently in the process of formalizing the lifecycle documents, both for the [working group (sandbox to incubating)](https://github.com/ossf/tac/pull/375) and for the [model signing project (was SIG in previous update)](https://github.com/ossf/tac/pull/347).
