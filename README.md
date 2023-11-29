# ovarian-cancer-subtype-classification

## Description
Solution for Kaggle competition UBC Ovarian Cancer Subtype Classification and Outlier Detection.
The goal of this competition is to classify the type of ovarian cancer from microscopy scans of biopsy samples. There are two categories of images: whole slide images (WSI) and tissue microarray (TMA). Whole slide images are at 20x magnification and can be quite large. The TMAs are smaller (roughly 4,000x4,000 pixels) but at 40x magnification.

## Pipeline
![UBC Ovarian Cancer](https://github.com/luciaurcelay/ovarian-cancer-subtype-classification/assets/93920109/af0768c7-3546-449a-a88e-80b54d3d15e2)


## Files
* [Exploratory Data Analysis](eda-wsi-tma.ipynb)
* [Dataset generator](ubc-tiles-preprocessing.ipynb)
* [Trainer](ubc-train-224px.ipynb)

## Results
Current model achieves 60% validation acuracy in 5 class classification.

## Future work
- The main limitation of the current approach is that the model is trained considering each patch as independent samples. This is undesirable because some of the patches may not contain cancerous cells and nonetheless trained to be classified as such.
- A proposed improvement is to train a binary classifier (cancerous / non-cancerous patch) previous to the 5 class classifier that has been already implemented. This approach will ensure that only cancerous patches are classified as one of the 5 cancer subtypes.

## Author

* Lucia Urcelay
