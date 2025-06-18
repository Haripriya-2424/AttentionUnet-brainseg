#  Brain Tumor Segmentation using Attention U-Net

This project focuses on segmenting brain tumors from MRI scans using the Attention U-Net model. The work is entirely developed and trained on **Google Colab** using PyTorch. Attention U-Net enhances the original U-Net by integrating attention gates, helping the model focus on tumor regions and improving segmentation accuracy.

---

##  Introduction

Brain tumors require accurate detection and segmentation to assist in diagnosis and treatment planning. Manual segmentation is time-consuming and error-prone. This project leverages deep learning to automate the process using Attention U-Net, which improves feature focus through attention mechanisms.

---

## Dataset Structure
The project uses the LGG MRI Segmentation dataset from Kaggle, which contains 110 FLAIR MRI scans of patients with lower-grade gliomas (LGG). Each image includes a corresponding manually annotated tumor mask. The dataset is ideal for training and evaluating brain tumor segmentation models like Attention U-Net.


The dataset is stored in Google Drive and organized as:

```

BraintumorSegmentation
├── Dataset
│   ├── images      # Input MRI scans (.tif)
│   └── masks      # Corresponding binary masks (.tif)

````

Ensure each image has a corresponding mask with the same base name followed by `_mask`.

---

##  Model

The Attention U-Net model is used for segmentation. It improves the basic U-Net by using attention blocks in skip connections, allowing the model to highlight tumor areas more effectively.

---

## Project Workflow

The code is divided into six snippets in Google Colab:

1. **Mount Google Drive** – for loading dataset and saving model.
2. **Import Libraries** – load required packages like `torch`, `numpy`, etc.
3. **Model** – define the Attention U-Net architecture.
4. **Load Data** – create a custom dataset class to read images and masks.
5. **Train Model** – train the model and save the `.pth` file.
6. **Visualize & Evaluate** – show segmentation output and print evaluation metrics like Dice, IoU, Accuracy, and BCE Loss.

---

## Metrics

The model is evaluated using:

- Dice Coefficient  
- Intersection over Union (IoU)  
- Binary Accuracy  
- Binary Cross-Entropy Loss

---

##  Visualization

The output includes:

- Original MRI image  
- Ground truth mask  
- Predicted segmentation mask

This helps verify how well the model detects tumor regions.

---

## Requirements

Install the required packages:

```bash
pip install torch torchvision matplotlib numpy pillow tqdm
````

Or use directly in Google Colab where most are pre-installed.

---

## Conclusion

This project demonstrates how deep learning can assist in medical imaging. The Attention U-Net model delivers reliable brain tumor segmentation, helping radiologists make better decisions faster.


