# Self-Adaptive Cognitive Debiasing for Large Language Models in Decision-Making

This repository provides implementations and evaluation pipelines for self-adaptive cognitive debiasing methods applied to large language models (*LLMs*) in decision-making scenarios.

## Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [Pipeline](#pipeline)
- [APIs](#apis)
- [Dataset Preparation](#dataset-preparation)
- [Evaluation](#evaluation)
- [Obtaining Results](#obtaining-results)
- [File Descriptions](#file-descriptions)
- [Citation](#citation)

## Overview

This project explores various debiasing techniques for LLMs in decision-making, including Chain-of-Thought (CoT), Zero-Shot, Few-Shot, Multi-Agent Debate, Reflexion, and our proposed SACD method. Experiments span multiple domains and bias types.

## Quick Start

1. **API Keys**
   - Before running any `.ipynb` files, add your API keys:
     - **OpenAI** (`gpt-3.5-0125`, `gpt-4o`): Obtain keys from [OpenAI](https://platform.openai.com/)
     - **Groq (LLaMA3-70B)**: Obtain free API keys from [Groq](https://groq.com/)

2. **Setting API Keys**
   - Insert your API key at the top of relevant `.ipynb` files:
   ```python
   client = OpenAI(api_key="YOUR_OPENAI_API_KEY")
   ```

## Pipeline

![pipeline](pic/pipeline.png)
_Visualization of the cognitive debiasing pipeline for LLMs._

## APIs

- **OpenAI models** used: `gpt-3.5-0125` and `gpt-4o`
- **Groq models** used: `llama3-70b` (free API keys available)

## Dataset Preparation

1. Download the original dataset from the paper's official link.
2. Create a `data/` directory and add the dataset files.
3. Run **`data_process.ipynb`** to preprocess data and generate the `.jsonl` file in the `data` folder.

## Evaluation

You can evaluate various bias types and debiasing methods using the generated `.jsonl` file.

- Ensure your API keys are set at the beginning of each notebook.
- Execute the notebook file for your desired method/domain:
  - For **Bias Only**: `Availableing-bias.ipynb`
  - For **Chain-of-Thought (CoT)**: `Cot.ipynb`
  - For **Zero-Shot**: `Zero-shot.ipynb`
  - For **Few Shot**: `Few shot.ipynb`
  - For **Multi-Agent Debate**: `Multi-agent debate.ipynb`
  - For **Self Help**: `Self_help.ipynb`
  - For **Reflexion**: `Reflexion.ipynb`
  - For **Our Method (SACD)**: `SACD.ipynb`

## Obtaining Results

- To evaluate the accuracy of responses, run **`judge_correct.ipynb`**.

## File Descriptions

Each domain and bias type (as in the paper) contains several notebooks:

| File Name             | Description                                                      |
|-----------------------|------------------------------------------------------------------|
| Availableing-bias.ipynb | Baseline (biased answers, no debiasing)                        |
| Cot.ipynb               | Chain-of-Thought debiasing                                     |
| Zero-shot.ipynb         | Zero-shot debiasing                                            |
| Few shot.ipynb          | Few-shot debiasing                                             |
| Multi-agent debate.ipynb| Multi-agent debate debiasing                                   |
| Self_help.ipynb         | Self-help method                                               |
| Reflexion.ipynb         | Reflexion method                                               |
| SACD.ipynb              | Our method (Self-Adaptive Cognitive Debiasing)                |

## Citation

If you use this work, please cite:

```bibtex
@misc{lyu2025selfadaptivecognitivedebiasinglarge,
      title={Self-Adaptive Cognitive Debiasing for Large Language Models in Decision-Making}, 
      author={Yougang Lyu and Shijie Ren and Yue Feng and Zihan Wang and Zhumin Chen and Zhaochun Ren and Maarten de Rijke},
      year={2025},
      eprint={2504.04141},
      archivePrefix={arXiv},
      primaryClass={cs.CL},
      url={https://arxiv.org/abs/2504.04141}, 
}
```

---

Feel free to open issues or pull requests for questions or suggestions!
