# OpenSSF Labs

The OpenSSF Labs provide a space for open source projects that are in the
earliest stages of their lifecycle to experiment, foster collaboration, and grow
their community prior to transitioning into the OpenSSF [project lifecycle].

OpenSSF Labs follow a similar model to Hyperledger Labs.

## Benefits

The OpenSSF Labs provide OSS developers several benefits:

* A common governance and legal framework under the OpenSSF that
facilitates cross-organization or -vendor collaboration.
* The lowest barrier to starting brand new projects.
* A dedicated GitHub repository, if starting a lab from scratch.
* A streamlined transition into the [Sandbox stage] of the OpenSSF [project
lifecycle].

## Lab Responsibilities

Developers of OpenSSF labs are responsible for:

* Submitting a [new lab proposal] for review by the [OpenSSF TAC].
* Ensuring all commits are properly signed-off to avoid issues related to
  Developer Certificate of Origin ([DCO]).
* Notifying the TAC if the lab needs to be suspended or archived.

Labs are also highly encouraged to engage with the existing
Technical Initiatives (working groups, projects or SIGs) in OpenSSF to build
their community and find a potential pathway towards acceptance as an OpenSSF
project.

## New Lab Proposal Process

1. Fork the `github.com/openssf-labs/process` repo.

2. Fill out the [proposal template](templates/LAB_NAME_lab_stage.md)
   and save it into the `active` subdirectory under the name of
   your lab, such as `coolnewlab.md`.
   <br/>
> [!TIP]
> It is expected that your lab repository on GitHub will have the same
> name as the proposal, so keep that in mind when submitting your proposal.

3. In the proposal template, there is an entry for sponsor(s). Although this
   is not required, proposers are encouraged to seek a sponsor in the OpenSSF
   community who can help them create ties with the rest of the community
   and review the proposal to make sure it is novel and aligned with the
   [OpenSSF mission].
   <br/>
   To find sponsors:
     1. use your connections to existing projects and ask maintainers,
     2. engage with existing [working groups](https://openssf.org/community/openssf-working-groups/) and [projects](https://openssf.org/projects/)
	with affinities to the proposed lab and pitch it in their
	[public meetings] or [Slack channels](https://slack.openssf.org/). It's
	good to have the template already filled out when you reach out.
   <br>
> [!IMPORTANT]
> Lab sponsors may, but are not required to, actively participate in
> the lab once the proposal has been reviewed and accepted.

4. Commit your changes with proper sign-off. This means that your commit
   log message must contain a line that looks like the following one,
   with your actual name and email address:

   `Signed-off-by: John Doe <john.doe@example.com>`

   Adding the `-s` flag to your `git commit` command will add that line
   automatically. You can also add it manually as part of your commit
   log message or add it afterwards with `git commit --amend -s`.

5. Submit a Pull Request to the `github.com/openssf-labs/process` repo.

The [OpenSSF TAC] will then review your proposal. Like sponsors, TAC members
may, but are not required to, participate in ongoing work like contributing or
reviewing code in the lab.

### License requirement

OpenSSF Labs must use one of the following licenses as required in section 4a
of the [OpenSSF charter](https://charter.openssf.org/):

#### Software source code

(1) Apache License, Version 2.0, available at [https://www.apache.org/licenses/LICENSE- 2.0](https://www.apache.org/licenses/LICENSE- 2.0); or

(2) MIT License available at [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

#### Data

Any of the Community Data License Agreements, available at [https://www.cdla.io](https://www.cdla.io)

#### Specifications

Community Specification License, Version 1.0, available at [https://github.com/CommunitySpecification/1.0](https://github.com/CommunitySpecification/1.0)

#### All other Documentation

(1) Creative Commons Attribution 4.0 International License, available at [https://creative commons.org/licenses/by/4.0/](https://creative commons.org/licenses/by/4.0/)

### Transferring an existing repository

By default, OpenSSF staff will create a new GitHub repository in the ossf-labs
organization for you to start a new lab in. If you have an existing GitHub repo
you would like to bring to your proposed lab, you have the option to request
permission to transfer that repo into the openssf-labs GitHub organization
instead. This request is noted as part of the [new lab proposal].

However, we require that every commit in the existing repo to bring is
signed-off so there are no issues related to [DCO].
If that is not the case, you will need to transfer your existing code by
squashing all of your commits into a single first commit made against
your new lab repo with your sign-off.

**Note**: We strongly recommend that existing repos follow the
[lab license requirements](#license-requirement). A full intellectual property
(IP) and legal review is not needed for OpenSSF Labs, but will be required if
the lab seeks to transition to [Sandbox stage].

## Archiving

The TAC will periodically check on the activity of labs. Labs that have not been
actively maintained for an extended period (6+ months), or are explicitly
suspended by the maintainers, will be moved into the Archived stage.

### Archiving process

1. Submit a Pull Request to the `github.com/openssf-labs/process` repo.

Move the LAB_NAME_lab_stage.md from the `active` to the `archived` directory.

2. Mark the lab repository as archived.

Once the PR is merged, OpenSSF staff will mark the archived lab repository as
"archived" (read-only) on GitHub. The repo can be reactivated if there is
interest in resuming work on a lab. Please open a PR moving the lab document
back into the `active` directory in the `openssf-labs/process` repo.

## Code of Conduct

All OpenSSF community members must adhere to the
[Code of Conduct](https://openssf.org/community/code-of-conduct/).

[DCO]: https://developercertificate.org/
[new lab proposal]: #new-lab-proposal-process
[OpenSSF mission]: https://openssf.org/about/
[OpenSSF TAC]: https://github.com/ossf/tac/blob/main/README.md#tac-members
[project lifecycle]: https://github.com/ossf/tac/blob/main/process/project-lifecycle.md
[public meetings]: https://calendar.google.com/calendar/u/0/embed?height=600&wkst=1&bgcolor=%238E24AA&ctz=America/New_York&showTitle=1&mode=WEEK&showCalendars=0&showTabs=1&showPrint=0&title=OpenSSF+Community+Calendar&src=czYzdm9lZmhwNWk5cGZsdGI1cTY3bmdwZXNAZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ&color=%238E24AA
[Sandbox stage]: https://github.com/ossf/tac/blob/main/process/project-lifecycle.md#sandbox
