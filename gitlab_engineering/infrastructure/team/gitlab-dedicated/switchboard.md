---
title: Switchboard team
---

## Summary

Switchboard is a team within the [Dedicated Group](/handbook/engineering/infrastructure/team/gitlab-dedicated/). Our mission is to empower external GitLab Dedicated customers to manage their tenant environments and reduce the operational overhead on the Environment Automation team so we can scale up the GitLab Dedicated offering. We follow the same processes as listed on the [the Dedicated Group](/handbook/engineering/infrastructure/team/gitlab-dedicated/), unless a difference exists which is explicitly noted on this page.

### Resources

- [Switchboard Direction Page](https://about.gitlab.com/direction/saas-platforms/switchboard/)
- [Switchboard Demo Library](https://gitlab.com/gitlab-com/gl-infra/gitlab-dedicated/switchboard/-/blob/main/docs/walkthrough-library.md)

## Team Members

{{< team-by-manager-slug "ashiel" >}}

Product Manager: [Loryn Bortins](/handbook/company/team/#lbortins)
Technical Writer: [Lysanne Pinto](/handbook/company/team/#lyspin)
Product Designer: [Divya Alagarsamy](/handbook/company/team/#divyaalagarsamy)

## Working with us

To engage with the Switchboard team:

- [Create an issue](https://gitlab.com/gitlab-com/gl-infra/gitlab-dedicated/team/-/issues/new) in the GitLab Dedicated team issue tracker
- Label the issue with:
  - `component::Switchboard`
  - `workflow-infra::Triage`
  - `team::Switchboard`
- When creating an issue, it is not necessary to `@`mention anyone
- In case you want to get attention, use a specific team handle (Ex: @gitlab-dedicated/switchboard ) as defined in [Dedicated group hierarchy](/handbook/engineering/infrastructure/team/gitlab-dedicated/#gitlab-group-hierarchy)
- [Switchboard issue board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/4498935?label_name[]=component%3A%3ASwitchboard) tracks all of the team's current work
- We are in the process of adapting to use the [Product Development Flow](/handbook/product-development-flow/)

- Slack channels
  - For Switchboard specific questions, you can find us in [#g_dedicated-switchboard-team](https://gitlab.slack.com/archives/C04DG7DR1LG)
  - Our Slack group handle is `@dedicated-switchboard-team`
  - Other teams in Dedicated group have their own work channels for team work discussions:
      - [#g_dedicated-team](https://gitlab.slack.com/archives/C025LECQY0M)
      - [#g_dedicated-us-pubsec](https://gitlab.slack.com/archives/C03R5837WCV)

## Requesting Access to the Switchboard application

- Create an [Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Individual_Bulk_Access_Request) specifying
   - the specific environment ( Test / Beta / Production )
   - level of access required (Readonly, Support, Provisioner, Operator)
   - justification for the access
- Access & Provision Details for the application can be found in the `Switchboard - GitLab Dedicated` section of the [Tech Stack](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/d3561ab939029faf4ac25f32612c57e861eb8b39/data/tech_stack.yml)

## How we work

### Meetings and Scheduled Calls

Our preference is to work asynchronously, within our project issue tracker as described in [the project management section](/handbook/engineering/infrastructure/team/gitlab-dedicated/#project-management).

The team does have a set of regular synchronous calls:

- `Switchboard Sync` - During this call, we are sharing important information for team-members day-to-day, as well as project items requiring a sync discussion
- 1-1s between the Individual Contributors and Engineering Managers

Impromptu Zoom meetings for discussing Switchboard work between individuals are created as needed.
It is expected that these meetings are private streamed, or recorded(1*), and then uploaded to [GitLab Unfiltered playlist](https://www.youtube.com/playlist?list=PL05JrBw4t0Kp3NBMl7c0DGXCjW5rSPeOK).
The outcome of the call is shared in a persistent location (Slack is not persistent). This is especially important as the team grows, because any decisions that are made in the early stage have will be questioned in the later stages when the team is larger.

`1*` Exceptions to the recording rule are: 1-1 calls, discussions around non-project work, and in cases where parties do not feel comfortable with recording or we cannot record due to the nature of content discussed. However, even with the exceptions, outcome of project related discussions need to be logged in a persistent location, such as the main issue tracker.

### Tracking & Planning Work

#### Resources
- [Switchboard team roadmap](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/roadmap?state=all&sort=start_date_asc&layout=WEEKS&timeframe_range_type=CURRENT_QUARTER&label_name[]=team::Switchboard&progress=COUNT&show_progress=true&show_milestones=false&milestones_type=ALL&show_labels=false)
- [Switchboard team top-level epic](https://gitlab.com/groups/gitlab-com/gl-infra/-/epics/1048)
- [Switchboard team issue board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/4498935?label_name[]=team%3A%3ASwitchboard)
- [Switchboard technical writing board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/7068209?label_name[]=component%3A%3ASwitchboard&label_name[]=Technical%20Writing)
- [Dedicated Issue Tracker](https://gitlab.com/gitlab-com/gl-infra/gitlab-dedicated/team/-/issues/?sort=created_date&state=opened&first_page_size=100)

#### Quarterly Planning

Quarterly planning is owned and driven by the Switchboard EM and PM.

1. EM or PM creates a quarterly planning issue using the Dedicated `quarterly_planning` issue template.
    - Set the issue title to `Switchboard - FYXXQY planning` where XX is the year and Y is the quarter
    - Ideally planning should be kicked off at least a quarter in advance. The planning issue for the upcoming quarter should be created on or before the first day of the second month of the current quarter

2. EM & PM brainstorm asynchronously on the issue
3. During month 3 of the current quarter EM or PM
   - Reach out to the team for input
   - Ensure all dependencies are communicated with the relevant teams
   - Prioritise the objectives
   - Document the associated epics
4. EM creates a delivery epic for the quarter that will be used in Grand Reviews and updates the epic-summaries bot to reflect this change

#### Epic Refinement

Switchboard team process to refine epics:
1. Identify a [DRI](/handbook/people-group/directly-responsible-individuals/) for the epic
   - Team members can volunteer or the EM may ask team ask specific team members to act as DRI
1. Identify any missing requirements
   - All team members ask questions in the comments of this issue to drive out any edge cases
1. DRI labels the epic as ~"workflow-infra::Ready"
1. Assign Due Date & Start Date
   - DRI, EM & PM work together to assign due date based on team capacity, external deadlines and amount of work involved
1. DRI identifies at least one demo that will be delivered with the epic and adds a brief outline to the epic description (see [Switchboard Demos](#switchboard_demos)).
1. EM or DRI labels individual issues as ~"workflow-infra::Triage"
1. DRI enables issues to be worked on in parallel where possible so that multiple engineers can contribute to a single epic
1. If the epic involves both Frontend and Backend implementation the issues should be labelled accordingly
1. Team members pick up issues and start working on them
1. Team members use Progress Threads to track progress in individual issues
1. Team checks in on progress during Switchboard Sync
   - Any epics with no issues to raise can be read-only
   - Priority given to discussions of epics based on soonest due date
1. If due date is not realistic team member comments on the issue as early as possible so that the team can work together to address this

Note 1, 2 & 4 can be carried out in parallel

#### Issue Refinement

Switchboard team process to refine issues:
1. When an issue is created and ready to be refined it is labelled ~"workflow-infra::Triage"
1. PM and EM ensure that the `Open` and ~"workflow-infra::Ready" columns are prioritised
1. Team members look at issues in the `Open` column of the [issue board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/4498935?label_name[]=team%3A%3ASwitchboard) and ask questions on the issue to drive clarity
1. When there are no outstanding questions on the issue it can be labelled ~"workflow-infra::Ready" and it will automatically move into the `Ready` column
1. If the issue exposes text to users in any way the `technical writing` label should be added. For example if the issue changes UI text, shows an error message, adds a field etc
1. If the issue requires Frontend implementation the `frontend` label should be used
1. DRI enables issues to be worked on in parallel where possible so that multiple engineers can contribute to a single epic
1. The default is to keep both frontend and backend implementation for a single piece of functionality on the same issue so that discussions are centralised, implementation is carried out in parallel and frontend and backend engineers are in sync
1. Frontend and backend implementation should be delivered in separate MRs
1. If the implementation cannot be done in parallel, or there is a likely to be a meaningful delay between backend and frontend implementations, or if the backend can deliver value independently the issue should be split and the relationship clearly identified by linking the issues

#### Issue & Epic tracking
1. Engineers use Progress Threads to share progress in an async fashion
1. At the beginning of the Switchboard Sync the team will check in on epics labelled ~"workflow-infra::In Progress" or ~"workflow-infra::Triage" to ensure due dates are appropriate and highlight any blockers
1. Epic DRIs update the status in the Epic Description every Wednesday in preparation for the [Grand Review](https://handbook.gitlab.com/handbook/engineering/infrastructure/platforms/project-management/#projects-are-reviewed-weekly-in-the-grand-review)
1. Epic DRIs review the due date weekly. The epic status update should include the DRI's confidence level in the due date and any risks to delivery

#### Picking up work / What to work on next

1. ~"workflow-infra::Ready" column on the [issue board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/4498935?label_name[]=team%3A%3ASwitchboard)
   1. Pick an issue from the ~"workflow-infra::Ready" column on the [issue board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/4498935?label_name[]=team%3A%3ASwitchboard)
   1. Assign the issue to yourself and set to ~"workflow-infra::In Progress"
   1. Update the issue description with an `Implementation Plan` where relevant
   1. Create a `Progress Thread` on the issue and update daily

1. [Switchboard team top-level epic](https://gitlab.com/groups/gitlab-com/gl-infra/-/epics/1048)
    1. Look at the Switchboard top level epic and offer to work on issues with the nearest due date
    1. Use the [Switchboard team roadmap](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/roadmap?state=all&sort=start_date_asc&layout=WEEKS&timeframe_range_type=CURRENT_QUARTER&label_name[]=team::Switchboard&progress=COUNT&show_progress=true&show_milestones=false&milestones_type=ALL&show_labels=false) for guidance

1. `Open` column on the [issue board](https://gitlab.com/groups/gitlab-com/gl-infra/gitlab-dedicated/-/boards/4498935?label_name[]=team%3A%3ASwitchboard)
   1. Look at the issues at the top of the `Open` column
   1. For each issue ask questions and drive a discussion to identify any missing information
   1. Mark the issue as ~"workflow-infra::Ready" if it is ready to be worked on or @mention the EM if you are not confident to do so

#### Switchboard Demos

A demo enables a team member to share progress or the final output of an issue or epic. The focus is on sharing information, not creating an oscar winning documentary, so as a team we use the [boring solution](/handbook/values/#boring-solutions) of either a screen recording, a recorded Zoom meeting or Loom. A link to the recording is added to the epic description.

The epic [DRI](/handbook/people-group/directly-responsible-individuals/) is responsible for identifying at least one demo that will be delivered with the epic when the epic is being kicked off. For example _When the functionality x is delivered (or issue y is Done) we will demo functionality x_.
 Team members are encouraged to time demos to be delivered shortly before the fortnightly Switchboard Team Syncs whenever possible so that any synchronous Q&A can happen during already reserved time.
Team members may choose to create additional demos to share progress or delivery milestones.

### Merge Request Review Guidelines

We specifically adhere to the [GitLab Code Review Guidelines](#gitlab-code-review-guidelines) and follow
the [Dedicated group principles](/handbook/engineering/infrastructure/team/gitlab-dedicated/#merge-requests) when requesting merge request reviews.

#### Merge request review process

As the Switchboard team is currently small, we use an 'Approve and Merge' approach:

1. When you're ready to have your merge request reviewed, select one or more [Switchboard reviewers](https://gitlab.com/groups/gitlab-dedicated/switchboard/reviewers/-/group_members).
   * If you're not certain about who to choose, you can use the [reviewer roulette](#reviewer-roulette) to randomly select a reviewer.
   * If the issue is labelled `technical writing` add the Switchboard technical writer as a reviewer
1. Reviewers will perform a review based on [reviewing a merge request guidelines](https://docs.gitlab.com/ee/development/code_review.html#reviewing-a-merge-request).
1. If satisfied, a reviewer will approve and merge unless other reviewers have questions or suggestions that are not addressed.
1. If the merge request contains the required approvals, the reviewer will trigger a pipeline and set auto-merge.
   * If the reviewer does not have merge permission, they should seek out a maintainer for merging.

Notes:
- It is our intention to move towards a typical 'reviewers and maintainers' approach which would require two reviews as soon as we have the team members to support this.
- Merge requests should be approved based on the [approval guidelines](#approval_guidelines).
- As per the [GitLab Review Guidelines](https://docs.gitlab.com/ee/development/code_review.html#merging-a-merge-request) there are scenarios where it is appropriate for the author to merge the merge request: If there are no blocking comments, and the merge request has all the required approvals, the author or maintainer can merge.
- Switchboard project is configured to use [pipelines for merged results](https://docs.gitlab.com/ee/ci/pipelines/merged_results_pipelines.html) which means that reviewers need to run a pipeline pre-merge to guarantee that updates are compatible with the latest main branch.
- When reviewing merge requests, reviewers should use the [Conventional Comment labels](https://conventionalcomments.org/#labels) to convey your intent.
  - For the avoidance of doubt `Suggestion:`, `Issue:` and `Chore:` comments are all blocking, unless decorated with a `(non-blocking)` statement.
- We label merge requests using the [Specialization labels](https://gitlab.com/gitlab-org/gitlab-foss/-/blob/master/doc/development/labels/index.md#specialization-labels) found in the [GitLab documentation](https://gitlab.com/gitlab-org/gitlab-foss/-/blob/master/doc/development/labels/index.md). MRs should be labelled ~"frontend", ~"backend" or ~"documentation"

#### Approval guidelines

| If your merge request includes  | It must be approved by a |
| ------------------------------- | ------------------------ |
| `~backend` changes        | [Backend maintainer](https://gitlab.com/groups/gitlab-dedicated/switchboard/maintainers/-/group_members). |
| `~frontend` changes       | [Frontend maintainer](https://gitlab.com/groups/gitlab-dedicated/switchboard/maintainers/-/group_members). |

#### Reviewer roulette

Reviewer roulette is an internal tool for use on GitLab.com projects that randomly picks a maintainer for each area of the codebase. To select a maintainer:

1. Go to the [reviewer roulette](https://gitlab-org.gitlab.io/gitlab-roulette/?currentProject=switchboard&sortKey=stats.avg30&mode=show&order=-1) page.
1. Select the Switchboard project.
1. Choose the desire role: `~maintainer::frontend`, `~maintainer::backend`, `~reviewer::backend`, `~reviewer::frontend`.
1. Click on `Spin the wheel`.

#### GitLab Code Review Guidelines

- [Having your merge request reviewed](https://docs.gitlab.com/ee/development/code_review.html#having-your-merge-request-reviewed)
- [Reviewing a merge request](https://docs.gitlab.com/ee/development/code_review.html#reviewing-a-merge-request)
- [The Right Balance](https://docs.gitlab.com/ee/development/code_review.html#the-right-balance)
- [Quality](https://docs.gitlab.com/ee/development/code_review.html#quality)
- [Performance, reliability and availability](https://docs.gitlab.com/ee/development/code_review.html#performance-reliability-and-availability)
- [Merge request performance guidelines](https://docs.gitlab.com/ee/development/merge_request_concepts/performance.html)

### Reviewers and maintainers

There are two groups for Switchboard, [Reviewers and Maintainers](https://gitlab.com/gitlab-dedicated/switchboard):

* All Switchboard team members are included in the `Reviewer` group.
* When a team member is fully onboarded and feel confident in their knowledge of the codebase they are invited to the Maintainer group.



