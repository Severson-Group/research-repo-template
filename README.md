# GitHub for Organizing Research <!-- omit from toc -->

This document describes the recommended implementation of using GitHub to manage our group's research projects.

## Table of Contents <!-- omit from toc -->

- [1. File Structure and Conventions](#1-file-structure-and-conventions)
  - [File Structure](#file-structure)
    - [File Naming](#file-naming)
    - [Large Files](#large-files)
- [2. GitHub Project Boards Rationale](#2-github-project-boards-rationale)
- [3. Implementation](#3-implementation)
  - [3.1 Issues](#31-issues)
    - [3.1.1 Types](#311-types)
    - [3.1.2 Closing an Issue](#312-closing-an-issue)
  - [3.2 Project](#32-project)
    - [3.2.1 Roadmap View](#321-roadmap-view)
    - [3.2.2 Board View](#322-board-view)
- [4. Best Practices](#4-best-practices)
  - [4.1 Keep Everything Up-to-Date](#41-keep-everything-up-to-date)
  - [4.2 Meetings](#42-meetings)
- [5. Create a New Project](#5-create-a-new-project)

## 1. File Structure and Conventions

### File Structure

Every folder should have a `README.md` file that acts like a landing page for that folder and explains its contents.

#### File Naming

Files should be named following best practices for their file type.

##### Markdown Documentation (and any other file type not called out below) <!-- omit from toc -->

Use the `dash-case` naming convention:

- Do this: `this-is-my-amazing-file.md` (all lower case, hyphens instead of spaces)
- Not this `thisIsMyAmazingFile.md` nor this `This Is My Amazing File.md`, etc.

Follow this same naming convention for supporting files linked into markdown docs, i.e., images and PDF files.

See the [docs.amdc.dev repository](https://github.com/Severson-Group/docs.amdc.dev) as an example.

##### MATLAB / Simulink <!-- omit from toc -->

Follow the Camel Case naming convention described in the [Knowledgebase's MATLAB article](https://github.com/Severson-Group/KnowledgeBase/blob/main/code/matlab/README.md#style-guidelines).

##### Python <!-- omit from toc -->

Follow the naming convention described in the [Knowledgebase's Python article](https://github.com/Severson-Group/KnowledgeBase/blob/main/code/python/README.md#style-guidelines), which is [snake case](https://en.wikipedia.org/wiki/Snake_case) for most file types.

##### Software <!-- omit from toc -->

When committing software, use the naming convention of the software:

- MATLAB naming convention is [listed here](code/matlab/README.md#style-guidelines)
- Python naming convention is [listed here](code/python/README.md#style-guidelines)

#### Large Files

Don't do it! **Files larger than 15MB should never be committed** *(files less than 300kB are preferred; and files larger than 1 MB should be avoided)*. Large files can be stored in Google Drive and linked into Markdown articles.

In the future, we may also explore using [Git Large File Storage](https://git-lfs.github.com/).

If you accidentally committed a file larger than 15MB:

1. submit a new commit that eliminates this file (i.e., replace it with a smaller file),
2. ensure that the PR is merged via a `Squash and Merge` so that the large file does not appear in the repo history.

## 2. GitHub Project Boards Rationale

We are using GitHub to track project progress, items we need to finish and discuss, and to give structure to our meetings. This approach is similar in nature to using Trello with a Kanban board configuration. We use this over Trello because of our success with using GitHub in our code and controls development and to minimize the number of different tools we have going.

## 3. Implementation

### 3.1 Issues

#### 3.1.1 Types

We have two types of issues: `todo` issues and `roadmap` issues. We set up the repositories to be pre-loaded with templates for each of these issues.

`todo` issues:

- One GitHub issue == one `todo` item; see [this example todo issue](https://github.com/Severson-Group/Research-Repo-Template/issues/11)
- The template prompts the user to provide information in the following fields: `Abstract`, `Context`, and `Approach`. Populating these fields is optional, but encouraged.  
- Either make these issues small enough in scope that they can be reasonably completed within one week OR make the issue be a checklist of smaller `todo` under the `Approach` heading, see [this example](https://github.com/Severson-Group/Research-Repo-Template/issues/13)
- When you need to quickly record that something needs to get done, but don’t have time to properly articulate the issue: get that issue created with a partial description. **And then, later, come back and explain it.**
- These issues have the label `todo` applied to them.

`roadmap` issues:

- These issues describe required tasks that correspond to a project statement of work and are timebound in nature, meaning they must adhere to a schedule.
- The template prompts the user to paste-in the exact text from the statement of work and then to break up the work up a list of `todo` issues.
- The user should indicate the start/stop dates of the scheduled task.
- Usually these issues are created once at the start of a project, with due dates revised if the project timeline is revised.
- These issues have the label `roadmap` applied to them.

#### 3.1.2 Closing an Issue

To close a `todo` issue, leave a comment explaining how the issue has been completed and where a person would go to see the result. Depending on the nature of the issue, indicate where the completed work is by presenting your work in the issue for us to discuss or linking to a PR or code you added to the repo, attaching a picture or screenshot, or linking to a file in Google drive.

Did finishing an issue result in something of archival value? The issue should not be the only place that you store the result. I.e., add it to the repo. Or place it in Google Drive. Or... something else that is more permanent than the issue.

### 3.2 Project

Each research project being organized in GitHub will have one GitHub Project. The project will have `status`, `Start date`, and `Due date` fields that can be populated on all issues. GitHub Workflows will be used to facilitate east of project management. The Project will consist of two key views: `Roadmap` and `Board`, which are now described in conjunction with how they make use of the issue fields and Workflows.

#### 3.2.1 Roadmap View

The goal of this view is to provide a project management perspective on project timeline. It is meant to facilitate the team checking in on the critical milestones and obtain a quick glimpse into whether the project is on track. An example roadmap view can be found [here](https://github.com/orgs/Severson-Group/projects/14) (select a date in October 2023 to view the issues).

This view is configured as GitHub's `Roadmap` layout and applies the filter `label:roadmap` so that it only shows `roadmap` issues. The layout's `Date fields` are configured for the `Start date` and `Due date` fields of the `roadmap` issue (note that these fields are only used on `roadmap` issues; they are not used on `todo` issues).

With this configuration, the `roadmap` issues are mapped out on a timeline. At team meetings, members can easily click on each of the issues to see the list of `todo` issues that need to be completed (and whether or not they are completed).

#### 3.2.2 Board View

The goal of this view is to provide a modified Kanban style board to check in on `todo` issues. This view is where researchers will spend most of their time, checking in and updating on project progress. It is meant to quickly show what each team member is focusing on this week, what work has been completed, and what work remains. The project team will talk through this board at each check in meeting. An example board view can be found [here](https://github.com/orgs/Severson-Group/projects/14/views/2).

The view is configured as GitHub's `Board` layout and applies the filter `-label:roadmap`. It is set up with six categories that `todo` issues (and PRs) are placed within to indicate their status, from left to right:

- `>1 Month`: issues where work is scheduled to start over one month away
- `Next Month`: issues where work is scheduled to start sometime within the next month
- `This Week`: issues that are planned to be started this week (if plans change, move these to another box)
- `In Progress`: issues where work is currently in progress
- `Hold`: issues where progress is blocked; e.g., waiting for parts or another researcher to answer a question
- `Done`: issues that have been completed and should be discussed at the next check in meeting (once these items have been discussed, the team archives them and they disappear from the board).

Project Workflow automation is set up to automatically add each new issue (and PR) to the `This Week` status and to move closed issues (and PRs) to the `Done` status. Researchers are expected to manually drag issues across the board to the other categories based on their current progress.

## 4. Best Practices

### 4.1 Keep Everything Up-to-Date

1. Graduate researchers should be hands-on and active with the `todo` issues: create, edit, update, comment, re-organize--make them make sense for you and what you are working on.
2. Continually update the Project `Board` to make sure each issue is in the correct status category. Issues move left to right across the board--future plans to completed.
3. Don't work on too many things at once! Keep your `In Progress` and `This Week` categories focused with only a manageable number of issues.
4. Interlink items on GitHub to provide context. Sometimes all that is needed in the `Context` field is a link to another issue
    - Link PRs to issues
    - Link issues to issues
    - You can even link to items across different repositories within the group account, i.e., `Severson-Group/RepoWithIssue#32`
    - Tag people when you want to bring them into a discussion, i.e., `@elsevers, what do you think?`
5. In a typical research week, try to complete at least one `todo` issue. If you are having trouble doing this, it probably means the issue is too big and needs to be broken up into smaller issues.
6. Start every week by populating the `This Week` box. Aim to empty this box by the end of the week.
7. Who is responsible for breaking issues up into smaller issues? The researcher it is assigned to! 
    - Keep the original issue, but modify the `Approach` section to be a list of smaller `todo` issues
8. Keep an active research dialog going on the `todo` issues. Some helpful examples can be found [here](https://github.com/Severson-Group/ARL-eturbo/issues/21), [here](https://github.com/Severson-Group/CHP_Bearingless_Drive/pull/10), and [here](https://github.com/Severson-Group/ARL-eturbo/issues/11)
    1. Aren't sure what to do with an issue? Indicate that in the comments. Get help and revise the issue to make it clear what to do.
    2. Make some exciting progress with a `todo` issue? Add this info to the comments.
    3. Are you stuck and need help with a `todo` issue? Document your problems in the comments.

### 4.2 Meetings

Check in meetings are run by reviewing the `Board View` going right to left. Start by going through the items wih a status of `Done`, and either archive or re-open each item here. Then move to the items that have a `Hold` status, then `In Progress`, `This Week`, and so on.

## 5. Create a New Project

To quickly set up a new repository using this system,

1. Use the `Research-Repo-Template` repository as a template (select `Research-Repo-Template` from the `Repository template` dropdown box when creating a new repo) and
2. In the new repo, turn on branch protection rules for `main` by going to settings -> `Branches` -> `Add rule` -> `Branch name pattern` set to `main` and check `Require a pull request before merging`, `Dismiss stale...`, `Require... codeowners`.
3. Create a new project from `[TEMPLATE] Research Project`, by navigating [here](https://github.com/orgs/Severson-Group/projects/14) and clicking `Use this template` in the top right corner.
4. On the new project, modify the Workflows by enabling `Auto-add to project`
