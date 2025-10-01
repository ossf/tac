# 2025 Q3 Sigstore

## Overview

Over the last quarter, the Sigstore community has continued to focus on client development and infrastructure improvements.

## New Projects

The Sigstore organization welcomed two new community projects:

* [model-validation-operator](https://github.com/sigstore/model-validation-operator), a Kubernetes admissions controller to validate AI models.
  Learn more on [our blog](https://blog.sigstore.dev/model-validation-operator-v1.0.1/)
* [sigstore-a2a](https://github.com/sigstore/sigstore-a2a), a library and CLI to sign [Agent-to-Agent](https://github.com/a2aproject/A2A) agent cards

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

We are about to announce our [beta release](https://github.com/sigstore/sigstore-blog/pull/86), with client support for Rekor v2
added to Cosign and the Go, Python and Java SDKs. We've also updated the client conformance test suite for clients
to test against. 

### Up Next

We are [actively working on productionization](https://github.com/orgs/sigstore/projects/14/views/12), working
towards deploying a public-good instance of Rekor v2 that meets Sigstore's 99.5% SLO.

Longer term, we will be working with the community to grow the number of publicly available Sigstore logs.

### Questions/Issues for the TAC

None at this time.

## Cosign v2.6.0

Hot off the press, we've released a [new minor version of Cosign, v2.6.0](https://github.com/sigstore/cosign/releases/tag/v2.6.0)
containing a number of new features including:

* Signing an in-toto statement rather than Cosign constructing one from a predicate,
  along with verifying a statement's subject using a digest and digest algorithm rather than providing a file reference
* Uploading a signature and its verification material (a ["bundle"](https://github.com/sigstore/protobuf-specs/blob/main/protos/sigstore_bundle.proto))
  as an OCI Image 1.1 referring artifact, completing [sigstore/cosign#3927](https://github.com/sigstore/cosign/issues/3927)
* Providing service URLs for signing and attesting using a [SigningConfig](https://github.com/sigstore/protobuf-specs/blob/4df5baadcdb582a70c2bc032e042c0a218eb3841/protos/sigstore_trustroot.proto#L185).
  which also enables [Rekor v2](https://github.com/sigstore/rekor-tiles) support

### Up Next

This will likely be our last minor release of Cosign v2 before we release a new major version of Cosign.
Cosign v3.0 will include very few changes. We'll be updating Cosign to default to producing and consuming
the new bundle format to be conformant with all other Sigstore SDKs.
Cosign v3 will be fully backwards compatible, in that you can verify old and new signature bundles produced
with previous versions of Cosign, and if you need signing to produce the older format, you'll just need to flip a boolean flag.

## OSSF TI Funded Monitoring

Through the sponsorship of the [OpenSSF TI fund](https://github.com/ossf/tac/issues/470), Trail of Bits
has been actively developing Sigstore's log monitor.

### Purpose

The ability to monitor a transparency log is one of Sigstore's primary benefits over traditional signing schemes.
An ecosystem that uses transparency logs must provide tooling to simplify and encourage monitoring.
A signature present in an unaudited log adds little value, rather the value comes from the discoverability of the signature by its creator.

### Current Status

Trail of Bits has reviewed the codebase and is actively completing open feature requests and issues. We have also shifted some development
hours towards Rekor v2 support.

### Next Steps

Continued development and preparation for a major 1.0 release.

## BigQuery Research Dataset

We've published a BigQuery dataset containing all Rekor v1 entries for researchers and interested parties
who would like to easily query Rekor to learn more about the contents of the log.

Learn more on [Sigstore's blog](https://blog.sigstore.dev/rekor-bigquery-dataset/).
