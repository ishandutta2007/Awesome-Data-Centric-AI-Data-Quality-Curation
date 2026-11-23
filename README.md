# Awesome-Data-Centric-AI-Data-Quality-Curation

# Top Data-Centric AI & Data Quality Curation Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Label Error Detection, Data Curation & Self-Hosted Quality Scoring*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Data-Centric AI & Data Quality Curation**. These tools help ML teams improve model performance by improving the data itself—detecting mislabeled examples, outliers, duplicates, and drift—covering everything from automated error detection libraries to commercial platforms for annotation, curation, and evaluation.

**Examples** include Cleanlab, Snorkel, Encord, Labelbox, V7, and cleanlab/cleanlab (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted data quality scoring, open-source label error detection, and community-driven curation—ideal for teams seeking to own their data pipeline without per-seat or per-row SaaS fees. The open-source landscape is anchored by **cleanlab**, the standard library for automated data issue detection with 11.7K+ stars , and **Snorkel**, the reference implementation for programmatic weak supervision .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Cleanlab Studio](https://cleanlab.ai/studio/)**  
  **The commercial no-code interface for cleanlab's automated data quality engine.** Ranks every datapoint by likelihood of having an issue, finds label errors and outliers, and provides an interface for efficiently re-labeling and fixing data . **Cut time spent on data quality by 1/3 and labeling spend by 5x–50x** according to the company . Supports tabular, text, image, video, and audio data. **Free to use at app.cleanlab.ai with demo data**; enterprise features via company email signup . Best for teams wanting Cleanlab's algorithms without writing code.

- **[Snorkel Flow](https://snorkel.ai/)**  
  **Programmatic labeling platform for bootstrapping datasets from domain expertise.** Users write labeling functions (heuristics, patterns, distant supervision rules) that Snorkel combines into probabilistic training labels . **Excels when labeled data is scarce or nonexistent**—enables creating 100k+ labeled examples in hours instead of months . **Tightly couples labeling with model training** for rapid iteration . Best for organizations with deep domain knowledge but no existing labels, especially in regulated NLP projects where rules can encode compliance requirements .

- **[Encord](https://encord.com/)**  
  **Multimodal data platform with active learning and curation built in.** Supports images, video, DICOM, documents, and audio, plus **RLHF-style evaluation workflows** for generative and multimodal models . **Encord Active** adds data curation and **label-error detection**—automatically surfacing likely mistakes for re-review . **Audit-grade traceability** useful in regulated industries . Pricing is quote-based with team plans . Best for teams combining vision, documents, and model-evaluation workflows who need curation alongside annotation.

- **[Labelbox](https://labelbox.com/)**  
  **Enterprise data platform with governance and workforce options.** Covers image, video, text, audio, PDFs, and geospatial tiles. **Catalog** for data management, model-assisted labeling (SAM 2 integration), active-learning-style prioritization, and **model evaluation** in one workspace . **QA is a strong point**: multi-step review queues, gold-set tasks, consensus scoring, and per-labeler analytics . **Free tier: 5,000 data rows, 3 users**; Starter from **$25/seat/month**; Enterprise includes SSO, SCIM, and on-prem options . Best for ML teams needing governance and workforce options in one place—costs scale quickly with volume .

- **[V7 (Darwin / Go)](https://www.v7labs.com/)**  
  **Best for medical imaging and document-heavy workflows.** **V7 Darwin** handles image, video, and 3D annotation with strong auto-annotate tools; **V7 Go** adds agentic automation for document extraction (receipts, invoices, contracts) with OCR for printed and handwritten text . **DICOM/NIfTI medical imaging support** makes it a favorite in healthcare, life sciences, and insurance . Pricing is custom-quoted by seats, data volume, and workflows . Best for regulated and visual-heavy domains needing strong automation out of the box.

- **[SuperAnnotate](https://www.superannotate.com/)**  
  **AI-assisted computer vision platform with optional managed annotation teams.** Supports image, video, text, audio, LiDAR point clouds, and documents. **Magnetic polygon tool** speeds complex outlines; foundation-model-assisted segmentation and a Python SDK for pipeline integration . **Multi-level review, per-annotator quality scores, and approve/disapprove states** make QA first-class. Free tier for small teams; paid plans quoted per seat plus usage . Best when computer vision is the core use case and outsourcing part of the workload is a possibility.

## Open-Source GitHub Projects

- **[cleanlab](https://github.com/cleanlab/cleanlab)**  
  **The standard open-source library for automated data and label issue detection.** **Apache-2.0**, **11.7K+ GitHub stars** . **Works with any ML model** by operating on predicted probabilities or feature embeddings—no model-specific dependency . **Detects label errors, outliers, near-duplicates, IID violations, and underperforming groups** via `Datalab.find_issues()` . **`CleanLearning`** trains a robust version of any scikit-learn-compatible classifier by automatically filtering low-quality data before fitting . **Beyond standard classification**: multi-label data (image/document tagging), sequence prediction (entity recognition), and data labeled by multiple annotators . **Install**: `pip install cleanlab` . **Best for teams wanting the reference implementation** for data-centric AI with a proven track record of finding thousands of label errors in ImageNet, MNIST, and other benchmarks .

- **[Snorkel (Open Source)](https://github.com/snorkel-team/snorkel)**  
  **The reference implementation for programmatic weak supervision.** **Apache-2.0** . Enables writing labeling functions (heuristics, patterns, distant supervision) that are combined into probabilistic training labels—**bootstrapping datasets when manual annotation is too expensive or slow** . **Active maintenance has slowed** as the community shifted toward Snorkel Flow and LLM-based labeling sources, but the library remains the most cited reference implementation . **Best for teams wanting to start with weak supervision** before committing to the commercial platform.

- **[Argilla](https://github.com/argilla-io/argilla)**  
  **Data-centric NLP platform with weak supervision integrations.** **Apache-2.0** . Focused on **data quality curation for NLP**—annotation, review, and dataset management with human-in-the-loop workflows . **Best for NLP teams** wanting a self-hosted curation platform with weak supervision support.

- **[fastdup](https://github.com/visual-layer/fastdup)**  
  **Fast, free tool for generating insights from image and video datasets.** **1.9K+ stars** . Helps **enhance data quality and labels** while reducing data operation costs, with unmatched scalability for visual datasets . **Best for computer vision teams** needing rapid dataset quality assessment.

- **[DataProfiler](https://github.com/capitalone/DataProfiler)**  
  **What's in your data? Extract schema, statistics, and entities from datasets.** **Apache-2.0**, **1.6K+ stars** . **Best for structured data profiling** as a first step before curation.

### Additional Strong Open-Source Options

- **Data-Juicer** (7.2K+ stars, Apache-2.0) — Data processing for and with foundation models; covers cleaning, filtering, deduplication, and quality scoring for LLM training data [citation:14].
- **DataFlow** (8.4K+ stars, Apache-2.0) — Easy data preparation with LLM-based operators and pipelines [citation:14].
- **Curator** (1.8K+ stars, Apache-2.0) — Scalable data preprocessing and curation toolkit for LLMs [citation:14].
- **text-dedup** (764+ stars, Apache-2.0) — All-in-one text de-duplication [citation:14].
- **skweak** (MIT) — Snorkel-style weak supervision specialized for NLP and sequence labeling [citation:15].
- **WRENCH** (Apache-2.0) — Benchmark and evaluation suite for weak supervision [citation:15].
- **Autodistill** (Apache-2.0) — Foundation model labeling pipelines for computer vision [citation:15].

**Frameworks for building custom systems**: Combine **cleanlab** for automated label error detection, **Snorkel** for programmatic labeling when data is scarce, and **Argilla** for human-in-the-loop NLP curation. For LLM training data, **Data-Juicer** and **DataFlow** provide scalable cleaning and filtering pipelines.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Data curation tools process training datasets that may contain sensitive or proprietary information; enforce access controls and validate data handling policies, especially when using SaaS platforms that ingest raw data.
- **Tool choice depends on whether you need to clean existing data or create new labels.** **Cleanlab excels at auditing and cleaning existing datasets**—it found 4.4% of ImageNet training labels as likely incorrect, and retraining improved accuracy by over 1.5 percentage points . **Snorkel Flow excels when labeled data is scarce**—it bootstraps datasets from domain-expert rules rather than cleaning what exists . **Encord and Labelbox bundle curation with annotation and evaluation** for teams wanting one platform across the workflow . **Open-source cleanlab is genuinely production-ready** with Apache-2.0 licensing and active maintenance , while **Snorkel's open-source maintenance has slowed** . Validate whether you need cleaning (cleanlab), labeling from scratch (Snorkel), or an end-to-end platform (Labelbox, Encord) before committing.

---

**Made for ML engineers, data quality analysts, and teams building reliable training data pipelines.**  
Let's make data-centric AI and data curation more open, auditable, and quality-driven.
