# How to Create New Research Repositories From This Template <!-- omit from toc -->

**Instructions for using GitHub to create new research repositories.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [Instructions](#instructions)
- [Template for Research Repo Section 3](#template-for-research-repo-section-3)
- [Related Issues / PRs](#related-issues--prs)

## Purpose of Document

This document provides step-by-step instructions for setting up new research repositories for the eLev Lab. The instructions are intended for use with GitHub and leverage the GitHub Projects feature.

## Instructions

To set up a new repository using this system, do the following:

1. Use the [`research-repo-template`](https://github.com/severson-group/research-repo-template/) repository as a template (select `research-repo-template` from the `Repository template` dropdown box when creating a new repo)
2. In the new repo, commit the following modifications:
   1. In [`environment.yml`](./environment.yml), replace `this-repo-name` with the name of the new repo. Modify packages listed as needed.
   2. In this [`README.md`](./README.md),
      1. Update the title, abstract, purpose of document sections
      2. Do a find and replace for `this-repo-name`, replacing it with the name of this repo.
      3. Replace Section 2 with a `## 2. Project Description` section.
      4. Replace Section 3 with the [Section 3 template](#template-for-research-repo-section-3) below.
      5. Delete the contents of [Section 7](./README.md#7-related-issues--prs) (leave it empty).
   3. Delete `github-project-management.md` and `repo-structure.md`
   4. Optionally, delete all subfolders.
3. In the GitHub settings for the new repo, turn on branch protection rules for `main` by going to settings -> `Branches` -> `Add rule` -> `Branch name pattern` set to `main` and check `Require a pull request before merging`, `Dismiss stale...`, `Require... codeowners`.
4. Create a new GitHub project from `[TEMPLATE] Research Project`, by navigating [to this project](https://github.com/orgs/Severson-Group/projects/14) and clicking `Use this template` in the top right corner.
5. On the new project, modify the Workflows by enabling `Auto-add to project`

## Template for Research Repo Section 3

```markdown
## 3. Key Information

**Key locations:**

- [Shared Google Drive](./add-link): used for meeting notes, excessively large files, confidential material.
- [Project Slack channel](./add-link).

**Setup instructions after cloning the repo:**

1. [Initialize submodules](#42-submodules)
2. [Create Conda environment](#61-initial-setup)

> [!Tip]
> This repository is being developed following the guidelines described in the [eLev Lab Research Repo Template](https://github.com/severson-group/research-repo-template/). Be sure to review the following documents:
>
> 1. [Research Repo Template README](https://github.com/Severson-Group/research-repo-template/blob/features/reorg-instructions/README.md)
> 2. [Recommended Research Repository Folder Structure](https://github.com/Severson-Group/research-repo-template/blob/main/repo-structure.md)
> 3. [GitHub Usage for Project Management](https://github.com/Severson-Group/research-repo-template/blob/reorg-instructions/github-project-management.md)
```

## Related Issues / PRs

- [Issue #49: Clean up research repo main README](https://github.com/Severson-Group/research-repo-template/issues/49)
