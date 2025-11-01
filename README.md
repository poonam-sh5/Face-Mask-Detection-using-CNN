
# Mask Detection 
## Overview
This project implements a **Face Mask Detection System** using deep learning, trained on a large dataset of facial images both with masks and without masks. The goal is to automatically classify if a person in an image is wearing a mask.

## Dataset
- Dataset sourced from Kaggle: `omkargurav/face-mask-dataset`
- Download and extract instructions are included in the notebook
- **Number of Images**:
  - With mask: 3725
  - Without mask: 3828
  - **Total**: 7553

## Labels
- 1: With mask
- 0: Without mask

## Dependencies

You need the following Python libraries:
- numpy
- matplotlib
- PIL
- opencv-python
- scikit-learn  
Most dependencies are auto-installed in Google Colab.

Additional packages (as per notebook):

pip install kaggle bleach certifi charset-normalizer idna protobuf python-dateutil python-slugify requests setuptools six text-unidecode tqdm urllib3 webencodings

The notebook uses Google Colab for GPU acceleration.

## Data Preparation

- The images are resized to **128x128 RGB**
- Converted to numpy arrays, normalized between 0-1
- Labels generated and combined for training

## Model Training

- **Train-Test Split**: 80% training, 20% testing
- Scaling done by dividing pixel values by 255
- Neural network model built and trained (code not shown in summary above, but Capable of typical CNN architecture; layers can be inferred)
- Training and testing data shapes:  
  - Training: (6042, 128, 128, 3)
  - Testing: (1511, 128, 128, 3)

## Example Usage

To predict if a person is wearing a mask:
- Load the image (`cv2.imread`)
- Resize and scale to 128x128, RGB
- Use the trained model to predict (`model.predict`)
- Output will be 1 (mask) or 0 (no mask)

## Results

- Model predicts if the person in the image is **wearing a mask** or **not**.
- Output is displayed in the notebook (plots and textual result).


## Quick Start

1. Clone/download the notebook
2. Upload your Kaggle API key `kaggle.json`
3. Run all cells in Google Colab

---

**Note:** This notebook provides full workflow from data ingestion to prediction. Customize or extend the neural network for improved accuracy or more classes as desired.

