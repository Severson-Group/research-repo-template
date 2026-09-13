# Results <!-- omit from toc -->

**Approach to organizing project experimental results.**

## Table of Contents <!-- omit from toc -->

- [1. Purpose of Document](#1-purpose-of-document)
- [2. Key Links](#2-key-links)
- [3. Results and Reports](#3-results-and-reports)
- [4. Organization of Experimental Data and Analysis Files](#4-organization-of-experimental-data-and-analysis-files)
  - [4.1 Google Drive Layout](#41-google-drive-layout)
  - [4.2 Active vs Archive Folders](#42-active-vs-archive-folders)
    - [4.2.1 `active` Folders](#421-active-folders)
    - [4.2.2 `archive` Folders](#422-archive-folders)
  - [4.3 Lab Notebooks](#43-lab-notebooks)
  - [4.4 Raw Data](#44-raw-data)
  - [4.5 Analysis](#45-analysis)
  - [4.6 Reports](#46-reports)
- [5. Related Issues / PRs](#5-related-issues--prs)

## 1. Purpose of Document

This document provides template instructions for archiving test data, analysis scripts, and results.

> [!Important]
> **All contents and links** in this document are drafted as an example, borrowing from other projects. Users will of course need to update this to match their project. The document provides several `!Important` boxes to comment on other modifications that may need to be made.

## 2. Key Links

The following results-related links are frequently used by the research team:

- [`results` Google folder](https://drive.google.com/drive/folders/1zir2tsX1gCl5QM1R2pqUqepB_WJda1n7): contains the lab notebooks, raw data, and analysis for all tests.
- [`lab-notebooks` Google folder](https://drive.google.com/drive/folders/1B8E1znPFXZ0amY7ncg5V9rhf0lHH4sDp): contains the lab notebooks for all tests.
- [`lab-notebook-template`](https://docs.google.com/presentation/d/1jssPYmyvypIYgd5w6xAPeCtB-RgWlsoIxTKTk2ZGQXo/edit?usp=drive_link): contains the template for all lab notebooks, including what needs to be recorded for each entry.
- [`data` Google folder](https://drive.google.com/drive/folders/1JyHGdamE8yzh7S08sHY-U0SSgV7OntNw): contains the raw data and analysis files for all tests.

> [!Important]
> These links have been prepopulated with an example project. They need to be updated for each project this is used in.

## 3. Results and Reports

**Table 1.** Links to the test plan and report for the prototype tests.

| Test | Test Plan | P9 Report | BP9 Report |
| :--- | :---: | :---: | :--: |
| Hipot | | | |
| Phase Impedance $R$, $L$ | | | |
| Phase Sequence Confirmation | | | |
| Motor Cooling System | | | |
| Bearing Run-in | | | |
| Back-EMF Based Rotor Temperature Parameters | | | |
| Encoder Offset Angle | | | |
| No-Load Losses | | | |
| Spin Down | | | |
| Flag Plot | | | |
| $k_\mathrm{t}$ Parameter | | | |
| Torque-Speed-Efficiency Map | | | |
| System ID of Suspension RL Plant | | | |
| Eddy Current Sensor Calibration | N/A | | |
| Rotor Levitation | N/A | | |
| $k_\mathrm{f}$ and $k_{\delta}$ Measurement | N/A | | |

> [!Important]
> This is an example table that would need to be updated based on the project this is used in. The idea of the table is to provide links to the test plan and final report produced for each test.

## 4. Organization of Experimental Data and Analysis Files

### 4.1 Google Drive Layout

The team uses the Shared Google Drive as the archive of all raw data files, as outlined below:

```plaintext
.
└── experiments/
    └── results/
        ├── lab-notebooks/
        │   ├── active/         in-progress lab notebooks, team has full access
        │   └── archive/        previous lab notebooks, team has read-only access
        └── data/
            ├── active/         in progress data collection
            │   ├── bp9/
            │   │   └── [Test Name]/
            │   │       ├── [YYYY]-[MM]-[DD]-run-01/
            │   │       ├── [YYYY]-[MM]-[DD]-run-02/
            │   │       └── [YYYY]-[MM]-[DD]-run-03/
            │   └── p9/
            │       └── [Test Name]/
            │           ├── [YYYY]-[MM]-[DD]-run-01/
            │           └── ...
            └── archive/          data is moved here when each test is done
                ├── bp9/
                │   └── [Test Name]/
                │       ├── [YYYY]-[MM]-[DD]-run-01/
                │       └── ...
                └── p9/
                    └── [Test Name]/
                        ├── [YYYY]-[MM]-[DD]-run-01/
                        └── ...
```

For each date of data collection, start with `run-01`. Larger run numbers are only used when there are multiple runs of the same test on the same day.

### 4.2 Active vs Archive Folders

This is used to manage file access permissions so that the full team has access to files related to data currently being collected or analyzed, while providing a means to protect previously collected data from accidental edits.

#### 4.2.1 `active` Folders

- All team members have edit access.
- Locate all files here in the correct nested subfolder (see folder structure above and description below) as once they are finalized they will be placed in the same nested subfolder within `archive`.

#### 4.2.2 `archive` Folders

- Only the PI has edit access, all other team members have view access
- Folders will be moved from active to archive when:
  - When the relevant report is ready to merge
  - or a new year begins
  - or the team alerts the PI that a folder/file is finalized and should be made read-only

Moving from active to archive can be done incrementally (i.e., a single day's worth of tests can be moved) while an analysis Google Sheet stays in the active folder or can be done as a final batch of all files for a single test. Best practice is to move archived data as soon as it is final.

> [!tip]
> Be careful to avoid broken links during the transition from active to archive. Google URLs will remain functional when the folder is moved. However, MATLAB / Python scripts in GitHub may need to be updated.

### 4.3 Lab Notebooks

- Each lab notebook has its own Google Slide deck with one lab notebook per motor per time period
  - The current time period is by year, but this can be changed in future
  - Lab notebooks that are in-progress are stored in the [lab-notebooks/active/](https://drive.google.com/drive/folders/1djMWI-TleKDvKh3UAkipIrhIowG6Y8E1) folder in Google Drive, within the [p9](https://drive.google.com/drive/folders/1-U38e8s3DafdSa5XI34X-_bertqpvc04) or [bp9](https://drive.google.com/drive/folders/1iAVK8ZiUO3T7LTqZMJ4wrRNwciT4ZLxe?usp=drive_link) folders depending on what motor is being tested
- Each entry in the lab notebook is a day of testing and includes: the date, a list of personnel running the test, links to the raw data and analysis files, a record of test conditions (observations, photographs, firmware used, notes on any deviation from the test plan), and a log of any test stand changes.
  - All lab notebook entries are made in Google Slides and follow the [lab-notebook-template](https://docs.google.com/presentation/d/1jssPYmyvypIYgd5w6xAPeCtB-RgWlsoIxTKTk2ZGQXo/edit?usp=drive_link)

> [!Important]
> This example plan uses Google Slides for lab notebooks. Alternately, the team could use Google Docs. The important detail here is to use a collaborative tool that allows everyone easy access without risk of overwriting records and automatically backsup.

### 4.4 Raw Data

- The raw data includes `.csv` files, screenshots, etc. from the test equipment
  - The raw data is uploaded from the test equipment to the [data](https://drive.google.com/drive/folders/1JyHGdamE8yzh7S08sHY-U0SSgV7OntNw) folder in Google Drive in the [active/p9](https://drive.google.com/drive/folders/1mx1Rj7gM5MOtgGqszN1uoQktXDii4f3Q?usp=drive_link) or [active/bp9](https://drive.google.com/drive/folders/1d8nQGpMrDSz53JgfON3Cy41_XvkZXnOc?usp=drive_link) folders depending on what motor is being tested
  - The raw data is further divided into folders based on the test being run and then into folders for each individual test run
    - The folders for each test run are named with the date and then the test run number for that date
    - After tests are complete, these folders are moved to the `archive/` folder, as described above.

### 4.5 Analysis

- Intermediate analysis files are primarily Google Sheets, so the cells can be manipulated with equations, and kept in the Google Drive `[Motor Name]/[Test Name]` subfolders in the [`data`](https://drive.google.com/drive/u/0/folders/1JyHGdamE8yzh7S08sHY-U0SSgV7OntNw) folder in Google Drive
- Final analysis files are placed in the git repo `experiments/results/data/[Motor Name]/[Test Name]` folder depending on the motor and test
  - These will be MATLAB and Python scripts

### 4.6 Reports

- Follow the group's [report template](https://github.com/Severson-Group/KnowledgeBase/blob/main/writing/write-repo-report.md#readmemd-template)
- Will contain in the `Approach` section, a filled in version of **Table 2**, and steps to re-create the report's plots (i.e., which scripts to run). This should also explain any deviations from the test procedure documented in the test plan.
- The major finding(s) of the experiment and commentary/observations, including any extenuating circumstances and/or how the results compare to FEA simulations

**Table 2:** Experiment information.

| Document Name        | Link(s)                                |
| :---                 | :-----:                                |
| Test Plan            | `[Test Plan Name]`                     |
| Data Used in Report  | `[1st Test Run]`, `[2nd Test Run]`[^1] |
| Lab Notebook Entries | `[1st Entry]`, `[2nd Entry]`[^1]       |

[^1]: include as many as required, but only include the data / notebook entries that are relevant to the results (do not list datasets from the test that are not used to construct the final results)

>[!Important]
> We often run tests multiple times while we debug our methodology and test stand configuration, generating lots of datasets (test run folders), but only one trusted dataset. The **Approach** section should include an explanation of which of the raw dataset(s) were used (and which were not used) to obtain the results of this report.

## 5. Related Issues / PRs

- [Issue PFI#851: Set up lab notebooks folder, move existing notebooks over, and agree upon lab notebook template with team](https://github.com/Severson-Group/nsf_pfi_bearingless/issues/851)
- [PR PFI#874: Add results README explaining how to archive test data, analysis scripts, and final reports](https://github.com/Severson-Group/nsf_pfi_bearingless/pull/874)
- [Issue #51: Create instructions on how to archive test data, analysis scripts, and final reports](https://github.com/Severson-Group/research-repo-template/issues/51)
