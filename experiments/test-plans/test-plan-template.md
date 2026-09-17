# Test Plan Name <!-- omit from toc -->

**This article provides the test procedure to measure _[INSERT brief phrase about measurement goals]_.**

## Table of Contents <!-- omit from toc -->

- [1. Purpose of Document](#1-purpose-of-document)
- [2. Safety Instructions](#2-safety-instructions)
  - [2.1 Risk Levels](#21-risk-levels)
  - [2.2 Additional Safety Instructions](#22-additional-safety-instructions)
- [3. Required Equipment](#3-required-equipment)
  - [3.1 Equipment list](#31-equipment-list)
  - [3.2 Special Considerations](#32-special-considerations)
- [4. Test Plan](#4-test-plan)
  - [4.1 Measurement Configuration](#41-measurement-configuration)
  - [4.2 Procedure](#42-procedure)
  - [4.3 Instrument Configuration Instructions](#43-instrument-configuration-instructions)
  - [4.4 Data to be Collected](#44-data-to-be-collected)
- [5. Analysis](#5-analysis)
  - [5.1 Post Processing Data](#51-post-processing-data)
  - [5.2 Success Criteria](#52-success-criteria)
- [6. Related Tests from Previous Projects](#6-related-tests-from-previous-projects)
- [7. Related Issues / PRs](#7-related-issues--prs)

## 1. Purpose of Document

The purpose of this article is to document the detailed test procedure for the _[INSERT: brief description of the test]_ test. _[INSERT: optional additional sentence about why this test is being conducted (what high level thing does it allow one to learn about the prototype?)]_.

## 2. Safety Instructions

Standard eLev Lab and eTorque testcell safety policies apply.

Key links:

- Google [Shared Drive Safety Folder](https://drive.google.com/drive/u/0/folders/1U7TKoIDYLqgXNWcrX0taFcNDifeHO_rO)
- eLev lab [safety article](https://github.com/Severson-Group/KnowledgeBase/tree/main/lab/safety)
- eTorque facility [safety policies](https://github.com/Severson-Group/etorque-testbed/tree/main/safety)

> [!Tip]
> If the test is not conducted at MERL, remove references to the eTorque facility.

### 2.1 Risk Levels

_**State whether the electrical hazard is low, medium, or high risk**, according to [this table](https://docs.google.com/presentation/d/1bF_Lsw4f45h2ZfhxKL6wHZyp7JDuLXzI8HSQxaIIn4Y/edit?slide=id.g32f6d5ce020_2_53#slide=id.g32f6d5ce020_2_53). Include what training is required for the stated risk level._

### 2.2 Additional Safety Instructions

_**Include any additional safety instructions** or precautions that should be followed which are not covered by the material listed above._

## 3. Required Equipment

### 3.1 Equipment list

_**Bullet list of equipment** required to perform the test._

### 3.2 Special Considerations

_**Bullet list of any important considerations** when performing the test, such as wiring / gaurding / fixturing to avoid damaging the equipment._

## 4. Test Plan

### 4.1 Measurement Configuration

_**Include a schematic that illustrates the connection of this test's required equipment.** The source of this image must be shared with the team so that it can be easily revised. Preferred methods: 1) an SVG committed directly into the repo; 2) a webp file generated from a Google Drawing that is stored in the Shared Google Drive at `experiments/test-plans/images` -- provide a link to the source in the figure capton._

_**Bullet list of planned physical quantities** to measure and the measurement equipment required to measure each of them._

### 4.2 Procedure

_**Numbered list of steps** required for carrying out this test. Keep it brief and focused on the narrative of steps need to be done to make the measurement. Save detailed instructions for configuring settings in the test equipment for [4.3 Instrument Configuration Instructions](#43-instrument-configuration-instructions)._

### 4.3 Instrument Configuration Instructions

_**Instructions** (or links to instructions / manuals) **on how to configure the test equipment.** Favor brevity. Don't waste time/space on describing "obvious" settings that every researcher in the lab should know (i.e., don't describe nuanced menu steps to configure the oscilloscope trigger for a standard measurement like 3 phase currents, but if an unconventional trigger setting is important to describe how to set that up). When possible, point readers to a relevant section in a user manual instead of retyping the steps from the manual. Link to other relavent markdown docs, articles, manuals, etc._

### 4.4 Data to be Collected

_**Bullet list of data** that should be saved from the test._

## 5. Analysis

### 5.1 Post Processing Data

_**Brief overview of how to analyze and interpret the data** obtained from the test. For example, if the goal of the test is to measure the torque constant_ $k_\mathrm{t}$ _and your procedure tells us to record phase currents at different torque points, you might tell us how to calculate_ $i_\mathrm{q}$ _from your phase currents or to make a plots of torque vs phase current amplitude. Don't get overly detailed; save that for your test report._

### 5.2 Success Criteria

_**How to know if the test was successful / whether we can trust the data**. Depending on the test, this can be easy to articulate ("thermal equilibrium reached within one hour"; or, "torque vs rotor position approximates FEA results documented report xxxx Fig. 2") or challenging. Again, keep this brief (2 - 3 sentences) and along the lines of a sanity check._

## 6. Related Tests from Previous Projects

_**Bullet list of links to similar tests** that were conducted as part of other projects to help plan this test._

## 7. Related Issues / PRs

- [Issue #53: Create instructions on drafting test plans](https://github.com/Severson-Group/research-repo-template/issues/53)
- [Issue #51: Create instructions on how to archive test data, analysis scripts, and final reports](https://github.com/Severson-Group/research-repo-template/issues/51)
- [Issue PFI#617: Create a template for detailed test plans](https://github.com/Severson-Group/nsf_pfi_bearingless/issues/617)
