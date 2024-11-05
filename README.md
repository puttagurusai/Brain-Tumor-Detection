# Brain-Tumor-Detection
Table of Contents
Project Overview
Dataset
What is Brain Tumor?
Setup and Installation
Data Preparation
Model Architecture
Results
Conclusions
Project Overview
This project focuses on detecting brain tumors from MRI scans using a Convolutional Neural Network (CNN) model based on the VGG-16 architecture. The objective is to create a binary classifier that identifies the presence or absence of a brain tumor from the scan images.

Metrics:
Model performance is measured by accuracy:

Accuracy
=
Number of correctly predicted images
Total number of tested images
×
100
%
Accuracy= 
Total number of tested images
Number of correctly predicted images
​
 ×100%
Final Results:

Dataset	Accuracy
Validation	~88%
Test	~80%
Dataset
The MRI scans used are from the Brain MRI Images for Brain Tumor Detection dataset. Images are labeled as either:

YES (with tumor) - encoded as 1
NO (without tumor) - encoded as 0
Note: The dataset's origin is not fully documented.

What is Brain Tumor?
A brain tumor is the growth of abnormal cells within the brain, categorized as either benign or malignant. Symptoms vary based on the tumor's location and may include headaches, vision problems, seizures, and other neurological symptoms. Learn more on Wikipedia.



Setup and Installation
Environment
To set up the environment, install the required Python packages:

bash
Copy code
pip install imutils numpy tqdm matplotlib opencv-python scikit-learn keras plotly
Ensure you have a GPU-enabled environment to handle the CNN training effectively.

Data Structure
The MRI scans are split into training, validation, and test sets:

objectivec
Copy code
brain_tumor_dataset/
├── TRAIN
│   ├── YES
│   └── NO
├── VAL
│   ├── YES
│   └── NO
└── TEST
    ├── YES
    └── NO
Data Preparation
The data is preprocessed as follows:

Images are resized for consistency.
Images are split into train, validation, and test sets (80% training, 10% validation, and 10% testing).
Model Architecture
The VGG-16 model is used as a base, with additional layers tailored for this binary classification task. The architecture is fine-tuned to maximize accuracy, using data augmentation to improve generalization.

Key model components:

Convolutional Layers based on VGG-16 pretrained weights.
Data Augmentation to increase the diversity of training samples.
Dense Layers for final classification.
Results
The model achieves the following performance:

Validation Accuracy: ~88%
Test Accuracy: ~80%
A confusion matrix and accuracy score provide further insights into the model’s performance.

Conclusions
The VGG-16 model proves effective in detecting brain tumors from MRI scans, achieving high accuracy on both validation and test sets. Future work may involve experimenting with different architectures or larger datasets to improve performance further.

License
This project is licensed under the MIT License. See the LICENSE file for details. ​
