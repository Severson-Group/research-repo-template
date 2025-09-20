# Reports

This folder will contain reports for the project. Each report should be created within its own subfolder and contain a `readme.md` file. The report may also optionally contain additional files that are necessary for its analysis and do not belong elsewhere in the repository.

This folder will contain reports for the project. Each report should:
- be in its own subfolder, named using [dash-case](https://github.com/Severson-Group/KnowledgeBase/blob/main/CONTRIBUTING.md#file-naming); i.e. `demag-analysis\` (camelCase is also acceptable in repos already using camelCase).
- contain a `README.md` file
- optionally contain additional files that are necessary for its analyses and do not belong elsewhere in the repository

## README file specification

Within the `README.md` file, the following sections must be present:
- `Objective`: Short section that outlines the objective of the study that resulted in this report. Bonus points for having it be a numbered list where each number is an objective.
- `Context`: Explanation of the broader context that led to performing this study / how the study fits into the goals of the research project. This is typically 1 paragraph long.
- `Approach`: Provide the methodology used in the study and specify all necessary information needed to interpret the results. When applicable, this section shold also provide instructions to recreate results (such as what script to run to create plots shown in the results section).
- `Results`: The results of the study.
- `Relevant Issues`: A bulleted list of links to all relevant issues where the issue title and number appears in each bullet.

### README template

Copy-paste this template into your `README.md` file to start a new report.

```markdown
# Report Name

## Objective

_Short section that outlines the objective of the study that resulted in this report. Bonus points for having it be a numbered list where each number is an objective._

_OPTIONAL: May include table of contents for long reports. See example [here](https://github.com/Severson-Group/KnowledgeBase/blob/main/CONTRIBUTING.md#article-template)._

## Context

_Explanation of the broader context that led to performing this study / how the study fits into the goals of the research project. This is typically 1 paragraph long._

## Approach

_Provide the methodology used in the study and specify all necessary information needed to interpret the results. When applicable, this section shold also provide instructions to recreate results (such as what script to run to create plots shown in the results section). May consist of subsections. When many subsections are used, please number them._

## Results

_The results of the study. Typically includes graphics. Screenshots of slides are welcome, but watch the file size (keep it below 0.5 MB). Large files should be stored separately, in a Google Shared Drive folder. The best practice is to have a Reports within the project's Shared Google Drive, which consists of subfolders of the same name as each report. This folder should have a README Google Doc that links back to this report. After the report is merged, restrict user access to the folder to view only to prevent accidental changes. May consist of subsections. When many subsections are used, please number them. Writers are encouraged to conclude with a key takeaways section that has a short bullet list of the most important findings._ 

## Relevant Issues / PRs

_Bullet list of all relevant issues to facilitate future readers in learning more about the material of the report._

- _Issue #120: Route traces for the flux capacitor <-- make this a link to the relevant issue_
- _Issue #130: Create a report on the flux capacitor <-- make this a link to the relevant issue_
- _PR #142: Add report on the flux capacitor field lines <-- make this a link to the relevant PR_
```

## Examples
See the ARL repo [BP4](https://github.com/Severson-Group/ARL-eturbo/tree/main/BP4/Control/Reports) and [BP7](https://github.com/Severson-Group/ARL-eturbo/tree/main/BP7/Reports) reports as examples. 
