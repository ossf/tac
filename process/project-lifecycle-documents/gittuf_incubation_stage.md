# gittuf incubation application

## Project has met all Sandbox requirement

  * Sandbox PR: https://github.com/ossf/tac/pull/198
  * Sandbox Licensing and DD PR: https://github.com/ossf/tac/pull/199
  * Sandbox Document: https://github.com/ossf/tac/blob/main/process/project-lifecycle-documents/gittuf_sandbox_stage.md

## List of project maintainers

The project must have a minimum of three maintainers with a minimum of two different organizational affiliations.
  * Aditya Sirish A Yelgundhalli, New York University / Bloomberg, adityasaky
  * Billy Lynch, Chainguard, wlynch
  * Patrick Zielinski, New York University, patzielinski
  * Reza Curtmola, New Jersey Institute of Technology, reza-curtmola
  * Justin Cappos, New York University, JustinCappos
  * Neil Naveen, Independent, neilnaveen

## Mission of the project

Source code is typically stored in a version control system, of which the most
popular is Git. To prevent software supply chain attacks that tamper with source
code, it's common to use access control policies (e.g., the developers trusted
to make changes to a branch in the repository, the number of review approvals
required for changes). Such policies are typically enforced by _source control
platforms_ (SCP). However, these platforms become a single point of trust; a
compromised SCP can undermine the security controls configured for the
repository. gittuf's mission is to make Git security policies _independently
verifiable / enforceable_, thereby removing the SCP as a fully trusted entity in
the supply chain.

## Project adoption

gittuf has recently reached a beta release. We've been collaborating with
industry and open source projects to run gittuf pilots to improve the system's
guarantees and user experience.

### Bloomberg

Bloomberg is currently running a pilot of gittuf.

> Dennis Roellke, a security architect at Bloomberg, is leading a Gittuf pilot
project in various departments of the financial news and information company.
His primary job responsibility is to ensure the integrity of the software supply
chain throughout different groups.
>
> [...]
>
> Roellke said his team is continuing to scale up its Gittuf interfaces for use
by larger and more varied teams of engineers inside Bloomberg.

Source: https://news.njit.edu/cybersecurity-researcher-njit-toughens-git-software-repositories

### Open Source Projects

Other projects in the software supply chain security space have begun piloting
gittuf.

#### GUAC

The GUAC project, incubated at the OpenSSF, has started using gittuf via the
GitHub app on their [documentation
repository](https://github.com/guacsec/guac-docs) to record pull request
approval and merge attestations. Example:
https://github.com/guacsec/guac-docs/pull/203#issuecomment-2898386819

#### in-toto

The in-toto project, a graduated project at the CNCF, has been dogfooding gittuf
in the [attestation-verifier
repository](https://github.com/in-toto/attestation-verifier) for a year. The
project recently switched over to using the gittuf GitHub app. Example:
https://github.com/in-toto/attestation-verifier/pull/77#issuecomment-2901762106

#### Chainsights

Kusari's open source [chainsights](https://github.com/kusari-oss/chainsights)
repository is part of the gittuf GitHub app pilot.

#### SLSA

gittuf is closely aligned with the upcoming SLSA source track. Work is underway
to allow gittuf to be used to achieve SLSA source level 3. The draft SLSA source
track specification lists gittuf as a way to enforce change management process.

> Enforcement of the organization-defined technical controls could be
accomplished by, for example:
> - The configuration of branch protection rules (e.g.GitHub, GitLab) which
>   require additional checks to ‘pass’ (e.g. unit tests, linters), or
> - the application and verification of gittuf policies, or
> - some other mechanism as enforced by the Change management tool.

Source: https://slsa.dev/spec/draft/source-requirements

## Governance

Project must have met publicly at least 5 times in the last quarter since becoming Sandbox
  * [2025 Notes](https://docs.google.com/document/d/1EbFAZu_pxayLwr4QWxhKCSZYhyJAcya7K-b_kuXlmpU/edit?tab=t.0)
  * [2024 Notes](https://docs.google.com/document/d/1tXFCVUHsICLpLKxcGvhzBDUWmpsY1LQvysFaX6AJRkk/edit?tab=t.0)

Projects must have documented, initial project governance
  * https://github.com/gittuf/community/blob/main/CHARTER.md

Project must have defined Contributor Guide
  * https://github.com/gittuf/gittuf/blob/main/CONTRIBUTING.md 

Project has attained an OpenSSF Best Practice Badge at "passing" level
  * https://www.bestpractices.dev/en/projects/7789

Project is integrated into the OpenSSF Scorecard
  * https://scorecard.dev/viewer/?uri=github.com%2Fgittuf%2Fgittuf

## IP policy and licensing due diligence

Not applicable now, completed when entering OpenSSF sandbox, tracked in
https://github.com/ossf/tac/issues/199.

The gittuf implementation is licensed under Apache 2.0. Source:
https://github.com/gittuf/gittuf/blob/main/LICENSE

## Security Baseline

The project meets all applicable Security Baseline requirements:
 * [x] [Security Baseline - Once Sandbox](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---once-sandbox)
 * [x] [Security Baseline - To Become Incubating](https://github.com/ossf/tac/blob/main/process/security_baseline.md#security-baseline---to-become-incubating)

## Project References

The project should provide a list of existing resources with links to the repository, website, a roadmap, contributing guide, demos and walkthroughs, and any other material to showcase the existing breadth, maturity, and direction of the project.

| Reference             | URL |
|-----------------------|-----|
| Repo                  | https://github.com/gittuf/gittuf |
| Meeting Agenda        | https://docs.google.com/document/d/1EbFAZu_pxayLwr4QWxhKCSZYhyJAcya7K-b_kuXlmpU/edit?tab=t.0 |
| OSSF Calendar Entry   | https://openssf.org/getinvolved/ |
| Website               | https://gittuf.dev |
| Contributing guide    | https://github.com/gittuf/gittuf/blob/main/CONTRIBUTING.md |
| Security.md           | https://github.com/gittuf/gittuf/blob/main/SECURITY.md |
| Roadmap               | https://github.com/gittuf/gittuf/blob/main/docs/roadmap.md  |
| Demos                 | https://github.com/gittuf/demo |
| Best Practices Badge  | https://www.bestpractices.dev/en/projects/7789 |
| Scorecard integration | https://scorecard.dev/viewer/?uri=github.com%2Fgittuf%2Fgittuf |
| Talks                 | https://www.youtube.com/watch?v=eCSeIEdMbCw&pp=ygUGZ2l0dHVm, https://www.youtube.com/watch?v=5bWpeZNK00Q&pp=ygUGZ2l0dHVm |
| Misc. Coverage        | https://lwn.net/Articles/972467/ |
| Research Paper        | https://www.ndss-symposium.org/ndss-paper/rethinking-trust-in-forge-based-git-security/ |
