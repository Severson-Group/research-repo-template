# Firmware <!-- omit from toc -->

**Documentation on project firmware folder.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [Folder Contents](#folder-contents)
- [How to Create a Control Subfolder](#how-to-create-a-control-subfolder)
- [Examples](#examples)
- [Related Issues / PRs](#related-issues--prs)

## Purpose of Document

This document explains the contents of the firmware folder and links to resources for documenting models.

## Folder Contents

This folder typically contains the [AMDC-Firmware](https://github.com/severson-group/amdc-firmware/) repo as a submodule (added by following [these steps](https://docs.amdc.dev/firmware/xilinx-tools/building-and-running-firmware.html#private-user-applications)) and will also contain other folders for user apps for the AMDC and Jupyter notebooks to control the AMDC.

Note that there should only be [AMDC-Firmware](https://github.com/severson-group/amdc-firmware/) submodule.

## How to Create a Firmware Subfolder

See the [Recommended Repo Structure](../repo-structure.md) for a specification on how to structure this folder. Check the latest version of our [research-repo-template](https://github.com/Severson-Group/research-repo-template/tree/main/control) for up to date instructions.

## Examples

- NSF PFI [firmware](https://github.com/Severson-Group/nsf_pfi_bearingless/tree/main/firmware)
- Sandia [firmware](https://github.com/Severson-Group/sandia_sco2/tree/main/firmware)

## Related Issues / PRs

_Bullet list of all relevant issues to facilitate future readers in learning more about the material of the article._

- _Issue #18: Simulate machine under load <-- make this a link to the relevant issue_
- _Issue #19: Order PCBs <-- make this a link to the relevant PR_
