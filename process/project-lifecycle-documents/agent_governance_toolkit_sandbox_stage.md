## Application for creating a new project at Sandbox stage

### List of project maintainers
The project must have a minimum of three maintainers with a minimum of two different organizational affiliations.
  * Imran Siddique, Microsoft, @imran-siddique (466 commits, project creator and lead)
  * Jack Batzner, Microsoft, @jackbatzner (31 commits, trusted contributor)
  * @lawcontinue, Independent, (9 commits, external contributor)
  * @kanish5, Independent, (8 commits, external contributor)
  * @tomjwxf, Independent, (8 commits, external contributor)

Note: While the project originated at Microsoft, it has 20+ contributors from multiple organizations. We are actively working to formalize community maintainer roles to further diversify organizational affiliation as part of OpenSSF onboarding.

### Sponsor
Most projects will report to an existing OpenSSF Working Group, although in some cases a project may report directly to the TAC. The project commits to providing quarterly updates on progress to the group they report to.
  * AI/ML Security WG

The Agent Governance Toolkit directly addresses the security challenges of AI agent systems, which aligns with the AI/ML Security Working Group's mission. The toolkit provides runtime governance, policy enforcement, and security tooling specifically designed for agentic AI workloads.

As a secondary fit, the project also aligns with:
  * Supply Chain Integrity WG: The toolkit includes SBOM generation, Sigstore signing, build provenance attestation, and supply chain verification for AI agent deployments.
  * Security Tooling WG: The toolkit provides reusable security tools (pre-commit hooks, GitHub Actions, CI workflows) that can benefit the broader open source security ecosystem.

### Mission of the project
The project must be aligned with the OpenSSF mission and either be a novel approach for existing areas, address an unfulfilled need, or be initial code needed for OpenSSF WG work. It is preferred that extensions of existing OpenSSF projects collaborate with the existing project rather than seek a new project.

The Agent Governance Toolkit addresses an unfulfilled need in the open source security ecosystem: **runtime governance and security enforcement for autonomous AI agents**.

AI agent frameworks (Microsoft Agent Framework, LangChain, CrewAI, Google ADK, OpenAI Agents SDK) enable agents to call tools, spawn sub-agents, and take real-world actions. However, the existing open source security tooling ecosystem lacks comprehensive runtime security models for these workloads:

- **No policy enforcement**: Agents can call any tool with any arguments without authorization checks
- **No identity verification**: Agents cannot prove who they are to each other or to the services they consume
- **No execution isolation**: A compromised agent can access resources beyond its intended scope
- **No reliability engineering**: No SLOs, error budgets, or chaos testing specifically designed for agent workloads

The OWASP Agentic Security Initiative (ASI) Top 10 codifies these risks. The Agent Governance Toolkit addresses 10 of 10 ASI risks with working, tested implementations.

**Why this is novel and not an extension of existing OpenSSF projects:**

The Agent Governance Toolkit operates at a different layer than existing OpenSSF projects:
- **SAFE-Framework** (OpenSSF Sandbox): Catalogs agentic failure modes and provides mitigation guidance. AGT provides the runtime enforcement engine that implements those mitigations. The projects are complementary, not competing.
- **Model Signing** (OpenSSF Sandbox): Focuses on ML model integrity verification. AGT uses model provenance as one input to its trust scoring system but focuses on runtime agent behavior governance.
- **Sigstore** (OpenSSF Graduated): AGT uses Sigstore for release signing and build provenance. AGT extends supply chain integrity into the agent runtime, tracking not just code provenance but agent identity and behavioral provenance.
- **SLSA**: AGT generates SLSA build provenance attestations for its own releases and provides tooling to help AI agent deployments achieve SLSA compliance.
- **Scorecard**: AGT has integrated Scorecard into its CI/CD pipeline and scores actively. The governance toolkit extends the "shift-left security" philosophy from code repositories to AI agent runtime.

We are committed to collaborating with existing OpenSSF projects rather than duplicating their work. For example, AGT already integrates Sigstore for signing, uses the OpenSSF Best Practices badge criteria as a quality baseline, and runs Scorecard assessments.

**Key capabilities:**

| Package | Description | Tests |
|---------|------------|-------|
| Agent OS Kernel | Core governance kernel: policy engine, capability model, audit logging, syscall interception, MCP gateway | 2,500+ |
| AgentMesh | Inter-agent trust: Ed25519 DID identity, SPIFFE/SVID credentials, trust scoring (0-1000), A2A/MCP/IATP protocol bridges | 1,600+ |
| Agent Runtime | Execution isolation: 4-tier privilege rings (Ring 0-3), saga orchestration, kill switch, Shapley-value fault attribution | 326 |
| Agent SRE | Reliability engineering: SLO engine, error budgets, chaos testing, progressive delivery, anomaly detection | 1,071+ |
| Agent Compliance | Compliance framework: OWASP ASI mapping, regulatory frameworks (EU AI Act, ISO 42001, Singapore MGF, CSA ATF) | 200+ |

Total: 9,500+ automated tests across all packages. Multi-language SDKs: Python, TypeScript, .NET, Rust, Go.

**OWASP Agentic Security Initiative Top 10 Coverage:**

| Risk | ID | Coverage | Component |
|------|----|----------|-----------|
| Agent Hijacking | ASI-01 | Covered | Policy Engine: blocked patterns, content safety |
| Tool Misuse | ASI-02 | Covered | Capability Sandbox: tool allow/deny, rate limits |
| Insecure Identity | ASI-03 | Covered | AgentMesh: DID identity, IATP, SPIFFE certs |
| Supply Chain | ASI-04 | Covered | SBOM generation, Sigstore signing, build provenance |
| Insecure Output | ASI-05 | Covered | Runtime: execution rings, output validation |
| Memory Poisoning | ASI-06 | Covered | VFS + CMVK (content-addressable memory) |
| Insufficient Monitoring | ASI-07 | Covered | Agent SRE: SLOs, OTel export, anomaly detection |
| Error Handling | ASI-08 | Covered | Circuit breakers, saga compensation, error budgets |
| HITL Bypass | ASI-09 | Covered | Approval workflows, human-in-the-loop gates |
| Uncontrolled Autonomy | ASI-10 | Covered | Kill switch, resource limits, goal drift detection |

### Alignment with the OpenSSF MVSSR
The mission of the Project must be aligned with the Mission, Vision, Values, Strategy, and Roadmap (MVVSR) of the OpenSSF. Please indicate to which of the three strategies and four pillars of the OpenSSF the Project contributes to.

Strategies:

**i) Catalyst for Change**: The Agent Governance Toolkit introduces a new paradigm: treating AI agent security as a first-class concern at the same level as traditional software security. Just as OpenSSF championed SBOM, supply chain integrity, and scorecard for traditional software, AGT brings these same principles to the emerging AI agent ecosystem. The toolkit demonstrates that governance can be deterministic, enforceable, and external to the agent, establishing new best practices for an entirely new class of software.

**ii) Educate and Empower the Modern Developer**: The toolkit includes 45+ tutorials covering every aspect of agent governance, from basic policy writing to advanced multi-agent trust networks. It provides pre-commit hooks, GitHub Actions, and CI workflow templates that developers can adopt incrementally. The shift-left governance approach (catch violations at commit time, not runtime) directly empowers developers to build secure agents from the start.

**iii) Ecosystem Leader**: The toolkit integrates with 12+ agent frameworks (Microsoft, Google, OpenAI, Anthropic, open-source) and has active proposals with 4 standards bodies (OWASP ASI, CoSAI/OASIS, LF AI and Data, CSA ATF). It provides a vendor-neutral governance layer that works across the entire agentic AI ecosystem, positioning OpenSSF as the home for AI agent security standards.

Pillars:

**i) Programs and Projects**: AGT is a production-grade open source project with 9,500+ tests, CI/CD automation, and multi-language SDKs. It provides reusable security tooling (GitHub Actions, pre-commit hooks, policy templates) that can benefit other OpenSSF projects and the broader community.

**ii) Education**: 45+ tutorials, comprehensive documentation, quickstart guides, and example integrations. The toolkit's tutorial structure follows a learning path from basic concepts to advanced production deployment patterns.

**iv) Community and Events**: Active community engagement with 20+ contributors, GitHub Discussions, and integration proposals across the agent framework ecosystem. The project has been presented at standards body meetings and has active community contributions from multiple organizations.

### IP policy and licensing due diligence
When contributing an existing Project to the OpenSSF, the contribution must undergo license and IP due diligence by the Linux Foundation (LF).
  * Yes, IP and license due diligence will be required. The project is licensed under MIT and all dependencies use permissive licenses (MIT, Apache 2.0, BSD). A TAC issue for tracking the LF IP review will be created upon acceptance. The project was approved for open source release by Microsoft's CELA (Corporate, External, and Legal Affairs) team.

### Project References
The project should provide a list of existing resources with links to the repository, and if available, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference           | URL |
|---------------------|-----|
| Repo                | https://github.com/microsoft/agent-governance-toolkit |
| Website             | https://github.com/microsoft/agent-governance-toolkit (MkDocs documentation site) |
| Contributing guide  | https://github.com/microsoft/agent-governance-toolkit/blob/main/CONTRIBUTING.md |
| Security.md         | https://github.com/microsoft/agent-governance-toolkit/blob/main/SECURITY.md |
| Roadmap             | https://github.com/microsoft/agent-governance-toolkit/blob/main/docs/ROADMAP.md |
| Demos               | https://github.com/microsoft/agent-governance-toolkit/tree/main/demo |
| Tutorials           | https://github.com/microsoft/agent-governance-toolkit/tree/main/docs/tutorials (45+ tutorials) |
| OpenSSF Badge       | https://www.bestpractices.dev/projects/12085 (99% passing) |
| PyPI Packages       | https://pypi.org/project/agent-os-kernel/, https://pypi.org/project/agentmesh-platform/, https://pypi.org/project/agent-sre/, https://pypi.org/project/agent-runtime/, https://pypi.org/project/ai-agent-compliance/ |
| npm Package         | https://www.npmjs.com/package/agentos-mcp-server |
| OWASP Compliance    | https://github.com/microsoft/agent-governance-toolkit/blob/main/docs/OWASP-COMPLIANCE.md |
| Architecture        | https://github.com/microsoft/agent-governance-toolkit/blob/main/docs/ARCHITECTURE.md |
| Threat Model        | https://github.com/microsoft/agent-governance-toolkit/blob/main/docs/THREAT_MODEL.md |
| CHANGELOG           | https://github.com/microsoft/agent-governance-toolkit/blob/main/CHANGELOG.md |
| Examples            | https://github.com/microsoft/agent-governance-toolkit/tree/main/examples |
