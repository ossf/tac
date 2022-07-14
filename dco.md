# Developer Certificate of Origin (DCO)

A [*Developer Certificate of Origin (DCO)*](https://developercertificate.org/)
is an affirmation that the source code being submitted originated
from the developer, or that the developer has permission to submit the code. 
It provides some additional legal protections while being
relatively easy to do.

The [OpenSSF Charter](https://cdn.platform.linuxfoundation.org/agreements/openssf.pdf)
section 5b requires DCOs. More specifically it says that
"Technical Initiatives will require that all new inbound source
code contributions must also be accompanied by a Developer Certificate
of Origin (https://developercertificate.org) sign-off in the source
code system that is submitted through a TAC-approved contribution
process...".

Adding a DCO is easy when you create a proposed change in git.
If you use `git commit`, just use its `-s` option. If you're making commits
by hand, just append `Signed-off-by: NAME <EMAIL>` to the commit message.
Note that these are not cryptographic (aka digital) signatures, but
instead a "sign off" saying that the commit complies with the
[Developer Certificate of Origin (DCO)](https://developercertificate.org/).

The TAC has chosen to implement this DCO requirement by automatically
enforcing DCOs on inbound pull requests across its GitHub organization.
This helps ensure that DCOs are really done.

If you'd like to enforce DCOs on your non-OpenSSF project on GitHub, you can
go to <https://probot.github.io/apps/dco/>,
click on "Add to GitHub" on the right,
and then select the repo/org & approve it.
This will add an integration with a GitHub app to enforce the check
(you can see this in a repo under its settings
Integrations / GitHub apps).
If you want to learn more about this probot DCO checker (which is
open source software), see:
<https://probot.github.io/apps/dco/>.
You can also enable
[GitHub's feature to require signoff of commits made through the web UI](https://github.blog/changelog/2022-06-08-admins-can-require-sign-off-on-web-based-commits/).


The email address must be, at the time the commit was created,
a valid email address that can be used to effectively contact
the committer if it is needed.

Please note that NAME does *not* need to be a legal name.
As explained by [Mike Dolan](https://github.com/cncf/foundation/issues/383#issuecomment-1178254458):

> The DCO is a representation by someone stating they have the right to contribute the code they have proposed for acceptance into a project. That representation is important for legal purposes and was the community-developed outcome after a $1 billion lawsuit by SCO against IBM. The representation is designed to prevent issues but also keep the burden on contributors low. It has proven very adaptable to other projects, is built into git itself (and now also GitHub), and is in use by thousands of projects to avoid more burdensome requirements to contribute (such as a CLA).
> ...
> The DCO requires the use of a real name that can be used to identify someone in case there is an issue about a contribution they made. A real name does not require a legal name, nor a birth name, nor any name that appears on an official ID (e.g. a passport). Your real name is the name you convey to people in the community for them to use to identify you as you. The key concern is that your identification is sufficient enough to contact you if an issue were to arise in the future about your contribution. Your real name should not be an anonymous id or false name that misrepresents who you are.
