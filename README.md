# Comparative-Analysis-of-Probabilistic-Methods-for-Brain-Tumor-Segmentation-Images
This repository contains the implementation and research findings of a comparative study analyzing three probabilistic methods for brain tumor segmentation in MRI images.

## Overview

The study compares three main approaches:
- Gaussian Mixture Models (GMM)
- Hidden Markov Models (HMM)
- Hybrid Hidden Monte Carlo (HMC) with Chan-Vese model

## Performance Results

| Method | Dice Similarity Coefficient (DSC) |
|--------|----------------------------------|
| GMM    | 0.7550                          |
| HMM    | 0.6389                          |
| HMC    | >0.8                            |

## Key Features

### GMM Implementation
- Uses Expectation-Maximization (EM) algorithm
- Optimal cluster determination using Silhouette Score
- Effective pixel intensity clustering
- Computationally efficient

### HMM Implementation
- Adaptive state creation
- Row-by-row initialization
- Spatial relationship modeling
- Viterbi algorithm for decoding

### HMC-Chan-Vese Hybrid
- Combines Markov Random Fields with variational energy minimization
- Superpixel segmentation using SLIC
- Enhanced spatial coherence
- Better handling of intensity inhomogeneities

## Methodology

1. **Preprocessing**
   - Contrast Limited Adaptive Histogram Equalization (CLAHE)
   - Noise reduction
   - Image normalization

2. **Segmentation**
   - GMM: EM algorithm with optimal cluster determination
   - HMM: Adaptive state creation with Viterbi decoding
   - HMC: Probabilistic parameter estimation with contour refinement

3. **Evaluation**
   - Dice Similarity Coefficient (DSC)
   - Comparison with ground truth bounding boxes
   - Performance analysis across methods

## Key Findings

1. **GMM**
   - Achieved DSC of 0.7550
   - Effective at clustering pixel intensities
   - Lacks spatial structure modeling

2. **HMM**
   - Achieved DSC of 0.6389
   - Better spatial modeling
   - Challenges with cluster proliferation in complex images

3. **HMC-Chan-Vese**
   - Achieved DSC above 0.8
   - Most robust segmentation
   - Higher computational cost
   - Better handling of intensity inhomogeneities

## Future Work

- Enhance scalability of spatial models like HMM
- Integrate boundary refinement techniques
- Improve segmentation performance on diverse medical imaging datasets
- Optimize computational efficiency of the hybrid model

## References

Key references from the paper are available in the main document, including works by:
- Bal et al. (2018)
- Gordillo et al. (2013)
- Huang et al. (2021)
- Kamnitsas et al. (2017)
- Shelhamer et al. (2017)

## Dataset

The study uses brain images from Hugging Face's Brain Tumor Object Detection repository, which provides annotated brain images with tumor regions.
