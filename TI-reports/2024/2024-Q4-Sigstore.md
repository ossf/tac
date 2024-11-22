# 2024 Q4 Sigstore

## Overview

### Conference

Our second [SigstoreCon: Supply Chain Day](https://events.linuxfoundation.org/sigstorecon-supply-chain-day/) conference just wrapped up. With just over 90 attendees, SigstoreCon brought together individuals and organizations excited about not only Sigstore but other supply chain initiatives such as SLSA, SBOM, or in-toto. Talks are recorded [here](https://www.youtube.com/playlist?list=PLM6mY5TOhY1E02_fQWqfQk_gMRHHtX0q6).

### Adoption

Last year, we saw the first major adoption of Sigstore with [npm leveraging Sigstore](https://blog.sigstore.dev/npm-provenance-ga/) for signed provenance. This year saw a rapid increase of adoption of Sigstore, with:

* PyPI's implementation of [PEP 740](https://peps.python.org/pep-0740/), signed attestations for releases done through trusted publishing. Note that this pattern of leveraging trusted publishing workflows to drive adoption of signed builds and attestations is a pattern we'd like to see repeated across packaging ecosystems.
* Maven Central [supporting uploading and verifying](https://blog.sigstore.dev/announcing-sigstore-java-1-0/) Sigstore signatures in addition to PGP signatures
* [GitHub Artifact Attestations](https://docs.github.com/en/actions/security-for-github-actions/using-artifact-attestations/using-artifact-attestations-to-establish-provenance-for-builds), producing Sigstore-signed SLSA attestations for CI workflows
* Homebrew's beta release of [Sigstore-signed provenance](https://blog.sigstore.dev/homebrew-build-provenance/), built on top of GitHub Artifact Attestations.

### Client development

The client libraries for Sigstore saw active development under the [Sigstore clients SIG](https://github.com/sigstore/sig-clients):

* The first major release of [sigstore-java](https://github.com/sigstore/sigstore-java), along with Maven and Gradle plugins
* A v3 release of [sigstore-python](https://github.com/sigstore/sigstore-python) and [sigstore-js](https://github.com/sigstore/sigstore-js)
* A beta release of [sigstore-go](https://github.com/sigstore/sigstore-go), and we're working towards a 1.0 release and integrating sigstore-go into Cosign
* A release of [sigstore-ruby](https://github.com/sigstore/sigstore-ruby)

This development was sped up due to the [conformance test suite](https://github.com/sigstore/sigstore-conformance) to verify clients are producing and consuming the same content. We began work to make Cosign conformant, producing standardized "bundles" which contain verification metadata, along with consuming a "trust root" on verification to simplify and improve the verification process. Work will continue into next year to simplify Cosign's UX, add bundle support for signed OCI, and reduce code duplication between Cosign and sigstore-go.

### Infrastructure

Supported by the public good operations SIG and a multi-vendor oncall rotation staffed by Chainguard, GitHub, Google, Red Hat, and Stacklok, the public-good instance maintained its 99.5% availability SLO throughout the year, handling the increased load from additional adoption without issue.

### Documentation

Sigstore also requested [TI funding](https://github.com/ossf/tac/issues/339) to help modernize the documentation. This work is underway, with an increased focus on the [additional clients](https://docs.sigstore.dev/language_clients/language_client_overview/) and a restructuring of documentation. Into the coming year, we'll add more documentation on generating signatures on and verifying signatures from CI.

### Next Year

#### Adoption

Looking forward to next year, we'll see continued adoption of Sigstore. RubyGems has approved an [RFC](https://github.com/rubygems/rfcs/pull/57) for Sigstore bundles, with development underway. OS package registries like Debian have expressed interest, sparked by [discussions with the Python community](https://discuss.python.org/t/pep-761-deprecating-pgp-signatures-for-cpython-artifacts/67180) around deprecating PGP-signed cpython releases in favor of Sigstore-signed releases (PEP 761). Bazel Central Registry has also proposed supporting [Sigstore-signed SLSA attestations](https://github.com/bazelbuild/bazel-central-registry/discussions/2721).

#### Infrastructure

For the long-term sustainability of the Sigstore ecosystem, we will be focusing on driving down the operational cost of our transparency log Rekor. Building on recent developments in the Certificate Transparency ecosystem, we will be redesigning Rekor to be backed by a "tile-based" log, which is cheaper and easier to manage. We've created a [proposal](https://docs.google.com/document/d/1Mi9OhzrucIyt-UCLk_FxO2_xSQZW9ow9U3Lv0ZB_PpM/edit?resourcekey=0-4rPbZPyCS7QDj26Hk0UyvA&tab=t.0#heading=h.bjitqo6lwsmn) to summarize what we will be doing, with implementation and rollout in the next year. We will also look to onboard additional log operators once the operational costs are cheaper.

### Roadmap

We'll continue to update the [community roadmap](https://github.com/sigstore/community/blob/main/ROADMAP.md) as we make progress on these various projects.
