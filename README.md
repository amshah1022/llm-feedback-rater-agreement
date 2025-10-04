# LLM Feedback Rater Agreement

This project evaluates the consistency of formative feedback scoring in clinical education using both human annotators and a large language model (Claude). The goal is to assess how well structured rubrics can support reliable evaluation—and whether AI tools can serve as consistent, pedagogically aligned raters.

## Overview

We computed:
- **Krippendorff’s Alpha** to measure inter-rater agreement across three trained human annotators.
- **Cohen’s Kappa** to measure alignment between Claude scores and the human majority vote.

The rubric applied scored feedback across 7 traits (e.g., Constructive Tone, Actionable Suggestions, Student Learning) using binary scoring (0 = does not meet criterion, 1 = meets criterion).

## Results

- **Krippendorff’s Alpha** (Human-Human Agreement): `0.575`
- **Cohen’s Kappa** (Claude vs. Human Majority): `0.738`

Traits with observable anchors (e.g., tone, specificity) had stronger agreement. Traits requiring interpretive judgment (e.g., learning value) showed more variability.

## Files

- `Cleaned_Long-Format_Scores.csv` – Long-format dataset with rater, trait, score, and feedback ID.
- `analysis.py` – Script to compute Krippendorff’s Alpha and Cohen’s Kappa.
- `README.md` – Project documentation.

## Dependencies

- Python 3.x
- `pandas`
- `numpy`
- `scikit-learn`
- `krippendorff`

Install with:

```bash
pip install pandas scikit-learn krippendorff
