---
title: Proteins at Scale Cookbook
subtitle: Recipes for running structural biology workflows at scale on CHTC
short_title: Proteins at Scale
---

The **Proteins at Scale Cookbook** collects step-by-step recipes for running protein and structural biology workflows on the [Center for High Throughput Computing (CHTC)](https://chtc.cs.wisc.edu) system. Each recipe is a complete workflow that has been run on CHTC: it comes with HTCondor submit files, container images, a toy dataset, and guidance on GPU selection, data movement, and failure modes.

The recipes are written for researchers who already know *what* they want to model and need to know *how* to run it as hundreds or thousands of jobs. They are not an introduction to structural biology.

## Recipes

:::{card} Predicting Protein Structures with AlphaFold3 on CHTC GPUs
:link: ./01-AlphaFold3/01.1-Introduction.md

Run AlphaFold3 as a two-stage workflow: CPU jobs that generate alignments against pre-staged databases, then GPU jobs that predict structures. Covers preparing input JSONs from a CSV manifest, choosing GPU memory by token count, unified memory for ultra-large complexes, and visualizing the results.
:::

More recipes are in preparation. See [how to contribute](https://dmora127.github.io/chtc-biocafe-cookbook/frontmatter/contribute) if you have a workflow to share.

## Before You Start

Every recipe assumes that you:

* Have a CHTC HTC account and can log into an Access Point (for example `ap2001.chtc.wisc.edu`). Request an account through the [CHTC account request form](https://chtc.cs.wisc.edu/uw-research-computing/form.html).
* Have a `/staging` directory for large files. Request one through the [CHTC large data guide](https://chtc.cs.wisc.edu/uw-research-computing/file-avail-largedata).
* Can submit and monitor HTCondor jobs. If you are new to HTCondor, complete the [Roadmap to getting started](https://chtc.cs.wisc.edu/uw-research-computing/htc-roadmap) first.
* Are comfortable on the Linux command line.

## Companion Repositories

The executables, submit files, and container definitions used by each recipe live in a companion GitHub repository that you clone onto the Access Point:

| Recipe | Repository |
|--------|------------|
| AlphaFold3 on CHTC GPUs | [CHTC/tutorial-CHTC-AF3](https://github.com/CHTC/tutorial-CHTC-AF3) |

## How to Cite

If this cookbook helped your research, please cite it. A citation file (`CITATION.cff`) is included in the repository, and a DOI is minted for each tagged release.

> Morales, D. A. (2026). *Proteins at Scale Cookbook*. Center for High Throughput Computing, University of Wisconsin-Madison. https://github.com/dmora127/Proteins-at-Scale-Cookbook

## Part of the CHTC Bioinformatics Cookbooks

This cookbook is one volume of the [CHTC Bioinformatics Cookbooks](https://dmora127.github.io/chtc-biocafe-cookbook/), which also include conceptual chapters on high-throughput computing for bioinformatics and the [Genomics at Scale Cookbook](https://github.com/dmora127/Genomics-at-Scale-Cookbook). Content is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
