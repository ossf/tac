# 2026 Q3 Sigstore

## Overview

The bulk of the activity was continued work to finalize the PQC transition plan
(now Sigstore 2.0). Spent quite a bit of time aggregating feedback from
adopters/integrators, their use-cases, tooling, security expectations, and so
on. Work is underway to start with the transition by setting the feature
scaffolding.


## PQC Proposal Vote

Various presentations regarding PQC transition plan. Notably [Hayden's overview is quite illuminating](https://docs.google.com/presentation/d/1T_Y2yUgrgOu1GbKB_njOu-s8F5_5QyC8ZAb-xe0auG4/edit?resourcekey=0-qnwfJfQ8FFHEgkPH-E5VOw&slide=id.g3f6c27e244b_22_0#slide=id.g3f6c27e244b_22_0).
A lot of candid discussions on accommodating various use-cases (e.g., private
Sigstore deployments, or hybrid private/public components). Ultimately, the
community coalesced on the design described above.


### Up Next

Tickets have been created and some have been implemented. In the coming
days/week we will prepare a GitHub project to track progress with more
granularity.

Some preliminary PRs are landing in sigstore/sigstore, sigstore/sigstore-go, sigstore/cosign:
- https://github.com/sigstore/sigstore/pull/2416
- https://github.com/sigstore/sigstore/pull/2417 
- https://github.com/sigstore/timestamp-authority/pull/1472


## General ecosystem highlights


- [Noteworthy Contributions] TLS flag support for [rekor](https://github.com/sigstore/rekor/pull/2920) and [fulcio](https://github.com/sigstore/fulcio/pull/2418) -- Thanks Anitha Natarajan from RedHat!
- [Academic Presence] Sigstore had wide presence in USENIX Security 2026 (3 pieces of work), encompassing [usability user studies](https://www.usenix.org/conference/usenixsecurity26/presentation/kalu), [privacy enhancements](https://www.usenix.org/conference/usenixsecurity26/presentation/abu-ishgair), and [talks](https://www.usenix.org/conference/usenixsecurity26/steindler)
- [Adoptions] two tools can emit Sigstore bundles:
    - Tejolote (K8s SIG Release tool): https://github.com/kubernetes-sigs/tejolote/pull/664/changes
    - Tekton Chains: https://github.com/tektoncd/chains/pull/1831

## Funding requests and updates

### 

[Through OSSF TI funding](https://github.com/ossf/tac/issues/536), work continues to
build a website for monitoring the Rekor transparency log, akin to https://www.gopherwatch.org/.
See [an early version](https://github.com/trailofbits/rekor-watch), which will be merged
into [sigstore/rekor-monitor](https://github.com/sigstore/rekor-monitor) shortly. We will
work with the broader community to identify an organization to stand up an instance of the monitor.

In addition, the request for the [Rust client
audit](https://github.com/ossf/tac/issues/574) has been approved and funds
allocated. Trail of Bits will be completing this audit.

