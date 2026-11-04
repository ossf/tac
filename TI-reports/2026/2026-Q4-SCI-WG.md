# 2026 Q4 Supply Chain Integrity (SCI) WG

## Overview

**Mission**: [Scalable standardized attestable practices for supply chain security][mission]

**Key Resources**:

* [Charter][charter]
* [GitHub][sci-gh]
* [Mailing List][list]
* [Slack][slack]
* [Meeting Notes][notes]

**tl;dr**: Charter v2.0 ([wg-supply-chain-integrity#86][pr86]) is open as a draft, and we're bringing the
TAC an early look at work to reorg the WG and rescoping plans. Stephen Augustus and Adolfo García Veytia
joined Nicole Bates and Justin Cappos as co-chairs. SLSA merged Build Level 4 into its draft spec, and
gittuf, Zarf, Trustify, AMPEL, and Darnit cut releases. BOMHort has moved to the SBOM & VEX WG.

**Health**: Meeting attendance is low: the four meetings since September 1 averaged about five named
attendees ([notes][notes]). We'll work to improve that with a concerted outreach effort to all existing
Technical Initiatives. Distinct human authors of merged PRs, 2026-07-01 to 2026-10-16:

| Project | Authors |
| --- | --- |
| SLSA | 10 |
| GUAC (core 14, Trustify 25) | 39 |
| gittuf | 21 |
| Zarf | 27 |
| AMPEL | 3 |
| Darnit | 11 |

**Project sections are pending confirmation from each project's maintainers**, who are asked to confirm or
correct them on this PR.

## Reorg and rescoping

### Purpose

Reorg the WG and rescope its work.

### Current Status

* Charter v2.0 ([#86][pr86]) is open as a draft, with review feedback still to address. The charter's
  focus will move to maintainer enablement and external engagement, aligned with the Governing Board's
  priorities (GB P1).
* We've had discussions about bringing the Security Architecture group into the WG.
* We're working with the Ambassadors group on how to coordinate maintainer feedback.
* The external OSS adoption initiative and the GB/GC ask, both reported as stalled in Q3, will be
  reconsidered as part of the rescoping, including @gkunz's suggestion of an OpenSSF-wide, Security
  Slam-style activity ([#642][tac642-gkunz]).

### Up Next

* Revise charter v2.0 around maintainer enablement and external engagement.
* Outreach to all existing Technical Initiatives to grow meeting participation.
* Bring the reorg and rescoping plans to the TAC.

### Funding requests and updates

None.

### Questions/Issues for the TAC

* Feedback on the reorg and rescoping plans. The VD, SCI, and SBOM/VEX WG scope boundaries
  ([ossf/tac#660][tac660]) feed into them.
* The WG has no TAC Sponsor ([README][sci-readme]). Is a TAC member willing to sponsor it?

## Leadership

[#90][pr90] (merged 2026-09-11) added Stephen Augustus and Adolfo García Veytia as co-chairs and removed
Michael Lieberman. The chairs are Nicole Bates, Justin Cappos, Stephen Augustus, and Adolfo García Veytia
([README][sci-readme]).

## SLSA

### Purpose

A pragmatic supply chain security framework covering key functional areas, and providing for improved
comprehension and security of software supply chains.

### Current Status

* **Spec:** the dependency track merged as a Working Draft ([slsa#1627][slsa1627], [slsa#1648][slsa1648]),
  and Build Level 4 ("dependencies complete") merged into the draft spec ([slsa#1646][slsa1646]).
* **Tooling:** `slsa-verifier` and `slsa-github-generator` are no longer actively maintained and point
  users to GitHub artifact attestations. Their successors, [`verifier`][slsa-verifier] and
  [`attester`][slsa-attester], released v0.1.0 on 2026-10-04.
* **Adoption:** SLSA v1 provenance generation merged into the Kubernetes release process.
* **Governance:** the 2026 Steering Committee was seated ([governance#35][slsa-gov35]).

### Up Next

* Dependency track review ([draft][slsa-dep]).
* Admit `verifier` as a Core project ([slsa#1641][slsa1641]) and finish the tooling move-in
  ([slsa#1647][slsa1647]).
* A v1.3 release cut ([slsa#1635][slsa1635]).

### Funding requests and updates

Interest in AI credits on [ossf/tac#661][tac661].

### Questions/Issues for the TAC

Feedback on the [dependency track draft][slsa-dep].

## GUAC

### Purpose

Observability for the software supply chain

### Current Status

* **GUAC core:** `main` gained CycloneDX 1.7 support, new certifiers, and Postgres deadlock fixes
  ([merged PRs][guac-prs]).
* **Trustify:** v0.5.0 through v0.7.0 ([releases][trustify-rel]). v0.7.0 adds CycloneDX 1.7, CSAF
  validation, and post-quantum crypto policy evaluation for CBOM assets.
* **Maintainers:** Gagan H R joined GUAC core ([governance#106][guac-gov106]) and Jeff Mendoza moved to
  emeritus ([governance#108][guac-gov108]). James Fuller joined Trustify ([governance#104][guac-gov104]).

### Up Next

A safety-relevance adapter (SRAC) for ingesting product-specific safety assertions.

### Funding requests and updates

None.

### Questions/Issues for the TAC

None.

## gittuf

### Purpose

Verifiable security governance for git-based source repositories

### Current Status

* **Releases:** [v0.16.0][gittuf-0160] added SHA-256 repository support. [v0.17.0][gittuf-0170] added
  faster Sigstore verification and an experimental go-git backend.
* **Advisories:** [GHSA-qc8j-pcph-6q9x][gittuf-ghsa1] (medium, fixed in v0.16.0) and
  [GHSA-774m-m728-236h][gittuf-ghsa2] (low, fixed in v0.17.0).
* **Maintainers:** Paulo Gomes joined as a maintainer and Neil Naveen moved to emeritus. A new reviewer
  role was added ([MAINTAINERS.txt][gittuf-mt], [community#24][gittuf-comm24]).

### Up Next

* Working with source forges to adopt gittuf.
* Hash agility (GAP-1): prototype options for moving from SHA-1 to SHA-256.

### Funding requests and updates

The [ossf/tac#608][tac608] security audit, a prerequisite for leaving beta, was approved in July 2026.
Status: pending gittuf.

### Questions/Issues for the TAC

None.

## Zarf

### Purpose

Secure Software Delivery for connected and disconnected systems

### Current Status

* **Releases:** v0.81.0 through v0.88.0 ([releases][zarf-rel]). v0.87.0 added component signing and
  verification.
* **Design proposals:** ZEP-0051 (v1beta1 schema), ZEP-0048 (API version support policy), ZEP-0021, and
  ZEP-0026 updates merged ([proposals][zarf-zeps]).

### Up Next

v1.0.0, targeted for 2026-11-09 ([milestone][zarf-m59]).

### Funding requests and updates

The GoReleaser Pro renewal ([ossf/tac#475][tac475]), shared with Sigstore, passed in July 2026.

### Questions/Issues for the TAC

None.

## AMPEL

### Purpose

Policy engine for attestations

### Current Status

* **Repository:** moved to [`policylabs/ampel`][am-repo], with key supporting libraries.
* **Releases:** v1.3.2 through [v1.4.2][am-142], adding SPDX 3 support.
* **IP review:** no TAC IP/license review issue yet ([project lifecycle][lc-ip]).

### Up Next

Move the CEL runtime to v1.

### Funding requests and updates

None.

### Questions/Issues for the TAC

None.

## Darnit

### Purpose

Agentic harness for adoption of security best practices

### Current Status

* **Governance:** moved to [`darnitdevorg/darnit`][dn-repo] and adopted an LF Projects technical charter
  ([CHARTER.md][dn-charter]).
* **Releases:** v0.1.0 and v0.1.1, the first releases ([releases][dn-rel]).
* **Advisory:** [GHSA-96qw-w4fw-5hcm][dn-ghsa] (high), fixed in v0.1.1.
* **IP review:** no TAC IP/license review issue yet ([project lifecycle][lc-ip]).

### Up Next

* RFC-0001, a core rearchitecture ([RFC][dn-rfc]).
* Adopt an AI policy.

### Funding requests and updates

Interest in AI credits on [ossf/tac#661][tac661].

### Questions/Issues for the TAC

None.

## Additional Information

* BOMHort has moved to the SBOM & VEX WG. The TAC [README](https://github.com/ossf/tac/blob/main/README.md)
  still lists SCI as its sponsor.
* OpenBao asked on 2026-09-23 whether SCI could serve as its WG; that request is open ([notes][notes]).
* [ossf/tac#671][tac671] (2027 mentorship pilot) lists SCI, gittuf, Zarf, and Darnit for mentees.

[am-142]: https://github.com/policylabs/ampel/releases/tag/v1.4.2
[am-repo]: https://github.com/policylabs/ampel
[charter]: https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md
[dn-charter]: https://github.com/darnitdevorg/darnit/blob/main/CHARTER.md
[dn-ghsa]: https://github.com/darnitdevorg/darnit/security/advisories/GHSA-96qw-w4fw-5hcm
[dn-rel]: https://github.com/darnitdevorg/darnit/releases
[dn-repo]: https://github.com/darnitdevorg/darnit
[dn-rfc]: https://github.com/darnitdevorg/darnit/blob/main/docs/rfcs/0001-core-rearchitecture.md
[gittuf-0160]: https://github.com/gittuf/gittuf/releases/tag/v0.16.0
[gittuf-0170]: https://github.com/gittuf/gittuf/releases/tag/v0.17.0
[gittuf-comm24]: https://github.com/gittuf/community/pull/24
[gittuf-ghsa1]: https://github.com/gittuf/gittuf/security/advisories/GHSA-qc8j-pcph-6q9x
[gittuf-ghsa2]: https://github.com/gittuf/gittuf/security/advisories/GHSA-774m-m728-236h
[gittuf-mt]: https://github.com/gittuf/gittuf/blob/main/MAINTAINERS.txt
[guac-gov104]: https://github.com/guacsec/governance/pull/104
[guac-gov106]: https://github.com/guacsec/governance/pull/106
[guac-gov108]: https://github.com/guacsec/governance/pull/108
[guac-prs]: https://github.com/guacsec/guac/pulls?q=is%3Apr+is%3Amerged+merged%3A%3E%3D2026-07-01
[lc-ip]: https://github.com/ossf/tac/blob/main/process/project-lifecycle.md#ip-policy-and-license-review
[list]: https://lists.openssf.org/g/openssf-supply-chain-integrity
[mission]: https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md#mission
[notes]: http://ssci.io/sci-notes
[pr86]: https://github.com/ossf/wg-supply-chain-integrity/pull/86
[pr90]: https://github.com/ossf/wg-supply-chain-integrity/pull/90
[sci-gh]: https://github.com/ossf/wg-supply-chain-integrity
[sci-readme]: https://github.com/ossf/wg-supply-chain-integrity/blob/main/README.md#governance
[slack]: https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K
[slsa-attester]: https://github.com/slsa-framework/attester/releases/tag/v0.1.0
[slsa-dep]: https://slsa.dev/spec/draft/dependency-track
[slsa-gov35]: https://github.com/slsa-framework/governance/pull/35
[slsa-verifier]: https://github.com/slsa-framework/verifier/releases/tag/v0.1.0
[slsa1627]: https://github.com/slsa-framework/slsa/pull/1627
[slsa1635]: https://github.com/slsa-framework/slsa/pull/1635
[slsa1641]: https://github.com/slsa-framework/slsa/issues/1641
[slsa1646]: https://github.com/slsa-framework/slsa/pull/1646
[slsa1647]: https://github.com/slsa-framework/slsa/issues/1647
[slsa1648]: https://github.com/slsa-framework/slsa/pull/1648
[tac475]: https://github.com/ossf/tac/issues/475
[tac608]: https://github.com/ossf/tac/issues/608
[tac642-gkunz]: https://github.com/ossf/tac/pull/642#discussion_r3913082361
[tac660]: https://github.com/ossf/tac/issues/660
[tac661]: https://github.com/ossf/tac/issues/661
[tac671]: https://github.com/ossf/tac/issues/671
[trustify-rel]: https://github.com/guacsec/trustify/releases
[zarf-m59]: https://github.com/zarf-dev/zarf/milestone/59
[zarf-rel]: https://github.com/zarf-dev/zarf/releases
[zarf-zeps]: https://github.com/zarf-dev/proposals/pulls?q=is%3Apr+is%3Amerged
