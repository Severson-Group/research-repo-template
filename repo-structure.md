# Recommended Research Repository Structure <!-- omit from toc -->

**This article documents the folder structure recommended for use in research repositories.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [Motivation](#motivation)
- [Exceptions to Structure](#exceptions-to-structure)
- [Recommended Repo Structure](#recommended-repo-structure)
- [Related Issues / PRs](#related-issues--prs)

## Purpose of Document

The goal of this article is to provide a bird's eye view of the recommended research repository structure.

## Motivation

The detailed repository structure provided in [Recommended Repo Structure](#recommended-repo-structure) is recommended for all research repositories. This is intended to establish uniformity across our research repositories. The ultimate goals being to

1. make our repositories easier to navigate and
2. make decisions about how to structure research material easier, quicker, and better.

## Exceptions to Structure

Since the nature of research is "to do the unexpected," deviations from the [Recommended Repo Structure](#recommended-repo-structure) will be necessary from time to time. The most common deviations are expected to include:

1. Omission of folders that are listed below (not every repo will need everything in here, especially early on).
2. Contents of the project sponsor documents folder (these are expected to vary significantly from project to project, especially if one repo houses a project sponsored by multiple entities).
3. Organization of the experiments folder (will vary based on the nature of the project and number of distinct experiments and prototypes).

> [!TIP]
> Do follow the recommended structure whenever possible. More often than not, research material will benefit from being conformed to fit this structure. A succinctly worded README file explaining rationale and file placement can do wonders to make things work.
>

## Recommended Repo Structure

All directories should contain a README file. Refer to the [research-repo-template](https://github.com/Severson-Group/research-repo-template) folders detailed explanations of individual files/folders.

```
research repo
│
├── README.md (repo landing page)
├── control/ (archive of control algorithms and code)
│   ├── README.md
│   ├── AMDC-Firmware/ (git submodule)
│   ├── elev-control-lib/ (git submodule)
│   ├── jupyter/ (collection of notebooks to operate AMDC)
│   ├── project-firmware (AMDC firmware for this project)
│   │   ├── ldscript.ld
│   │   ├── Xilinx.spec
│   │   └── usr/
│   │       ├── blink/
│   │       ├── usr-app-1/
│   │       ⋮
│   │       └── usr-app-x/
│   └── simulink/
│       ├── README.md 
│       ├── control-sim-1/ (often used to autogen code)
│       │   ├── README.md
│       │   ├── control-sim-1.slx
│       │   ⋮
│       ⋮
│       └── control-sim-x/
│
├── experiments/ (optionally organized into subfolders, e.g. per prototype, round of experiment, project phase)
│   ├── README.md
│   ├── instrumentation/
│   │   ├── README.md (documenting overall setup, room layout, etc.)
│   │   ├── connection-schematic.svg
│   │   ├── ground-schematic.svg
│   │   ├── equipment-1/ 
│   │   │   ├── README.md (emphasizing any customization for project)
│   │   │   └── procurement/ (optional, only when it makes sense)
│   │   ⋮
│   │   └── equipment-x/
│   ├── results/
│   │   └── README.md (e.g., where lab notebook & data is stored, list relevant reports)
│   └── test-plans/
│       ├── README.md
│       ├── plan-1.md
│       ├── plan-2.md
│       ⋮
│       └── plan-x.md
│
├── modeling/ (archive of models developed in the research)
│   ├── README.md
│   ├── eMachPrivate/ (git submodule)
│   │   └──eMach/ (git submodule)
│   ├── model-1/ (often FEA, but could be analytic or other)
│   │   ├── README.md
│   │   ⋮
│   │   └── ...
│   ⋮
│   └── model-x/
│
├── project-sponsor-documents/ (highly dependent on project)
│   ├── README.md
│   ├── annual-reports/ (depending on the project)
│   │   ├── 2025/
│   │   ⋮   
│   │   └── 20xx/
│   └── proposal/ 
│
├── prototypes/ (archive of prototypes designs used in the project)
│   ├── power-electronics/ (or, locate in instrumentation)
│   │   ├── README.md (include connection tables)
│   │   ├── connection-schematic.svg
│   │   └── ... (follow other prototype folders' structure) 
│   ├── prototype-1-name/
│   │   ├── README.md (landing page for key information on the prototype, often includes nameplate)
│   │   ├── cad/
│   │   │   ├── README.md (includes revision table, design history, and SolidWorks version used)
│   │   │   ├── part.sldprt (optionally sorted into folders)
│   │   │   ├── assy.sldasm (optionally sorted into folders)
│   │   │   ├── drawings/
│   │   │   │   ├── *.sldrw
│   │   │   │   └── *.pdf
│   │   │   └── hardware/ (standard, off-the-shelf parts like bolts, nuts, sensors)
│   │   │       ├── *.sldprt
│   │   │       └── *.step
│   │   └── procurement/
│   │       ├── README.md (include table summarizing all orders)
│   │       ├── bom.csv 
│   │       ├── major-component-1/ (rename based on component)
│   │       │   ├── README.md (summarizes specification and results of quoting process, links to key files)
│   │       │   ├── quote-1.pdf
│   │       │   ├── quote-2.pdf
│   │       │   ├── quote-3.pdf
│   │       │   └── fabrication-files/ (files sent to vendor for these quotes)
│   │       │       ├── *.stl
│   │       │       ├── *.step
│   │       │       └── *.dxf
│   │       └── major-component-2/ (rename based on component)
│   │           ├── README.md (summarizes specification and results of quoting process, links to key files)
│   │           ├── quote.pdf
│   │           └── fabrication-files/ (files sent to vendor for these quotes)
│   │               ├── *.stl
│   │               ├── *.step
│   │               └── *.dxf
│   ├── prototype-2-name/
│   │   ├── README.md 
│   │   └── ...
│   ⋮   
│   ├── prototype-x-name/
│   │   └── ...
│   └── shared-components (components used in multiple prototypes)
│       ├── README.md (table indicating which prototypes use each component)
│       ├── component-1-name/
│       │   └── ... (same as prototype folders)
│       ⋮
│       └── component-x-name/
│
├── publications/ (archive of publications)
│   ├──ECCE2025/
│   │   ├── digest/
│   │   │   ├── README.md (use publication template)
│   │   │   └── images/
│   │   │       ├── flowchart.svg 
│   │   │       ├── pareto-front.svg
│   │   │       └── ...
│   │   └── paper/
│   │       ├── README.md
│   │       └── images/
│   ├──ITEC2026/
│   │   ├── digest/
│   │   └── paper/
│   ├──TIA2026/
│   │   ├── README.md
│   │   └── images/
│   ⋮
│   └──CONFYEAR/
│
└── reports/ (archive of engineering reports)
    ├── report-1-name/
    │   ├── README.md (use report template)
    │   ├── optional-file.pdf
    │   └── images/ (optional)
    │       ├── fun-fig-1.svg
    │       ├── fun-fig-2.svg
    │       └── ...
    ├── report-2-name/
    ⋮
    └── report-x-name/
```

## Related Issues / PRs

- [Issue #33: Document prototypes folder folder contents specification](https://github.com/Severson-Group/research-repo-template/issues/33)
- [Issue #292: Brainstorm ideas on KB article on creating and releasing CAD designs](https://github.com/Severson-Group/KnowledgeBase/issues/292)
- [PR #42: Document overall research repo readme structure](https://github.com/Severson-Group/research-repo-template/issues/42)
