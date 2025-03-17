# 2025 Q1 Sigstore

## Overview

We kick off the year with a few engineering efforts and continued adoption of Sigstore by package registries. RubyGems added
[support for attestations](https://www.ruby-lang.org/en/news/2024/12/25/ruby-3-4-0-released/#:~:text=Add%20%2D%2D-,attestation,-option%20to%20gem)
late last year, and [support for provenance](https://github.com/bazelbuild/bazel-central-registry/discussions/2721) in Bazel Central Registry
is under development.

## Rekor v2 - Tile-backed transparency log

Rekor on Tiles, aka Rekor v2, is a redesigned and modernized Rekor, Sigstore's signature transparency log, transitioning its backend to a modern,
[tile-backed transparency log](https://transparency.dev/articles/tile-based-logs/) implementation to simplify maintenance and lower operational costs.

More info: [Proposal](https://docs.google.com/document/d/1Mi9OhzrucIyt-UCLk_FxO2_xSQZW9ow9U3Lv0ZB_PpM/edit?resourcekey=0-4rPbZPyCS7QDj26Hk0UyvA&tab=t.0#heading=h.bjitqo6lwsmn)
and [design doc](https://docs.google.com/document/d/1qZ-lkpbQkBzV45rtemWYmT6ReqCwjTt5TbMDFLdaPyM/edit?resourcekey=0-bMAyN9EKPDvB0H3edYi_Cw&tab=t.0#heading=h.xzptrog8pyxf)

Follow its development at https://github.com/sigstore/rekor-tiles.

### Purpose

As outlined in the proposal, Rekor v2 greatly simplifies the complexity of log maintenance and drives down operational costs,
replacing Trillian, a set of services that supports transparency log deployment, with a new library called Tessera to enable
a log backed by "tiles". Tiles are cheaper to store and trivially cacheable. Tessera also reduces the service footprint down
to just a database and tile storage, simplifying deployment complexity.

### Current Status

Development is underway. Follow along on the [public project tracker](https://github.com/orgs/sigstore/projects/14).

### Up Next

We aim to complete an Alpha release of the service by end of Q1/early Q2. We will be deploying a public-good instance of the
service to our staging environment in Q2, and begin working with Sigstore clients to implement support for Rekor v2.

Longer term, we will be working with the community to grow the number of publicly available Sigstore logs.

### Questions/Issues for the TAC

None at this time.

## Cosign Modernization

Cosign continues to be updated to support the Sigstore bundle format.

### Purpose

Cosign, being the first client developed for Sigstore, naturally has some technical debt. As the ecosystem
evolved, Sigstore clients created a standard format for input/output, and Cosign development has picked up recently
to catch up to the more modern Sigstore clients.

### Current Status

Last year, Cosign added support for this bundle format using `--new-bundle-format`, backed by the development of sigstore-go.

Most recently, implementation of the new [Cosign bundle spec](https://github.com/sigstore/cosign/blob/main/specs/BUNDLE_SPEC.md),
for storing attestations in the bundle format in OCI Image Manifest v1.1 objects and retrieving them via the OCI
Referrers API, was completed.

### Up Next

We will be publishing a roadmap for Cosign v3 and beyond, including deprecation of the old bundle format,
cleaning up the CLI UX, [providing utilities to transform old bundles to new bundles](https://github.com/sigstore/cosign/issues/3794),
and eventually replacing its internal API with sigstore-go.

We will also be publishing a specification for [storing signatures as OCI artifacts](https://github.com/sigstore/cosign/issues/3927).

### Questions/Issues for the TAC

None at this time.

## Project tiers

Define the various levels of support and adoption for projects under the Sigstore organization.

### Purpose

As Sigstore has grown, so too have the number of projects in the organization. The TSC has begun
[classifying projects](https://github.com/sigstore/community/pull/551) to denote which projects
are actively supported by the TSC and which are driven by community members. Adopters should
consider these classifications when selecting clients and tools to use in their pipelines.
