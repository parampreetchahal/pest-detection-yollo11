# pest-detection-yollo11


## Overview
The Pest Detection Model is an AI-based solution that identifies various pests using deep learning techniques. It leverages the YOLOv11 pre-trained model for real-time pest detection, classifying pests accurately from image inputs. The model is trained and evaluated using a dataset of insect images annotated in Excel files.

## Features
- **Real-time Pest Detection:** Identifies pests from images and live camera feeds.
- **High Accuracy:** Utilizes a pre-trained YOLOv11 model for robust classification.
- **Dataset Handling:** Supports JPG images with annotations in Excel format.
- **Evaluation Metrics:** Computes accuracy, confusion matrix, recall, and precision.
- **Performance Visualization:** Generates a graph of learning rate vs. accuracy.

## Dataset
- **Format:** JPG images with corresponding Excel annotation files.
- **Structure:**
  - `train/` - Training images
  - `validation/` - Validation images
  - `test/` - Testing images
  - `annotations.xlsx` - Annotation file with class labels and bounding boxes

## Model Training & Evaluation
1. **Preprocessing:**
   - Convert Excel annotations to YOLO format.
   - Normalize and resize images.
2. **Training:**
   - Train using YOLOv11 on annotated datasets.
   - Monitor learning rate and accuracy.
3. **Evaluation:**
   - Compute confusion matrix, precision, recall, and accuracy.
   - Validate using test dataset.

## Installation
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/pest-detection-model.git
   cd pest-detection-model
   ```
2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Download Pre-trained Weights:**
   - Place YOLOv11 weights in the `weights/` directory.

## Usage
- **Train the Model:**
  ```bash
  python train.py --epochs 50 --batch-size 16
  ```
- **Test the Model:**
  ```bash
  python test.py --weights weights/yolov11.pth --source test/
  ```
- **Real-time Detection:**
  ```bash
  python detect.py --source webcam
  ```

## Output
- **Detected Images:** Results are saved in the `output/` directory.
- **Performance Metrics:** CSV file with accuracy, precision, recall, and loss.
- **Graphs:** Learning rate vs. accuracy visualization.


## Contributors
- **Your Name** - Developer
- **Contributors** - Additional contributors (if any)

## License
This project is licensed under the MIT License.


