# OSS-CRS TI Sandbox Application

## List of project maintainers (alphabetic order)

* Andrew Chin, Georgia Institute of Technology,  @azchin
* Cen Zhang, Georgia Institute of Technology, @occia
* Dongkwan Kim, Georgia Institute of Technology, @0xdkay
* Fabian Fleischer, Georgia Institute of Technology, @fab1ano
* Hanqing Zhao, Georgia Institute of Technology, @hq1995
* Jiho Kim, Georgia Institute of Technology, @jhkimx2
* Taesoo Kim, Georgia Institute of Technology & Microsoft, @tsgates
* Younggi Park, Independent Researcher, @grill66
* Youngjoon Kim, Georgia Institute of Technology, @acorn421
* Yu-Fu Fu, Georgia Institute of Technology, @fuyu0425

Note: Maintainers may be updated in the future (some can become inactive or other AIxCC team members may join).

## Sponsor

AI / ML Security Working Group

The project commits to providing quarterly updates on progress to the AI / ML Security Working Group.

## Mission of the project

OSS-CRS (Open Source Software Cyber Reasoning System) provides a standardized infrastructure for building, running, and evaluating Cyber Reasoning Systems (CRS) that perform automated vulnerability discovery and remediation in open source software.

### Problem Statement

Automated vulnerability discovery is critical for securing the open source software supply chain. While fuzzing tools like OSS-Fuzz have proven effective at finding bugs, the ecosystem lacks:

1. **Standardized CRS interfaces**: Each vulnerability discovery tool has unique deployment requirements, making comparison and integration difficult
2. **Reproducible evaluation frameworks**: No common infrastructure exists for fairly evaluating and benchmarking different CRS approaches
3. **LLM integration standards**: As AI-assisted security tools emerge, there is a lack of framework for developing, integrating, and assessing LLM-enhanced security analysis tools

### Solution

OSS-CRS addresses these gaps by providing:

- **Unified CLI interface** (oss-bugfind-crs / oss-patch-crs run) for any CRS implementation
- **Docker Compose-based orchestration** for reproducible multi-container deployments
- **Resource management** with configurable CPU, memory, and LLM budget allocation
- **LiteLLM integration** for standardized LLM access across different CRS implementations
- **OSS-Fuzz compatibility** to leverage Google's existing fuzzing infrastructure
- **Ensemble support** for combining multiple CRS approaches

### Alignment with OpenSSF Mission

OSS-CRS directly supports OpenSSF's mission to secure the open source supply chain by:

1. **Democratizing advanced security tooling**: Making sophisticated CRS capabilities accessible through simple CLI commands
2. **Enabling fair CRS evaluation**: Providing infrastructure for benchmarking vulnerability discovery tools (CRSBench ecosystem)
3. **Accelerating security research**: Lowering the barrier to experiment with and deploy new vulnerability discovery techniques
4. **Supporting AI-augmented security**: Providing standards for integrating LLMs into security workflows

### Novel Contributions

OSS-CRS represents a novel approach in the security tooling space:

- First open infrastructure for standardized CRS deployment and evaluation
- Bridges traditional fuzzing (OSS-Fuzz) with modern LLM-augmented approaches
- Supports both bug-finding and bug-fixing CRS modes
- Part of the larger CRSBench ecosystem for advancing automated vulnerability research

## IP policy and licensing due diligence

This is a new project developed at Georgia Institute of Technology and will be contributed under MIT license.

If applicable, the Linux Foundation will conduct IP due diligence upon approval for the Sandbox stage.

## Project References

| Reference          | URL                                                    |
|--------------------|--------------------------------------------------------|
| Repo                      | https://github.com/sslab-gatech/oss-crs                   |
| Website                  | (To be created upon Sandbox approval)                  |
| Contributing guide  | (To be created upon Sandbox approval)                  |
| Security.md            | (To be created upon Sandbox approval)                  |
| Roadmap               | See below                                                                 |
| Demos                   | See README.md in repository                                |
| Other-1                  | Bundled repo: [Our Benchmark]( https://github.com/sslab-gatech/CRSBench) |
| Other-2                  | Related: [OSS-Fuzz](https://github.com/google/oss-fuzz)|

Note: Our bundled benchmark repository is still under AIxCC competition organizer review procedure for open-source and we assume its release doesn’t block the Sandbox approval.

## Current Capabilities

- **Bug-finding CRS support**: Build and run CRS implementations for vulnerability discovery
- **Bug-fixing CRS support**: Infrastructure for automated patch generation
- **Multiple CRS integrations**:
  - `atlantis-c-libafl` - LibAFL-based fuzzer for C projects
  - `atlantis-c-bullseye` - Directed fuzzer for C projects
  - `atlantis-multilang-dind` - Team Atlanta multilang bug finding module
  - `atlantis-multilang-given_fuzzer` - Team Atlanta multilang version libfuzzer
  - `atlantis-java-main` - Team Atlanta Java bug finding module
  - `atlantis-java-atljazzer` - Team Atlanta Java bug finding module, directed fuzzer
  - `crs-libfuzzer` - Default libfuzzer
  - `atlantis-claude-code` - Team Atlanta patch agent: claude-code-like agent
  - `swe-agent` - Team Atlanta patch agent SWE-Agent
  - `atlantis-vincent` - Team Atlanta patch agent vincent
  - `atlantis-prism` - Team Atlanta patch agent prism
  - `atlantis-multi-retrieval` - Team Atlanta patch agent multi-retrival
  - `42-patch-agent` - Team 42-b3yond-6ug patching module
  - `buttercup-patcher` - Team Trail of Bits patching module
  - Ensemble configurations combining multiple CRS approaches
- **Resource management**: YAML-based configuration for CPU cores, memory limits, LLM budgets
- **LiteLLM integration**: Automated proxy deployment for LLM access control

### Roadmap

1/12/26 Roadmap Presentation to CRS SIG meeting: https://docs.google.com/presentation/d/1R9XAF6VOVimdlXL346CnNrMkOzJFVyFhJF9lrYtHnZI/edit?slide=id.g3b67cb90a0c_0_0#slide=id.g3b67cb90a0c_0_0

1. **Infrastructure Hardening**
   - Add SECURITY.md and vulnerability reporting process
   - Create comprehensive CONTRIBUTING.md
   - Improve documentation and user guides

2. **CRS Ecosystem Expansion**
   - Support additional CRSes from AIxCC teams and community
   - Add more language support beyond C and Java
   - Integrate with additional LLM providers

3. **Evaluation Framework**
   - Standardized benchmark suite integration
   - Automated metrics collection and reporting
   - CI/CD integration for CRS testing

4. **Community Building**
   - Public issue tracker and discussion forums
   - Regular community calls
   - Integration with other OpenSSF security tooling projects

