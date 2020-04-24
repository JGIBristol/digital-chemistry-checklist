# Contributing to Chemspeed Helper

Welcome to the `chemspeed-helper` repository! We're excited you're here and want to contribute.

If you have any questions that aren't discussed below, please let us know by opening an [issue][issues_link]!

Before you start you'll need to set up a free [GitHub][link_github] account and sign in.
Here are some [instructions][link_signupinstructions].


## Joining the conversation

Most of our discussions about the documentation will take place on open [issues][issues_link], and we'd like to welcome you to join the discussions there. 


## Contributing through GitHub

[git][link_git] is a really useful tool for version control.
[GitHub][link_github] sits on top of git and supports collaborative and distributed working.

You'll use [Markdown][markdown] to chat in issues and pull requests on GitHub.
You can think of Markdown as a few little symbols around your text that will allow GitHub
to render the text with formatting.
For example you can write words as bold (`**bold**`), or in italics (`*italics*`).

GitHub has a helpful page on
[getting started with writing and formatting Markdown on GitHub][writing_formatting_github].


## Understanding issues

**Issues** are individual pieces of work that need to be completed to move the project forwards.
A general guideline: if you find yourself tempted to write a great big issue that
is difficult to describe as one unit of work, please consider splitting it into two or more issues.

## Repository Structure of this repository

In the 
[chemspeed-helper repository](https://github.com/Jean-Golding-Institute/chemspeed-helper), we keep all the documentation in the [documents](documents/) folder. 

We have two types of documents: general information for the design of the data management system, which are kept in the [documents](documents/) folder itself, and templates, which are designed to be edited, and distributed to users and technicians in research groups using Chemspeed machines. These are kept in [documents/templates](documents/templates/).

At the moment, we have the following documentation:
* [documents/our-approach.md](documents/our-approach.md): Gives an overview of our approach.
* [documents/it-setup.md](documents/it-setup.md): Explains how to set up a computer attached to a Chemspeed machine in order to facilitate our approach. Useful to share with your IT department. 
* [documents/templates/technician-template.md](documents/templates/technician-template.md): Template guidelines, for a technician working with users of a Chemspeed machine.
* [documents/templates/user-template.md](documents/templates/user-template.md): Template guidelines, for regular users of a Chemspeed machine.

## Making a change

We appreciate all contributions to `chemspeed-helper`, but those accepted fastest will follow a workflow similar to the following:

**1. Comment on an existing issue or open a new issue referencing your addition.**

This allows other members of the jupyter-book development team to confirm that you aren't overlapping with work that's currently underway and that everyone is on the same page with the goal of the work you're going to carry out.

[This blog][link_pushpullblog] is a nice explanation of why putting this work in up front is so useful to everyone involved.

**2. [Fork][link_fork] the [jupyter-book repository][link_jupyter-book] to your profile.**

This is now your own unique copy of jupyter-book.
Changes here won't effect anyone else's work, so it's a safe space to explore edits to the code!

Make sure to [keep your fork up to date][link_updateupstreamwiki] with the master repository.

**3. Make the changes you've discussed.**

Try to keep the changes focused. 

Working on a [new branch][link_branches] makes it easier to keep your changes targeted.

**4. Submit a [pull request][link_pullrequest].**

A member of the core team will review your changes to confirm that they can be merged into the main code base.
When opening the pull request, we ask that you follow some [specific conventions](#pull-requests).

Pull requests should be submitted early and often!

If your pull request is not yet ready to be merged, please open your pull request as a draft.
More information about doing this is [available in GitHub's documentation][link_drafts].
This tells the development team that your pull request is a "work-in-progress",
and that you plan to continue working on it.

When your pull request is Ready for Review, you can select this option on the PR's page,
and a project maintainer will review your proposed changes.


## Recognizing contributors

We welcome and recognize all contributions from documentation to testing to code development.
You can see a list of current contributors in the [README][contributors_link].

## Thank you!

You're awesome.

<br>

*&mdash; Based on contributing guidelines from the [Jupter Book][link_jupyter_book] project.*

[link_git]: https://git-scm.com
[link_github]: https://github.com/https://github.com/jupyter/governance/blob/master/conduct/code_of_conduct.md
[link_signupinstructions]: https://help.github.com/articles/signing-up-for-a-new-github-account

[writing_formatting_github]: https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github
[markdown]: https://daringfireball.net/projects/markdown

[link_pullrequest]: https://help.github.com/articles/creating-a-pull-request/
[link_fork]: https://help.github.com/articles/fork-a-repo/
[link_pushpullblog]: https://www.igvita.com/2011/12/19/dont-push-your-pull-requests/
[link_updateupstreamwiki]: https://help.github.com/articles/syncing-a-fork/
[link_branches]: https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/

[contributors_link]: https://github.com/Jean-Golding-Institute/chemspeed-helper/README.md
[jupyter_book_link]: https://github.com/ExecutableBookProject/jupyter-book/
[issues_link]: https://github.com/Jean-Golding-Institute/chemspeed-helper/issues
