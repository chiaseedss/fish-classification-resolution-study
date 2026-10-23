# Fish Classification and Image Resolution Study

## Overview

A nine-class image-classification experiment comparing three input resolutions with a dense neural network, rather than a convolutional neural network. Source: [LA2_Olivares.ipynb](LA2_Olivares.ipynb).

## Technologies Used

Python, Jupyter, TensorFlow/Keras, KaggleHub, NumPy, pandas, Pillow, scikit-learn, Matplotlib and Seaborn.

## Methodology

Ground-truth mask folders are excluded. Images are resized to 32×32, 64×64 or 128×128 and passed to a Flatten → Dense(256) → Dense(128) → softmax classifier. Saved counts are 7,200 training, 904 validation and 896 test images. Resolution-comparison experiments use 15 training epochs.

## Results

Historical notebook measurements, not independently rerun results:

| Image size | Comparison-loop test accuracy | Training time |
|---|---:|---:|
| 32×32 | 0.9364 | 78.2 s |
| 64×64 | 0.9163 | 108.3 s |
| 128×128 | 0.9152 | 249.5 s |

A separate evaluation reports 0.9375 accuracy for the selected 32×32 model. This is distinct from its comparison-loop score. The shuffled take/skip validation–test subdivision requires verification for stable, disjoint membership; near-duplicate images and evaluation consistency also require review. Timings are specific to the original execution environment.

## Dataset

The notebook requests [A Large Scale Fish Dataset on Kaggle](https://www.kaggle.com/datasets/crowww/a-large-scale-fish-dataset). No original fish-image files were found in the inspected project folders or coursework ZIPs. No dataset download or substitute sample was added; source terms and image attribution still require review.

## Contributors

**Author:** Tischia Ann R. Olivares\
**Project Type:** Individual Academic Project
