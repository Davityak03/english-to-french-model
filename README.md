# english-to-french-seq-to-seq-model

This repository contains a sequence-to-sequence (Seq2Seq) model that translates English sentences to French using the `fra.txt` dataset. The model is implemented using TensorFlow and Keras and is based on an encoder-decoder architecture.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Model Architecture](#model-architecture)
4. [Model Summary](#model-summary)
5. [Dependencies](#dependencies)
6. [Results](#results)

## Project Overview

The goal of this project is to build a  model that translates English sentences to French. The model leverages a sequence-to-sequence architecture focus on specific parts of the input sentence when generating the translation.

## Dataset

The dataset used is `fra.txt`, which consists of English-to-French sentence pairs. Each line in the file contains an English sentence followed by its corresponding French translation.

Example format:
```
Go.    Va !
Hello. Bonjour !
```

## Model Architecture

The model follows a standard encoder-decoder architecture:

- **Encoder**: The encoder is a bidirectional LSTM that reads the input English sentence and converts it into a context vector.
- **Decoder**: The decoder is another LSTM that takes the context vector from the encoder and generates the corresponding French sentence.

### Model Summary

- **Input**: English sentence.
- **Output**: French translation.
- **Loss Function**: Sparse categorical cross-entropy.
- **Optimizer**: Rmsprop

### Dependencies:
- TensorFlow 2.x
- NumPy
- Pandas

## Results

After training for 100 epochs:-

Sample translations:
- **Input**: "I am happy."
- **Output**: "Je suis heureux."

- **Input**: "What is your name?"
- **Output**: "Quel est votre nom ?"
