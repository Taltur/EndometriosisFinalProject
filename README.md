# Endometriosis MRI Classification using DenseNet121

Deep learning final project developed as part of a Software Engineering degree.

This project focuses on automated classification of pelvic MRI scans for endometriosis detection using transfer learning with DenseNet121 and combined T1/T2 MRI modalities.

## Project Overview

Endometriosis diagnosis often requires time-consuming clinical evaluation and imaging interpretation.  
The goal of this project was to explore whether a deep learning model could assist in classifying MRI scans for endometriosis detection.

The final solution uses a pretrained DenseNet121 model with fine-tuning on selected layers and image augmentation techniques to improve generalization.

## Technologies Used

- Python
- PyTorch
- DenseNet121 (ImageNet pretrained)
- NumPy
- Matplotlib
- Google Colab

## Model Configuration

- Architecture: DenseNet121
- Transfer Learning: ImageNet pretrained weights
- Fine-tuned layers: `denseblock4` + `norm5`
- Input modalities: Combined T1 + T2 MRI images
- Batch size: 64
- Epochs: 75
- Dropout: 0.5
- Label smoothing: 0.1
- Optimizer: Adam (`lr=1e-5`, `weight_decay=1e-4`)
- Learning rate scheduler: ReduceLROnPlateau
- Early stopping enabled

## Final Results

Performance on the test set:

- Accuracy: **93.46%**
- Precision: **94.13%**
- Recall: **92.03%**
- F1 Score: **93.07%**

## Repository Contents

- `DenseNet121_Endometriosis_Classification.ipynb` — final training and evaluation notebook
- `Endometriosis_DeepLearning_Project_Report.docx` — project documentation
- `Endometriosis_Project_Presentation.pptx` — final presentation

## Dataset Note

The MRI dataset used in this project is private and therefore not included in this repository.

Only the implementation, documentation, and project artifacts are shared.
