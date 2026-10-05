# 🌾 Rice Leaf Disease Classification

A Deep Learning project for automatically classifying rice leaf diseases from images using **Convolutional Neural Networks (CNNs)** and **MobileNetV2 Transfer Learning**.

The model identifies three rice leaf diseases:

* 🟤 Brown Spot
* 🍂 Leaf Smut
* 🦠 Bacterial Leaf Blight

The project focuses on image preprocessing, data augmentation, model comparison, cross-validation, and transfer learning.

---

## 📸 Disease Classes

| Brown Spot        | Leaf Smut         | Bacterial Leaf Blight |
| ----------------- | ----------------- | --------------------- |
| 🟤                | 🍂                | 🦠                    |
| Rice leaf disease | Rice leaf disease | Rice leaf disease     |

> Add your actual disease images to the repository under `images/` and replace the placeholders above with GitHub image paths.

Example:

```markdown
![Brown Spot](images/brown_spot.jpg)
![Leaf Smut](images/leaf_smut.jpg)
![Bacterial Leaf Blight](images/bacterial_leaf_blight.jpg)
```

---

## 🎯 Objective

The objective is to build an automated computer vision system that can identify rice leaf diseases from digital images and support early disease detection.

The dataset contains **120 images — 40 images per class**.

---

## 🚀 Key Features

* Image dataset exploration
* Image dimension and quality analysis
* Data augmentation
* 5-Fold Stratified Cross-Validation
* Custom CNN model
* MobileNetV2 Transfer Learning
* Early stopping
* Model comparison
* Training and validation analysis
* Final trained model saved as `.h5`

---

## 🤖 Models Used

### Simple CNN

A CNN trained from scratch using:

* Convolution layers
* Max pooling
* Dropout
* Dense layers
* Softmax classification

### MobileNetV2

A pretrained ImageNet model is used as the feature extractor, with the pretrained layers frozen and a custom classification head added.

**MobileNetV2 Transfer Learning** is selected as the recommended model because the dataset is very small and transfer learning provides better stability than training a CNN from scratch.

---

## 🔄 Workflow

```text
Rice Leaf Images
       ↓
Data Exploration
       ↓
Image Resizing (150 × 150)
       ↓
Data Augmentation
       ↓
5-Fold Cross Validation
       ↓
Model Training
   ┌───────────────┐
   │   CNN         │
   │   MobileNetV2 │
   └───────────────┘
       ↓
Model Comparison
       ↓
Final MobileNetV2 Model
       ↓
Disease Classification
```

---

## 📊 Data Augmentation

To reduce overfitting on the small dataset, the project uses:

* Rotation
* Horizontal flipping
* Zoom
* Width/height shifting
* Shearing

The notebook also compares MobileNetV2 performance **with and without data augmentation**.

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* MobileNetV2
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Pillow

---

## 📂 Project Structure

```text
Rice-Leaf-Disease-Classification/
│
├── main.ipynb
├── data/
│   ├── Brown_Spot/
│   ├── Leaf_Smut/
│   └── Bacterial_Leaf_Blight/
│
├── images/
│   ├── brown_spot.jpg
│   ├── leaf_smut.jpg
│   └── bacterial_leaf_blight.jpg
│
├── rice_leaf_disease_model.h5
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
pip install tensorflow notebook ipykernel matplotlib seaborn scikit-learn pandas numpy opencv-python pillow
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
main.ipynb
```

---

## 💾 Trained Model

The final MobileNetV2 model is saved as:

```text
rice_leaf_disease_model.h5
```

It can be used for future rice leaf disease predictions or integrated into a web/mobile application.

---

## ⚠️ Challenges

The main challenge was the **small dataset of only 120 images**.

To reduce overfitting, the project uses:

* Transfer learning
* Data augmentation
* Dropout
* Early stopping
* 5-fold stratified cross-validation

Images are also resized to **150 × 150 pixels** to provide a consistent input size.

---

## 🔮 Future Improvements

* Increase the dataset size
* Add more rice disease classes
* Build a Streamlit web application
* Deploy the model as an API
* Add real-time camera-based disease detection
* Improve model performance with fine-tuning
