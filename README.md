# 🍅 Tomato Leaf Disease Classification using CNN & Transfer Learning

## 📌 Overview

This project implements an image classification pipeline for **tomato leaf disease detection** using the PlantVillage dataset.

Three deep learning models are implemented and compared:

- Custom CNN trained from scratch
- MobileNetV2 using Transfer Learning
- ResNet50 using Transfer Learning

The models are evaluated based on classification performance, training time, and model complexity.

---

## 🎯 Objectives

- Classify tomato leaf diseases using CNN.
- Apply image preprocessing and data augmentation.
- Train a custom CNN from scratch.
- Apply transfer learning using MobileNetV2 and ResNet50.
- Perform feature extraction and fine-tuning.
- Compare models using Accuracy, Precision, Recall and F1-score.
- Compare training time and number of parameters.
- Analyze the advantages and limitations of each model.

---

## 📚 Research Paper

**Title:** Comparing pre-trained models for efficient leaf disease detection: a study on custom CNN

**Authors:** Touhidul Seyam Alam, Chandni Barua Jowthi and Abhijit Pathak

**Year:** 2024

**DOI:** 10.1186/s43067-024-00137-1

**Paper:**  
https://link.springer.com/article/10.1186/s43067-024-00137-1

The implementation follows the comparative methodology of the research paper while focusing on the **10 tomato classes** of the PlantVillage dataset and using Custom CNN, MobileNetV2 and ResNet50.

---

## 📂 Dataset

**PlantVillage Dataset – Kaggle**

https://www.kaggle.com/datasets/abdallahalidev/plantvillage-dataset

Only the tomato portion of the dataset is used.

### Dataset Details

- Total Images: **18,160**
- Classes: **10**
- Training: **12,712**
- Validation: **2,724**
- Testing: **2,724**
- Image Size: **224 × 224**
- Batch Size: **32**

### Tomato Classes

- Bacterial Spot
- Early Blight
- Late Blight
- Leaf Mold
- Septoria Leaf Spot
- Spider Mites
- Target Spot
- Yellow Leaf Curl Virus
- Tomato Mosaic Virus
- Healthy

---

## 🧠 Models

### Custom CNN

A CNN is trained completely from scratch using convolution, max-pooling, dense and dropout layers.

**Maximum Epochs:** 10  
**Optimizer:** Adam  
**Learning Rate:** 0.001

### MobileNetV2

MobileNetV2 is used with ImageNet pretrained weights.

- Feature extraction with frozen base
- Fine-tuning of the last 30 layers
- Fine-tuning learning rate: `1e-5`

MobileNetV2 was selected because it is lightweight and computationally efficient.

### ResNet50

ResNet50 is used with ImageNet pretrained weights.

- Feature extraction with frozen base
- Fine-tuning of the last 30 layers
- Fine-tuning learning rate: `1e-5`

ResNet50 was selected because its deep residual architecture provides strong feature extraction capability.

---

## 📊 Results

| Model | Accuracy | Precision | Recall | F1-Score | Training Time |
|---|---:|---:|---:|---:|---:|
| Custom CNN | 87.04% | 87.21% | 87.04% | 86.70% | 214.92 sec |
| MobileNetV2 | 91.56% | 91.72% | 91.56% | 91.29% | 289.71 sec |
| **ResNet50** | **94.93%** | **95.17%** | **94.93%** | **94.90%** | 653.89 sec |

### Model Complexity

| Model | Parameters |
|---|---:|
| **MobileNetV2** | **2.27 M** |
| Custom CNN | 5.63 M |
| ResNet50 | 23.61 M |

---

## 🔍 Comparative Analysis

- **ResNet50** achieved the highest classification performance.
- **MobileNetV2** provided the best balance between accuracy and model complexity.
- **Custom CNN** had the shortest training time.
- Transfer learning improved performance compared with the custom CNN.

### Final Conclusion

**ResNet50** performed best in terms of Accuracy, Precision, Recall and F1-score.

However, **MobileNetV2** is more suitable for resource-constrained applications because it uses significantly fewer parameters while still achieving high accuracy.

The **Custom CNN** provides a simple and fast baseline but achieved lower classification performance.

---

## 📈 Evaluation & Visualizations

The project includes:

- Class distribution
- Sample images
- Accuracy and loss curves
- Confusion matrices
- CNN feature-map visualization
- Precision, Recall and F1-score
- Training-time comparison
- Parameter comparison
- Final prediction demonstration

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab
- Kaggle API

---

## 🚀 How to Run

1. Open the `.ipynb` notebook in **Google Colab**.
2. Select **T4 GPU** from Runtime settings.
3. Configure the Kaggle API token using Colab Secrets.
4. Run the notebook cells sequentially.
5. The dataset will be downloaded automatically.
6. Models will be trained and evaluated.
7. Comparative results and predictions will be generated.

---

## 📁 Project Structure

```text
Tomato-Leaf-Disease-Classification/
│
├── README.md
└── Amruta_Kanase_GenerativeAI_practical1.ipynb
