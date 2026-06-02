# Modeling <!-- omit from toc -->

**Documentation on project modeling folder.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [Folder Contents](#folder-contents)
- [How to Create a Modeling Subfolder](#how-to-create-a-modeling-subfolder)
- [Examples](#examples)
- [Related Issues / PRs](#related-issues--prs)

## Purpose of Document

This document explains the contents of the modeling folder and links to resources for documenting models.

## Folder Contents

This folder typically contains the [eMachPrivate](https://github.com/Severson-Group/eMachPrivate) repo as a submodule and may also contain other model folders and modeling and optimization code as well as Simulink models.

Each modeling initiative gets its own subfolder. However, there should be only one [eMachPrivate](https://github.com/Severson-Group/eMachPrivate) submodule.

## How to Create a Modeling Subfolder

At the time of creating this `README.md`, we do not have a specification for this folder. Check the latest version of our [research-repo-template](https://github.com/Severson-Group/research-repo-template/tree/main/modeling) for up to date instructions.

In the meantime, please refer to the [examples](#examples) below.

## Examples

- AMB unloader [modeling](https://github.com/Severson-Group/amb_unloader/tree/main/modeling/)
- ARL repo [BP7 modeling](https://github.com/Severson-Group/ARL-eturbo/tree/main/BP7/Modeling)
- NSF PFI [modeling](https://github.com/Severson-Group/nsf_pfi_bearingless/tree/main/modeling)
- Sandia [modeling](https://github.com/Severson-Group/sandia_sco2/tree/main/modeling)

Note that our guidelines for creating modeling folders have evolved over time. Some of these example reports may have been created based on earlier guidelines.

## Related Issues / PRs

_Bullet list of all relevant issues to facilitate future readers in learning more about the material of the article._

- _Issue #7: Create and exercise detailed 3D JMAG models of prototype <-- make this a link to the relevant PR_
- _Issue #9: Characterize the design space with eMach <-- make this a link to the relevant issue_
- _Issue #11: Create 3D FEA model using quarter symmetry <-- make this a link to the relevant issue_
- _Issue #13: Create torque speed efficiency map <-- make this a link to the relevant issue_
- _Issue #20: Create python script to call the eMach analyzer over a range of torque and speed points <-- make this a link to the relevant issue_
- _Issue #21: Run python script to collect torque-speed-efficiency data <-- make this a link to the relevant issue_
