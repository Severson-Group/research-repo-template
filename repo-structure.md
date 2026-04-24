# Recommended Research Repository Structure <!-- omit from toc -->

**This article documents the folder structure recommended for use in research repositories.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [Recommended Repo Structure](#recommended-repo-structure)
- [Related Issues / PRs](#related-issues--prs)

## Purpose of Document

The goal of this article is to provide a bird's eye view of the recommended research repository structure.

## Recommended Repo Structure

```
research repo
|
├── README.md (repo landing page)
├── control/
|   ├── README.md
|   ├── AMDC-Firmware/ (git submodule)
|   ├── elev-control-lib/ (git submodule)
|   ├── jupyter/ (collection of notebooks to operate AMDC)
|   ├── project-firmware (AMDC firmware for this project)
|   |   ├── ldscript.ld
|   |   ├── Xilinx.spec
|   |   └── usr/
|   |       ├── blink/
|   |       ├── usr-app-1/
|   |       ⋮
|   |       └── usr-app-x/
|   └── simulink/
|       ├── README.md 
|       ├── control-sim-1/ (often used to autogen code)
|       |   ├── README.md
|       |   ├── control-sim-1.slx
|       |   ⋮
|       |   └── ...
|       ⋮
|       └── control-sim-x/
|
├── experiments/ (optionally organize into subfolders, e.g. per prototype or experiment)
|   ├── README.md
|   ├── instrumentation/
|   |   ├── README.md
|   |   ├── connection-schematic.svg
|   |   ├── ground-schematic.svg
|   |   ├── equipment-1/
|   |   |   └── README.md
|   |   ⋮
|   |   └── equipment-x/
|   └── results/
|   |   └── README.md (e.g., overview of where lab notebook & data is stored)
|   └── test-plans/
|       ├── README.md
|       ├── plan-1.md
|       ├── plan-2.md
|       ⋮
|       └── plan-x.md
|
├── modeling/
|   ├── README.md
|   ├── eMachPrivate/ (git submodule)
|   ├── model-1/ (often FEA, but could be analytic or other)
|   |   ├── README.md
|   |   ⋮
|   |   └── ...
|   ⋮
|   └── model-x/
|
├── project-sponsor-documents/
|   ├── README.md
|   ├── annual-reports/
|   |   ├── 2025/
|   |   ⋮   
|   |   └── 20xx/
|   └── proposal/
|
├── prototypes/
|   ├── power-electronics/ (or, locate in instrumentation)
|   |   ├── README.md (include connection tables)
|   |   ├── connection-schematic.svg
|   |   └── ... (follow other prototype folders' structure) 
|   ├── prototype-1-name/
|   |   ├── README.md (landing page for key information on the prototype, often includes nameplate)
|   |   ├── cad/
|   |   │   ├── README.md (includes revision table, design history, and SolidWorks version used)
|   |   │   ├── part.sldprt (optionally sorted into folders)
|   |   │   ├── assy.sldasm (optionally sorted into folders)
|   |   │   ├── drawings/
|   |   │   │   ├── *.sldrw
|   |   │   │   └── *.pdf
|   |   │   └── hardware/ (standard, off-the-shelf parts like bolts, nuts, sensors)
|   |   │       ├── *.sldprt
|   |   │       └── *.step
|   |   └── procurement/
|   |       ├── README.md (include table summarizing all orders)
|   |       ├── bom.csv 
|   |       ├── major-component-1/ (rename based on component)
|   |       │   ├── README.md (summarizes specification and results of quoting process, links to key files)
|   |       │   ├── quote-1.pdf
|   |       │   ├── quote-2.pdf
|   |       │   ├── quote-3.pdf
|   |       │   └── fabrication-files/ (files sent to vendor for these quotes)
|   |       │       ├── *.stl
|   |       │       ├── *.step
|   |       │       └── *.dxf
|   |       └── major-component-2/ (rename based on component)
|   |           ├── README.md (summarizes specification and results of quoting process, links to key files)
|   |           ├── quote.pdf
|   |           └── fabrication-files/ (files sent to vendor for these quotes)
|   |               ├── *.stl
|   |               ├── *.step
|   |               └── *.dxf
|   ├── prototype-2-name/
|   |   ├── README.md 
|   |   └── ...
|   ⋮   
|   ├── prototype-x-name/
|   |   └── ...
|   └── shared-components (components used in multiple prototypes)
|       ├── README.md (table indicating which prototypes use each component)
|       ├── component-1-name/
|       |   └── ... (same as prototype folders)
|       ⋮
|       └── component-x-name/
|
├── publications/
|   ├──ECCE2025/
|   |   ├── digest/
|   |   |   ├── README.md (use publication template)
|   |   |   └── images/
|   |   |       ├── flowchart.svg 
|   |   |       ├── pareto-front.svg
|   |   |       └── ...
|   |   └── paper/
|   |       ├── README.md
|   |       └── images/
|   ├──ITEC2026/
|   ├──TIA2026/
|   ⋮
|   └──CONFYEAR/
|
└── reports/
    ├── report-1-name/
    │   ├── README.md (use report template)
    │   ├── optional-file.pdf
    │   └── images/ (optional)
    │       ├── fun-fig-1.svg
    │       ├── fun-fig-2.svg
    |       └── ...
    ├── report-2-name/
    ⋮
    └── report-x-name/
```

## Related Issues / PRs

*Bullet list of all relevant issues to facilitate future readers in learning more about the material of the article.*

- _Issue #120: Route traces for the flux capacitor <-- make this a link to the relevant issue_
- _Issue #130: Create a report on the flux capacitor <-- make this a link to the relevant issue_
- _PR #142: Add report on the flux capacitor field lines <-- make this a link to the relevant PR_