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

I recently went back to a large-scale medical imaging dataset paper from MICCAI this year. I will not name it here, because the point is less about one paper than about a style of dataset work that I find increasingly difficult to understand.

The paper looks impressive at first glance: tens of thousands of 3D MRI–report pairs, structured clinical labels, multimodal models, expert involvement, and a set of “clinical” evaluation metrics. All of them are very modern.

The strange part is that, after reading the paper, I still had rather basic questions about the dataset itself.

How exactly were the structured labels constructed? Were experts independently re-reading the images under a unified annotation protocol, or were labels mainly extracted from existing reports and then corrected? What were the operational definitions for the taxonomy? Which grading standards were used? How were ambiguous cases handled? What did the label distribution actually look like?

For a model paper, these might be implementation details. For a dataset paper, these *are the method*.

That distinction seems obvious, but large dataset papers sometimes receive a curious methodological discount. Once the sample size becomes sufficiently large, the number itself starts doing rhetorical work that would normally have to be done by validation.

A large number is certainly useful. It is not an annotation protocol.

The phrase *expert-annotated* deserves similar care. Human–AI collaborative annotation is completely reasonable, especially at scale. A model can structure reports, generate candidate labels, and reduce enormous amounts of repetitive work. Experts can then verify and correct those outputs.

There is nothing wrong with that workflow. But it is not the same as independent image-level expert annotation, and the difference should be made painfully clear. Report-derived labels inherit whatever was documented in the original report, including omissions, uncertainty, reporting habits, and institutional conventions. If those labels later become benchmark “ground truth,” then annotation reliability becomes one of the most important results in the paper.

I would therefore expect things such as inter-reader agreement, adjudication statistics, error rates before and after expert correction, or at least a carefully validated subset. Instead, we are often told how many expert hours were involved. Hours are useful information. They are not a reliability statistic.

I had a similar reaction to the clinical evaluation. The paper introduced several clinically named metrics, but the final scoring was performed by a large language model using structured prompts.

Again, this can be useful.

An LLM-based evaluator may be a perfectly practical way to compare thousands of generated reports. But if the metric is supposed to support claims about clinical validity, I would like to see quantitative evidence that its scores agree with clinicians. “Experts thought the outputs looked reasonable” and “the evaluator agrees with experts” are different levels of evidence.

There is also a framing problem that appears quite often in medical multimodal work. Report generation, image understanding, diagnostic reasoning, and clinical diagnosis gradually become interchangeable terms as the paper progresses.

They are not interchangeable.

Generating a report that resembles a reference report is a legitimate and useful task. It does not automatically demonstrate autonomous diagnosis, clinical reasoning, or clinical decision-making. Those stronger words require stronger evidence.

What makes this slightly ironic is that the missing information is not exotic. Nobody is asking for a new architecture.

I would happily trade another benchmark table for:

- a complete annotation schema;
- exact label definitions;
- severity-grading criteria;
- cohort and label distributions;
- a clear account of what was extracted from reports and what was independently judged from images;
- quantitative annotation-quality analysis;
- and validation of the proposed clinical metrics against human readers.

This material is sometimes treated as supplementary detail because conference pages are limited.

I am not fully convinced by that argument.

If the main contribution is a dataset, then the dataset should probably fit into the dataset paper.

A benchmark can always add one fewer model.

The broader lesson, at least for me, is that dataset science has to be boring in exactly the right places. Cohort composition, label provenance, annotation rules, reader agreement, uncertainty, and versioning are not glamorous. They do not produce colorful architecture diagrams.

They are also the parts that determine whether everyone else's future experiments mean anything.

So I remain very enthusiastic about large medical datasets.

I am simply becoming less enthusiastic about treating **scale as evidence of quality**.

A dataset can be large, expert-assisted, clinically motivated, and still be methodologically under-described.

And when the dataset itself is the contribution, “we will provide the details elsewhere” is a surprisingly ambitious thing to ask the reader to accept.
