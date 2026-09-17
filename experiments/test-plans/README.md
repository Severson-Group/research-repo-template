# Test Plans <!-- omit from toc -->

**Instructions on creating experiment test plans.**

## Table of Contents <!-- omit from toc -->

- [Purpose of Document](#purpose-of-document)
- [When Test Plans are Needed](#when-test-plans-are-needed)
- [Approach](#approach)
- [Example Test Plans](#example-test-plans)
- [Related Issues / PRs](#related-issues--prs)

## Purpose of Document

This article provides instructions on establishing test plans for experiments. The goal is to provide a framework for creating formal plans that are reviewed and approved by the full team prior to conducting an experiment.

## When Test Plans are Needed

The need for test plans depends on the broader context of the experiment. The instructions provided here are intended for when formal, archival data needs to be collected for a peer reviewed paper or sponsored research project, or the level of hazard in the experiment is significant enough that formal procedures must be followed.

This document does not pertain to simple "debugging" of test benches in the lab.

### Examples of when test plans are needed <!-- omit from toc -->

- measuring motor parameters with the dyno at the eTorque facility
- measuring prototype parameters of a bearingless motor on the mill
- "running-in" your bearings on a 200 kW motor connected to a 20,000 r/min dyno (because the hazards involved in doing this to both personnel and equipment are significant).

### Examples of when test plans are not needed <!-- omit from toc -->

- Getting your current regulator to work for a low risk system
- Levitating your maglev motor for the first time

## Approach

Test plans should be created by using the [test-plan-template.md file](./test-plan-template.md).

Files should be stored within [`test-plans` folder](./). They can optionally be organized into subfolders based on prototype.

Where possible, draft test plans to be general so that they could be applied to any prototype by simply changing the parameters.

Keep the plans brief and use direct language.

## Example Test Plans

- [NSF PFI Repository test plans](https://github.com/Severson-Group/nsf_pfi_bearingless/tree/main/experiments/test-plans)

In the future, we plan to create standard test plans for frequently performed tests in the lab that can be adapted for use in individual repositories. This section will link to those plans.

## Related Issues / PRs

- [Issue #53: Create instructions on drafting test plans](https://github.com/Severson-Group/research-repo-template/issues/53)
- [Issue #51: Create instructions on how to archive test data, analysis scripts, and final reports](https://github.com/Severson-Group/research-repo-template/issues/51)
- [Issue PFI#617: Create a template for detailed test plans](https://github.com/Severson-Group/nsf_pfi_bearingless/issues/617)
