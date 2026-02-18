# Image Processing – Motion Classification Project

## Overview
This project implements a video-based motion classification system that distinguishes between **walking** and **waving** actions using spatio-temporal blocks and 3D-DCT features, following the methodology presented in the course paper.

## Pipeline
1. Video preprocessing (grayscale, resize to 64×64)
2. Motion-based spatio-temporal block sampling
3. 3D-DCT feature extraction
4. Mutual Information based feature selection
5. Bernoulli Naive Bayes classification
6. Block-level and video-level decision making
7. Confidence-based filtering and visualization

## Dataset Structure
data_raw/
├── train/
│ ├── walk/
│ └── wave/
└── test/
├── walk/
└── wave/


## Baseline Results
- Block-level accuracy: **~0.89**
- Confusion matrix and detailed metrics are provided in `results/baseline_metrics.txt`.

## Improvements
- Confidence thresholding (τ) to trade off accuracy vs coverage
- Video-level aggregation of block predictions
- Dynamic motion visualization with color overlays

## Visual Outputs
All generated plots and visualizations are available under the `results/` directory:
- Confusion matrix
- Accuracy vs confidence threshold
- Motion overlay visualizations

## Reproducibility
All experiments were run with a fixed random seed.
The full pipeline is executable from the provided notebook.

## References
- Keren, D. (2003). Recognizing image "style" and activities in video 
using local features and naive Bayes. Pattern Recognition Letters, 24(16), 2913–2922.
