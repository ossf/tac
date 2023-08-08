# Special Interest Group (SIG) Life Cycle

Special Interest Groups are bound to achieving a very specific goal. These groups may be terminated upon completion of their designating tasking or continued for larger and ongoing efforts. The creation of a SIG must dictate the focus, intent, goals, and deliverable(s) as appropriate. SIGs may report to a WG or directly to the TAC as their governing body.

It is expected that the primary output of a SIG is not software. If the primary output is software, the work should be organized as a [project](./project-lifecycle.md).

SIG process should be minimal, however we do need some process to at least ensure we have an accurate list of all the active SIGs in the OpenSSF. This document uses "must" to describe what items are required, "should" to suggest items that should be strongly considered (but not required), and "may" for suggested guidance.

The SIG life cycle begins with interested contributors deciding to undertake this process, at which time the SIG is `Tentative`. A SIG becomes `Active` when a governing body agrees to take it on, at which point the SIG goes about achieving its goals and deliverables. Once that work is completed, or if the effort stalls out, the SIG becomes `End-of-Life` and some administrative cleanup will be done. The details for each phase follow.

## To become `Tentative`:

* This is the default state of a new SIG that is not yet active

## To become `Active`:

* A governing body must agree to govern the SIG
  * The governing body may have its membership vote, with notice given at the meeting prior to the vote

## Once `Active`:

* The governing body must list information about the SIG on its README, including current state, chairs, and a statement of focus, intent, goals, and/or deliverables
  * SIGs may have a repository (prefixed with `sig-`) that include the information listed above
* SIGs may have regular meetings separate from their governing body, if so:
  * They should appear on the OpenSSF calendar
  * They should have a document with upcoming agendas and notes from past meetings

## To become `End-of-Life`:

* The chairs of a SIG can decide to conclude their work, in which case they must notify their governing body
* The chairs of the governing body must periodically review their active SIGs and determine if any should end
  * This review should happen at least annually
  * The chairs of the governing body may have its membership vote, with notice given at the meeting prior to the vote

## Once `End-of-Life`

* The governing body must update their README to reflect that the SIG has ended
  * They should list the SIG as end-of-life instead of removing it completely
* If a repository exists, it should be marked read-only
* If meetings are on the OpenSSF calendar, they should be removed
* Any other administrative items (mailing lists, docs) should similarly be put to closure as needed
