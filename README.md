# PIQA
This repository contains the training parameters and code for finetuning BERT and RoBERTa models on the PIQA (Physical Interaction: Question Answering) dataset.

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



