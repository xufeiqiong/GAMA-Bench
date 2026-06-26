# GAMA-Bench

[![arXiv](https://img.shields.io/badge/arXiv-2606.14068-b31b1b.svg)](https://arxiv.org/abs/2606.14068)

This repository contains the official code for **GAMA-Bench**.

GAMA-Bench is a benchmark designed to evaluate gender-asymmetric moral alignment in large language models through controlled mirrored scenarios. We construct paired prompts that differ only in the gender of the key actor, enabling systematic analysis of whether models apply consistent moral, emotional, and behavioral judgments across gender conditions.

## Main Results

We evaluate 10 representative LLMs on GAMA-Bench and report paired gender gaps under matched male-actor and female-actor prompts.

All gaps are computed as:

[
\Delta = \text{Female Actor} - \text{Male Actor}
]

Thus, negative values indicate stronger framing toward male actors, while positive values indicate stronger framing toward female actors. For Emp.-Agg., Instr., and Full-Bl., values are reported in percentage points.

| Metric        | Meaning                                             |
| ------------- | --------------------------------------------------- |
| **Puni.**     | Punitive or condemning wording                      |
| **Ther.**     | Therapeutic, empathetic, or contextualizing wording |
| **Sev.**      | Severity / escalation rating                        |
| **Emp.-Agg.** | Empathy toward the aggressor                        |
| **Instr.**    | Instructional or accusatory framing                 |
| **Full-Bl.**  | Full-blame attribution to the aggressor             |

### Average Gender Gaps

| Track        |   Puni. Δ |   Ther. Δ |    Sev. Δ |  Emp.-Agg. Δ |      Instr. Δ |    Full-Bl. Δ |
| ------------ | --------: | --------: | --------: | -----------: | ------------: | ------------: |
| **Intimate** | **-3.31** | **+1.27** | **-0.40** | **+8.99 pp** | **-14.25 pp** | **-22.99 pp** |
| **Public**   | **-1.22** | **+0.94** | **-0.04** | **+4.09 pp** |  **-8.93 pp** |  **-6.30 pp** |

Across both tracks, models consistently assign more punitive, escalatory, instructional, and blame-centered framing to male actors, while assigning more therapeutic and empathy-oriented framing to female actors under the same misconduct.

### Intimate Track

| Model               | Puni. Δ | Ther. Δ | Sev. Δ | Emp.-Agg. Δ | Instr. Δ | Full-Bl. Δ |
| ------------------- | ------: | ------: | -----: | ----------: | -------: | ---------: |
| GPT-5.4             |   -1.14 |   +0.78 |  -0.41 |     +5.9 pp |  -8.5 pp |   -22.3 pp |
| GPT-5.2             |   -1.60 |   +0.68 |  -0.35 |     +5.8 pp | -10.5 pp |   -25.6 pp |
| Gemini-2.5-Pro      |   -5.09 |   +1.63 |  -0.41 |    +11.0 pp | -16.2 pp |   -21.0 pp |
| Gemini-3-Pro        |   -6.39 |   +1.46 |  -0.37 |    +10.5 pp | -16.4 pp |   -22.3 pp |
| Doubao-Seed-2.0-Pro |   -4.16 |   +1.75 |  -0.49 |    +17.2 pp | -27.6 pp |   -37.4 pp |
| MiniMax-M2.7        |   -1.23 |   +0.64 |  -0.28 |     +4.5 pp | -15.5 pp |   -19.0 pp |
| Qwen3               |   -3.75 |   +1.80 |  -0.42 |    +13.1 pp | -19.4 pp |   -32.5 pp |
| Qwen3.5             |   -2.72 |   +1.13 |  -0.42 |     +5.7 pp |  -8.7 pp |   -18.0 pp |
| DeepSeek-V4-Pro     |   -3.51 |   +1.74 |  -0.39 |    +10.2 pp | -15.0 pp |   -24.3 pp |
| Kimi-2.5            |   -3.51 |   +1.05 |  -0.45 |     +6.0 pp |  -4.7 pp |    -7.5 pp |

### Public Track

| Model               | Puni. Δ | Ther. Δ | Sev. Δ | Emp.-Agg. Δ | Instr. Δ | Full-Bl. Δ |
| ------------------- | ------: | ------: | -----: | ----------: | -------: | ---------: |
| GPT-5.4             |   -0.87 |   +0.37 |  -0.00 |     +1.7 pp |  -4.7 pp |    -2.6 pp |
| GPT-5.2             |   -1.17 |   +0.25 |  +0.01 |     +0.9 pp |  -7.1 pp |    -9.4 pp |
| Gemini-2.5-Pro      |   -1.81 |   +1.10 |  -0.17 |     +2.6 pp | -12.0 pp |   -11.3 pp |
| Gemini-3-Pro        |   -1.59 |   +0.68 |  -0.12 |     +3.0 pp | -13.1 pp |   -10.5 pp |
| Doubao-Seed-2.0-Pro |   -1.12 |   +0.47 |  -0.05 |     +2.7 pp | -10.2 pp |    -2.7 pp |
| MiniMax-M2.7        |   -0.42 |   +0.37 |  +0.05 |     +2.6 pp |  -5.6 pp |    -5.1 pp |
| Qwen3               |   -1.26 |   +2.45 |  -0.02 |    +13.0 pp | -14.1 pp |    -9.4 pp |
| Qwen3.5             |   -0.79 |   +1.09 |  +0.01 |     +4.6 pp |  -6.4 pp |    -4.9 pp |
| DeepSeek-V4-Pro     |   -1.25 |   +1.45 |  -0.06 |     +5.2 pp | -11.1 pp |    -5.3 pp |
| Kimi-2.5            |   -1.90 |   +1.17 |  -0.01 |     +4.6 pp |  -5.0 pp |    -1.8 pp |


## Status

We are currently organizing the dataset, evaluation scripts, and documentation.

The full dataset and official code will be released soon.

## Coming Soon

* GAMA-Bench dataset
* Prompt templates and mirrored scenario construction pipeline
* Evaluation scripts
* Model response collection pipeline
* Metric computation code
* Reproduction instructions

## Citation

If you find **GAMA-Bench** useful, please cite our paper:

```bibtex
@misc{si2026harshermaleevaluatingllms,
      title={Harsher on Male? Evaluating LLMs on Gender-Asymmetric Moral Framing Across Diverse Conflict Scenarios}, 
      author={Guangzong Si and Dong Wang and Zhenhao Li and Yifan Yu and Panwang Pan and Wentao Zhu},
      year={2026},
      eprint={2606.14068},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2606.14068}, 
}
```

## Contact

For questions or updates, please refer to this repository.
