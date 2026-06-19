# Aspect-Target-Aware Contextual Abusive Content Detection Dataset for Bengali Social Media

## Overview

This repository provides a manually annotated **Bengali abusive content dataset** designed to support research on abusive language detection, contextual content analysis, target identification, and computational social science in low-resource languages.

The dataset consists of **1,500 Bengali social media comments** collected from publicly available YouTube discussions on major Bangladeshi news channels, including *Jamuna TV, Somoy TV, ATN News,* and *RTV*. Unlike conventional abusive language datasets that treat comments as isolated instances, this corpus preserves conversational structure through parent-child relationships and thread-level context, enabling context-aware abusive content analysis.

The dataset was developed as part of our research on **aspect-aware and contextual abusive content detection in Bengali social media**.

---

## Dataset Characteristics

| Attribute           | Description                         |
| ------------------- | ----------------------------------- |
| Language            | Bengali                             |
| Source              | Public YouTube comments             |
| Domain              | News and public affairs discussions |
| Total Comments      | 1,500                               |
| Labels              | Abusive / Non-abusive               |
| Context Information | Parent comment, thread sequence     |
| Aspect Categories   | 11                                  |
| Target Categories   | 4                                   |

---

## Dataset Schema

Each record contains the following fields:

| Column         | Description                                          |
| -------------- | ---------------------------------------------------- |
| `ID`           | Unique identifier of the comment                     |
| `post_title`   | Title of the source YouTube post/video               |
| `Comment`      | Target comment text                                  |
| `parent`       | Parent comment identifier for contextual linkage     |
| `sequence`     | Position of the comment within the discussion thread |
| `aspect`       | Topic category associated with the comment           |
| `target`       | Abuse target category                                |
| `abusive(y/n)` | Binary abuse label (Yes/No)                          |

The inclusion of `parent` and `sequence` fields enables researchers to reconstruct conversation threads and investigate contextual dependencies in abusive language.

---

## Aspect Categories

The dataset contains annotations across the following aspect categories:

* Politics
* Sports
* Education
* Economy
* Social
* Religion
* Entertainment
* Behavior
* gender
* none

These categories facilitate aspect-aware abusive content analysis and enable fine-grained investigations of abuse across different discussion topics.

---

## Target Categories

Abusive comments are further categorized according to their primary target:

* Individual
* Group
* Society
* Others

This target-level annotation supports research on abuse target identification and harmful content understanding.

---

## Annotation Examples

### Example 1: Abusive Comment

**Comment:**

> এরা ছাত্র না, এ রাজাকারের বাচ্চা।

**English Translation:**

> They are not students; they are the children of collaborators.

**Annotations:**

| Label   | Value    |
| ------- | -------- |
| Abusive | Yes      |
| Aspect  | Politics |
| Target  | Group    |

---

### Example 2: Non-Abusive Comment

**Comment:**

> বাংলাদেশ দল আজ দারুণ খেলেছে, গর্বিত বোধ করছি।

**English Translation:**

> The Bangladesh team played really well today; I feel proud.

**Annotations:**

| Label   | Value  |
| ------- | ------ |
| Abusive | No     |
| Aspect  | Sports |
| Target  | Group  |

---

## Potential Research Applications

This dataset can be used for:

* Abusive language detection
* Context-aware text classification
* Aspect-based abusive content analysis
* Abuse target identification
* Explainable AI for content moderation
* Bengali NLP research
* Low-resource language studies
* Computational social science

---

## Citation

If you use this dataset in your research, please cite dataset repository.

## License

This dataset is intended solely for academic and research purposes. Users are responsible for complying with the terms of the source platforms and applicable ethical guidelines when using the data.
