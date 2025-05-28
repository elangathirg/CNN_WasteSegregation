# CNN_WasteSegregation
Upgrad Assignment CNN_WasteSegregation
## 🎯 Project Aim

The aim of this project is to develop an advanced **waste material segregation system** using **Convolutional Neural Networks (CNNs)** to automatically classify waste into clearly defined categories.  
This system is designed to:

- 🚀 Boost recycling efficiency  
- 🌍 Reduce environmental pollution  
- 🌱 Promote sustainable waste management practices

---

## ✅ Key Objectives

- 🏷️ **Accurately classify** waste materials into categories such as **cardboard**, **glass**, **paper**, and **plastic**.
- ⚙️ **Improve segregation efficiency** to facilitate recycling and minimize waste sent to landfills.
- 🧠 **Extract insights** from the characteristics of various waste materials to refine and optimize sorting strategies for sustainability.


# 🧾 Waste Classification: Data Understanding and Model Training

## 📁 1. Data Understanding

### 🗂️ Dataset Overview
The dataset consists of images representing commonly encountered waste materials, grouped into the following categories:

- Cardboard  
- Food Waste  
- Glass  
- Metal  
- Paper  
- Plastic  
- Other  

### 🗃️ Data Structure
Images are organized in a hierarchical directory format, where each subfolder corresponds to a specific waste class.

Example directory structure:
dataset/
├── Cardboard/
├── Food_Waste/
├── Glass/
├── Metal/
├── Paper/
├── Plastic/
└── Other/

Each folder contains images of items in that category. However, individual items are not subcategorized.  
For example, the `Food_Waste` folder may include images of coffee grounds, tea bags, or fruit peels without explicitly identifying them.

---

## 🔍 1.1 Insights and Observations

### 📊 Class Distribution
A bar plot was used to visualize the number of images per category. This helps identify class imbalances, which can negatively affect model training and performance.

### 🖼️ Image Dimensions
The dataset included images of various sizes. The smallest and largest dimensions were recorded.  
All images were resized to a consistent shape of **224×224** pixels to standardize model input.

### 🏷️ Label Encoding
Folder names were used as class labels and encoded into numerical values using `LabelEncoder`.

---

## 🧪 2. Model Training Results

### 🧱 Model Architecture
A Convolutional Neural Network (CNN) was implemented with the following structure:

- 3 Convolutional Layers  
- Batch Normalization after each convolution  
- MaxPooling Layers  
- Dropout Layers for regularization  
- Dense Layers for classification  
- Softmax output for multi-class prediction

### ⚙️ Model Compilation
- **Optimizer:** Adam  
- **Loss Function:** Categorical Crossentropy  
- **Evaluation Metric:** Accuracy  

### 🏃 Training Strategy
- Data was split into training and validation sets  
- `ImageDataGenerator` was used for image rescaling and augmentation  
- The model was trained using `model.fit()` with validation performance monitoring  

### 📈 Evaluation on Test Set
Performance was measured using the following metrics:

- **Accuracy**  
- **Precision**  
- **Recall**  
- **F1-Score**

These metrics provided a comprehensive view of the model's classification performance across all waste categories.

---
