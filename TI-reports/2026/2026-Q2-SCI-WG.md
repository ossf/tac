# 2026 Q2 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**

* [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) (Not updated in a while) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)
* [GitHub](https://github.com/ossf/wg-supply-chain-integrity); 23 contributors (**–**)
* [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity); 182 members (**–**)
* [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K); 980 members (**–**)
* [Meeting Notes](http://ssci.io/sci-notes); approx. 5–10 attendees per meeting (**▼**)

**tl;dr**: Meeting attendance has continued to decline. The new co-chairs are raising a question to the TAC about whether the SCI WG's current scope is still the right shape, or whether the WG should refocus (e.g., on adoption of SCI projects by maintainers) or wind down. The sub-projects (SLSA, GUAC, Zarf, gittuf) continue to make independent progress.

**Headlines**:

* WG:
  * Meeting attendance has fallen off significantly this quarter.
  * Co-chairs are raising an open question to the TAC on the WG's future direction — see **Questions/Issues for the TAC** below.
* SLSA:
  * Dependency Track likely to split — the attestable portion stays in SLSA, non-attestable best-practices portion likely moves to ORBIT WG.
  * SLSA tooling in a rough spot; exploring a refresh toward more generic (non-GitHub-specific) tooling.
  * Steering committee and maintainer turnover; building out a new strategic vision.
* GUAC:
  * Quiet quarter; Kusari maintainers are pulling back significantly with limited capacity to continue, though non-maintainer contributions to guacsec/guac are up.
* Zarf:
  * v1.0.0 scoped and underway; keyless signing + offline verification landed; v1beta1 package schema proposal approved.
* gittuf:
  * v0.14.1 released; v0.15.0 in flight with UX focus; v1.0.0 promotion to stable raised in priority.
* SBOMit:
  * Prototype working using eBPF; upstream patches ready for Syft, Trivy, and Witness; ~30 SBOMit-derived SBOMs produced.

### Questions/Issues for the TAC

The SCI WG's current scope is quite broad, and in practice recent meetings have largely been status updates from the sub-projects rather than working-group-level work. Combined with declining attendance, the co-chairs feel the WG is "grasping at straws" to find substantive WG-level work that isn't just rolling up project updates.

We'd like to raise this with the TAC as an open question on the WG's future. A few possibilities we see:

1. **Archive the WG.** Most of the sub-projects (SLSA graduated; GUAC, Zarf, gittuf operating largely independently) no longer need the WG as an umbrella. The WG could wind down and the sub-projects continue as standalone TIs.
2. **Refocus the WG on adoption.** Adam (@Puerco) raised the idea of repositioning SCI around adoption of SCI-group projects by *maintainers* — analogous to how ORBIT's Launchpad effort is focused on adoption by *manufacturers*. This would give the WG a concrete, non-status-update mission.
3. **Pause meetings.** Stop running regular meetings for a quarter or two while sub-projects continue, and revisit.

We'd appreciate TAC guidance on which (if any) of these the WG should pursue.

## **SLSA**

### Purpose

A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.

### Current Status

* **Dependency Track:** the track is likely to be split — the attestable portion will remain a SLSA dependency track, while the non-attestable best-practices portion will likely move to the ORBIT WG in some capacity.
* **SLSA tooling:** in a rough spot. There is a desire to refresh the tooling story, potentially by building something more generic rather than the current GitHub-specific tooling.
* **Governance:** turnover on the SLSA steering committee and across the list of maintainers.

### Up Next

* Building out a new strategic vision for SLSA in light of the dependency-track split, tooling refresh, and leadership turnover.

### Funding Requests

* None

### Questions/Issues for the TAC

* None

## **GUAC**

### Purpose

Observability for the software supply chain

### Current Status

* Increase in non-maintainer contributions to `guacsec/guac` this quarter, primarily small feature additions.
* Several regular Trustify releases in March and April; none so far in May.
* Kusari maintainers are pulling back significantly and have limited capacity to continue working on GUAC.

### Up Next

* Roadmap is business-as-usual.

### Funding Requests

* None

### Questions/Issues for the TAC

* None

## **Zarf**

### Purpose

Secure Software Delivery for connected and disconnected systems

### Current Status

* [v1.0.0](https://docs.zarf.dev/roadmap) scoped and underway.
* Packages can now be signed with keyless signing and verified offline.
* Package Values now support standard import composition.
* Development of the next package schema (v1beta1) proposal has been approved.

### Up Next

* Package Values support continuing for schema definitions, imports, and new ComponentConfigs.
* Development of a new v1beta1 package schema.
* Package signing and verification enhancements for keyless signing user experience.
* Dependency vendoring, audit and reduction planned where possible.
* Security and deprecation policy updates.

### Funding Requests

* No funding requests at this time.

### Questions/Issues for the TAC

* No questions or issues for the TAC at this time.

## **gittuf**

### Purpose

Verifiable security governance for git-based source repositories

### Current Status

* v0.14.1 released.
* Talk given at OpenSSF Community Day NA 2026.
* Discussions ongoing with projects that are interested in deploying gittuf, particularly those with strong threat models.
* Work continues on improving the UX, especially for getting started with gittuf.

### Up Next

* v0.15.0 release upcoming, focused on various UX improvements.
* v1.0.0 and promotion to full release/stable from beta has been increased in priority.
* Summer mentees start June 1st and will work on various parts of the project. By the end of the program, we hope to have substantial improvements in how easy it is to get started with and manage gittuf.

### Funding Requests

* None at this time.

### Questions/Issues for the TAC

* None at this time.

## **SBOMit**

### Purpose

Make SBOMs actually accurate by collecting attestations during the build process, eliminating "unknown unknowns" where something is missing from the SBOM.

### Current Status

* Working prototype using eBPF and related techniques.
* Giving talks and demos to various groups (CRA WG, Microsoft, PyCon, etc.).
* Upstream patches ready for Syft and Trivy.
* Attestation patches upstreamed to Witness.
* Demo site created for attestation upload.
* Provided accuracy comparisons against other SBOM tools.
* Created SBOMit-derived SBOMs for ~30 projects to date.

### Up Next

* Land the patches upstream in Witness, Syft, and Trivy.
* Integrate with SeeBOM (hoping to meet with @Jeffrey Sica this week).
* Possibly move to Incubating — waiting to understand OpenSSF / CNCF plans for SeeBOM, etc.
* More comparisons / validation:
  * Will provide SBOMit SBOMs for any project on request (Zephyr is next in the queue).
  * Happy to have external parties run comparisons as well.

### Funding Requests

* No funding requests at this time, though some outside evaluation could be useful.

### Questions/Issues for the TAC

* What questions would TAC members have before adopting SBOMit in their org? What should we focus on? We feel like we're reaching the end of the "known" improvements for the project and would value direction on where to push next.

## **Security Insights**

Moved to the ORBIT WG in Q1 2026 — no longer tracked here.
