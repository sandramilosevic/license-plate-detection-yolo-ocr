# license-plate-detection-yolo-ocr
# License Plate Detection and Recognition System

End-to-end computer vision project for license plate detection and recognition using YOLOv8 and OCR.

## Overview

This project detects vehicle license plates in images and extracts the text from the detected plate region. The system was built in Google Colab and uses a YOLOv8 model for plate localization followed by OCR for text recognition.

## What the project does

- Downloads the dataset through an API.
- Prepares the data for training.
- Trains a YOLOv8 model for license plate detection.
- Evaluates the model on validation and test data.
- Crops detected license plates and applies OCR to extract text.
- Visualizes detection results on sample images.

## Technologies Used

- Python
- Google Colab
- YOLOv8
- OpenCV
- OCR
- NumPy
- Matplotlib
- Kaggle API
- scikit-learn

## Dataset

The dataset was accessed programmatically through an API in Google Colab.  
It was then used to train and evaluate the YOLOv8 detection model.

## Model Training

A YOLOv8s model was fine-tuned for one-class object detection.  
Training was performed with early stopping, and the best checkpoint was saved as `best.pt`.

## Results

The best model achieved the following test performance:

- Precision: 87.0%
- Recall: 81.6%
- mAP50: 86.8%
- mAP50-95: 46.6%

## How It Works

1. Load the dataset through the API.
2. Split the data for training, validation, and testing.
3. Create the YOLO configuration file.
4. Train the YOLOv8 model.
5. Validate the best checkpoint.
6. Run inference on test images.
7. Apply OCR to the detected plate region.

## Installation

```bash
pip install ultralytics
pip install fast-plate-ocr
pip install opencv-python
pip install matplotlib
pip install kaggle
pip install scikit-learn
```

## Usage

### Clone the repository

```bash
git clone https://github.com/sandramilosevic/license-plate-detection-yolo-ocr.git
cd license-plate-detection-yolo-ocr
```

### Run the notebook

Open `plate-recognition.ipynb` in Google Colab and run the cells step by step.

## Project Structure

```text
├── plate-recognition.ipynb
├── README.md
└── requirements.txt
```

## Example Output

The model detects license plates in an image, draws bounding boxes around them, and extracts the plate text using OCR.

## Future Improvements

- Improve OCR accuracy on low-quality images.
- Add real-time video support.
- Test different detection models.
- Improve robustness on angled or partially occluded plates.
