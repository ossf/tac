# Special Interest Group (SIG) Life Cycle

Special Interest Groups are bound to achieving a very specific goal. These groups may be terminated upon completion of their designating tasking or continued for larger and ongoing efforts. The creation of a SIG must dictate the focus, intent, goals, and deliverable(s) as appropriate. SIGs may report to a WG or directly to the TAC as their governing body.

It is expected that the primary output of a SIG is not software. If the primary output is software, the work should be organized as a [project](./project-lifecycle.md).

SIG process should be minimal, however we do need some process to at least ensure we have an accurate list of all the active SIGs in the OpenSSF. This document uses "must" to describe what items are required, "should" to suggest items that should be strongly considered (but not required), and "may" for suggested guidance.

The SIG life cycle begins with interested contributors deciding to undertake this process, starting with the steps listed under "To become `Sandbox`". A SIG becomes `Sandbox` when a governing body determines the SIG has completed the listed steps, and the governing body agrees to take on the SIG. Then the SIG goes about achieving its goals and deliverables. Once that work is completed, or if the effort stalls out, the SIG becomes `Archived` and the listed administrative cleanup will be done. Here are the details for how to move through the phases:

## To become `Sandbox`:

* There must be a proposal of the focus, intent, goals, and/or deliverables of the SIG
  * This could be in an Issue of the governing body's repository, a shared document, or in a README of the SIGs repository (if they have one)
* The initial membership should be at least 3 individuals from 2 different organizations
* A governing body must agree to govern the SIG
  * The governing body may have its membership vote, with notice given at the meeting prior to the vote

## Once `Sandbox`:

* The governing body must list information about the SIG on its README, including current state, chairs, and a statement of focus, intent, goals, and/or deliverables
* SIGs may have regular meetings separate from their governing body, if so:
  * They should appear on the OpenSSF calendar
  * They should have a document with upcoming agendas and notes from past meetings
* If the SIG starts to produce code or specifications, they should consider becoming a [project](./project-lifecycle.md) instead

## To become `Incubating`:

* The governing body must agree that the SIG has made substantial progress on a deliverable

## Once `Incubating`:

* The governing body should update the state of the SIG on its README

## To become `Graduated`:

* The governing body must agree that the SIG has completed a major deliverable

## Once `Graduated`:

* The governing body should update the state of the SIG on its README

## To become `Archived`:

* The chairs of a SIG can decide to conclude their work, in which case they must notify their governing body
* The chairs of the governing body must periodically review their active SIGs and determine if any should end
  * This review should happen at least annually
  * The chairs of the governing body may have its membership vote, with notice given at the meeting prior to the vote

## Once `Archived`

* The governing body must update their README to reflect that the SIG has ended
  * They should list the SIG as end-of-life instead of removing it completely
* If a repository exists, it should be marked read-only
* If meetings are on the OpenSSF calendar, they should be removed
* Any other administrative items (mailing lists, docs) should similarly be put to closure as needed

## Submission Process

### SIG creation or change of lifecycle stage

SIGs can be created and managed without a formal vote from the TAC. However, for documentation purposes, group leads should record a lifecycle document when creating a SIG or changing a SIG's lifecycle stage. To this end, a SIG lead (or anyone in the case of an Archived SIG) creates a PR in this repository with the following changes:

* A new file in the `sig-lifecycle-documents` directory containing the information pertinent to the creation of the SIG or its lifecycle change. This file must be based on the template for the respective lifecycle stage in the `templates` directory. The `SIG_NAME_` prefix of the template must be replaced by the SIG name.

* Modification of the table listing all SIGs in the [README](../README.md) of this repository by either updating the status field of the SIG in the table to the intended new lifecycle stage or by adding the SIG to the table in case of a SIG creation.

Because no formal vote by the TAC is required, the PR can be merged by any TAC or staff member without needing a majority of the TAC to approve the PR.
