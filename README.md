# PIQA
This repository contains the training parameters and code for finetuning BERT and RoBERTa models on the PIQA (Physical Interaction: Question Answering) dataset.

## Download Model Weights

You can download the model weights from the following link:

[Download Model Weights](https://drive.google.com/drive/folders/1ifEm5ejkWjFLvyzZNHVTgQsWwQ46tw37?usp=drive_link)


## Training and Optimization Parameters

| Parameter                | BERT-base | RoBERTa-base |
|--------------------------|-----------|--------------|
| **Learning Rate**         | 3e-5      | 1e-5         |
| **Train Batch Size**      | 8         | 4            |
| **Eval Batch Size**       | 8         | 4            |
| **Betas (Optimizer)**     | (0.9, 0.999) | (0.9, 0.98)   |
| **Epsilon (Optimizer)**   | 1e-8      | 1e-6         |
| **Weight Decay**          | -         | 0.1          |
| **Max Grad Norm**         | -         | 1.0          |
| **Warmup Steps**          | -         | 604          |
| **Scheduler Type**        | -         | Polynomial   |
| **Num Train Epochs**      | 3         | 3            |
| **Gradient Accumulation Steps** | -   | 8            |
| **Seed**                  | -         | 42           |
| **Pretrained**            | True      | True         |

> Figure: Training and optimization parameters for BERT-base and RoBERTa-base models.


## Zero-shot Chain-of-Thought Prompting
For this work **zero-shot chain-of-thought prompting technique (CoT)** was used on both GPT-4.0 and Mistral Large-2. The phrase *"Let's think step by step"* was employed to initiate the CoT process.
## Accuracy Comparison

| Category                         | Model         | Size  | Accuracy (%) Validation |
|-----------------------------------|---------------|-------|-------------------------|
| **Fine-Tuned Models**             | BERT-base     | 110M  | 65.9                    |
|                                   | RoBERTa-base  | 125M  | 70.5                    |
| **State-of-the-Art Generative Models** | GPT-4.0       | N/A   | 94.8                    |
|                                   | GPT-4.0 (CoT)¹ | N/A   | 94.6                    |
|                                   | Mistral Large-2 | 123B  | 89.0                    |
|                                   | Mistral Large-2 (CoT)² | 123B | 74.8                 |
| **Human**                         | –             | –     | 94.9 [↓2]               |

> **Table**: Accuracy Comparison for BERT-base, RoBERTa-base, and State-of-the-Art Models.
> 
> [↓2] Yonatan Bisk, Rowan Zellers, Ronan Le Bras, Jianfeng Gao, and Yejin Choi. *PIQA: Reasoning about physical commonsense in natural language*, 2019.
Explanation:
