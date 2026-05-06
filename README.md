# Safety in Spanish: A Cross-Lingual Evaluation of Jailbreak Vulnerability in LLMs

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Paper

[Paper Link](https://openreview.net/forum?id=qUiN68s7ot)

## Description

This repository contains the code and data for evaluating the safety of Large Language Models (LLMs) in Spanish contexts, focusing on cross-lingual jailbreak vulnerabilities. The project assesses how well various LLMs resist prompt injection attacks when prompts are translated into Spanish, using benchmarks such as AdvBench, HarmBench, and JailbreakBench.

The analysis includes:

- Attack Success Rate (ASR) evaluation
- Statistical tests (e.g., McNemar tests)
- Response language analysis
- Comparative performance across models

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/spanish_prompts_injection.git
   cd spanish_prompts_injection
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   Note: The `requirements.txt` file includes packages such as `scikit-learn`, `pandas`, `matplotlib`, `seaborn`, and `statsmodels`.

## Usage

### Data Preparation

- Raw data is located in `data/raw/`.
- Processed benchmarks are in `data/final/`.
- Model responses are in `data/responses/`.

### Running Analysis

Use the Jupyter notebooks in `notebooks/`:

- `notebooks/analysis/analysis.ipynb`: Main analysis notebook for ASR, statistical tests, and visualizations.
- `notebooks/evaluation/evaluation.ipynb`: Evaluation scripts.
- `notebooks/inference/experiments.ipynb`: Inference experiments.

To run the analysis:

1. Open the notebook in Jupyter or VS Code.
2. Execute the cells to load data, perform analysis, and generate results.

### Key Scripts

- Load judgments from `results/judgments.jsonl`.
- Analyze responses from `data/responses/responses_all.csv`.
- Use benchmark data from `data/final/benchmark.csv`.

## Data

### Benchmarks

- **AdvBench**: Adversarial prompts for misinformation and harmful content.
- **HarmBench**: Harmful behavior prompts.
- **JailbreakBench**: Jailbreak attack prompts.

Prompts are available in both English (`en`) and Spanish (`es`), with attack types including:

- Direct
- Roleplay
- Hypothetical

### Models Evaluated

- Mistral-7B-Instruct-v0.3
- Qwen2.5-3B-Instruct
- Qwen2.5-7B-Instruct
- Meta-Llama-3-8B-Instruct
- Claude-Haiku (custom version)

### Results

- Judgments and labels in `results/judgments.jsonl` and `results/judgments.csv`.
- Manual labels in `results/manual_labels.jsonl`.
- Analysis outputs include ASR tables, plots, and statistical comparisons.

## Results

The project provides insights into:

- How LLMs perform on Spanish prompts compared to English.
- Vulnerability to different attack types.
- Cross-model comparisons.

Key outputs:

- ASR@1 tables
- McNemar test results
- Response language breakdowns
- Visualizations (plots)

See `notebooks/analysis/analysis.ipynb` for detailed results and code.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If you use this code or data, please cite:

```
@misc{yourname2024safetyspanish,
  title={Safety in Spanish: A Cross-Lingual Evaluation of Jailbreak Vulnerability in LLMs},
  author={Your Name},
  year={2024},
  url={https://github.com/yourusername/spanish_prompts_injection}
}
```
