# OpenSSF Labs

<!-- What other names might we consider instead of "OpenSSF Labs"? -->

The OpenSSF Labs provide a space for open source projects that are in the
earliest stages of their lifecycle to experiment, foster collaboration, and grow
their community prior to transitioning into the OpenSSF [project lifecycle].

<!-- Right now, the focus is on Projects, but should we consider broadening the labs to any type of TI? -->

OpenSSF Labs follow a similar model to Hyperledger Labs.

## Benefits

The OpenSSF Labs provide OSS developers several benefits:

* A common governance and legal framework under the OpenSSF that
facilitates cross-organization or -vendor collaboration.
* The lowest barrier to starting brand new projects.
* A dedicated GitHub repository, if starting a lab from scratch.
* A streamlined transition into the [Sandbox] stage of the OpenSSF [project
lifecycle].

## Project Responsibilities

Developers of OpenSSF labs are responsible for:

* Submitting a [new lab proposal] for review by the [OpenSSF TAC].
* Ensuring all commits are properly signed-off to avoid issues related to [DCO].
* Notifying the TAC if the lab needs to be suspended or archived.

Labs projects are also highly encouraged to engage with the [existing
Technical Initiatives] (working groups, projects or SIGs) in OpenSSF to build
their community and find a potential pathway towards acceptance as an OpenSSF
project.

## Archiving

The TAC will periodically check on the activity of labs. Labs that have been
inactive for an extended period (6+ months), or are explicitly suspended by
the maintainers, will be marked as "archived" in GitHub.

Archived labs are not actively maintained and read-only, and can be reactivated
if there is interest in resuming work on a project.

## New Lab Proposal Process

1. Fork the <TBD> repo.

2. Fill out the [proposal template](templates/LAB_NAME_lab.md)
   and save it into the `labs` subdirectory under the name of your lab,
   such as `coolnewproject_lab.md`.
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
     2. engage with [existing Technical Initiatives] (working groups, projects
	    or SIGs) with affinities to the proposed lab and pitch the project in
		their meetings or [Slack channels](https://slack.openssf.org/). It's
		good to have the template already filled out when you reach out.
   <br>
> [!IMPORTANT]
> Lab sponsors may but are not required to actively participate in
> the lab once the proposal has been reviewed and accepted.

4. Commit your changes with proper sign-off. This means that your commit
   log message must contain a line that looks like the following one,
   with your actual name and email address:

   `Signed-off-by: John Doe <john.doe@example.com>`

   Adding the `-s` flag to your `git commit` command will add that line
   automatically. You can also add it manually as part of your commit
   log message or add it afterwards with `git commit --amend -s`.

5. Submit a Pull Request to the <TBD> repo.

The [OpenSSF TAC] will then review your proposal. Like sponsors, TAC members may
but are not required to participate in ongoing work like contributing or
reviewing code in the lab.

### Transferring an existing repository

By default, OpenSSF staff will create a new GitHub repository for you to
start a new lab in. If you have an existing GitHub repo you would like to
bring to your proposed lab, you have the option to request for that
repo to be transferred into the <TBD GH org> instead.

However, we require that every commit in the existing repo to br
signed-off so there are no issues related to [DCO].
If that is not the case, you will need to transfer your existing code by
squashing all of your commits into a single first commit made against
your new lab repo with your sign-off.

### License requirement

<!-- This is something that other Labs require of the projects they host. What, if any requirements should we include here? -->

## Code of Conduct

All OpenSSF community members must adhere to the
[Code of Conduct](https://openssf.org/community/code-of-conduct/).

[DCO]: https://developercertificate.org/
[existing TIs]: https://github.com/ossf/tac/blob/main/README.md#technical-initiatives
[new lab proposal]: #new-lab-proposal-process
[OpenSSF mission]: https://openssf.org/about/
[OpenSSF TAC]: https://github.com/ossf/tac/blob/main/README.md#tac-members
[project lifecycle]: https://github.com/ossf/tac/blob/main/process/project-lifecycle.md
[Sandbox stage]: https://github.com/ossf/tac/blob/main/process/project-lifecycle.md#sandbox
