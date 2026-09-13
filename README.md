# Template Research Repository <!-- omit from toc -->

This document describes the recommended implementation of using git and GitHub to manage our group's research projects.

## Table of Contents <!-- omit from toc -->

- [1. Purpose of Document](#1-purpose-of-document)
- [2. How to Create New Research Repositories From This Template](#2-how-to-create-new-research-repositories-from-this-template)
- [3. GitHub Projects, Repo Structure, and Naming Conventions](#3-github-projects-repo-structure-and-naming-conventions)
  - [3.1 GitHub Usage](#31-github-usage)
  - [3.2 Folder Structure](#32-folder-structure)
  - [3.3 File Naming, Contents, and Size](#33-file-naming-contents-and-size)
- [4. Git](#4-git)
  - [4.1 Basic Git Usage](#41-basic-git-usage)
  - [4.2 Submodules](#42-submodules)
- [5. Markdown Development Settings](#5-markdown-development-settings)
  - [5.1 Visual Studio Code markdownlint Extension Instructions](#51-visual-studio-code-markdownlint-extension-instructions)
  - [5.2 Renaming Files in Visual Studio Code](#52-renaming-files-in-visual-studio-code)
- [6. Python Usage](#6-python-usage)
  - [6.1 Initial Setup](#61-initial-setup)
  - [6.2 Activating the Environment \& VS Code Configuration](#62-activating-the-environment--vs-code-configuration)
  - [6.3 Updating the Environment](#63-updating-the-environment)

## 1. Purpose of Document

This repository is intended to document the [eLev Lab](https://elev.umn.edu/) approach to using git and GitHub to manage research projects. The repository also serves as a template that can be cloned to create new project repositories.

## 2. How to Create New Research Repositories From This Template

To set up a new repository using this system, do the following:

1. Use the [`research-repo-template`](https://github.com/severson-group/research-repo-template/) repository as a template (select `research-repo-template` from the `Repository template` dropdown box when creating a new repo)
2. In the new repo, commit the following modifications:
   1. In [`environment.yml`](./environment.yml), replace `this-repo-name` with the name of the new repo. Modify packages listed as needed.
   2. In this [`README.md`](./README.md),
      1. Update the title, abstract, purpose of document sections
      2. Do a find and replace for `this-repo-name`, replacing it with the name of this repo.
      3. Replace Section 2 with a `## 2. Project Description` section.
      4. Replace Section 3 with the [Section 3 template](#template-for-research-repo-section-3) below.
      5. Delete Section 4.
   3. Delete `github-project-management.md` and `repo-structure.md`
   4. Optionally, delete all subfolders.
3. In the GitHub settings for the new repo, turn on branch protection rules for `main` by going to settings -> `Branches` -> `Add rule` -> `Branch name pattern` set to `main` and check `Require a pull request before merging`, `Dismiss stale...`, `Require... codeowners`.
4. Create a new GitHub project from `[TEMPLATE] Research Project`, by navigating [to this project](https://github.com/orgs/Severson-Group/projects/14) and clicking `Use this template` in the top right corner.
5. On the new project, modify the Workflows by enabling `Auto-add to project`

<!-- omit from toc -->
### Template for Research Repo Section 3

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

## 3. GitHub Projects, Repo Structure, and Naming Conventions

### 3.1 GitHub Usage

This repository is configured to support project management via GitHub's features. This is explained in a separate [GitHub Project Management article](./github-project-management.md).

### 3.2 Folder Structure

**See [repo-structure.md](repo-structure.md) for a complete map of the recommended folder structure.**

Every folder should have a `README.md` file that acts like a landing page for that folder and explains its contents.

### 3.3 File Naming, Contents, and Size

See the [eLev Lab's Contributing Guide](https://github.com/Severson-Group/.github/blob/main/CONTRIBUTING.md).

## 4. Git

### 4.1 Basic Git Usage

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

Use the `markdownlint` extension in VS Code (Extension ID `DavidAnson.vscode-markdownlint`).

#### Configuration <!-- omit from toc -->

For optimal lint configuration, use the [`.markdownlint.json`](./.markdownlint.json) file. This file contains four key settings:

- `"MD013": false`: disables line-length rule, preventing warnings from appearing when our line length is over 80 characters.
- `"MD033": false`: disables no-inline-html rule. This disables warnings when we embed images using html, which is very convienent.
- `"MD049": { "style": "underscore" }`: use `_` character to italicize text (not `*`)
- `"MD050": { "style": "asterisk" }`: use `*` character to bold text (not `_`)

#### Periodically check for lint errors in the repo <!-- omit from toc --> 

To do this:

1. Open the Command Pallet in VS Code: `Ctrl+Shift+P` on Windows/Linux or `Cmd+Shift+P` on Mac.
2. Start typing `markdownlint` and look for `markdownlint: Lint all Markdown files in the workspace with markdownlint` in the filtered list.
3. Click it or highlight it and press Enter.
4. On the bottom, inspect the `Problems` pane. Double click on each item to be taken to the problem location to fix it.

### 5.2 Renaming Files in Visual Studio Code

Use [`.vscode/settings.json`](.vscode/settings.json) file. Among other things, this file sets up VS Code detect if you rename a file or folder _in VS Code_ that breaks a Markdown link. If this is detected, VS Code offers to fix the links for you.

For this to work, the file or folder must have been renamed within VS Code.

## 6. Python Usage

To use the repo's Python code (scripts and juypter notebooks), all users should install [Anaconda](https://www.anaconda.com/download) or [Miniconda](https://www.anaconda.com/docs/getting-started/concepts/anaconda-or-miniconda).

Maintain a conda environment for the repo that can has the necessary packages for to use all the of the Python code in the project. Do this by maintaining an [`environment.yml`](environment.yml) file.

### 6.1 Initial Setup

After cloning the repository for the first time, open your terminal (or Anaconda Prompt on Windows) and navigate to the root directory of the repository. Create the Conda environment by running:

```bash
conda env create -f environment.yml
```

### 6.2 Activating the Environment & VS Code Configuration

To use the environment in your terminal, you must activate it. Run the following command:

```bash
conda activate this-repo-name
```

#### To configure VS Code to use this environment  <!-- omit from toc -->

1. Open any Python `.py` file or Jupyter Notebook `.ipynb` in the repository.
2. Open the Command Palette (`Ctrl+Shift+P` on Windows/Linux or `Cmd+Shift+P` on Mac).
3. Type and select `Python: Select Interpreter`.
4. Choose the Conda environment associated with this repository (e.g., `this-repo-name`). VS Code will now automatically use this environment for execution, linting, and Jupyter server kernels.

### 6.3 Updating the Environment

#### When the `environment.yml` file is updated (e.g., pulling a colleague's changes)  <!-- omit from toc -->

If the `environment.yml` file has been modified to add or remove dependencies, update your local environment by running the following command. The `--prune` flag ensures that packages removed from the `.yml` file are also uninstalled from your environment:

```bash
conda env update --file environment.yml --prune
```

#### When you want to update the installed packages  <!-- omit from toc -->

If you want to update all existing packages within your active environment to their latest allowable versions:

```bash
conda update --all
```
