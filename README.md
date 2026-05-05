# AR-XMER: Adversarially Robust and Explainable Multimodal Emotion Recognition

This repository contains the implementation used for the paper:

**AR-XMER: Adversarially Robust and Explainable Multimodal Emotion Recognition**

AR-XMER is a multimodal emotion-recognition framework designed to study the interaction between clean prediction performance, adversarial sensitivity, and explanation stability. The current implementation evaluates the model on the IEMOCAP dataset using text, audio, and video modalities, adversarial audio-PGD perturbations, Integrated Gradients explanations, and the Explanation Robustness Index (ERI).

## Overview

The notebook implements a multimodal pipeline with the following components:

- Text processing from IEMOCAP transcripts
- Audio feature extraction from IEMOCAP `.wav` files
- Video feature extraction from IEMOCAP video files
- Multimodal dataset construction and alignment
- BERT-based text representation
- Lightweight audio and video MLP encoders
- Multimodal fusion and classification
- Clean evaluation on a held-out split
- Adversarial evaluation using audio-PGD
- Integrated Gradients attribution for audio and video features
- Explanation Robustness Index (ERI) computation between clean and perturbed samples

The goal of the code is not only to report classification accuracy, but also to analyse how the model behaves under perturbation and whether its explanations remain stable.

## Repository Structure

```text
AR-XMER.ipynb        Main notebook containing preprocessing, model definition, training, evaluation, adversarial testing, and ERI computation
README.md           Repository description and usage instructions
