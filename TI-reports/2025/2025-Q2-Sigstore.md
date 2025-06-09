# 2025 Q2 Sigstore

## Overview

Over the last quarter, the Sigstore community has been focused on client development and infrastructure improvements.

## Rekor v2 - Tile-backed transparency log update

Rekor on Tiles, aka Rekor v2, is a redesigned and modernized Rekor, Sigstore's signature transparency log, transitioning its backend to a modern,
[tile-backed transparency log](https://transparency.dev/articles/tile-based-logs/) implementation to simplify maintenance and lower operational costs.

### Purpose

Rekor v2 greatly simplifies the complexity of log maintenance and drives down operational costs,
replacing Trillian, a set of services that supports transparency log deployment, with a new library called Tessera to enable
a log backed by "tiles". Tiles are cheaper to store and trivially cacheable. Tessera also reduces the service footprint down
to just a database and tile storage, simplifying deployment complexity.

### Current Status

Development is underway. Follow along on the [public project tracker](https://github.com/orgs/sigstore/projects/14).

We cut our first code-complete [alpha release](https://blog.sigstore.dev/rekor-v2-alpha/) and deployed the service to our
staging environment. We are actively adding support for Rekor v2 to the Go, Python and Java clients, with Javascript
and Ruby to follow later.

### Up Next

We are completing client development for our beta release. We will then be working on infrastructure productionization
and deploying an instance of the log to our production environment.

Longer term, we will be working with the community to grow the number of publicly available Sigstore logs.

### Questions/Issues for the TAC

None at this time.

## Model Signing 1.0 release

The model-signing project had its [first major release](https://blog.sigstore.dev/model-transparency-v1.0/),
in collaboration with Nvidia and HiddenLayer.

### Purpose

As outlined in the linked blog, supply chain security for models looks a lot like supply chain
security for binaries. Model signing adds integrity and authenticity to the model production pipeline.

### Up Next

Further adoption of model signing within model hubs like Kaggle.

### Questions/Issues for the TAC

None at this time.

## sigstore-go 1.0 release

The Sigstore community released its [first major version](https://blog.sigstore.dev/sigstore-go-1-0-now-available/)
of the Go Sigstore client library.

### Purpose

sigstore-go provides a stable, modular, and flexible library for developers to integrate their Go applications with Sigstore's signing and verification infrastructure.

This new library was created to address the limitations of the previous Go API within the Cosign tool.
As Cosign evolved from a container signing tool to a more feature-rich solution, its internal API became
less suitable for developers who needed to integrate Sigstore's capabilities into their own Go projects.

### Up Next

We're looking for community feedback on the library! Try out the library and let us know what works and what doesn't!

## Sigstore & Post-Quantum Cryptography

We've published a [blog post](https://blog.sigstore.dev/post-quantum-2025/) on how Sigstore and post-quantum cryptography intersect
and how we can begin to experiment with PQC.

### Purpose

In the coming years, systems will begin to transition to post-quantum cryptographic algorithms (PQCA).
There is some inherent tension in these transitions as we learn things through adoption, and making decisions too soon can saddle us with tech debt.
We want to enable experimentation in Sigstore so we can begin to learn more about the challenges of integrating PQCA
while also recognizing that users and private deployers may have different requirements.

### Current Status

Over the last few months, we've been working on cryptographic agility, making it easier
to plug in different algorithms. As part of this work, we've uncovered some bugs and found
opportunities to clarify our client specification.

### Up Next

The community will be experimenting with PQC algorithms to measure the performance
and operational costs. We'll be publishing more blog posts based on our experimentation.
