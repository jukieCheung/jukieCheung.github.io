---
title: "A Small Note on Large Medical AI Datasets"
date: 2026-09-29
categories:
  - blog
tags:
  - MICCAI
  - medical imaging
  - datasets
  - medical AI
---

I recently went back to look at a large-scale dataset paper from MICCAI 2026. The dataset itself is, at least on paper, impressive: a large number of 3D medical images, paired reports, structured labels, and a benchmark built around multimodal models.

What bothered me was not the scale. The scale is obviously useful.

What bothered me was how easily scale can start to substitute for dataset science.

A dataset paper should probably be most rigorous exactly where ordinary model papers are often weakest: cohort description, annotation protocol, label definitions, uncertainty, inter-reader consistency, versioning, and the relationship between the released data and the benchmark claims. These are not supplementary details. They are the method.

Yet large datasets sometimes receive a strange kind of methodological discount. If the number is sufficiently impressive, the paper can begin to feel complete before those questions are actually answered.

I am also increasingly cautious about the phrase *expert-annotated*. In modern medical AI, that phrase can describe many different workflows. It may mean that experts independently reviewed every image. It may also mean that labels were first extracted from reports by a model, generated into a structured format, and then corrected by clinicians.

Both workflows can be reasonable.

They are not the same workflow.

The distinction matters because report-derived labels inherit what was written, what was omitted, and how the original report was phrased. If those labels later become “ground truth” for a benchmark, I would like to know much more about their reliability than simply how many clinician-hours were involved.

The same applies to “clinical” evaluation. If a model-generated report is scored by another large language model against a reference report and structured labels, that may be a useful consistency metric. Calling it clinical validation is more ambitious. I would personally want to see quantitative agreement with human readers before becoming too enthusiastic about that wording.

Another thing I find increasingly important is dataset lineage.

A dataset can evolve. New annotations can be added. New tasks can be created. VQA and reasoning labels can be layered on top of an existing image-report corpus. That is completely normal and often very valuable.

But once the same underlying dataset starts appearing in multiple forms, the relationship between those forms should be painfully explicit.

Which version corresponds to the published paper?

Which annotations were available at the time?

Which train/test split was used?

What changed later?

A benchmark should not become a moving target simply because the repository behind the paper keeps growing.

None of this means large medical datasets are unimportant. Quite the opposite. They are important enough that they deserve boring, meticulous documentation.

I would much rather read three pages of cohort statistics, annotation reliability, label definitions, and version history than another table showing twelve multimodal models producing slightly different BLEU scores.

There is a general lesson here for medical AI.

**Scale is valuable. Scale is not validation.**

“Expert-annotated” is not a reliability statistic.  
“Clinically aligned” is not a study design.  
“Reasoning” is not automatically image-grounded reasoning.  
And a large number in the title does not make the uncomfortable methodological questions disappear.

Sometimes the least glamorous part of a dataset paper is the part that matters most.
