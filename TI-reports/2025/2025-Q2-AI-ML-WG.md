# 2025 Q2 AI/ML WG and model signing project

## Overview

We continue our mission to enable security for AI and use AI for security of
open source. There are similar AI related groups in other places, but this
working group seems to be the central place where AI and security for OSS meets.
We spent time in each meeting to discuss the interlocks between these groups,
besides the work being done here.

We continue the work on model signing and the ML supply chain, mapping AI/ML
workflows to an MLSecOps diagram, as well as looking over starting a new SIG for
applying AI to understand the OSS security economics for any OSS project -- this
is currently under discussion.

## General WG updates

### Purpose

We aim for the WG to be the central place to collect all information regarding
ML and security, but we are also planning to deliver technical initiatives, such
as the model signing project and a very research-focused proposed work to use AI
to understand security economics.

The goal is that the groups serves as a central place to collate any
recommendation for using AI securely ("security for AI") and using AI to improve
security of other products ("AI for security").

### Current Status

The AI/ML working group now has incubating status.

We have updated the list of
[interlocks with other working groups in the AI security space](https://docs.google.com/spreadsheets/d/1XOzf0LwksHnVeAcgQ7qMAmQAhlHV2iEf4ICvUwOaOfo/edit?gid=0#gid=0).
We have started some work on a taxonomy of all these groups and what areas we
can collaborate on, what updates we can give/receive, what areas we can work on.
This helps in identifiying gaps and prevent duplication and dillution/fracturing
of communities.

There is ongoing work on
[mapping AI development lifecycle on the MLSecOps diagram from Ericsson](https://github.com/ossf/ai-ml-security/issues/16).
The members working on this have scheduled to publish a whitepaper by OSS NA.
This will also likely tie in with the personas effort.

### Up Next

The main item of discussion in the past few meetings has been
[the AI economics SIG](https://github.com/ossf/ai-ml-security/issues/27). We
just voted to launch the group after discussing if it is the best fit for the
SIG and planning some clearly defined deliverables, making sure that the topic
matches the working group.

The AI/ML WG is planning for significant projects to work on in 2025, to [bring
added value](https://github.com/ossf/ai-ml-security/issues/26).

## Model signing project

The model signing project aims to create a cryptographic signing specification
for AI models, taking into account difficulties that arise when trying to
protect the integrity of large blobs. This specification will be part of the
library developed at https://github.com/sigstore/model-transparency and a full
version of the specification will be included with the first stable release.

### Current Status

Launch of v1.0 scheduled for this week. This will have a stable API, clear
documentation, a standardized signature format. We aim to then build upon this
signature format to start incorporating additional ML metadata to make all of
this tamper proof.

The library is currently being tested internally at Google and Nvidia and
several companies in the ML ecosystem (Kaggle, HuggingFace, Cohere) have also
been contacted to explore collaborations and integrations. Dell and RedHat have
also mentioned interest in testing the library in one community call.

Our aim for the project is to be agnostic with regard to the signing scheme. It
should support Sigstore, public key infrastructure, etc. However, the signature
must be in the same format -- we agreed on using the Sigstore bundle format. We
have talked with Sigstore maintainers for the needed changes to support these
additional signing scenarios.

### Up Next

Integrating the model signing library in ML frameworks and model hubs is the
next goal. Building upon this layer to add additional ML metadata (e.g., model
cards) in a tamper proof format is an equally important goal.

## Questions/Issues for the TAC

None

## Additional Information

None
