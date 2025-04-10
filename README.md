# Knowledge-Distillation Implementation
This project demonstrates **Knowledge Distillation** by training a compact **student model** to mimic a large **BERT-base-uncased teacher** for the task of **intent classification** on the [CLINC150 dataset](https://github.com/clinc/oos-dataset). The goal is to reduce model size and inference time while maintaining high accuracy.

---

## Overview

- **Teacher Model**: `bert-base-uncased` fine-tuned on intent classification.
- **Student Model**: Smaller transformer (e.g., `distilbert`) trained using knowledge distillation.
- **Dataset**: CLINC150 – a benchmark dataset with 150 diverse intent classes.
- **Objective**: Match teacher performance using a more efficient model via:
  - Cross-entropy loss (student vs true labels)
  - KL-Divergence loss (student vs teacher predictions)

---
## Results 

- After training the student model and running Inference, I could achieve a *38.8%* decrease in model size, while achieving a *61.9%* increase in inference time, with only *2.68%* loss in accuracy.

*This project was heavily inspired from The paper *"Distilling the Knowledge*  *in a Neural Network" (2015), G.Hinton, et,al*
