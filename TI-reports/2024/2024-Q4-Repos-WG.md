# 2024 Q4 Securing Software Repositories (Repos) WG

## Overview

**Mission**: Improve security of software repositories by providing a forum for discussion, a maturity model for security roadmaps, and guidance for individual security capabilities.

**Links**:
- [GitHub repository](https://github.com/ossf/wg-securing-software-repos)
- [Slack channel](https://openssf.slack.com/archives/C034CBLMQ9G)
- [WG meeting docs](https://docs.google.com/document/d/1HzA4M4toiExUYQAkuLqimy4EuuunHagUQ7rZKJDb1Os/edit?usp=sharing)

**Latest News**:

[Last update June 2024](https://docs.google.com/presentation/d/1PWxTw8yiSnLlClMK0K83hff5XHnkKDkw0OYM0ldWKsk/edit?usp=sharing)

- Published [Trusted Publishing for All Package Repositories](https://repos.openssf.org/trusted-publishers-for-all-package-repositories)
  - Cited by [Rust Crates.io Trusted Publishing RFC](https://github.com/rust-lang/rfcs/pull/3691)
  - Also cited by [NuGet Trusted Publishing RFC](https://github.com/NuGet/Home/pull/13673)
  - Trusted publishing is a stepping stone for further attestations, see [PEP-0740](https://peps.python.org/pep-0740/)

- Repository Service for TUF (RSTUF) proof of concept with RubyGems and PyPI
  - Working towards v1.0 release

- Working on [Binary Transparency for Artifact Registries](https://github.com/ossf/wg-securing-software-repos/pull/48)

## Securing Software Repositories Working Group

### Purpose

Improve security of software repositories by providing a forum for discussion, a maturity model for security roadmaps, and guidance for individual security capabilities.

### Current Status

- Helping security capabilties move from ecosystem to ecosystem
  - Trusted publishing: PyPI -> RubyGems -> NuGet -> Rust Crates
  - Signing / provenance / attestations: npm -> Homebrew -> PyPI -> Maven Central

- Support for [PEP-0740: Index support for digital attestations](https://peps.python.org/pep-0740/)
  - CPython + 10k+ Python packages with trusted publishing could be a critical mass for OS package repositories to implement support for in-toto attestations signed by public good Sigstore instance

### Up Next

- Working on [Binary Transparency for Artifact Registries](https://github.com/ossf/wg-securing-software-repos/pull/48)

### Questions/Issues for the TAC

- None at this time

## RSTUF Project

### Purpose

Provide a service to protect repository index from tampering by distributing them with The Update Framework (TUF) 

### Current Status

- Proof of concept with RubyGems and PyPI

### Up Next

- Working towards v1.0 release

### Questions/Issues for the TAC

- None at this time

## Additional Information

[Tracking ~30 security improvements over ~10 ecosystems over the past 2 years](https://docs.google.com/spreadsheets/d/1JydRQSJ2jTHREmWXXlzlFdhKJ_sY7cORKp_6AI6mRNw/edit?usp=sharing)

