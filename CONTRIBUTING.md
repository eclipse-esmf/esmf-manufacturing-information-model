# Contribution Guideline ESMF I4.0 Core Information Model

Thank you for your interest in contributing to the ESMF I4.0 Core Information Model. Use this
repository to contribute to this specification as easy and transparent as possible, whether it is:

* Reporting a bug
* Discussing the current state of the Technical Specifications
* Submitting a fix
* Proposing new features
* other

With the remainder of this document, we want to support interested contributors in bringing in your
proposal.

# Contributing Source Code and Technical Specifications for this Project (using GitHub)
* We use this GitHub repository for the technical specifications related to this project, to track
  issues and feature requests, as well as discuss and manage all pull requests related to this
  project.
* Opening `Issues` and `PRs` in GitHub is the preferred way to interact with the community around
  this repository and the ESMF I4.0 Core Information Model.

## Branching
We follow the [Git branching guidance](https://docs.microsoft.com/en-us/azure/devops/repos/git/git-branching-guidance?view=azure-devops).

More specifically the repository has the following branches:

name of branch | description
----| ----
`main` | Contains the latest state of the repository
`v{version_number}-agreement` | A state on which the `maintainers` agreed on.
`v{version_number}` | A release of the respective version which is approved by the `maintainers`.
`feature/{feature-name}` | Contains the development on a specific feature and is intended to be
merged back into the `main` branch as soon as possible. Note, that it is recommended for
contributors to create and develop feature branches in a personal fork and not the upstream
repository.
`bug/{bug-name}` | Contains the development of (usually smaller) changes in files of the repository
that do not introduce new functionality but fix mistakes, errors or inconsistencies. These branches
should be merged back into the `main` branch as soon as possible.

## Issues
We use the `Issues` feature of GitHub for tracking all types of work in the repository.

We distinguish between the following types of issues;

Issue Types        |   Description
-------------------| ------------------------------------------------------
`Bug Report`         | This `Issue` is dedicated to reporting a problem.
`Task` | This `Issue` is used for describing and proposing a new work item (e.g., a new feature)

If there are issues that link to the same topic, the creator of the issue shall mention those other
Tasks in the description. To group tasks that can belong together, one could further create an issue
mentioning and describing the overall user story for the referenced tasks.

## Pull Requests
Proposals for changes to the content of the repository are managed through Pull Requests (`PRs`).

### Opening Pull Requests

To open such a `PR`, implement the changes in a new `feature branch`. Each `PR` must reference an
issue and follows the naming schema: `<issue-number>-<feature-name>`. For a new `PR` the target
branch is the `main` branch while the source branch is your `feature branch` The `feature branch`
branch should be developed in a fork of the upstream repository. So before working on your first
feature, you need to create such a fork (e.g., by pressing the `Fork` button in the top right corner
of the GitHub page)

When opening a `PR` please consider the following topics:

* optional: Rebase your development on the branch to which you plan to create the `PR`.
* Each `PR` must be linked to an `Issue`:
    - Reference the `Issue` number in the name of your `feature branch` and the description of the
      `PR`.
    - Mention the `Issue` in one of the commit messages associated to the `PR` together with a
      GitHub keyword like `closes #IssueNumber` or `fixes #IssuesNumber`. For more details visit the
      [GitHub documentation on linking PR with
      Issues](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword)

* Each `PR` should only contain changes related to a single work item. If the changes cover more
  than one work item or feature, then create one `PR` per work item. You may need to create new more
  specific `Issues` to reference if you split up the work into multiple `feature branches`.
* Commit changes often. A `PR` may contain one or more commits.

## Eclipse Development Process

This Eclipse Foundation open project is governed by the Eclipse Foundation Development Process and
operates under the terms of the Eclipse IP Policy.

* https://eclipse.org/projects/dev_process
* https://www.eclipse.org/org/documents/Eclipse_IP_Policy.pdf

## Eclipse Contributor Agreement

In order to be able to contribute to Eclipse Foundation projects you must electronically sign the
Eclipse Contributor Agreement (ECA).

* http://www.eclipse.org/legal/ECA.php

The ECA provides the Eclipse Foundation with a permanent record that you agree that each of your
contributions will comply with the commitments documented in the Developer Certificate of Origin
(DCO). Having an ECA on file associated with the email address matching the "Author" field of your
contribution's Git commits fulfills the DCO's requirement that you sign-off on your contributions.

For more information, please see the Eclipse Committer Handbook:
https://www.eclipse.org/projects/handbook/#resources-commit


## Labeling
After new `Issues` or `PRs` are created, the `bug` and `task` label will be added automatically
according to the chosen issue type. Later on one of the `maintainers` may further assign a `label` to
it according to this table:

Label Types        | Description
-------------------| ----------------------------------------
`to be discussed`        | Involvement and discussion of the `maintainers` are needed.
`request for information`| The `maintainers` are requesting further information from the creator of
the `Issue` or `PR`. If for a pre-defined time no information is received, then the `Issue` or `PR`
can be closed.
`approved` | Has been discussed and approved by the `maintainers`.
`not accepted` | Has been discussed by the `maintainers` with the decision to close this issue.

### PR or Issue Discussion and Decision

* You can provide comments to any `PR` or `Issue` via the comment function in GitHub

* If no further involvement from the `maintainers` is required, a `maintainer` may merge a `PR`. This
  mostly applies to bug fixes when no substantial changes are performed. A `PR` for a bug fix may
  reference an issue of type `Bug Report`.

* The `maintainers` may assign the label `to be discussed` to a proposal. This then triggers the
  following steps:
1. The `maintainers` put the proposal up for discussion in one of the next `maintainers` meetings.
2. The `maintainers` then use Consensus Decision-Making with one of the following outcomes:

| Decision | Next Steps |
| ------ | ------- |
|`Approved`| The `Issue` or the `PR` gets the label `approved`. In the case of a `PR`, the `maintainers` merge the respective `PR`. |
| `Discussion`| The `Issue` or the `PR` get the label `request for information`.
|`Close` | The `Issue` or the `PR` are closed and get the label `not accepted`. |

3. The label `to be discussed` is removed.

* If the `maintainers` feel that further information is required to explain a `PR` or an `Issue`,
  they may request this information through the comment section of the `PR` or `Issue` and assign
  the label `request for information`. The `maintainers` may close the issue if no answer is
  received after a pre-defined time.

Note, that merging a `PR` leads to the closing of the `Issue` if it is linked in the `PR`.

### Review Checklist
The following checklist can be seen as a basis for performing reviews on new `PRs`:

- [ ] brief and useful commit messages
- [ ] document style is followed
- [ ] the contribution matches to the linked issue and the description of the PR
- [ ] provide clear documentation of new features (if applicable)
- [ ] outline added third party dependencies

### Commit Messages
Separate the subject from the body with a blank line because the subject line is shown in the Git
history and should summarize the commit body. Use the body to explain what and why with less focus
on the details of the how. This [blog post](https://chris.beams.io/posts/git-commit/#seven-rules)
has more tips and details. Before you push your commits to a repository, you can squash your commits
into one or more logical units of work, e.g., if you want to add a new feature solely in a single
commit.

## License Headers & Licensing
All files contributed require headers - this will ensure the license and copyright clearing at the
end. Also, all contributions must have the same license as the source. The header should follow the
following template:

```
////
Copyright (c) {YEAR} {NAME OF COMPANY X}
Copyright (c) {YEAR} {NAME OF COMPANY Y}

See the AUTHORS file(s) distributed with this work for additional information regarding authorship.

This Source Code Form is subject to the terms of the Mozilla Public License, v. 2.0.
If a copy of the MPL was not distributed with this file, You can obtain one at https://mozilla.org/MPL/2.0/
SPDX-License-Identifier: MPL-2.0
////
```

When using the template, one must replace "{NAME OF COMPANY X}" with the name of the involved
companies and "{YEAR}" with the year of the contribution. For each involved company you need a new
line starting with "Copyright" as outlined in the example.

This example uses the Commenting Option of Ascii-Doc, so if your file is of another type you may
have to adapt the comment syntax accordingly.

If you use third-party content (e.g., import / include ...), you are required to list each
third-party content explicitly with its version number in the documentation and your pull-request
comment. Please note that software licensed under GPL, AGPL or, a similar strong copy-left license
cannot be approved.

## Versioning
We use Semantic Versioning to identify versions of published ESMF SDS I4.0 Information Model
Ontologies and Knowledge Graphs. Semantic Versioning is documented [here] (https://semver.org). It
proposes to have a versioning number with the following elements:

````
Given a version number MAJOR.MINOR.PATCH, increment the:
- MAJOR version when you make incompatible API changes,
- MINOR version when you add functionality in a backwards compatible manner, and
- PATCH version when you make backwards compatible bug fixes.
Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.
````

Whereas the Major version must be incremented if the API has backward-incompatible changes (e.g.,
has breaking changes), the Minor version must be changed if new backward-compatible features are
introduced and, the Patch version must be incremented if backward-compatible bugfixes are
introduced.

### Pre-Release
The `maintainers` may decide to add a pre-release identifier to the release number. This identifies
the state of the released content as agreed but not finalized and thus being subject to change.
Hence, it is not advised to use releases which include a pre-release identifier for productive
scenarios.

For the pre-release identifieres the `maintainers` distinguish between the following:
* "M" - Milestone: A milestone release represents an intermediate state on the path to a new actual
  release. There is the option for further breaking changes between a milestone and the subsequent
  release. The aim of a milstone release is to allow early adopters to make first evaluation of new
  features.
* "RC" - Release Candidate: A release candidate that may be released prior to an actual release to
  allow final testing and feedback. Hence, the differences between the subsequent release and the RC
  should be as small and do not add new major features.

### Breaking Changes
For the definition of a breaking change, we follow the definition as in the [Microsoft REST API
Guidelines](https://github.com/Microsoft/api-guidelines/blob/vNext/Guidelines.md#123-definition-of-a-breaking-change)
which are licensed under [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0). This definition
states:

```
Changes to the contract of an API are considered a breaking change. Changes that impact the
backwards compatibility of an API are a breaking change.
```

In the context of the ESMF I4.0 Core Information Model, one may consider the names of entities and
relationships between the different elements of the ESMF I4.0 Core Information Model in a wider
sense as some kind of API. So to evaluate whether a change is breaking or not, one needs to consider
the implications and required changes in the specific models that are based on the ESMF I4.0 Core
Information Model.

The following table gives examples for breaking and non-breaking changes:

Examples for non-breaking changes are:
* Adding a new Entity, Property or Relationship
* Changing the label or comment of a Property, Entity or Relationship
* Extending existing entities, properties or relationships using subclassing or sub-property relationships
* Making a mandatory Property optional

Examples for breaking changes are:
* Renaming an existing Entity, Property or Relationship
* Removing an existing Entity, Property or Relationship
* Change of the relationship between two entities (e.g. inheritance, aggregation, composition, etc.)

### Version Syntax for Specific Environments

Git version tag

vX.Y.Z-[pre-release-identifier]

Examples:

v1.0.0-RC1, v1.0.0

# Resources

## GitHub Resources
* [For a Repo](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork)
* [Issue Creation](https://help.github.com/en/github/managing-your-work-on-github/creating-an-issue)
* [PR Creation](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)
