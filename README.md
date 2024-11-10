

# RNN vs LSTM in Encoder-Decoder Model

link for presentation: [Project presentation](https://docs.google.com/presentation/d/1IIEFGb0Evj3qw8i2bQjIIVzO3g0653PC0b7Ex_bs6ug/edit?usp=sharing)

This project explores the differences between using a SimpleRNN and an LSTM in an encoder-decoder sequence-to-sequence model. The model is designed for a machine translation task, where the source language is encoded and translated into the target language. 

The primary goal is to compare the performance of SimpleRNN and LSTM layers in terms of translation quality, loss, and BLEU score.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Model Architecture](#model-architecture)
3. [Implementation](#implementation)
4. [Training](#training)
5. [Results](#results)
6. [Examples](#examples)
7. [BLEU Score](#bleu-score)
8. [Conclusion](#conclusion)

---

## Project Overview

This project compares the use of SimpleRNN and LSTM layers in an encoder-decoder sequence-to-sequence model. The focus is to see how well each architecture translates input text in the source language to the target language and to evaluate each model's effectiveness.

### Objective
To evaluate:
- **Translation quality** based on BLEU scores
- **Loss** and **accuracy** during training
- How the model generalizes to **new inputs**

---

## Model Architecture

The encoder-decoder architecture consists of two primary components:
1. **Encoder**: Converts the input sentence from the source language into a fixed-length context vector.
2. **Decoder**: Uses the context vector from the encoder to generate the target language translation.

### RNN and LSTM Variants
- **RNN-based Encoder and Decoder**: Uses SimpleRNN layers for encoding and decoding.
- **LSTM-based Encoder and Decoder**: Uses LSTM layers for encoding and decoding, leveraging hidden and cell states for better long-term memory.

---

## Implementation

### Prerequisites
- **Python** 3.11
- **TensorFlow** 2.15
- Other libraries: `matplotlib` for plotting, `nltk` for BLEU score calculation

### Code Structure

- `train.ipynb`: Script to train the model.


---

## Training

### Hyperparameters
- **Vocabulary size**: _Specify vocabulary size_
- **Embedding dimension**: _Specify embedding dimension_
- **Units**: _Specify units_
- **Batch size**: _Specify batch size_
- **Epochs**: _Specify number of epochs_

### Training Procedure
1. Train the encoder-decoder model using SimpleRNN layers.
2. Train the encoder-decoder model using LSTM layers.
3. Record the **loss** and **accuracy** over epochs.

**Plots of Loss and Accuracy over Epochs**  
_RNN Model Loss/Accuracy Plot_  
![RNN Loss Plot](path/to/rnn_loss_plot.png)

_LSTM Model Loss/Accuracy Plot_  
![LSTM Loss Plot](path/to/lstm_loss_plot.png)

---

## Results

| Model      | Training Loss | Validation Loss | BLEU Score |
|------------|---------------|-----------------|------------|
| RNN        | 0.0030 2.5675| 2.5675  | 0.0082 |
| LSTM       | 0.0004        | 2.4243          | 0.0100 |

---

## Examples

### Sample Translations

**Example 1**  
**Input** (Source Language): _"in the western half the volume increased from million per year in 1998 to in and in 2011
"_  
**RNN Output**: _"Kita harus membiarkan tom pergi eos"_  
**LSTM Output**: _"Ketika masuk rumah di jepang sepatu dibuka eos "_

**Example 2**  
**Input** (Source Language): _"she obtained a scholarship from the department to study politics in the us"_  
**RNN Output**: _"Kita harus membiarkan tom pergi eos"_  
**LSTM Output**: _"Dia menginap di hotel beberapa hari eos"_

---

## BLEU Score

The BLEU (Bilingual Evaluation Understudy) score is a metric for evaluating the quality of text that has been machine-translated from one language to another. Here, we use it to measure the quality of translations produced by the RNN and LSTM models.

**BLEU Score Results**  
_RNN BLEU Score_: 0.0082 
_LSTM BLEU Score_: 0.0100

---

## Conclusion

Based on the experiments conducted, we observed the following:

- **Translation Quality**: _Describe findings, e.g., "The LSTM model consistently performed better than the RNN model on test data, achieving higher BLEU scores."_
- **Training Stability**: _Describe findings, e.g., "The RNN model showed signs of instability in loss convergence, while the LSTM maintained smoother loss reduction."_
- **Generalization to New Inputs**: _Discuss how well each model handled new examples._