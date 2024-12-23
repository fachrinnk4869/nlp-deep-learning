

# NLP Model Comparison

link for presentation: [Project presentation](https://docs.google.com/presentation/d/1IIEFGb0Evj3qw8i2bQjIIVzO3g0653PC0b7Ex_bs6ug/edit?usp=sharing)

This project explores the differences between RNN, LSTM, Transformer, T5, Phi3.5 in sequence-to-sequence task. The model is designed for a machine translation task, where the source language is encoded and translated into the target language. 

The primary goal is to compare the performance of all models above in terms of translation quality, loss, and BLEU score.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Implementation](#implementation)
3. [Training](#training)
4. [Results](#results)
5. [Examples](#examples)

---

## Project Overview

This project compares the use of SimpleRNN and LSTM layers in an encoder-decoder sequence-to-sequence model. The focus is to see how well each architecture translates input text in the source language to the target language and to evaluate each model's effectiveness.

### Objective
To evaluate:
- **Translation quality** based on BLEU scores
- **Loss** during training
- How the model generalizes to **new inputs**

---

## Implementation

### Prerequisites
- **Python** 3.11
- **TensorFlow** 2.15
- Other libraries: `matplotlib` for plotting, `nltk` for BLEU score calculation

### Code Structure

- `train_mt{name-of-model}.ipynb`: Script to train the model.
- `{name-of-model}/evaluation_{name-of-model}_test.csv`: evaluation result of name_model
- `{name-of-model}/evaluation_{name-of-model}_test.csv`: prediction test result of name_model
---

## Training

### Hyperparameters
- **Vocabulary size**: _Specify vocabulary size_
- **Embedding dimension**: _Specify embedding dimension_
- **Units**: _Specify units_
- **Batch size**: _Specify batch size_
- **Epochs**: _Specify number of epochs_

### Training Procedure
1. Record the **loss** over epochs.

**Plots of Loss and Accuracy over Epochs**  
_RNN, LSTM, Transformer, T5 Model Loss Plot_  
![image](https://github.com/user-attachments/assets/42b7531e-dcde-4d2f-90df-66f151401d03)

_Phi 3.5 Finetune Model Loss Plot_  
![image](https://github.com/user-attachments/assets/2aa87340-67ba-41ff-b7b8-1fab9fdb7a36)

---

## Results

| Model      | Training Loss | Validation Loss | BLEU Score |
|------------|---------------|-----------------|------------|
| RNN        | 0.0030 | 2.5675  | 0.0082 |
| LSTM       | 0.0004        | 2.4243          | 0.0100 |
| Transformer| 0.0001        | 0.9      | 0.54869 |
| T5         | 0.0004 | 2.4243   | 0.2098 |
| Phi3_5 finetuned_one_shot | 1.092100  | 1.079701   | 0.2780 |
| Phi3_5 finetuned_few_shot | 1.092100  | 1.079701   | 0.2837 |
| Phi3_5 raw_one_shot       |         |           | 0.3978 |
| Phi3_5 raw_few_shot       |         |           | 0.3820 |

---
### Charts
**Average Time Taken Each Epoch Each Model**
![image](https://github.com/user-attachments/assets/3a1c26ec-c3c2-4213-9c6a-d13334664694)

**Bleu Score Each Model**
![image](https://github.com/user-attachments/assets/8d39fa40-037e-40ed-8c91-72204d74a8f6)

## Examples

### Sample Translations

**Example 1**  
![image](https://github.com/user-attachments/assets/4bcaade3-d08f-4bd8-89d3-1c7cc2f314d4)

**Example 2**  
![image](https://github.com/user-attachments/assets/0893da68-8fd6-4293-bb61-aa64150b41c1)

**Example 3**  
![image](https://github.com/user-attachments/assets/2dfee1ff-04c1-4a84-ba99-15239fbcb423)

---
