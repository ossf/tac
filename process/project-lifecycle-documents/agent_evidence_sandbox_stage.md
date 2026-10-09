## Application for Agent Evidence at Sandbox stage

Agent Evidence is one project made of five repositories that share one release discipline: conformance vectors, a controlled vocabulary, admission rules and two small libraries for checking signed records about what an AI agent or an AI-assisted build actually did.

### List of project maintainers

* Sankalp Gilda, independent, @astrogilda

### Community growth plan

The project enters with one maintainer. The plan to reach three maintainers from two or more organizations:

* Independent implementers are already the project's test of itself. The vectors are written so that a verifier built from the specification alone can be scored against them, and runs by other implementers are recorded in the repository with their results, including the runs that went badly ([RUNS.md](https://github.com/probityai/agent-evidence-vectors/blob/main/RUNS.md)). Implementers who keep running the suite in their own CI are the first candidates for maintainer seats.
* Every case family is reviewed in the standards venue that owns the format it tests (in-toto attestation, the W3C agent conformance community group, OpenSSF working groups), and a reviewer who contributes a case is invited to review the next family.
* The project will hold a public call at least monthly once accepted, with notes on the sponsoring working group's list.

### Sponsor

* Sponsoring Working Group: Supply Chain Integrity WG ([ossf/wg-supply-chain-integrity](https://github.com/ossf/wg-supply-chain-integrity)). The vectors test attestation and provenance records of the kind SLSA, in-toto and gittuf produce, which is that group's ground. The AI/ML Security WG is the second home we would accept, since part of the corpus covers records written by AI agents.
* Sponsor: not yet confirmed. I am asking on the Supply Chain Integrity WG list and at its next meeting, and I ask the TAC to help identify a sponsor if none comes forward there.

The project commits to bi-annual progress updates to the sponsoring WG.

### GitHub organization

* https://github.com/probityai/agent-evidence-vectors
* https://github.com/probityai/agent-evidence-vocabulary
* https://github.com/probityai/agent-evidence-admission
* https://github.com/probityai/jcs-admit
* https://github.com/probityai/dsse
* I confirm the five repositories will be hosted under the OpenSSF GitHub Enterprise Cloud instance. One constraint goes with the move: signed records already in circulation carry predicate type URIs served from GitHub Pages under the current organization. Those URIs are inside signed bytes, so they must keep resolving to identical content after the transfer. The move plan keeps them served at their existing addresses before any repository changes hands.

### Mission of the project

Many specifications now define a signed record about software or agent behavior: build provenance, an attestation that an AI agent took an action, a receipt for a tool call. Few of them ship a corpus that a second implementation can be checked against, and two implementations of the same specification can disagree about the same bytes without anyone being able to tell which one is right.

Agent Evidence supplies that corpus. Each case is a fixed input, an expected verdict and a reason code, and every rejecting case sits beside the accepting case it differs from in one field, so a verifier that accepts everything fails and a reader who trusts neither implementer can see where they diverge. Each corpus carries a revision number and a digest over its own contents, so a reported score names exactly what it was measured against. The corpus ships as a Python package (`pip install agent-evidence-vectors==0.17.5`), a Go module and a GitHub Action, so another project's CI runs it as a pinned dependency.

The other four repositories make the corpus usable: the vocabulary defines the terms a verdict uses, the admission rules apply verdicts in OPA, Kyverno and the Sigstore policy-controller, `jcs-admit` checks JSON before RFC 8785 canonicalization, and `dsse` signs and verifies DSSE envelopes with explicit threshold and key handling.

This addresses an unfulfilled need. It extends existing OpenSSF work rather than competing with it: the cases test in-toto and DSSE records, and the project would rather contribute cases to SLSA, gittuf or model signing than duplicate them.

### Alignment with the OpenSSF MVSSR

Strategies:
* Catalyst for Change: a public conformance corpus turns "our verifier checks provenance" into a claim anyone can re-run.
* Ecosystem Leader: the corpus is already cited in in-toto attestation review and in OpenSSF Global Cyber Policy WG input to an ENISA consultation on AI-assisted development.

Pillars:
* Programs & Projects: the corpus and its Action run in other projects' CI.
* Public Policy: regulators asking for evidence of AI-assisted changes (the EU Cyber Resilience Act, the ENISA technical advisory) need test cases a relying party can run, not prose.

### IP policy and licensing due diligence

* Yes. All five repositories are Apache-2.0. I will open the IP policy and license review issue in this repository and link it here.

### Project References

| Reference           | URL |
|---------------------|-----|
| Repo                | https://github.com/probityai/agent-evidence-vectors (and the four repositories above) |
| Website             | https://probityai.github.io/agent-evidence-vectors/ |
| Contributing guide  | https://github.com/probityai/agent-evidence-vectors/blob/main/CONTRIBUTING.md |
| Security.md         | https://github.com/probityai/agent-evidence-vectors/blob/main/SECURITY.md |
| Roadmap             | https://github.com/probityai/agent-evidence-vectors/blob/main/TODO.md |
| Demos               | https://github.com/probityai/agent-evidence-vectors/tree/main/demo |
| Other               | PyPI: https://pypi.org/project/agent-evidence-vectors/ ; crates.io: https://crates.io/crates/jcs-admit , https://crates.io/crates/dsse |
