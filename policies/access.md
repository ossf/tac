# Github Access Management Policy

## Teams, not Individuals

Access to repositories will be granted only to Github teams, not to individuals. A repo may have any number of teams added to it, with the appropriate access levels.

## Team Structure

Teams will be nested, using parent/child relationships, as needed. A child team will implicitly have any privileges its parent team does, so, the most deeply nested team should be the one with the most privileges.

### Top-level teams

Note: this list is intentionally not exhaustive.

 - [TAC](https://github.com/orgs/ossf/teams/tac)
    This team is for current TAC members. Individuals should be added or removed from this team to reflect current membership.
 - [Staff](https://github.com/orgs/ossf/teams/staff)
    This team is for OpenSSF staff members. Individuals on the top-level team are there as a catch-all, but may be moved to subteams as the need arises.
    - [PMs](https://github.com/orgs/ossf/teams/pms)
      This teams is for PMs, who often need Maintain or Admin access on repos.
    - [Marketing](https://github.com/orgs/ossf/teams/marketing)
 - [Working Groups](https://github.com/orgs/ossf/teams/working-groups)
    This is the parent team for Working Groups. Every WG should have a subteam contained within this one. All WG subteams must start with `wg-` for consistency.
 - [SIGs](https://github.com/orgs/ossf/teams/sigs)
    This is the parent team for SIGs. Every SIG should have a subteam contained within this one. All SIG subteams must start with `sig-` for consistency.
 - [Projects](https://github.com/orgs/ossf/teams/projects)
    This is the parent team for projects. Every project (eg scorecard, AO) should have a subteam contained within this one.
    Teams for individual repositories go under here, which start with `repo-`, but team names may otherwise be unconstrained.

 ## Github Org Membership

 Membership in the Github org should be freely given - it inherently confers no permissions or privileges, only a badge on the user's profile if they enable it - and it _does_ allow for easier team management. Someone should only be removed from the org in extreme circumstances where their association with OpenSSF would be problematic, and people should be encouraged to remain in the org in perpetuity.

 Individuals who choose not to be a member of the org will be unable to retain access to repositories due to being ineligible to being on Github teams.

 ## Principle of Least Privilege

 Permission levels should be as high as they need to be, and no higher.

  - There's few settings that justify Admin access over Maintain, so prefer Maintain.
  - Explicit Read access has an advantage: users with Read can be assigned to issues and requested as PR reviewers even if they're not the author
