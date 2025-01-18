# 2024 Q3 AI/ML WG and model signing project

## Overview

We continue our mission to enable security for AI and use AI for security of open source. The community is healthy, although there are multiple similar groups in various other organisations. This means we have to dedicate time to create interlocks between these groups, to share the knowledge and developments, and make sure work is not duplicated. It also means we have to find the niche where this group can bring added value -- we are currently engaging in determining this. At the same time, we continue work on model signing and experiments towards covering more of the ML supply chain.

## General WG updates

### Purpose

We aim for the WG to be the central place to collect all information regarding ML and security, but we are also planning to deliver technical initiatives, such as the model signing project.

### Current Status

The AI/ML working group now has incubating status.

We have updated the list of interlocks with other working groups in the AI security space. We have started some work on a taxonomy of all these groups and what areas we can collaborate on, what updates we can give/receive, what areas we can work on.  This helps in identifiying gaps and prevent duplication and dillution/fracturing of communities.

There is ongoing work on [mapping AI development lifecycle on the MLSecOps diagram from Ericson](https://github.com/ossf/ai-ml-security/issues/16). Goal is to create an LLMSecOps version as one of the technical outputs of this group in this year.

### Up Next

The group is planning for significant projects to work on in 2025, to [bring
added value](https://github.com/ossf/ai-ml-security/issues/26).

### Questions/Issues for the TAC

None

## Model signing project

### Purpose

Serve as a central place to collate any recommendation for using AI securely ("security for AI") and using AI to improve security of other products ("AI for security").

The model signing project aims to create a cryptographic signing specification for AI models, taking into account difficulties that arise when trying to protect the integrity of large blobs.

### Current Status

We are on the final stretches towards a 1.0 release with stable API, clearer documentation and potential users in mind. The aim is to have these users prototype integrations of model signing and together we can quickly iterate and build an even more secure ML supply chain.

The library is currently being tested internally at Google and Nvidia and several companies in the ML ecosystem (Kaggle, HuggingFace, Cohere) have also been contacted to explore collaborations and integrations. Dell and RedHat have also mentioned interest in testing the library in one community call.

Our aim for the project is to be agnostic with regard to the signing scheme. It should support Sigstore, public key infrastructure, etc. However, the signature must be in the same format -- we agreed on using the Sigstore bundle format. We have talked with Sigstore maintainers for the needed changes to support these additional signing scenarios.

We also had a presentation from Dreadnote about a similar project for model integrity, but focused more on the runtime requirements of the model. Long term, we aim to merge the two efforts.

Similarly, we had a presentation from Intel about trust in third parties throughout ML model lifecycle.

### Up Next

We aim to do the 1.0 release in Q1, with a coordinated press release across multiple blogs. To achieve the release, we need to stabilize the API, both in terms of using the project as a library and in using it as a CLI tool. We also need to ensure that documentation is clear, both for users and for integrators.

Another planned item here is to work on extending the signature file to also record tamper-proof metadata about other model properties (e.g., evaluation scores). Basically, we want to create a human-and-machine readable, tamper-proof version of model cards.

### Questions/Issues for the TAC

None

## Additional Information

At SigstoreCon Supply Chain 2024 we gave [a forward looking talk](https://www.youtube.com/watch?v=uqU3fnmK0BA&list=PLM6mY5TOhY1E02_fQWqfQk_gMRHHtX0q6&index=4) about what OpenSSF technologies can be used to fully understand the ML supply chain, end to end. Assuming we have complete SLSA provenances that record both inputs and outputs for every stage in the ML pipeline, we can use GUAC to quickly analyze the e2e ML supply chain, react to compromises, and determine what models need to be retrained to react to incidents while minimizing amount of resources used. This vision can be achieved by evolving several OpenSSF tools in the supply chain security ecosystem so that they are ML aware. This would be a focus for the AI/ML WG in the next year as well as a potential place to integrate the WG with other TIs under OpenSSF.
