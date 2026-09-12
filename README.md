# GitHub for Organizing Research <!-- omit from toc -->

This document describes the recommended implementation of using GitHub to manage our group's research projects.

## Table of Contents <!-- omit from toc -->

- [1. Purpose of Document](#1-purpose-of-document)
- [2. Create a New GitHub Repo and Project](#2-create-a-new-github-repo-and-project)
- [3. GitHub Configuration and Usage](#3-github-configuration-and-usage)
- [4. Repo Structure and Naming Conventions](#4-repo-structure-and-naming-conventions)
  - [Folder Structure](#folder-structure)
  - [File Naming, Contents, and Size](#file-naming-contents-and-size)
- [4. Git](#4-git)
  - [4.1 Basic Usage](#41-basic-usage)
  - [4.2 Submodules](#42-submodules)
- [5. Markdown Development Settings](#5-markdown-development-settings)
  - [5.1 Visual Studio Code markdownlint Extension Instructions](#51-visual-studio-code-markdownlint-extension-instructions)
  - [5.2 Renaming Files in Visual Studio Code](#52-renaming-files-in-visual-studio-code)
- [6. Python Usage](#6-python-usage)

## 1. Purpose of Document

## 2. Create a New GitHub Repo and Project

To set up a new repository using this system, do the following:

1. Use the `Research-Repo-Template` repository as a template (select `Research-Repo-Template` from the `Repository template` dropdown box when creating a new repo) and
2. In the new repo, turn on branch protection rules for `main` by going to settings -> `Branches` -> `Add rule` -> `Branch name pattern` set to `main` and check `Require a pull request before merging`, `Dismiss stale...`, `Require... codeowners`.
3. Create a new project from `[TEMPLATE] Research Project`, by navigating [to this project](https://github.com/orgs/Severson-Group/projects/14) and clicking `Use this template` in the top right corner.
4. On the new project, modify the Workflows by enabling `Auto-add to project`

## 3. GitHub Configuration and Usage

This repository is configured to support project management via GitHub's features. This is explained in a separate [GitHub Project Management article](./github-project-management.md).


## 4. Repo Structure and Naming Conventions

### Folder Structure

**See [repo-structure.md](repo-structure.md) for a complete map of the recommended folder structure.**

Every folder should have a `README.md` file that acts like a landing page for that folder and explains its contents.

### File Naming, Contents, and Size

See the [eLev Lab's Contributing Guide](https://github.com/Severson-Group/.github/blob/main/CONTRIBUTING.md).

## 4. Git

### 4.1 Basic Usage

Follow branch naming, issues, and PR guidelines in the [How to Use Git to Contribute to the Repository](https://github.com/severson-group/.github/?tab=contributing-ov-file#3-how-to-use-git-to-contribute-to-the-repository) section of the [eLev lab contributing guidelines](https://github.com/Severson-Group/.github/blob/main/CONTRIBUTING.md).

### 4.2 Submodules

Research repositories typically rely on one or more [Git Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules). Follow these instructions to maintain submodules:

#### 4.2.1 Initialize Submodules <!-- omit from toc -->

After freshly cloning the repo from GitHub, you must initialize all submodules to load their contents onto your harddrive. Do this by running the following command from the repository root directory:

```bash
git submodule update --init --recursive
```

#### 4.2.2 Update Submodules <!-- omit from toc -->

Use this command to update to the most recent version of all submodules:

```bash
git submodule update --remote --merge
```

This will update each submodule to the latest commit on the branch specified in the `.gitmodules` file (e.g., branch = `develop`).

> [!Tip]
> Both of these commands act on all submodules within the repo. You can also run commands that act on only a single submodule at a time.

## 5. Markdown Development Settings

Configure your tools to help you be successful in writing Markdown Docs. [Visual Studio Code](https://code.visualstudio.com/) is highly recommended and the eLev Lab has a [KnowledgeBase Aricle on configuring and selecting extensions for VS Code](https://github.com/Severson-Group/KnowledgeBase/blob/main/tools/VS_Code.md).

### 5.1 Visual Studio Code markdownlint Extension Instructions

Use the `markdownlint` extension in VS Code (Extension ID `DavidAnson.vscode-markdownlint`). And periodically check that there are no lint errors.

For optimal lint configuration, use the [`.markdownlint.json`](./.markdownlint.json) file. This file contains four key settings:

- `"MD013": false`: disables line-length rule, preventing warnings from appearing when our line length is over 80 characters.
- `"MD033": false`: disables no-inline-html rule. This disables warnings when we embed images using html, which is very convienent.
- `"MD049": { "style": "underscore" }`: use `_` character to italicize text (not `*`)
- `"MD050": { "style": "asterisk" }`: use `*` character to bold text (not `_`)

Periodically check for lint errors in the repo. To do this:

1. Open the Command Pallet in VS Code: `Ctrl+Shift+P` on Windows/Linux or `Cmd+Shift+P` on Mac.
2. Start typing `markdownlint` and look for `markdownlint: Lint all Markdown files in the workspace with markdownlint` in the filtered list.
3. Click it or highlight it and press Enter.
4. On the bottom, inspect the `Problems` pane. Double click on each item to be taken to the problem location to fix it.

### 5.2 Renaming Files in Visual Studio Code

Use [`.vscode/settings.json`](.vscode/settings.json) file. Among other things, this file sets up VS Code detect if rename a file or folder _in VS Code_ that breaks a Markdown link. If this is detected, VS Code offers to fix the links for you.

For this to work, the file or folder must have been renamed within VS Code.

## 6. Python Usage

To use the repo's Python code (scripts and juypter notebooks), all users should install [Anaconda](https://www.anaconda.com/download) or [Miniconda](https://www.anaconda.com/docs/getting-started/concepts/anaconda-or-miniconda).

Maintain a conda environment for the repo that can has the necessary packages for to use all the of the Python code in the project. Do this by maintaining an [`environment.yml`](environment.yml) file.