## Application for gittuf at Sandbox stage

### List of project maintainers

* Aditya Sirish A Yelgundhalli (New York University, @adityasaky)
* Billy Lynch (Chainguard, @wlynch)
* Justin Cappos (New York University, @JustinCappos)
* Reza Curtmola (New Jersey Institute of Technology, @reza-curtmola)

### Mission of the project

Git is the most popular source control management system in the world but it
largely leaves security controls either to the developers or to the hosts
storing a copy of some repository. gittuf's mission is to implement security
controls into Git repositories using existing Git semantics like its support for
cryptographic signatures and its content addressed store. By embedding source
security policies into the repository, gittuf makes policies transparent that
enables _distributed verification_ by all repository users. Further, as gittuf
versions and tracks changes to policies using Git semantics, past repository
states can be _audited_ against the then-applicable policies.

gittuf aims to embed features like distribution, rotation, and revocation of the
keys trusted for repositories. In addition, gittuf allows repository owners to
define access control policies for Git branches, tags, and files. Also, gittuf
aims to implement support for SLSA's (under development) source security track
by allowing repository owners to define policies for code review attestations,
automated testing attestations, and more. Finally, gittuf presents an extensible
layer that can implement more Git-specific security features in future.

In summary, gittuf aims to offer the following improvements / properties to
Git's security:
* Key Management: distribute and revoke Git signing keys in the context of
  repositories
* Reference State Log: unambiguous, ordered log of repository activity with
  authorship verified using cryptographic signatures
* Access Control Policies: create policies that dictate which developers can
  write to specific Git branches, tags, and files tracked in the repository
  using the reference state log
* Support Attestations: support in-toto and SLSA source track attestations to
  enable verifying source code policies like code review requirements, test
  results and more
* Distributed and Transparent Verification: enable all developers to verify
  without reliance on centralized policy verification
* Auditable Repository Policies: track all versions of policies using the
  reference state log so historic repository states can be verified against the
  then-applicable policies, making repositories more auditable
* Git-native and Backwards Compatible: compatible with all Git repositories,
  including existing repositories, with no hard requirement of specific
  Git-ecosystem tools
* Extensible Security Layer: support the addition of security features as new
  solutions or desirable Git repository properties emerge

#### Alignment with the OpenSSF

The mission of the gittuf project aligns with the
[OpenSSF's Technical Vision](https://openssf.org/about/), especially with:

> Developers, auditors, and regulators can create and easily distribute security
policies that are enforced through tooling and automation, providing continuous
assurance of the results.

gittuf also has synergy with the mission of the [OpenSSF Supply Chain Integrity
Working Group](https://github.com/ossf/wg-supply-chain-integrity):

> scalable standardized attestable practices for supply chain security

gittuf provides a framework to implement such practices for securing Git
repositories, and is complementary to other efforts under the working group like
SLSA.

Finally, gittuf meets the sandbox entry requirements. The project has active
maintainers from three organizations, aligns as described above with the OpenSSF
mission, and presents a novel approach to securing Git repositories. In
addition, gittuf has achieved the first level of the OpenSSF Best Practices
badge.

### IP policy and licensing due diligence

License due diligence is complete and no conflicts were found. Here are the
findings from the corresponding issue (https://github.com/ossf/tac/issues/199):

```
LICENSE INTAKE SCAN & ANALYSIS: OpenSSF: gittuf

    This intake scan is a static analysis of the source code in your repository. A dependency scan was not performed. Once a project is added to LFX, you can use SNYK to view a dependency scan for both licenses and vulnerabilities.

CODE SCANNED: https://github.com/gittuf [pulled 22–Sept-2023]
3 repos scanned

PROJECT LICENSE: Apache-2.0

SPDX LICENSE IDENTIFIERS: SPDX license identifiers were not found in any source file headers.

    We recommend that SPDX license identifiers be added to ALL source file headers. [see https://spdx.dev/ids for examples]

PERMISSIVE LICENSES: Apache-2.0

COPYLEFT LICENSES: None found

PROPRIETARY LICENSES: None found

LICENSE CONFLICTS: None found

BINARY / PACKAGE FILES: None found

THIRD PARTY CODE / DEPENDENCIES: None found

THIRD PARTY NOTICE FILE: None found

SUMMARY FINDINGS: The code is licensed under the Apache-2.0 license, which is the project license. SPDX license identifiers were not found and should be added to all source file headers. No license conflicts found.
```

### Project References

| Reference                              | URL                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------|
| Repo                                   | https://github.com/gittuf/gittuf                                                                     |
| Website                                | https://gittuf.github.io                                                                             |
| Contributing guide                     | https://github.com/gittuf/gittuf/blob/main/CONTRIBUTING.md                                           |
| Roadmap                                | https://github.com/gittuf/gittuf/blob/main/docs/roadmap.md                                           |
| Demos                                  | https://github.com/gittuf/demo                                                                       |
| Presentation to the SCI WG             | https://docs.google.com/presentation/d/12ivx9LwMe1xgOvazMqXeJpkmK80Z-rhD1_CIy8T2d6I/edit?usp=sharing |
| Video Recording of SCI WG Presentation | https://zoom.us/rec/play/X1-avN0pWIzxWRQLpFSlDcjWVVsrZvdXta_6lK88Gvz2DbBReDYVJgDaDigdHAb0eoBvzhhBYQEaDWpt.CkXNT4amJEseG6q8 |
