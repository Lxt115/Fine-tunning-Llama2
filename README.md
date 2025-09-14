# Fine-tuning Llama2 for Text Summarization

This repository contains the implementation and evaluation of a fine-tuned Llama2 model for text summarization tasks.

## 📁 Project Structure

```
├── fine-tune.ipynb          # Fine-tune Llama2 using LoRA on various datasets
├── test.ipynb               # Generate responses from both original and fine-tuned models
├── compute.ipynb            # Compute evaluation metrics (Rouge, BertScore, GPT-4o score)
└── README.md
```

## 📊 Key Findings

### 1. Model Comparison (Original vs. Fine-Tuned)
- Fine-tuned Llama2 models achieve **higher Rouge scores** and **higher BertScores** compared to the original (untuned) Llama2.


### 2. Dataset Comparison (In-Domain vs. Out-of-Domain)
- All models demonstrate **significantly better performance** on in-domain (ID) datasets than on out-of-domain (OOD) datasets.


### 3. Out-of-Domain (OOD) Dataset Comparison
- Among OOD datasets, the fine-tuned `peft model1` yields better scores. This is likely because the format of OOD Dataset 1 is more aligned with the in-domain dataset used for fine-tuning.

<img width="705" height="485" alt="image" src="https://github.com/user-attachments/assets/9a53164a-e27a-4039-a45f-e1f3d3e4d49c" />

### 4. Metric Correlation
- GPT-4o Score shows a **positive correlation** with both Rouge and BertScore.
- GPT-4o Score effectively distinguishes between original and fine-tuned models, confirming it as a **reliable evaluation metric**.

<img width="645" height="481" alt="image" src="https://github.com/user-attachments/assets/1a56cc97-1b55-4d05-9338-9296e9d466a6" />
<img width="641" height="338" alt="image" src="https://github.com/user-attachments/assets/1a620f35-b19b-4031-aef6-f093a51199ba" />

