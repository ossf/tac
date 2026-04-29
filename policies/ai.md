# AI Usage in OpenSSF Technical Initiatives

This policy defines how the OpenSSF approaches the use of AI development tools in contributions to its Technical Initiatives (TIs). It covers AI-assisted and AI-autonomous contributions, disclosure expectations, maintainer review practices, and repository-level agent configuration.

AI is reshaping open source dynamics. Organizations and foundations that prohibit AI usage risk falling behind; those that accept it uncritically risk quality, security, and legal exposure. This policy takes a pragmatic middle path — permissive by default, with clear accountability expectations — while acknowledging that the landscape is evolving rapidly and that questions around contributor consent, competitive dynamics, and community norms remain open.

This is a living document. It will be reviewed periodically and updated as the AI landscape evolves (see [Review Cadence](#review-cadence)).

## Scope

This policy applies to:

- Repositories under [github.com/ossf](https://github.com/ossf) and other OpenSSF-controlled organizations
- All interaction types: pull requests, issues, review comments, discussions, and automated activity
- All contributors, regardless of organizational affiliation

This policy does **not** replace:

- Individual TI contribution guidelines (`CONTRIBUTING.md`)
- The OpenSSF [Developer Certificate of Origin (DCO)](../dco.md) requirement
- Employer-specific policies that contributors may be subject to

Individual TIs may adopt **stricter** rules than this policy (see [TI-Level Exceptions](#ti-level-exceptions)) but may not be more permissive.

## Glossary

- **AI development tools**: Copilots, agents, editors, and other tools that generate or transform code, documentation, or other project artifacts.
- **AI-assisted contribution**: Any contribution (PR, issue, comment, review) where a human used AI development tools to help produce the work, but the human directed the process and reviewed the output.
- **AI-autonomous contribution**: Any contribution produced and submitted by an AI agent acting independently, without meaningful human direction or review of the specific output.
- **Repo agent config**: Files intended to guide coding agents (e.g., `AGENTS.md`, tool config files, agent instructions).

## Guiding Principles

These five principles govern how the OpenSSF approaches AI usage in its Technical Initiatives. They apply to all participants — maintainers, contributors, and reviewers.

1. **Be transparent.** Disclose AI usage. Don't obscure how contributions were produced. Transparency builds trust with maintainers and the broader community.

2. **Take responsibility.** The human contributor owns the contribution. AI development tools don't reduce accountability for correctness, security, or licensing. "The AI wrote it" is not a defense.

3. **Demonstrate understanding.** Contributors must be able to explain what they submit. If you cannot walk through the change and justify its design, it is not ready for review.

4. **Respect maintainer time.** AI has lowered the cost of producing contributions but not the cost of reviewing them. Contributors must ensure their submissions are worth the review effort and are appropriately scoped.

5. **Engage authentically.** Interact as if you were interacting with humans, not machines. Review comments, issue discussions, and community interactions should reflect genuine human engagement.

## Disclosure of AI Usage

The OpenSSF treats AI development tools as part of a contributor's workflow, comparable to editors, linters, or language servers. Tool use itself is not something reviewers need flagged. Contributors are fully responsible for every contribution they submit (see [Contributor Responsibility for AI-Assisted Work](#contributor-responsibility-for-ai-assisted-work)), and the [Developer Certificate of Origin (DCO)](../dco.md) provides the formal accountability attestation. Within that framework, disclosure of AI tool use is **not** required by default.

Disclosure **is** required in the two cases where the normal accountability assumption breaks down:

1. **AI-autonomous contributions** (see [AI-Autonomous Contributions](#ai-autonomous-contributions)): the contribution lacks a human who directed the work and reviewed the specific output.
2. **Unreviewed AI-produced content**: the contributor is submitting AI-produced content they have not meaningfully reviewed and cannot fully explain. For example, a large generated change the contributor is asking maintainers to evaluate without having walked through it themselves.

In both cases, disclosure exists so reviewers know the standard accountability assumption does not hold for the contribution, and can adjust their review accordingly. Outside these two cases, AI tool use is treated as workflow and does not require disclosure.

### Rationale

Disclosure adds value when it tells reviewers something they need to act on. Whether a contributor used an AI tool while working on a contribution does not, on its own, change what reviewers are evaluating. The change still has to be correct, in scope, well-explained, and aligned with project standards. AI tool use is heterogeneous across contributors, and across the lifecycle of a single contribution (research, drafting, refactoring, testing, documentation). Tracking it adds noise without improving review, and works against the policy's own *Respect maintainer time* principle.

Reviewers' work will change depending on whether a human is meaningfully behind the contribution. When a contribution is AI-autonomous, or when the contributor is forwarding AI-produced content they have not reviewed, the accountability frame the project relies on (DCO, contributor responsibility, ability to engage in review) is weaker. Those are the cases where reviewers benefit from explicit signal, and where this policy requires disclosure.

This framing is consistent with the broader policy: the contributor owns the contribution, AI tool use does not reduce responsibility, and "the AI wrote it" is not a defense. It is also consistent with [RedMonk's 2026 analysis](https://redmonk.com/kholterhoff/2026/02/26/generative-ai-policy-landscape-in-open-source/) of disclosure norms across open source organizations, which describes disclosure as a mechanism for surfacing accountability concerns rather than as a tracking mechanism for tool use.

### Pull Request Disclosure

Pull request templates should include at minimum:

1. An attestation that the contributor has read and understood the project's contribution guidelines (`CONTRIBUTING.md`).
2. An attestation that the contributor has reviewed the contribution and can explain its design and tradeoffs. If any AI-produced content in the contribution has not been meaningfully reviewed by the contributor, the PR description should say so and identify which parts, so reviewers can adjust their review accordingly.

The detailed expectations around AI usage should live in `CONTRIBUTING.md`. The PR template captures the attestation; `CONTRIBUTING.md` holds the substance.

### Commit Trailers

For machine-parseable provenance tracking, two conventions exist in the ecosystem:

- `Generated-by: <tool>` — Recommended by the [Apache Software Foundation](https://www.apache.org/legal/generative-tooling.html). This is a provenance marker indicating which tool was used. It does not imply authorship.
- `Co-authored-by: <tool>` — Widely used in practice and rendered by GitHub's UI. However, this implies co-authorship, which raises unresolved questions about whether AI development tools can hold authorship or copyright.

There is no industry standard for AI commit attribution. Current behavior varies across tools: Claude Code and Aider both default to `Co-authored-by:` trailers; GitHub Copilot's coding agent co-authors commits with the developer who assigned the task; other tools (Cursor, Windsurf, OpenAI Codex) either add no attribution by default or do not document their behavior. No major AI coding agent currently defaults to `Generated-by:`.

AI provenance trailers are recommended but not required at the policy level. Individual TIs may require them through their own contribution conventions. AI provenance trailers are additive — they do not replace or conflict with DCO `Signed-off-by:` trailers. Projects using [DCO Bot](https://probot.github.io/apps/dco/) or similar enforcement tools for `Signed-off-by:` are fully compatible with AI provenance trailers.

## Contributor Responsibility for AI-Assisted Work

Contributors are fully responsible for AI-assisted contributions. They must understand, test, and be able to explain every change they submit. AI assistance does not reduce contributor responsibility. TIs should document these expectations in their `CONTRIBUTING.md`.

### Rationale

AI has lowered the cost of producing contributions but not the cost of reviewing them. Maintainers report that low-quality AI-generated submissions create significant triage burden. Holding contributors to the same standards regardless of tooling ensures review effort is respected and code, issue, and comment quality is maintained.

### Requirements

All contributors must:

- **Understand and be able to explain** every meaningful change
- Run tests and verification appropriate for the change
- Keep PRs appropriately scoped; avoid large automated PRs unless coordinated with maintainers
- Write commit messages that explain what the change does and why. AI-drafted commit messages are acceptable when the contributor has reviewed them and can stand by what they say, the same standard that applies to any AI-assisted content
- **Do not use AI to respond to review comments** — reviewers expect to engage with the human author ([Kubernetes norms](https://www.k8s.dev/docs/guide/pull-requests/))

### Legal Obligations

Contributors using AI development tools must ensure:

1. **Tool terms compatibility**: The AI development tool's terms of service do not conflict with the project's open source license or the [Open Source Definition](https://opensource.org/osd). Most major tools grant users rights to generated output, but this varies by plan and terms of service. Contributors should verify.

2. **No third-party copyrighted material**: AI-generated output does not contain copyrighted third-party code, or if it does, that code is compatible with the project's license. When pre-existing copyrighted materials are included in AI-generated output, contributors should confirm they have permission to use and modify those materials (such as an open source license or public domain declaration that complies with the project's licensing policies), provide notice and attribution of third-party rights, and include information about the applicable license terms with their contribution. Contributors should review AI output for copied or closely adapted snippets and use code scanning tools where available. Note: as the [Linux Foundation's Generative AI Policy](https://www.linuxfoundation.org/legal/generative-ai) acknowledges, reliably identifying third-party materials in AI-generated output remains a practical challenge with current tools.

3. **Reasonable assurance**: Contributors have taken reasonable steps to verify the above, whether by reviewing tool terms, scanning output, or manually reviewing generated code. These conditions ask for diligence and attestation, not proof. The framing is analogous to DCO, but the AI legal landscape (copyright in generated output, training-data provenance, derivative-work questions) is unsettled and lacks DCO's accumulated precedent and tested practice. Contributors and TIs should treat the analogy as a working framework rather than a settled equivalence.

### Recommendations

Examples of reasonable AI development tool uses include, but are not limited to: explaining existing code, generating boilerplate, improving grammar for non-native English speakers, brainstorming design alternatives, and scaffolding tests.

When existing code is used as the basis for a change (whether transformed by hand or via AI tooling), contributors should note the source in the PR description. This is a source-attribution and licensing concern and is independent of whether the contribution otherwise requires disclosure under the rules above.

## AI-Autonomous Contributions

All contributions to OpenSSF repositories must have a responsible human who directed the work and can explain and defend it. Fully autonomous AI contributions — where an agent acts independently without meaningful human oversight of the specific output — are not accepted by default.

### Rationale

Autonomous AI agents can produce high volumes of contributions without the human accountability that open source collaboration depends on. This creates disproportionate review burden, degrades signal-to-noise in issue trackers, and undermines the authentic human engagement that sustains open source communities. No step in the contribution workflow should happen without a human in the loop.

### Details

The following autonomous agent behaviors are not acceptable:

- **Automated PR submission**: Agents opening pull requests without a human reviewing and approving the specific changes before submission
- **Automated issue filing**: Agents filing bug reports or feature requests without a human verifying the issue reflects a genuine, real-world use case
- **Issue claiming**: Agents claiming issues (especially "good first issue" labels) without a human intending to personally follow through on the work
- **Automated review comments**: Agents posting unsolicited code review feedback on others' pull requests
- **Automated discussion responses**: Agents responding in issue or discussion threads without human oversight of the specific response

A human using an AI development tool to *draft* any of the above — and then reviewing, editing, and submitting the output themselves — is an **AI-assisted** contribution, not an AI-autonomous one, and is acceptable under this policy.

### Exceptions

**GitHub Apps and bots authorized through OpenSSF governance processes prior to the effective date of this policy** (e.g., Dependabot, Scorecard, CI bots) are not subject to this policy. They predate it and are governed by their own approval processes. Bots authorized on or after that date are subject to this policy and must satisfy its requirements through whatever autonomous-behavior pathway the policy provides.

Individual TIs may permit specific autonomous agent behaviors in their repositories by documenting them in `AGENTS.md`. To be valid, a permitted behavior must:

- Be scoped to specific actions, not open-ended autonomy. For example, "post a structured CI summary on PRs" is in scope; "act on PRs" is not.
- Have a named maintainer team (ideally, more than one person) accountable for the agent's outputs and for revoking access if the behavior becomes harmful
- Identify the agent's account or bot username so reviewers can recognize it in the contribution stream.
- Be revocable by any maintainer if the behavior produces low-quality, off-target, or harmful output.

Permitted autonomous behaviors do not waive DCO, contributor responsibility, or the maintainer's authority to close or revert outputs. A TI may not use this mechanism to permit categories of autonomous activity that this policy explicitly prohibits in the [Details](#details) section above.

## Maintainer Review of AI-Assisted Contributions

Maintainers should review AI-assisted contributions on technical merit and project standards. They may close contributions that are not reviewable or that impose disproportionate review cost.

### Rationale

Maintainer time is the scarcest resource in open source. AI development tools have increased the volume of contributions without increasing review capacity. Maintainers need clear authority and consistent practices for handling AI-assisted and AI-autonomous submissions efficiently.

### Reviewing Pull Requests

Suggested maintainer checklist:

- Does the PR have a clear "what/why"?
- Is it appropriately scoped?
- Do tests/verification cover the change?
- Can the author explain the design and tradeoffs?
- Has the contributor disclosed AI usage as required?
- Any license/provenance red flags? (Review AI output for copied snippets, unusual style, or comments referencing other projects)

When a PR does not meet project standards, maintainers should first engage with the contributor — ask clarifying questions, request changes, and give the contributor a chance to demonstrate understanding. If the contributor is unwilling or unable to adhere to the project's contribution standards, maintainers may close the PR with a respectful rationale (per [Kubernetes norms](https://www.k8s.dev/docs/guide/pull-requests/)). The close message should reference this policy and offer the contributor the opportunity to reopen the PR if they are willing to meet the project's expectations.

For obvious spam or fully autonomous submissions with no human behind them, immediate closure is appropriate as a defensive measure.

### Handling AI-Generated Issues and Comments

Maintainers may:

- Close AI-generated issues that lack genuine use cases or real-world context
- Remove or flag AI-generated review comments that are unsolicited or misleading
- Reclaim issues that were claimed by automated agents without follow-through

When closing or removing AI-generated content, use a respectful, consistent rationale that references this policy.

### Proactive Recommendations

- Apply the project's existing commit conventions to AI-assisted contributions the same way as any other contribution. Projects without commit conventions may consider adopting basic standards (e.g., conventional commits, "what/why" format, squash-on-merge policy).
- **Reduce the attack surface for low-quality AI contributions proactively:**
  - Keep `CONTRIBUTING.md`, `README.md`, and issue templates current — outdated or vague guidance increases the likelihood that AI agents produce off-target submissions.
  - Minimize unnecessary dependency sprawl — each dependency is an additional surface for automated "bump" or "fix" PRs.
  - Use clear, specific "good first issue" labels and remove stale ones — AI agents often target these labels for automated issue claiming.

## AGENTS.md in OpenSSF Repositories

OpenSSF repositories should include an `AGENTS.md` file to set expectations for AI agent behavior.

### Rationale

`AGENTS.md` is a tool-agnostic standard for providing instructions to AI coding agents interacting with a repository, stewarded by the [Agentic AI Foundation (AAIF)](https://aaif.io/). Adopting `AGENTS.md` serves as a mitigation tool — it sets explicit expectations for how AI agents should behave in a repo, reducing low-quality automated contributions.

### Details

OpenSSF repos should follow the [AGENTS.md specification](https://agents.md/) for file naming and placement:

- Place an `AGENTS.md` file at the repository root, consistent with other community health files (`README.md`, `CONTRIBUTING.md`, `SECURITY.md`).
- For monorepos, nested `AGENTS.md` files may be placed in subpackages — the closest `AGENTS.md` to the edited file takes precedence.

`AGENTS.md` files in OpenSSF repositories must follow these guidelines:

- **Tool-agnostic content only.** Do not reference specific vendors or products. The file should work with any AI coding agent.
- **No confidential information.** Do not include non-public architecture details, infrastructure references, or information that is not already public in the repo.
- **Project-specific instructions.** Focus on contribution standards, testing requirements, coding conventions, and review expectations specific to the project.
- **Keep it maintained.** An outdated `AGENTS.md` is worse than none — it will produce contributions that don't match current project expectations. Treat it as a living document alongside `CONTRIBUTING.md`.
- **Maintainer-controlled.** `AGENTS.md` and other agent configuration files are maintained by project maintainers. Pull requests from external contributors that modify agent configuration files require explicit maintainer review and approval. This prevents tool-specific config sprawl and keeps agent instructions consistent with the project's contribution standards, while still allowing good-faith fixes (typos, broken links, outdated commands) to be reviewed on their merits.

For security-specific agent instructions, TIs should reference the [Security-Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions) published by the OpenSSF Best Practices Working Group.

## Security Considerations

As a security-focused foundation, the OpenSSF must be particularly attentive to the security implications of AI-generated contributions. This section highlights risks and review practices specific to AI-assisted work in security-critical open source projects.

### AI-Generated Code Security Risks

AI development tools can introduce security vulnerabilities through several mechanisms:

- **Insecure code patterns**: AI models may generate code with injection flaws, insecure defaults, improper input validation, or other [OWASP Top 10](https://owasp.org/www-project-top-ten/) vulnerabilities.
- **Outdated security practices**: AI-generated code may use deprecated cryptographic algorithms, insecure random number generation, or other patterns that were acceptable when the training data was produced but are no longer considered safe.
- **Dependency risks**: AI tools may suggest unmaintained, compromised, or non-existent packages (dependency confusion / hallucinated packages), introducing supply chain risk.
- **Sensitive data exposure**: Contributors must not include secrets, credentials, or sensitive data in AI tool prompts, as this data may be logged, stored, or used for model training depending on the tool's terms of service.

### Security Review of AI-Assisted Contributions

Maintainers of OpenSSF TIs should apply heightened scrutiny to AI-assisted contributions that touch security-sensitive areas, including:

- Cryptographic implementations or configurations
- Authentication and authorization logic
- Input validation and sanitization
- Supply chain tooling (build systems, dependency resolution, artifact signing)
- Security policy files (`SECURITY.md`, vulnerability disclosure processes)

For security-critical changes, maintainers should verify that AI-generated tests are not merely testing the AI-generated implementation against itself. Domain expert review is strongly recommended for any AI-assisted changes to security-critical logic.

### Relevant OpenSSF Resources

- [AI/ML Security Working Group](https://github.com/ossf/ai-ml-security) — Addresses security challenges unique to AI/ML in open source
- [Security-Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions) — Best practices for configuring AI coding agents with security in mind
- [SAFE Framework](https://github.com/SAFE-MCP/safe-mcp) — Security framework for AI agent interactions (OpenSSF Sandbox project)

## TI-Level Exceptions

This policy establishes a permissive default for OpenSSF Technical Initiatives. Individual TIs may adopt stricter rules — up to and including a prohibition on AI-assisted contributions — if justified by the TI's risk profile.

### Dimensions

"Stricter" rules are rules that raise requirements along one or more of the following dimensions, without weakening any other dimension below this policy's defaults:

- **Disclosure**: requiring disclosure of AI tool use beyond the cases this policy requires.
- **Autonomous contributions**: prohibiting categories of autonomous activity, or applying tighter constraints to autonomous behaviors that would otherwise be permitted.
- **Review process**: requiring additional review steps for AI-assisted contributions (e.g., two-maintainer approval, mandatory domain-expert sign-off for security-critical changes).
- **Provenance**: requiring `Generated-by:` or other provenance trailers that this policy treats as optional.
- **Scope of AI use**: prohibiting AI tool use in specific code areas (e.g., cryptography, authentication) or in the project as a whole.
- **Verification**: requiring specific verification practices for AI-assisted output (e.g., mandatory code scanning for copied snippets, mandatory end-to-end test runs).

Rules that weaken any dimension below this policy's defaults (for example, waiving DCO sign-off for AI-assisted commits, or accepting autonomous contributions this policy prohibits) are not "stricter" rules and may not be adopted at the TI level.

### Criteria

Criteria that may justify stricter rules:

- **Security-critical code**: Cryptography, authentication, access control, or code that directly handles secrets
- **Infrastructure code**: Code that runs in production environments where bugs have outsized impact
- **Regulatory or compliance requirements**: Projects subject to specific regulatory obligations
- **Maintainer capacity constraints**: Projects where the maintainer team has explicitly documented that AI-assisted contribution volume exceeds review capacity

### Process

1. TI leads propose the exception with a documented rationale, submitted as a PR to this repository.
2. The PR is reviewed per the [TAC Decision Process](../process/TAC-Decision-Process.md) as a Content-type decision (72h review, 3 approvers).
3. Approved exceptions must be documented in the TI's `CONTRIBUTING.md` so contributors can see the rules before submitting.
4. Exceptions include a review date (maximum 12 months from approval) at which point the exception must be renewed or it lapses.

## Review Cadence

This policy will be reviewed on at least an annual basis. Reviews may also be triggered by significant changes in the ecosystem.

### Review Triggers

- **Legal developments**: Court rulings or regulatory changes affecting AI-generated code, copyright, or licensing
- **Foundation guidance changes**: Updates to AI contribution guidance by major foundations (Linux Foundation, CNCF, TODO Group, Apache Software Foundation)
- **New AI capabilities**: Emergence of materially new AI development tool capabilities (e.g., fully autonomous agents, new interaction modes) that affect the assumptions in this policy
- **Community incidents**: Significant incidents involving AI-generated contributions in any open source ecosystem that reveal gaps in current guidance
- **TI feedback**: Patterns reported by OpenSSF TI maintainers that suggest this policy needs adjustment

Review outcomes are documented as updates to this policy document. Changes that modify requirements follow the [TAC Decision Process](../process/TAC-Decision-Process.md) (Content type for requirement changes, Editorial for clarifications).

## References

This policy draws from the following sources:

- [Linux Foundation: Generative AI Policy](https://www.linuxfoundation.org/legal/generative-ai) — Foundation-level guidance on AI-generated contributions, tool terms compliance, and third-party content attribution obligations
- [Apache Software Foundation: Generative Tooling Guidance](https://www.apache.org/legal/generative-tooling.html) — Contributor obligations for AI-generated code (tool terms, third-party materials, reasonable assurance), `Generated-by:` trailer convention
- [Kate Holterhoff / RedMonk: The Generative AI Policy Landscape in Open Source](https://redmonk.com/kholterhoff/2026/02/26/generative-ai-policy-landscape-in-open-source/) — Survey of 73 open source organizations' AI guidance; framework for stance, concern dimensions, and disclosure conventions
- [Kubernetes contributor guide: pull requests](https://www.k8s.dev/docs/guide/pull-requests/) — Author responsibility, explainability, discouraging AI-generated commit messages, allowing closure of unreviewable PRs
- [Probabl / scikit-learn maintainers: Maintaining Open Source in the Age of Gen AI](https://blog.probabl.ai/maintaining-open-source-age-of-gen-ai) — Maintainer burden, categories of problematic AI contributions, `AGENTS.md` as mitigation
- [Scientific Python community: Community Considerations Around AI Contributions](https://blog.scientific-python.org/scientific-python/community-considerations-around-ai/) — Guidelines on transparency, responsibility, understanding, and authentic engagement
- [AGENTS.md specification](https://agents.md/) — Standard format and placement for AI coding agent instructions
- [Agentic AI Foundation (AAIF)](https://aaif.io/) — Stewards the AGENTS.md standard under the Linux Foundation
- [OpenSSF: Security-Focused Guide for AI Code Assistant Instructions](https://best.openssf.org/Security-Focused-Guide-for-AI-Code-Assistant-Instructions) — Security best practices for AI coding agent configurations
- [OpenSSF AI/ML Security Working Group](https://github.com/ossf/ai-ml-security) — Working group addressing AI/ML security in open source
- [OpenSSF Developer Certificate of Origin](../dco.md) — DCO requirement for OpenSSF contributions
- [OpenSSF TAC Decision Process](../process/TAC-Decision-Process.md) — Governance process for policy changes
