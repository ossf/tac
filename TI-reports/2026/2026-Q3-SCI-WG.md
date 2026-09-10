# 2026 Q3 Supply Chain Integrity (SCI) WG

## **Overview**

**Mission**: Scalable standardized attestable practices for supply chain security

**Key Resources**

* [Vision Doc](https://docs.google.com/document/d/1SuJHaCr89Ih6TFvAIH2WM5M4_MlXwM8mqHynUBuungE/edit?resourcekey=0-wg-QROzZFa4Ju_uN_wOBNQ) and [Charter](https://github.com/ossf/wg-supply-chain-integrity/blob/main/governance/CHARTER.md)
* [GitHub](https://github.com/ossf/wg-supply-chain-integrity)
* [Mailing List](https://lists.openssf.org/g/openssf-supply-chain-integrity)
* [Slack](https://app.slack.com/client/T019QHUBYQ3/C01A1MA7A1K)
* [Meeting Notes](http://ssci.io/sci-notes)

**tl;dr**: AMPEL, Darnit, and BOMHort landed as sandbox projects. The WG's central initiative of driving adoption of OpenSSF architecture and tooling by open source projects outside the OpenSSF has produced almost no engagement, and the corresponding ask to the GB/GC has not gained traction. Michael Lieberman is stepping down as co-chair.

**Headlines**:

* Three new sandbox projects accepted: **AMPEL**, **Darnit**, **BOMHort**.
* External OSS adoption initiative is stalled; ambassador-driven outreach has not produced pilots.
* Ask to the GB/GC (one non-OpenSSF OSS project per GB member + 2 eng hours/month) needs engagement.
* **Michael Lieberman is stepping down as co-chair.**

## **External OSS Adoption Initiative**

### Purpose

Drive adoption of OpenSSF architecture, best practices, and tooling by open source projects that live *outside* the OpenSSF — to validate the work in real environments, generate credible reference deployments, and pull structured feedback back into the WG's projects.

### Current Status

The initiative has gone poorly. Concretely:

* **Almost no engagement from prospective adopters.** Despite direct outreach, we have not landed active pilots with non-OpenSSF projects.
* **Adopter feedback points at a real gap.** Projects we've spoken with cite the lack of clear, end-to-end adoption guides — "what do I actually do, in what order, and what do I get" - as a blocker to committing engineering time.
* **The ambassador program has not moved the needle.** Many of our ambassadors are relatively new to open source and don't have strong pre-existing relationships with maintainers of external projects they can bring in to pilot the work.
* **Attendance is very low.** We are seeing attendance of less than 5 people on average in the meetings.

### Ask to the GB / GC (unresolved)

We have asked the Governing Board and Governance Committee for:

* **One non-OpenSSF open source project per GB member** to be brought forward as a pilot adopter.
* **Two engineering hours per month, per project**, so that OpenSSF community members can work directly with those projects on onboarding to OpenSSF architecture, best practices, and tooling — and so those projects can give us structured feedback in return.

We have not gotten meaningful traction on this ask. Without either (a) named projects to work with or (b) committed engineering time, the initiative does not have a viable path forward in its current form.

### Up Next

* Formal co-chair transition (see below).
* Revisit the initiative's scope and shape under new leadership — including whether adoption should be pursued as a top-line WG goal at all if the GB/GC cannot commit projects and engineering time.
* Continue to invest in adoption *guides* regardless of leadership outcome, since that is the most consistent piece of feedback from external projects.

### Questions/Issues for the TAC

* How does the TAC want to handle the follow-up conversation with the GB/GC on the adoption ask? Absent a response there, the WG cannot realistically deliver on the external adoption goal.
* Guidance on scope refresh in light of the co-chair transition.

## **Leadership Transition**

Michael Lieberman is stepping down as co-chair of the Supply Chain Integrity WG. The primary driver is the lack of traction on the external OSS adoption push despite sustained effort, both on the community side and in trying to secure GB/GC commitment, and a resulting need for fresh leadership to reassess the WG's focus.

The remaining co-chairs continue in their roles. The WG will need to open a discussion on filling the seat and on refreshing scope; that discussion should be coordinated with the TAC.

## **Sandbox Projects**

Three projects landed as OpenSSF sandbox projects under the SCI WG this quarter:

* **AMPEL** — Policy enginer for attestations
* **Darnit** — Agentic harness for adoption of security best practices
* **BOMHort** — SBOM Aggregator

## **SLSA**

### Purpose

A pragmatic supply chain security framework covering key functional areas, and providing for improved comprehension and security of software supply chains.

### Current Status

Current focus is on dependency track. This track's purpose is in providing provenance and transparency into the trust of ingested dependencies.

Next generation of SLSA tools are still being developed.

### Up Next

Finish dependency track and reference tooling

### Questions/Issues for the TAC

We could use more feedback on the dependency track.

## **GUAC**

### Purpose

Observability for the software supply chain

### Current Status

<!-- TODO -->

### Up Next

<!-- TODO -->

### Questions/Issues for the TAC

None

## **gittuf**

### Purpose

Verifiable security governance for git-based source repositories

### Current Status

<!-- TODO -->

### Up Next

Working with source forges to adopt gittuf

### Questions/Issues for the TAC

None

## **Zarf**

### Purpose

Secure Software Delivery for connected and disconnected systems

### Current Status

<!-- TODO -->

### Up Next

<!-- TODO -->

### Questions/Issues for the TAC

None
