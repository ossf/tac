# 2026 Q1 Sigstore

## New Projects

* [sigstore-rust](https://github.com/sigstore/sigstore-rust), a Rust implementation of signing and verification
  that passes conformance testing, was donated to the organization. OpenSSF TI has also provided funding to do
  a thorough review of the project.

## Rekor v2 - Tile-backed transparency log update

[Development has finished](https://blog.sigstore.dev/rekor-v2-ga/), with a production
instance available for usage. As a reminder, adoption of this new log will simplify
maintenance, lower operational costs and improve log verifiability.

The public-good instance will default to Rekor v2 in the coming months. We are
[actively encouraging the community](https://github.com/sigstore/sigstore-blog/pull/92) to
update their clients.

## Cosign v3

[Cosign v3](https://github.com/sigstore/cosign/releases/tag/v3.0.5) was recently released,
which defaults to producing signature metadata that aligns with the Sigstore client specification.
[Bundles](https://blog.sigstore.dev/cosign-verify-end-user/) are now the default output, and
container signatures are uploaded as OCI referring artifacts.

## Public-good instance reliability improvements

Development is underway to have the public-good instance deployed to multiple regions
to improve reliability.
Ping on Sigstore's Slack for the design doc if you're interested in learning more.

## Post-quantum cryptography timeline

The community has proposed a [timeline and plan](https://docs.google.com/document/d/15wQW5RCk55_CrIOYEtzJ0IyazbBGdMK8KsaI8S8oJ7U/edit?pli=1&tab=t.0#heading=h.o3tezvh8snap)
for the adoption of PQC signatures in Sigstore clients and services. More to come
as we begin to flesh out the design.

## OpenSSF TI-funded log monitoring website

[Through OSSF TI funding](https://github.com/ossf/tac/issues/536), work is underway to
build a website for monitoring the Rekor transparency log, akin to https://www.gopherwatch.org/.
See an early version [here](https://github.com/trailofbits/rekor-watch).

## Funding requests and updates

We are not planning any additional funding requests at this time.

Updates for existing funding requests:

* [Log monitoring website](https://github.com/ossf/tac/issues/536) - Funds have been fully spent, work is underway following the timeline in the funding request
* [Rust client audit](https://github.com/ossf/tac/issues/574) - We are actively searching for a vendor to complete this work and should have an update shortly

