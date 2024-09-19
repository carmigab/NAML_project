# NAML_Project: Music Genre Classification using Auditory, Spectral, and Acoustic Features

## Project Overview

This repository contains the practical project for the **Numerical Analysis for Machine Learning (NAML)** university course. The project focuses on **music genre classification** using various feature sets, including auditory images, spectral, and acoustic features. The project aims to replicate and extend the work presented in a research paper that explored the efficacy of auditory image-based features in music genre recognition.

## Project Scope

The objective of this project was to replicate the original paper's experiments and explore additional approaches. The primary tasks included:
- **Dataset preprocessing**: Standardization and feature extraction from multiple datasets.
- **Feature extraction**: Use of auditory, spectrum, and acoustic features for classification.
- **Classifier training and evaluation**: Implementing and evaluating traditional classifiers (SVM, KNN) and a neural network model for direct image-based classification.

The goal was to compare the effectiveness of different features (auditory vs. spectrum) and classifiers, ultimately proposing improvements to music genre recognition models.

## Datasets

The project used three main datasets for music genre classification:
1. **GTZAN**: 10 genres, 30s audio clips, WAV format.
2. **Homburg**: 9 genres, 10s audio clips, MP3 format.
3. **ISMIR2004**: 6 genres, full-length songs, MP3 format.

Each dataset underwent preprocessing to convert audio formats, standardize sampling rates, and extract key features for training.

## Features

Three feature types were extracted:
1. **Acoustic Features**: Mel-frequency cepstral coefficients (MFCCs) and psycho-acoustic descriptors like Statistical Spectrum Descriptor (SSD) and Rhythm Histogram (RH).
2. **Spectrum Features**: Images of audio spectra, combined with texture descriptors (Local Binary Pattern, Fourier transform, etc.).
3. **Auditory Image Features**: Generated using the AIM2006 model, simulating human auditory processing.

## Classifiers and Experiments

Experiments were conducted using:
- **SVM**: The primary classifier used in the original paper.
- **KNN**: Evaluated as an alternative, often outperforming SVM in this work.
- **Neural Networks**: A custom feedforward neural network trained directly on auditory and spectrum images, offering slight performance improvements over traditional classifiers.

## Key Findings

- **KNN** generally outperformed SVM in music genre classification across all datasets.
- **Auditory image features** did not consistently improve classification performance, particularly when using KNN.
- **Neural networks** trained on raw spectrum images achieved slightly better accuracy compared to texture descriptor-based models but at the cost of increased training time.

## Conclusion

While auditory images show promise, their utility depends on the specific classifier and dataset. Spectrum and acoustic features remain highly effective, especially when paired with KNN or neural networks. Future work could focus on further optimizing the use of neural networks for large datasets.

## References

1. Foleis, J.H., Tavares, T.F.: Texture selection for automatic music genre classification. Applied Soft Computing, 2020.
2. [Rp_extract Library](https://github.com/tuwien-musicir/rp_extract)
3. [RICLBP Library](https://github.com/mnishant2/RICLBP)
4. [AIM2006 Library](https://www.acousticscale.org/wiki/index.php/AIM2006_Documentation)

---

This README provides a concise overview of the project and its outcomes. For a detailed description of the methods and experiments, refer to the project report provided.
