#  Enhanced Flower Recognition Using ResNet-50

## 📌 About the Project

This project implements a **flower image classification system using ResNet-50 Transfer Learning**.

A pre-trained **ResNet-50 model with ImageNet weights** is used as the backbone and fine-tuned to classify flower images into **5 different categories**.

The project focuses on improving flower recognition performance through **Transfer Learning, Data Augmentation, and Fine-Tuning**.

---

## 🎯 Objectives

* Classify flower images into five different categories.
* Utilize **ResNet-50 Transfer Learning** for image classification.
* Apply **data augmentation** to improve model generalization.
* Fine-tune the final layers of the pre-trained model.
* Evaluate model performance using multiple classification metrics.
* Visualize training performance and feature maps.

---

## 📂 Dataset

The project uses the **TensorFlow Flower Photos Dataset**.

### Flower Classes

| Class         | Description       |
| ------------- | ----------------- |
| 🌼 Daisy      | Daisy flowers     |
| 🌻 Dandelion  | Dandelion flowers |
| 🌹 Roses      | Rose flowers      |
| 🌻 Sunflowers | Sunflower images  |
| 🌷 Tulips     | Tulip flowers     |

### Dataset Details

* **Total Images:** 3,670
* **Number of Classes:** 5
* **Image Size:** 224 × 224
* **Batch Size:** 32

---

## 🧠 Model Architecture

The project uses **ResNet-50**, a deep convolutional neural network pre-trained on the **ImageNet dataset**.

### Architecture

```text
Input Image
     ↓
ResNet-50
(ImageNet Weights)
     ↓
Global Average Pooling
     ↓
Dropout
     ↓
Dense Layer
     ↓
Softmax
     ↓
5 Flower Classes
```

### Transfer Learning Strategy

1. Load the pre-trained ResNet-50 model with ImageNet weights.
2. Remove the original classification head.
3. Add a custom classification layer for 5 flower classes.
4. Initially train the new classification layers.
5. Unfreeze the last 20 layers of ResNet-50.
6. Fine-tune the model using the flower dataset.

---

## 🔄 Methodology

The overall workflow of the project is:

```text
Flower Dataset
      ↓
Data Loading
      ↓
Image Preprocessing
      ↓
Data Augmentation
      ↓
ResNet-50 Transfer Learning
      ↓
Train Classification Layers
      ↓
Fine-Tune Last 20 Layers
      ↓
Model Evaluation
      ↓
Performance Visualization
```

---

## 🛠️ Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **ResNet-50**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Google Colab / Jupyter Notebook**

---

## 📊 Model Evaluation

The trained model is evaluated using the following performance metrics:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **Confusion Matrix**

### Visualizations

The project also includes:

* Training Accuracy vs Validation Accuracy
* Training Loss vs Validation Loss
* Confusion Matrix
* Classification Performance
* Feature Map Visualization

These visualizations help analyze the model's learning behavior and classification performance.

---

## 📁 Project Structure

```text
GenerativeAI-Lab-Assignment1/
│
├── Amruta_Kanase_GenAI_LabAssignment1.ipynb
│
└── README.md
```

### File Description

**`.ipynb`**

Contains the complete implementation, including:

* Dataset loading
* Data preprocessing
* Data augmentation
* ResNet-50 model implementation
* Transfer learning
* Fine-tuning
* Model training
* Evaluation
* Visualization

**`README.md`**

Contains project documentation, methodology, technologies, and instructions for running the project.

---

## ▶️ How to Run

### 1. Clone the Repository

```bash
https://github.com/AmrutaKanse09/GenerativeAI-Lab-Assignment1
```

### 2. Open the Notebook

You can open the notebook using:

* **Google Colab**
* **Jupyter Notebook**
* **JupyterLab**
* **VS Code**

### 3. Install Required Libraries

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
```

### 4. Run the Notebook

Open:

```text
Amruta_Kanase_GenAI_LabAssignment1.ipynb
```

Run the cells **sequentially from top to bottom**.

---

## 💡 Key Features

✅ ResNet-50 Transfer Learning
✅ ImageNet Pre-trained Weights
✅ Data Augmentation
✅ Fine-Tuning of Last 20 Layers
✅ Five-Class Flower Classification
✅ Accuracy, Precision, Recall & F1-Score
✅ Confusion Matrix
✅ Training Performance Visualization
✅ Feature Map Visualization

---

## 🚀 Future Improvements

* Use a larger and more diverse flower dataset.
* Experiment with other architectures such as **EfficientNet, DenseNet, and MobileNet**.
* Apply hyperparameter optimization.
* Deploy the trained model using **Streamlit** or **TensorFlow Serving**.
* Add real-time flower recognition using a webcam or mobile camera.
* Compare ResNet-50 with other transfer learning models.

---

## 👩‍💻 Author

**Amruta Kanase**

---

## ⭐ Acknowledgements

* TensorFlow / Keras
* ImageNet
* TensorFlow Flower Photos Dataset
* Scikit-learn
* Google Colab

---

## 📜 License

This project is created for **educational and research purposes**.
