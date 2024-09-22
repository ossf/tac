## Overview
The purpose of the Open Source Security Foundation (the “OpenSSF”) is to inspire and enable the community to secure the open source software (OSS) we all depend on. The OpenSSF Security Baseline combines process, configurations, and tooling to help open source projects achieve this mission. The OpenSSF Security Baseline establishes the minimum practical security standards for OpenSSF software projects throughout various lifecycle stages, ensuring a strong Minimum Viable Secure Product (MVSP) across Linux Foundation projects and internal work.

Existing OpenSSF materials, including guides and other technologies will be used to frame the baseline, define objectives, provide implementation recommendations, and suggest verification methods. Through community engagement and collaboration, the baseline will first be adopted by a few software-based pilot projects before being fully adopted by all OpenSSF projects.

The Security Baseline provides a foundational framework for systematic adoption across the Linux Foundation. Collaboration with peer foundations is essential for baseline customization and adoption, aiming to enhance the security of the open source software ecosystem.

As technology and the threat landscape evolve, the baseline will continuously adapt. The primary goal of this initiative is to maintain a balance between security, reliability, performance, and cost-effectiveness.

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119/).

## Background
The initiative was one of the outcomes of the October 2023 Linux Foundation Member Summit. Making open source software more secure is one of the top priorities across the Linux Foundation. OpenSSF is leading the charge. 

The security of open source software is a matter of global interest and concern.  In the United States, open source software is used across all critical infrastructure sectors defined by CISA (Cybersecurity and Infrastructure Security Agency), for example, health care, defense, financial services, utilities, telecommunications, etc. Open source security directly impacts national security, economics and social stability. Enhancing open source security is imperative. NIST has published a [Secure Software Development Framework](https://csrc.nist.gov/Projects/ssdf) (SSDF) as a result of Executive Order (EO) 14028 on "[Improving the Nation's Cybersecurity](https://www.federalregister.gov/documents/2021/05/17/2021-10460/improving-the-nations-cybersecurity)".

In the European Union, [Cyber Resiliency Act](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CONSIL:ST_17000_2023_INIT) (CRA) has declared a new role - Open Source Steward(Article 3(18a). The legislation is to ensure that consumers of products with digital features are protected, and manufacturers of these products are held accountable for product security. Open source security is the foundation for manufacturers to be compliant with the legislation.     

## Success Criteria
The success of the security baseline SHOULD be quantified and qualified in a few dimensions:
 * **Adoption and Advancement of Security Technologies**
   * **Objective**: The Security Baseline promotes improved open source security outcomes.
   * **Approach**: Utilize technical outcomes from the OSS community to implement, and verify the security baseline.
   * **Collaborations**: Partner with other foundations to enhance OSS security through education, specifications, frameworks, and tooling.
   * **Automation and Tooling**: Identify opportunities for automation and tooling to ease the burden on maintainers and contributors, facilitating secure by design and secure by default principles.
 * **Increased Security Baseline Adoption Rate**
   * **Objective**: Ensure the Security Baseline is widely adopted.
   * **Metrics**:
     * Three OpenSSF software-based pilot projects meet the baseline requirements for each project's life cycle by 9/15/2024.
     * All OpenSSF software-based projects meet the baseline requirements for each project's life cycle by the end of 2024, an aspirational goal.
     * At least two other Linux Foundation (LF) foundations adopt the baseline by the end of 2024, an aspirational goal.
* **Reduction in Security Findings**
  * **Objective**: Measure the effectiveness of the baseline in improving a project’s security posture.
  * **Metrics**:
    * Use OpenSSF Scorecard statistics to track the reduction of Critical, High, and Medium risk findings through the project lifecycle. Benchmark is established at the adoption time. 
    * Monitor the number of exceptions at both project and foundation levels, expecting a decline as projects mature and become more secure.
* **Improved OSS Maintainer and Consumer Experience**
  * **Objective**: Enhance the experience for both OSS maintainers and consumers.
  * **Approach**: Shift security left in the OSS supply chain to reduce downstream risks.
  * **Shared Responsibility**: Encourage private sector consumers to support OSS security by funding or contributing developer hours.

## Scope
The Security Baseline SHALL apply to technical initiatives under the OpenSSF GitHub enterprise accounts. 

## Constraints
**Ecosystem support for tooling and configuration capabilities**: They vary depending on the programming languages and the roadmaps for new features or feature enhancements. 

**Shortage of contributors for tooling development**:  Security in open source can only be achieved at scale with the right tool. Lack of easily adopted tools prevents us from achieving a higher level of security baseline. 

**Maintainers' time constrained by disproportionate open-source consumer demands**: The security baseline aims to enable more secure software development at speed. Nevertheless, the primary constraint remains the limited time available to maintainers, coupled with the demand for open-source software maintenance, including the enhancement of software security.

## Basic Operating Principles 
To navigate these constraints, the following operating principles are adopted:

  * **Strong Bias Towards Automation and Automatability**
    * **Objective**: Enhance security by default and position security as an enabler rather than an inhibitor.
    * **Approach**: Prioritize automation and automatability to manage dependencies and vulnerabilities more effectively.[[Know, Prevent, Fix](https://security.googleblog.com/2021/02/know-prevent-fix-framework-for-shifting.html)], [[software supply chain transparency logical model](https://github.com/guacsec/guac?tab=readme-ov-file)]
  * **Minimal, Achievable, and Practical Security Baseline Requirements**
    * **Objective**: Design a security baseline that balances software reliability, performance, cost, and security.
    * **Approach**:
      * Ensure the Security Baseline is minimal and achievable with current technology.
      * Allow for incremental adoption throughout a software project’s lifecycle by shifting security left in the SDLC process.
      * Reuse existing OpenSSF guides and technologies with minimal new requirements.
  * **Documented Governance Process**
    * **Objective**:
      * Establish a consistent set of objective security measures for all participating foundations and projects.
      * Ensure the Security Baseline is an integral part of the TAC Technical Initiative life cycle process, and maintenance of the baseline follows the TAC decisioning process.  
    * **Approach**:
      * Provide clear, implementable, and definitive guidelines for maintainers and contributors.
      * Incorporate the baseline into OpenSSF Technical Advisory Council (TAC) [technical initiative life cycle process](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md).
      * Rely on every adopting project to submit issues to log the friction points and provide feedback to refine the Security Baseline, facilitating easier adoption.
      * Revision to the baseline will be a community effort following the [TAC Issue/PR process](https://github.com/ossf/tac/blob/main/process/TAC-Decision-Process.md#issuepull-request-types). 

## Security Baseline 
As a software project progresses through the [OpenSSF technical initiative life cycle](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md), it is beneficial to incrementally integrate more security measures.
  * Sandbox stage: Baseline awareness, and initial requirements
  * Incubation stage: Sandbox requirements plus additional baselines to sustain the secure project development and protect early adopters. 
  * Graduated stage: Incubation baseline plus additional baselines to prepare for its general availability and sustainability. 

This phased approach intends to support maintainers, contributors, and the community in innovating quickly with security built into the design or enabled by default.

### Security Baseline - Once Sandbox
When the project starts, it's critical to have a security foundation to reduce a class of vulnerabilities and secure your digital assets with strong credential protections. 

| Security Baseline | Objective | How to Implement | How to Verify|
|-------|-------|-------|-------|
| A memory-safe language is adopted for new projects or new components. | Reduce  memory safety vulnerabilities at scale. | Choose one of the [memory-safe languages](https://www.memorysafety.org/docs/memory-safety/) <br /> <br />  For preexisting projects in C or C++, follow the [Compiler Options Hardening Guide](https://best.openssf.org/Compiler-Hardening-Guides/Compiler-Options-Hardening-Guide-for-C-and-C++) | Check the [file extension](#Standard-File-Extensions-of-Common-Programming-Languages) and compare with the code. <br /> <br /> 
|Two-factor authentication (2FA) is enabled for repository interactive access. | Reduce the risks of credential compromise and attacks on the digital assets.| 2FA is enabled by default at the enterprise level for all the organizations.<br /> <br /> Refer to [SCM Best Practices](https://best.openssf.org/SCM-BestPractices/) for more information. <br /> <br /> See [instructions for device setup](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication).|[2FA verification, drift detection and correction](#2FA-Verification-Drift-Detection-and-Correction) provides details for verifying 2FA is enabled, monitoring and restoring 2FA if it’s disabled. |

### Security Baseline - To Become Incubating

As the project codebase grows and more features are added, increasing complexity, it becomes crucial to leverage security tools to identify vulnerabilities in the codebase or dependent software early on. Addressing critical issues early prevents costly fixes in the future. At this stage, projects MUST onboard to OpenSSF Scorecard by following the [installation instructions](https://github.com/ossf/scorecard-action#installation) of [Scorecard GitHub Action](https://github.com/ossf/scorecard-action). The Action runs on any repository change and raises alerts. ​​Repository administrators, organization owners, and people with write or maintain access to a repository can view the alerts in the repository’s Security tab. Ensure Scorecard is enabled for the project by following [Scorecard Verify Runs](https://github.com/ossf/scorecard-action?tab=readme-ov-file#verify-runs) instruction.

| Security Baseline | Objective | How to Implement | How to Verify|
|-------|-------|-------|-------|
| There are no hard-coded active secrets in the project source repository. |Prevent unauthorized access to repository assets.| GitHub secret scanning and push protection is enabled in the enterprise account. Repo admin can disable the setting for a sandbox project. The setting is monitored and enforced by the staff members.|[Secret Scanning and Push Protection Verification, Drift Detection and Correction](#Secret-Scanning-and-Push-Protection) provides information for verifying secret scanning and push protection config is as expected,  monitoring and restoring the config if it drifts.|
|Credentials are provisioned with minimal permissions.|Minimize security risks by only granting necessary access to reduce potential attack surfaces. |Apply [Principle of Least Privilege](https://csrc.nist.gov/glossary/term/least_privilege) to manage programmatic and interactive access.<br /><br />Follow this [guide](https://docs.github.com/en/actions/security-guides/automatic-token-authentication#modifying-the-permissions-for-the-github_token) to grant GITHUB_TOKEN the least required permissions in your workflows. <br /><br />Establish role-based access control by assigning [organization roles](https://docs.github.com/en/enterprise-cloud@latest/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization#permissions-for-organization-roles) and  [repository roles](https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization) based on members’ responsibilities.<br /><br />An Organization Owner SHOULD group members and manage their repo Permissions through [GitHub Teams](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams).<br /><br />Organization Owner role SHALL be assigned to a minimal number of 2 and maximum 3 members. Same practice applies to the Repo Admin role. <br /><br />Refer to [SCM Best Practices](https://best.openssf.org/SCM-BestPractices/) for more information.|[Scorecard checks Token-Permissions](https://github.com/ossf/scorecard/blob/98ec491a888a8a0db9d83a3c7d379ae1f46321de/docs/checks.md#token-permissions) and reports if your project's automated workflow tokens follow the principle of least privilege. <br /><br />Example report: [Scorecard](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard&sort_by=risk-level&sort_direction=desc) <br /><br />[Allstar](https://github.com/ossf/allstar) raises an issue against the repo when it detects tokens with excessive permission and adds new comments every 24 hours until the issue is resolved.<br /><br /> The Organization Owner SHALL periodically audit organization member permissions and token permissions manually before this can be automated.|  
|An initial set of metadata is established for gaining security insights into the project.|To start providing insights into your project’s security in both human and  machine processable format.|Create SECURITY_INSIGHTS.yml at the root of the repository and ensure [schema](https://github.com/ossf/security-insights-spec/blob/main/security-insights-schema.yaml) compliance.<br /><br />The insights SHALL provide header information, project lifecycle, and contributing policy. <br /><br />Example SECURITY_INSIGHTS.yml : <br />OpenSSF: [GUAC](https://github.com/guacsec/guac/blob/main/SECURITY-INSIGHTS.yml), [Security Insight](https://github.com/ossf/security-insights-spec/blob/main/SECURITY-INSIGHTS.yml)|SECURITY_INSIGHTS.yml is found at the root of the repository, and contains metadata for project life cycle and contribution guides.|SECURITY_INSIGHTS.yml is found at the root of the repository, and contains metadata for project life cycle and contribution guides.|
|A dependencies policy is published, maintained and followed.|Sets clear guidelines for selecting and maintaining secure dependencies.|Follow [Concise Guide for Evaluating Open Source Software](https://best.openssf.org/Concise-Guide-for-Evaluating-Open-Source-Software) to evaluate the  dependencies before using them in the project.<br /><br />Publish a dependencies policy to guide contributors on dependency management, using a stand-alone file or CONTRIBUTING.md.<br /><br />Example dependency policy:<br />CNCF: [Kubescape](https://github.com/kubescape/kubescape/blob/master/docs/environment-dependencies-policy.md), [Argo Helm](https://github.com/argoproj/argo-helm/blob/main/CONTRIBUTING.md#new-application-versions)<br /><br />The policy SHALL be added to SECURITY_INSIGHTS.yml section “dependencies” > “env-dependencies-policy”.<br /><br /> Example SECURITY_INSIGHTS.yml with dependencies policy: <br />CNCF: [Kubescape](https://github.com/kubescape/kubescape/blob/master/SECURITY-INSIGHTS.yml), [capsule](https://github.com/projectcapsule/capsule/blob/main/SECURITY-INSIGHTS.yml).|SECURITY_INSIGHTS.yml identifies the dependencies policy,  the policy provides guidance on dependencies evaluation and maintenance.|
|Direct dependencies are pinned in internet or infrastructure services and applications your project provides.|Ensures that only a known safe version of a dependency is used to protect against malware and credential compromise.|Follow Scorecard documentation to [pin dependencies](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#pinned-dependencies)<br /><br /> Examples:<br />OpenSSF: [Sigstore Fulcio](https://github.com/sigstore/fulcio?tab=readme-ov-file), [GUAC](https://github.com/guacsec/guac)|[Scorecard checks dependency pinning](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#license) and reports whether dependencies are pinned. <br /><br />Example report: <br />[Scorecard](https://github.com/ossf/scorecard/blob/49c0eed3a423f00c872b5c3c9f1bbca9e8aae799/SECURITY.md), [Sigstore Fulcio](https://api.securityscorecards.dev/projects/github.com/sigstore/fulcio).

### Security Baseline - Once Incubating
As a project matures and enters into the incubation stage, the project is expected to have more adopters. Additional security needs to be built into the project in order to sustain the secure project development and protect the consumers of the open source project. 

Some requirements might be only applicable to some projects, for example, architecture design will apply to projects that have systems integration. 

| Security Baseline | Objective | How to Implement | How to Verify|
|-------|-------|-------|-------|
|GitHub actions and workflows, if any,  are set up securely and remain secure.|To reduce the risk of repository compromise introduced by malpractices in CI/CD pipeline.| GitHub context is an attack surface that leads to script injection. Follow GitHub  hardening [guide](https://docs.github.com/en/actions/security-guides/security-hardening-for-github-actions#good-practices-for-mitigating-script-injection-attacks) to mitigate the risk.<br /><br /> GitHub triggers can be abused to introduce untrusted code into the build process. Follow this [article](https://securitylab.github.com/research/github-actions-preventing-pwn-requests/) for detailed analysis and practices to safeguard your actions and workflows.<br /><br />Refer to [SCM Best Practices](https://best.openssf.org/SCM-BestPractices/) for more information.|[Scorecard checks dangerous workflow](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#dangerous-workflow) and reports the finding if dangerous workflow is detected.<br /><br />Example report:<br />[Scorecard](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard&sort_by=risk-level&sort_direction=desc), [Sigstore Fulcio](https://api.securityscorecards.dev/projects/github.com/sigstore/fulcio)<br /><br />[Allstar](https://github.com/ossf/allstar) will raise an issue and add new comments every 24 until the issue is resolved.| 
|Static code analysis is run in CI/CD pipeline, if code exists, and critical severity exploitable  vulnerabilities MUST be fixed promptly.|To identify vulnerabilities in the codebase you develop, and remediate critical vulnerabilities that are exploitable, ensure your project is adoptable.|Adopt a Static Application Security Testing (SAST) tool to run static code analysis, e.g. CI/CD pipeline. The code analysis runs against the codebase that you develop, identify vulnerabilities and provide recommendations on remediation.<br /><br />Consider [Enable CodeQL](https://github.com/github/codeql-action#usage) in your CI/CD pipeline.<br /><br />Examples:<br />OpenSSF:[Sigstore Fulcio](https://github.com/sigstore/fulcio?tab=readme-ov-file), [Scorecard](https://github.com/ossf/scorecard/tree/49c0eed3a423f00c872b5c3c9f1bbca9e8aae799)|[Scorecard checks SAST](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#sast)is used in your CI/CD and reports the finding through the vulnerabilities check. You SHOULD see the report reflects the vulnerability fixes.<br /><br />Scorecard MAY not detect some SAST tools.<br /><br />Example report: [Scorecard](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard&sort_by=risk-level&sort_direction=desc)|
|A security policy is published and followed for vulnerability disclosure and response.|To provide clear guidance on how security findings are reported and the expected response.|SECURITY.md is established as part of the [OpenSSF default community health file](https://github.com/ossf/.github). It serves as the security policy, and provides generic information about how vulnerabilities are reported to the project. Project maintainers SHALL follow the [Guide to Coordinated Vulnerability Disclosure](https://github.com/ossf/oss-vulnerability-guide/blob/main/maintainer-guide.md#response-process) to provide project-specific vulnerability disclosure and response process. GitHub private vulnerability reporting SHALL be enabled at the repo level.<br /><br />The security policy SHALL be added to SECURITY_INSIGHTS.yml under section “vulnerability-reporting”.<br /><br />Examples SECURITY.md: <br />OpenSSF: [Sigstore](https://github.com/sigstore/cosign?tab=security-ov-file), [Scorecard](https://github.com/ossf/scorecard/blob/49c0eed3a423f00c872b5c3c9f1bbca9e8aae799/SECURITY.md)<br /><br />Example SECURITY_INSIGHTS.yml: <br />OpenSSF: [GUAC](https://github.com/guacsec/guac/blob/main/SECURITY-INSIGHTS.yml) <br />CNCF: [capsule](https://github.com/projectcapsule/capsule/blob/main/SECURITY-INSIGHTS.yml), [Kyverno](https://github.com/kyverno/kyverno/blob/main/SECURITY-INSIGHTS.yml)|[Scorecard checks security policy](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#security-policy) existence in a project and reports findings.<br /><br />The SECURITY_INSIGHTS.yml file identifies the security policy file (typically SECURITY.md).<br /><br />Example security insights :<br />OpenSSF: [GUAC](https://github.com/guacsec/guac/blob/main/SECURITY-INSIGHTS.yml)|
|Data in transit must be protected by cryptographic means.|To protect data from unauthorized access,  ensure data integrity, confidentiality and availability.|[Cryptographically Protecting Data in Transit, in Use and at Rest](#Cryptographically-Protecting-Data-in-Transit-in-Use-and-at-Rest) provides detailed rationale behind the baseline and implementation guidance.<br /><br />[TAC project lifecycle governance process](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md) SHALL be used if encryption is not achievable. |[Use curl and openssl to verify](https://docs.google.com/document/d/1-NBXdKvEJ9Wsh2i7lDNYven4fY9Bn6uvNJM5ySlMrdg/edit#heading=h.59ofury7nggp) the TLS protocol version, cipher and certificate chain for HTTPS traffic.|

### Security Baseline - To Become Graduated 
As a project matures and progresses towards graduation, it gains wider adoption. To prepare for its general availability and sustainability, additional security measures beyond the incubation baseline are necessary to safeguard project consumers.

| Security Baseline | Objective | How to Implement | How to Verify|
|-------|-------|-------|-------|
|Architecture design is created with up-to-date security controls for software-based projects.|Enhance security posture and reduce vulnerabilities.|[Design Doc at Google](https://www.industrialempathy.com/posts/design-docs-at-google/) is a good reference SECURITY_INSIGHTS.yml SHALL be updated under “security-artifacts” > “other-artifacts” to include architecture design. The design SHALL be maintained to be consistent with the implementation.|The SECURITY_INSIGHTS.yml file identifies the architecture design that provides information for the system design and security controls.|
|Project has no medium or higher severity vulnerabilities from SAST scan.|To ensure your project is safe for wide adoption and protect OSS consumers.|Continue to run SAST scan in your CI/CD pipeline, validate the vulnerabilities findings, remediate exploitable vulnerabilities in a timely fashion. Suppress findings that are not exploitable to reduce the false positives.|[Scorecard checks SAST](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#sast) is used in your CI/CD and reports the finding through the vulnerabilities check. You SHOULD see the report reflects the vulnerability fixes. <br /><br />Example report:<br />[Scorecard](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard&sort_by=risk-level&sort_direction=desc)|
|Publicly known vulnerabilities of critical severity are fixed promptly. Fixes are  released promptly. <br /><br />Publicly known vulnerabilities of medium or high severity are fixed. Fixes are  released within 60 days.|To protect your software from known vulnerabilities.<br /><br />To protect downstream consumers from vulnerable software via transitive dependency.|Follow [Scorecard instructions to use a  tool](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#sast) to automatically update dependencies. <br /><br />Follow [Scorecard instructions to fix vulnerabilities or suppress warnings](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#vulnerabilities) when the vulnerabilities are not exploitable.<br /><br />You can also add [GitHub dependency review for PR](https://github.com/actions/dependency-review-action) workflows. There's a 'warn-on-openssf-scorecard-level' parameter that you can configure to a custom Scorecard threshold to raise warning on the Scorecard checks that are important to the project.|[deps.dev](http://deps.dev) provides insights into your projects’ dependencies including transitive dependencies, the security advisories relevant to your project, and your projects’ Scorecard report at a high level.<br /><br />Example deps.dev insights:<br />[Sigstore Rekor](https://deps.dev/go/github.com%2Fsigstore%2Frekor)|
|Merging into the main branch requires a minimum of one maintainer approval (not including the PR submitter) and all CI/CD status checks passing.|Reduce the risks of malicious code injection into the repo, and unintentional errors that impact system availability|An Organization Owner or Repo Admin creates a [branch protection](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule) rule to enforce pull request approval by at least two maintainers.<br /><br />[TAC project lifecycle governance process](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md) SHALL be used for exception approval when the project does not have enough maintainers.|[Scorecard checks Branch Protection](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#branch-protection) and assigns a score at least 8 out of 10 when your project is enforcing this protection.<br /><br />Example report:<br />[Scorecard](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard&sort_by=risk-level&sort_direction=desc)| 
|Source repository is free of generated executable artifacts.|To eliminate  the risks of maliciously subverted executables, ensure that generated executables are reproducible from source code|Remove the executable files from the source repository, always build from source code.|Scorecard Binary-Artifacts check reports if your project has executable artifacts in the source repository. <br /><br />Example report: <br />[Scorecard](https://scorecard.dev/viewer/?uri=github.com/ossf/scorecard&sort_by=risk-level&sort_direction=desc)<br /><br />[Allstar](https://github.com/ossf/allstar) verifies that  binaries are checked into the source code repo for testing purposes, these binaries can be exempted from Scorecard binary check via [Maintainer Annotation](https://github.com/ossf/scorecard/blob/main/config/README.md). |
|If release artifacts are created, SBOM is generated and distributed as a release artifact.|To provide accurate and complete inventory of the software version, license,  dependencies and vulnerabilities to enhance supply chain security, in both human and  machine processable format.|Refer to [OpenSSF SBOM Everywhere SIG](https://github.com/ossf/sbom-everywhere) for the importance of  SBOM generation, consumption and process improvement.<br /><br />Generate SBOM’s in your project’s GitHub release workflow, ensure [minimal data fields recommended by NTIA](https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom) are populated.<br /><br />Example SBOM: <br />OpenSSF: [GUAC](https://github.com/guacsec/guac/blob/main/.github/workflows/release.yaml) SPDX<br />CNCF: [Kyverno](https://github.com/kyverno/kyverno/blob/68df5af40e9820633162e8d1c0b9966032eb7eb8/.github/actions/publish-image/action.yaml#L3) CycloneDX<br /><br />SECURITY_INSIGHTS.yml SHALL be updated under “dependencies” > “sbom” to include all the build SBOM’s.<br /><br />[TAC project lifecycle governance process](https://github.com/ossf/tac/blob/main/process/project-lifecycle.md) SHALL be used for exception approval when there is no tooling support to implement the baseline.|SECURITY_INSIGHTS.yml identifies the SBOM’s. SMOB’s provide information for dependency management, vulnerability management. |
|If release artifacts are created, release artifacts are cryptographically signed.|To ensure the integrity, authenticity, and trustworthiness of release artifacts|Projects SHOULD use [Sigstore](https://www.sigstore.dev/) for signatures. Follow [Scorecard Signed-Releases](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#signed-releases) documentation for detailed instructions. <br /><br />Examples signed release: <br />OpenSSF: [Sigstore Fulcio](https://github.com/sigstore/fulcio?tab=readme-ov-file), [Scorecard](https://github.com/ossf/scorecard/tree/49c0eed3a423f00c872b5c3c9f1bbca9e8aae799.)|[Scorecard Signed-Releases Check](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#signed-releases) reports that release artifacts are signed. When the Scorecard score is below 8, [Allstar](https://github.com/ossf/allstar) will raise an issue and add new comments every 24 hours until the issue is resolved.|
|If release artifacts are created, SLSA v1.0 Build Level 3 artifact attestation is generated and distributed as a release artifact.|To provide verifiable and non-forgeable claims about software origin and build process. |GitHub actions can be used to produce build provenance at SLSA v1.0 Build Level 3. For details, check [GitHub artifact attestation](https://docs.github.com/en/actions/security-guides/using-artifact-attestations-to-establish-provenance-for-builds) and [reusable workflow](https://docs.github.com/en/actions/using-workflows/reusing-workflows).<br /><br />To get familiar with SLSA specification and available tooling, visit this [workshop material](https://github.com/slsa-framework/oss-na24-slsa-workshop?tab=readme-ov-file). <br /><br />SECURITY_INSIGHTS.yml SHALL be updated under “security-artifacts” > “other-artifacts” to include attestation information.<br /><br />Examples:<br />OpenSSF: [Sigstore Fulcio](https://github.com/sigstore/fulcio/releases), [Scorecard](https://github.com/ossf/scorecard/blob/main/.github/workflows/slsa-goreleaser.yml) |[Scorecard Signed-Releases Check](https://github.com/ossf/scorecard/blob/7ce8609469289d5f3b1bf5ee3122f42b4e3054fb/docs/checks.md#signed-releases) reports attestation is generated as a release artifact. When the Scorecard score is > 8 and !=10, [Allstar](https://github.com/ossf/allstar) will raise an issue and add new comments every 24 hours until the issue is resolved.<br /><br />SECURITY_INSIGHTS.yml identifies  the attestation file. The attestation is  verifiable using these [instructions](https://docs.github.com/en/actions/security-guides/using-artifact-attestations-and-reusable-workflows-to-achieve-slsa-v1-build-level-3#step-2-verifying-artifact-attestations-built-with-a-reusable-workflow).|
|Logging of security events is implemented if your project provides internet or infrastructure service on behalf of the foundation.|To capture security relevant events for incident response.|Application/software level logging SHALL be in place to capture security relevant events, for example authentication. Sensitive information MUST NOT be logged.|Application/software logging is a continuous improvement process to help rapid incident response. The logs are consumed by the project’s maintainers.|
|Monitoring of security events is implemented if your project provides internet or infrastructure service on behalf of the foundation.|To monitor security relevant events for incident response.|If the project provides a service, monitoring SHALL be in place to raise actionable alerts when security relevant events meets pre-defined  thresholds, for example host level firewall configuration is changed.|Manual review.|
|If your project provides internet or infrastructure service on behalf of the foundation, an initial  security audit is conducted. Audit findings are addressed.|To identify and remediate the vulnerabilities in the internet service.|Security audit SHALL be funded through the [TAC TI funding process](https://github.com/ossf/tac/blob/main/process/TI%20Funding%20Request%20Process.md).<br /><br />SECURITY_INSIGHTS.yml SHALL be updated under “security-assessments” with a link to the audit report.|SECURITY_INSIGHTS.yml identifies the security audit report. The report provides details of the audit methodology, findings and recommendations.|

### Security Baseline - Once Graduated
Additional security MVP baseline on top of incubating baseline:

| Security Baseline | Objective | How to Implement | How to Verify|
|-------|-------|-------|-------|
|Publicly known vulnerabilities of critical severity are fixed and released in  coordination with project consumers promptly.<br /><br />Publicly known vulnerabilities of medium or high severity are fixed and released in  coordination with project consumers within 60 days.|To protect your software from known vulnerabilities.<br /><br />To protect downstream consumers from vulnerable software via transitive dependency|Continue to use automatic dependency update tools to actively manage vulnerabilities.<br /><br />Leverage [OSV](https://osv.dev/) to identify and remediate vulnerabilities.<br /><br /> Keep the project security policy up to date, follow the vulnerability disclosure and response process consistently.<br /><br />Subscribe to OpenSSF [SIREN](https://lists.openssf-vuln.org/g/siren) to receive real-time threat intelligence updates to stay connected with both open source community and OSS consumers.<br /><br />If tooling support is available, Collaborate with [OpenSSF vexctl](https://github.com/openvex/vexctl) to generate VEX statements when reported vulnerabilities are not exploitable, and update SECURITY_INSIGHTS.yml.|Monitor the vulnerabilities reported through the project vulnerability disclosure process and follow the response process.<br /><br />Monitor your project’s Scorecard report actively, especially vulnerabilities check results to validate vulnerabilities and take actions accordingly.<br /><br />SECURITY_INSIGHTS.yml  identifies the VEX statements. The statements provide evidence that the project is not subject to the vulnerability exploit.|
|If your project provides internet or infrastructure service on behalf of the foundation, a security audit is conducted on as-needed basis following the initial audit. Audit findings are addressed.|To keep the project up with the evolving threat landscape.|Security audit SHALL be funded through the OpenSSF [TAC TI funding process](https://github.com/ossf/tac/blob/main/process/TI%20Funding%20Request%20Process.md).<br /><br />SECURITY_INSIGHTS.yml SHALL be updated under “security-assessments” with a link to the new audit report.|SECURITY_INSIGHTS.yml  identifies the security audit report . The report provides details of the audit methodology, findings and recommendations.|

  


## Appendix
### Standard File Extensions of Common Programming Languages
  * Rust
    * .rs for source files
    * .toml for the Cargo configuration files
      * Cargo is Rust's build system and package manager.
  * Go
    * .go for source files.
  * C#: 
    * .cs for source files
    * .csproj for project files
  * Java
    * .java for source files
    * .class for compiled bytecode files
    * .jar For Java archive files
  * Swift
    * .swift for source files.
  * Python
    * .py for source files
    * .pyc for compiled bytecode files
  * JavaScript
    * .js for standard JavaScript files
    * [Common JavaScript File Extension](https://www.npmjs.com/package/common-js-file-extensions) provides a comprehensive list. 
  * C
    * .c for C source files
    * .h for header files.
  * C++
    * .cpp, .cxx, .cc, .C (uppercase C, less common) for C++ source files
    * .hpp, .hxx, .hh, or .H for C++ header files. 
    * .h is also commonly used for C++ header files in projects that are written in both C and C++.
  * Assembly
    * .asm for source files
    *  The file extensions for Assembly language can vary more widely depending on the target platform and the assembler being used. 
 
### 2FA Verification, Drift Detection and Correction
The 2FA setting changes are captured in the GitHub audit log. The enterprise audit log is being monitored and alerted on using Linux Foundation DataDog and Jira. Two OpenSSF staff members are the enterprise owners, and they are the first responders to the alerts.   

When 2FA is disabled in GitHub Enterprise or an organization, an alert MUST be raised for enterprise owners and organization owners to respond and re-enable 2FA. Enterprise owners MUST confirm 2FA enablement by verifying the event in the audit log. 
  * Enterprise account
    * Event
      * Disable 2FA: business.disable_two_factor_requirement 
      * Enable 2FA: business.enable_two_factor_requirement 
    * Response: 
      * DataDog will trigger an alert when detecting the above events
      * OpenSSF staff with the enterprise owner role MUST take action to triage and restore the setting, following change management process
  * Organization
    * Event
      * Disable 2FA: org.disable_two_factor_requirement 
      * Enable 2FA: org.enable_two_factor_requirement 
    * Response: 
      * DataDog will trigger an alert on detection of the above event
      * OpenSSF staff MUST take action to triage and restore the setting in “ossf” org, following change management process
      * OpenSSF staff MUST take action to inform the owner of the impacted organization and support restoring 2FA

### Secret Scanning and Push Protection 
The [Secret Scanning](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/about-secret-scanning) and [Push Protection](https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/push-protection-for-repositories-and-organizations) setting changes are captured in the GitHub audit log. The enterprise audit log is being monitored and alerted on using Linux Foundation DataDog and Jira. Two OpenSSF staff members are the enterprise owners, and they are the first responders to the alerts.  

When Secret Scanning and Push Protection features are disabled in GitHub Enterprise or an organization, an alert MUST be raised for enterprise owners to respond and coordinate with organizations owners or repo admins to restore the settings. Enterprise owners MUST confirm feature enablement by verifying the event in the audit log. 
  * Disable Secret Scanning and Push Protection 
    * Event 
      * Enterprise account
        * business_secret_scanning.disable 
      * Repository
        * repository_secret_scanning.disable
        * repository_secret_scanning_push_protection.disable
    * Response 
      * DataDog will trigger an alert when detecting the above events
      * OpenSSF staff with the enterprise owner role MUST take action to triage, identify where the setting has changed, and restore the setting in collaboration with organization and repo admins, following change management process.
  * Enable Secret Scanning and Push Protection 
    * Event 
      * Enterprise
        * business_secret_scanning.enable
      * From repository
        * repository_secret_scanning.enable

### Cryptographically Protecting Data in Transit, in Use, and at Rest

#### Data in Transit

Cryptographically protecting data in transit ensures that data transmitted over networks or between systems is protected from unauthorized access, man-in-the-middle attack ([MitM](https://csrc.nist.gov/glossary/term/man_in_the_middle_attack)), [tampering](https://csrc.nist.gov/glossary/term/tampering) of data and systems, and data [breach](https://csrc.nist.gov/glossary/term/breach). These attacks lead to disruptions to critical infrastructure operations, for example, health care, utilities, banking and telecommunications. Businesses and individuals suffer from financial and reputation losses, regulatory compliance consequences and intellectual property loss. Recent ransomware attack on US hospital networks [endangered patients’ health](https://www.cnn.com/2024/05/29/tech/ransomware-attacks-hospitals-patients-danger/index.html#:~:text=A%20ransomware%20attack%20on%20a,by%20the%20cyberattack%20told%20CNN.).<br /><br />Here are common use cases for encrypting data in transit to protect the  data confidentiality and integrity:
  * **Secure Web Communications (HTTPS)**: Web traffic is protected via HTTPS to  ensure that confidential information, such as login credentials, financial transactions, and personally identifiable information (PII), is protected from tampering and loss.
  * **Secure Messaging**: Applying cryptography to emails and instant messages ensures that the content of messages remains confidential and cannot be read or altered by unauthorized parties during transmission.
  * **File Transfers**: Applying cryptography to data during file transfers (e.g., using secure file transfer protocols like SFTP or FTPS) ensures that files exchanged between systems or individuals are protected from tampering and loss.
  * **Database Connections**: Applying cryptography to database connections (e.g., using TLS/SSL) ensures that data transmitted between applications and databases remains confidential and secure, preventing unauthorized access and data breaches.
  * **Remote Access**: Applying cryptography to remote access sessions (e.g., using VPNs or SSH) ensures that data transmitted across networks is protected from MitM.
  * **API Communications**: Applying cryptography to API communications ensures that data exchanged between different software applications or services over the network is protected from MitM, data loss and tamping.<br /><br />To protect data confidentiality, integrity, and authenticity during transmission over networks or between systems, applying cryptography to data in transit is critical.<br /><br />When using cryptographic libraries, refer to section “Use basic good cryptographic practices” in [OpenSSF Best Practice Badge](https://www.bestpractices.dev/en/criteria/0).<br /><br />HTTPS MUST be used for API communications. TLS 1.2 and above protocol SHALL be used.<br /><br />You can access GitHub repositories over HTTPS. If you have not installed GitHub CLI, you need to use a personal access token to run commands against GitHub. HTTPS access allows you to access GitHub API, or run Git commands using repositories HTTPS URL. <br /><br />You can use [SSH](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github) to authenticate to GitHub from the command line to work on your repositories. The setup is one time effort generating a SSH key pair, uploading a public key to GitHub, and pointing Git to the remote SSH URL. With SSH keys, you can connect to GitHub without supplying your username/password or personal access token every time when you log in to commit code, clone repo, etc. DSA SHALL NOT be used to generate SSH keys. The following algorithm SHALL be used:
  * RSA (Rivest-Shamir-Adleman):
    * Minimum recommended key length: 2048 bits
    * Higher security: 3072 bits or 4096 bits
  * ECDSA (Elliptic Curve Digital Signature Algorithm):
    * Minimum recommended key length: 256 bits
    * Higher security: 384 bits to 521 bits
  * Ed25519:
    * Fixed key length: 256 bits

#### Data in Use
The most practical way to protect data during execution is with Confidential Computing techniques.
Confidential Computing protects data in use by performing computation in a hardware-based, attested
Trusted Execution Environment. Typically this entails memory encryption and sometimes integrity
features controlled by a restricted mode of a CPU, GPU, or other processor. Features are available
across different levels of granularity to isolate regions of a process, the entirety of a process,
and the entirety of a virtual machine. Isolating the smallest region limits exposure, see:
[Trusted Computing Base](https://en.wikipedia.org/wiki/Trusted_computing_base)

Other means of protecting data during execution exist such as fully homomorphic encryption (FHE) and
multi-party computation (MPC). These cryptographic techniques do not rely on hardware techniques
for their security, but they do have nuanced limitations and compute costs that restrict their
utility to certain case. For more on the comparison between Confidential Computing and FHE see:
[Confidential Computing and Homomorphic Encryption](https://confidentialcomputing.io/2023/03/29/confidential-computing-and-homomorphic-encryption/).

Open source software and guides are freely available through the
[Confidential Computing Consortium](https://confidentialcomputing.io/resources/white-papers-reports/).


#### Data at Rest
For data at rest, follow the instructions from the storage solutions for encryption practices

### Curl and OpenSSL Tips
[curl](https://curl.se/docs/sslcerts.html) is a powerful CLI tool to troubleshoot and observe details of HTTPS traffic, including the TLS handshake and certificate information. For example the following command provides insights into a HTTPS GET request and response, including the x.509 certificate details, TLS protocol and cipher, etc. This [article](https://www.sectigo.com/resource-library/what-is-x509-certificate) provides a comprehensive overview of x.509 certificates. 
```
curl -vI  https://google.com

-v: verbose mode, provides more details about the HTTPS response, including the SSL handshake and server side certificate information.

-I: Fetches the headers only (HEAD request), not the body of the response.
```
[openssl](https://www.openssl.org/) is another powerful CLI tool to [create CSR’s](https://www.openssl.org/docs/man1.1.1/man1/openssl-req.html) and troubleshoot certificate related issues, especially issues along the certificate chain. For example, the following command provides details of the certificate chain for google.com, including the server certificate, the intermediate cert and the root CA that issues the intermediate cert. 
```
openssl s_client -showcerts -servername google.com -connect google.com:443 </dev/null
```






