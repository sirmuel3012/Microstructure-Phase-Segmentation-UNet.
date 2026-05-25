# Microstructure Phase Segmentation using U-Net

## Project Description

This project uses a U-Net deep learning model to analyze microstructure images and identify material phases such as ferrite, pearlite, and martensite through image segmentation.

The project combines image preprocessing, semantic segmentation, model training, performance evaluation, and a graphical user interface (GUI) for user interaction.

---

## Features

- Image segmentation using U-Net
- Microstructure phase detection
- Pixel-wise classification
- Predicted phase mask generation
- Overlay visualization
- Phase percentage estimation
- Interactive GUI using Gradio
- Upload and analyze custom microstructure images

---

## Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Google Colab
- CVAT
- Gradio
- GitHub

---

## Project Workflow

Collect microstructure images

↓

Label images using CVAT

↓

Generate segmentation masks

↓

Preprocess and normalize images

↓

Build U-Net architecture

↓

Train model

↓

Apply Dice Loss and Class Weighting

↓

Evaluate model performance

↓

Save trained model

↓

Create GUI interface

---

## Model Training Approach

The dataset consisted of microstructure images and corresponding segmentation masks.

Images were:

- Resized to 256 × 256 pixels
- Normalized between 0–1
- Split into training and testing datasets

Initially, the model predicted mostly background due to class imbalance.

To improve learning:

- Dice Loss was introduced
- Class weights were applied

This helped punish the model for predicting only dominant background pixels and encouraged learning of smaller regions such as ferrite, pearlite, and martensite.

---

## Evaluation Method

Model performance was evaluated using:

- Mean Intersection over Union (Mean IoU)

Result:

```text
Mean IoU ≈ 0.246
```

Due to the small dataset size, performance was limited but demonstrated successful segmentation behavior.

---

## GUI Implementation

A Gradio GUI interface was created that allows users to:

- Upload microstructure images
- Generate predicted masks
- Create overlay images
- Display predicted phase percentages

---

## Trained Model File

The trained U-Net model file:

```text
microstructure_unet_model.h5
```

was not uploaded directly to GitHub because its size (~250 MB) exceeds GitHub file upload limitations.

The model was trained and tested successfully in Google Colab and used for predictions and GUI demonstrations.

Model access link:

(https://drive.google.com/drive/folders/1cMxNKCeWHovmWWVnyvHL0NhYjyzRS-xW?usp=sharing)

---

## Limitations

- Small dataset (~31 images)
- Limited training samples
- Class imbalance
- Reduced generalization on unseen images

---

## Future Improvements

- Increase dataset size
- Improve image labeling accuracy
- Train on more material phases
- Improve model performance
- Add live camera/image acquisition support
- Deploy as a standalone application

---

## Author

Ayodele Babatunde (Arcada University of Applied Sciences)

Mechanical Engineering — Machine Learning / Image Segmentation Project
