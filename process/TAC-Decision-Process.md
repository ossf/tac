# TAC Decision Process #

The OpenSSF Technical Advisory Council (TAC) is a body comprised of 9 individuals that are either elected for a 2 year term or appointed by the governing board for a 1 year term.  

The election and appointment processes are described in a [separate document](/elections/tac-and-scir-election-process.md).

The TAC has a [chairperson and vice-chairperson](./tac-member-R&Rs.md#tac-chair) that are elected by the TAC members annually and are responsible for coordinating the work of the TAC.

Broadly, there are three main methods that the TAC will use to make decisions and ensure those decisions are appropriately documented:

## 1.) Simple and/or non-consequential changes ##
For asynchronous work items that do not have long-term/strategic consequences, the TAC will use lazy consensus to determine whether to adopt the proposal and ensure that it will be properly documented.  Issues and PRs should be created within the TAC GitHub repository and assigned to the TAC group for review.  Provided that at least two TAC members agree, support, and approve the suggested change, there are no objections raised by any TAC members, and no less than one week has transpired since the TAC was notified of the change, the proposal will be merged and adopted.

This includes such things as documentation updates/minor changes


## 2.) For work items discussed at the periodic TAC calls ##
The TAC must have quorum (majority of members present) and a simple majority of the members present must approve of a proposal or topic.  This decision will be captured in the TAC meeting notes as well as an issue within the TAC repository. 



## 3.) For  major items that require a formal vote ##
An issue or PR must be created within the TAC repository.  TAC members will be asked via the TAC mailing list to review, comment, and decline/approve the item within the GitHub issue/PR.  The TAC will be given 10 business days to review and consider the request.  These topics ideally should also be presented at a TAC meeting and publicly discussed/debated prior to the closing of voting.  

This includes items such as changes to the TAC technical vision, Foundation strategy, WG/project adoption, funding requests, adopting new Working Group, etc.).

# Issue/Pull request types #

Every Issue/PR must be categorized using one of the following <type> values. The purpose is twofold: to make it easier for readers to understand the scope of the PR at a glance, and to allow us to adjust the minimum review period and number of approvers based on how sensitive the Issue/PR is.

Use the closest entry in the table that applies, selecting the first one if multiple apply. If you are not sure which type to use, take a guess and a maintainer will update if needed.

|  Type  | Meaning | Waiting period |	# Approvers |
| ------ | ------- | -------------- | ----------- |
| Major  | Proposed changes to Charter, Technical Strategy, adopting a new TI, modifications to the TI Lifecycle process, or other cross-foundation changing proposals.  If approved, certain proposals will be moved to the Governing committee for review, move to GB. | 15d | 7 |
| TI Lifecycle | Filed PRs for movement of TIs to new stages of the TI Lifecycle | 10d | 5 |
| TI Funding Request | Issues opened by eligible OpenSSF Technical Initiative to petition for resources/funding. TAC review happens at the end of a quarterly submission period. If approved, recommended requests will be moved to the OpenSSF General Manager and the Governance Committee for dispensation. | 7d | 5 |
| TI Update | Issues opened by TI leads to document their quarterly update to the TAC. | 7d | 5 |
| Content |	A change to the process. Must include a changelog entry. |	72h |	3 |
| Editorial |	A clarification to the process that does not change its requirements or meaning, beyond a simple fix. |	24h |	2 |
| Nonspec | 	A change to a non-specification, non-blog page, beyond a simple fix. |	24h |	2 |
| Fix |	A fix for obvious typos, broken links, and similar. |	0h |	1 |
| Style |	A user-visible style or layout change. No content changes. |	0h |	1 |
| Impl | 	A user-invisible change, such as editing a README or the repo configuration. |	0h | 	1 |
