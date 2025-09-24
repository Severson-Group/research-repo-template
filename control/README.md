# Control <!-- omit from toc -->

**Documentation on project control folder.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [Folder Contents](#folder-contents)
- [How to Create a Publication Subfolder](#how-to-create-a-publication-subfolder)
- [Examples](#examples)

## Purpose of Document

This document explains the contents of the control folder and links to resources for documenting models.

## Folder Contents

This folder typically contains the [AMDC-Firmware](https://github.com/severson-group/amdc-firmware/) repo as a submodule (added by following [these steps](https://docs.amdc.dev/firmware/xilinx-tools/building-and-running-firmware.html#private-user-applications)) and will also contain other folders for user apps for the AMDC and for MATLAB Simulink control simulations and model-based-control development.

Note that there should only be [AMDC-Firmware](https://github.com/severson-group/amdc-firmware/) submodule.

## How to Create a Control Subfolder

At the time of creating this `README.md`, we do not have a specification for this folder. Check the latest version of our [research-repo-template](https://github.com/Severson-Group/research-repo-template/tree/main/modeling) for up to date instructions.

In the meantime, please refer to the [examples](#examples) below.

## Examples

- AMB unloader [control](https://github.com/Severson-Group/amb_unloader/tree/main/control/)
- ARL repo [BP4 control](https://github.com/Severson-Group/ARL-eturbo/tree/main/BP4/Control)
- NSF Revterra [control](https://github.com/Severson-Group/revterra-nsf-sttr/tree/main/Controls)
- NSF PFI [control](https://github.com/Severson-Group/nsf_pfi_bearingless/tree/main/control)
- Sandia [control](https://github.com/Severson-Group/sandia_sco2/tree/main/controls)

Note that our guidelines for creating control folders have evolved over time. Some of these example reports may have been created based on earlier guidelines.
