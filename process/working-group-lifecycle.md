# Working Group (WG) Life Cycle

Working Groups are under the governance of the Technical Advisory Committee (TAC).

Contributors interested in starting a new WG are encouraged to first review the existing WGs and projects. It is very likely that an existing WG could be extended to cover the new topic. If this is the case, please bring your time and energy into that existing working group. Your contributions are very welcome!

However, if no existing effort covers the topic feel free to make use of the existing WG meetings, mailing lists, and/or Slack channels to solicit support for a new WG. WGs must align with and contribute to the [Mission, Vision, Values, Strategy, and Roadmap (MVVSR)](https://openssf.org/about/) of the OpenSSF.

Please note that running a WG successfully requires an extended effort. Be prepared to commit at least several hours per week for a year or more.

The WG Life Cycle begins with establishing commitments from other interested contributors then making a proposal to the TAC. If accepted, the WG will begin as `Sandbox`. This is a boot strapping phase for the group to define and document what their goals are.
Once the WG has further defined its goals and garnered enough support it can apply to move to 'Incubating' stage. This is the phase for the WG to adopt OpenSSF community policies and norms. Once those are met the group becomes `Graduated` and will be fully recognized in OpenSSF. Either upon completing its objectives or no longer making forward progress a project will move to `Archived`. The details for each phase follow.

## To become `Sandbox`:

* Proposal of scope for review by TAC
    * This is to help ensure limited overlap with existing WGs
* Have at least 3 interested individuals from at least 2 different organizations supporting the proposal
* 1 TAC sponsor
    * TAC sponsor agrees to attend WG meetings regularly
    * TAC sponsor does not need to have a formal role in WG, e.g., chair
    * TAC sponsor requests TAC approval
* TAC will vote to approve or provide constructive guidance

## Once `Sandbox`:

* The TAC will add the WG to the list of WGs to its README.
* If the WG has meetings at this stage:
  * They should appear on the OpenSSF calendar
  * The WG should have a document with upcoming agendas and notes from past meetings
* The WG should develop a charter or mission statement defining its goals.
* The TAC sponsor ensures the WG operates within the scope of the OpenSSF, adheres to the OpenSSF code of conduct, legal and IP policies, and reserves the right to consult with the TAC to raise any related concerns.
 
## To become `Incubating`:

* Have a charter or mission statement for review by TAC
* Have met at least 5 times within the last calendar quarter since becoming `Sandbox`
    * For these, meeting notes (or ideally recordings) must be public
* Have at least 5 contributors from at least 3 different organizations attending regularly
* TAC will vote to approve or provide constructive guidance
* TAC sponsor and WG chair(s) should decide on continued TAC sponsor engagement going forward. Continued engagement may include, but is not limited to:
    * WG chair(s) may consult about WG direction with TAC sponsor as needed throughout the Incubating stage
    * TAC sponsor should continue to monitor WG activities, though regular meeting attendance is optional.

## Once `Incubating`:

* Operate as part of the OpenSSF adhering to community policies
* Deliver quarterly reviews to TAC
* Complete and request TAC approval of [README.md](https://github.com/ossf/project-template/blob/main/README.md) which defines the WG's Charter and lists primary point(s) of contact from the TAC to the WG (this is often the WG Chair).
* Meet on a regular cadence. Meetings are public, recorded, and on the calendar
* The TAC sponsor continues to ensure the WG operates within the scope of the OpenSSF, adheres to the OpenSSF code of conduct, legal and IP policies, and reserves the right to consult with the TAC to raise any related concerns.
* Have access to community resources (Zooms, YouTube channels, GitHub, Slack channels, etc.)
* Can request funding/other resources (subject to TAC/GB approval)
    * NOTE: _At this time, funding and resources beyond collaboration tools have not been established in the OpenSSF. WGs should expect that their main resource is the community contributions they are able to recruit._

## To become `Graduated`:

* Have received TAC approval of the README.md per `Incubating` requirements above
* Have met at least 4 times over a period of at least 2 months since becoming `Incubating`
* Have at least 5 contributors from at least 3 different organizations attending regularly as recorded in meeting minutes.
* Request TAC approval. TAC will vote to approve or provide constructive guidance.
* TAC sponsor monitoring and consultation become optional.

## To remain `Graduated`:

A WG is expected to continue operating per the above guidelines, and to provide the TAC with quarterly status updates, and to approach the TAC when seeking approval of substantial changes (such as when accepting or promoting new Projects).

## Once `Graduated`:

* (same as incubating, plus)
* Have at least annual goals and metrics for success

## To become `Archived`:

* Work has stopped
    * The WG has completed its chartered deliverables
    or
    * The WG is no longer progressing on its deliverables as determined by the TAC
* In either case the TAC will vote to formally end the WG.

## Once `Archived`:

* All significant artifacts should be archived as appropriate
* Meeting series removed from calendar, mail list closed, and any other administrative items
  similarly put to closure as needed

## Submission Process

### Working Group creation or change of lifecycle stage

For initiating the creation of a new WG or for requesting a change of a WG lifecycle stage, an application must be submitted to the TAC. To this end, a lead of the WG (or anyone in the case of an Archived WG) creates a PR in this repository with the following changes:

* A new file in the `wg-lifecycle-documents` directory containing all information requested for a WG creation or a lifecycle change review. This file must be based on the template for the respective lifecycle stage in the `templates` directory. The `WG_NAME_` prefix of the template must be replaced by the WG name.

* Modification of the table listing all projects in the [README](../README.md) of this repository by either updating the status field of the WG in the table to the intended new lifecycle stage or by adding the WG to the table in case of a WG creation request.

The TAC members review the PR and upon approval according to voting criteria defined in the [OpenSSF charter](https://cdn.platform.linuxfoundation.org/agreements/openssf.pdf), the PR can be merged. The new WG has been created and the new lifecycle stage is in effect after the PR is merged.
