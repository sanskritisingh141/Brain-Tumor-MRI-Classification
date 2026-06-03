# Brain Tumor MRI Classification Using Convolutional Neural Networks

## Project Overview
This project implements a deep learning–based image classification system to detect brain tumors from MRI images. A Convolutional Neural Network (CNN) is trained to classify MRI scans into four categories: Glioma, Meningioma, Pituitary Tumor, and No Tumor, helping demonstrate the application of deep learning in medical image analysis.

## Objective
The objective of this project is to build and evaluate a CNN model that can automatically identify the presence of brain tumors from MRI images, which can assist in early diagnosis and medical decision support.

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Dataset

The dataset consists of brain MRI images organized into training and testing directories. Each image belongs to one of the following classes:

- Glioma Tumor
- Meningioma Tumor
- Pituitary Tumor
- No Tumor

The dataset is structured as:
```
data/
│
├── train/
│   ├── glioma/
│   ├── meningioma/
│   ├── no_tumor/
│   └── pituitary/
│
├── val/
│   ├── glioma/
│   ├── meningioma/
│   ├── no_tumor/
│   └── pituitary/
│
└── test/
    ├── glioma/
    ├── meningioma/
    ├── no_tumor/
    └── pituitary/
```

The dataset contains approximately 7,000 MRI images and is used for multi-class brain tumor classification.

> **Note:** The dataset is not included in this repository due to size limitations.  
> Please place the dataset inside the `data/` directory before running the notebook.

## Project Structure
```
Brain-Tumor-MRI-Classification/
│── Brain_Tumor_MRI_Classification.ipynb
│── README.md
│── requirements.txt
│── results/
│ ├── confusion_matrix.png
│ └── classification_report.txt
│── data/ (not included)
```


## Methodology
- Image loading and resizing using TensorFlow utilities  
- Data augmentation and normalization  
- CNN model design with convolutional, pooling, and dense layers  
- Model training using categorical cross-entropy loss  
- Performance evaluation using confusion matrix and classification report  

## Model Architecture

The CNN model consists of:

- Convolutional Layers (feature extraction)
- ReLU Activation Functions
- Max Pooling Layers
- Flatten Layer
- Fully Connected Dense Layers
- Softmax Output Layer (4 classes)

## Evaluation Metrics
The model performance is evaluated using:
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Results

The CNN model achieved the following performance on the test dataset:

- Accuracy: 96%
- Macro F1-Score: 0.96
- Weighted F1-Score: 0.96

### Class-wise Performance

| Class | Precision | Recall | F1-Score |
|---------|---------|---------|---------|
| Glioma | 0.92 | 0.96 | 0.94 |
| Meningioma | 0.97 | 0.87 | 0.91 |
| No Tumor | 0.97 | 1.00 | 0.99 |
| Pituitary | 0.98 | 1.00 | 0.99 |

- The confusion matrix visualization is available below:

![Confusion Matrix](results/confusion_matrix.png)


## How to Run the Project
1. Clone the repository  
2. Install dependencies using:
`pip install -r requirements.txt`
3. Place the dataset inside the `data/` directory  
4. Open `Brain_Tumor_MRI_Classification.ipynb` in Jupyter Notebook or Google Colab  
5. Run all cells sequentially  

## Limitations
- Performance depends on dataset size and quality  
- The trained model file is not included due to size constraints  
- Limited generalization to unseen MRI datasets  

## Future Improvements
- Experiment with transfer learning models such as ResNet50, EfficientNet, and MobileNet
- Hyperparameter tuning for improved accuracy
- Deploy as a web application using Flask or Streamlit
- Integrate explainable AI techniques such as Grad-CAM 
- Use transfer learning models such as ResNet or MobileNet  

## Author
Sanskriti Singh

