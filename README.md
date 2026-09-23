# 🩺 Diabetes Data Analysis & Classification

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
  <img src="https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter">
</p>

<p align="center">
  <strong>Exploratory Data Analysis • Data Preprocessing • KNN • Cross-Validation • SVM</strong>
</p>

<p align="center">
  <a href="https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification">Overview</a> •
  <a href="https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification">Workflow</a> •
  <a href="https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification">Machine Learning</a> •
  <a href="https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification">Files</a> •
  <a href="#-technologies">Technologies</a>
</p>

---

## 📌 Overview

This repository presents a **Python-based diabetes data analysis and classification project** using the `diabetes.csv` dataset.

The project demonstrates a complete analytical workflow, beginning with **data loading and preprocessing**, followed by **exploratory data analysis**, feature inspection, and supervised machine-learning classification.

Two classification approaches are implemented:

* 🔵 **K-Nearest Neighbors (KNN)**
* 🟠 **Support Vector Machine (SVM)**

The KNN workflow additionally investigates different values of **K using 10-fold cross-validation** and identifies an optimal neighborhood size based on misclassification error.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* 📥 Load and inspect the diabetes dataset
* 🧹 Perform basic data preprocessing
* 🔍 Identify numerical and categorical features
* 📊 Explore dataset distributions
* 📈 Analyze the target variable
* 🧩 Define predictor and target variables
* ✂️ Split the data into training and testing sets
* 🔎 Evaluate different K values for KNN
* 🔄 Apply **10-fold cross-validation**
* 🎯 Determine an optimal K based on misclassification error
* 🤖 Train a KNN classification model
* 🧠 Train a Support Vector Machine classifier
* 📏 Evaluate model accuracy

---

# 🔬 Project Workflow

```text
                 ┌──────────────────────┐
                 │   Diabetes Dataset   │
                 │    diabetes.csv      │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │  Data Preprocessing  │
                 │  • Missing Values    │
                 │  • Duplicates        │
                 │  • Feature Inspection│
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Exploratory Analysis │
                 │ • Histograms         │
                 │ • Distributions      │
                 │ • Outcome Analysis   │
                 └──────────┬───────────┘
                            │
                            ▼
                 ┌──────────────────────┐
                 │ Train / Test Split   │
                 │      80% / 20%       │
                 └──────────┬───────────┘
                            │
                 ┌──────────┴──────────┐
                 ▼                     ▼
        ┌─────────────────┐    ┌─────────────────┐
        │      KNN        │    │       SVM       │
        │ 10-Fold CV      │    │ Classification  │
        │ Optimal K       │    │                 │
        └────────┬────────┘    └────────┬────────┘
                 │                      │
                 └──────────┬───────────┘
                            ▼
                 ┌──────────────────────┐
                 │ Model Evaluation     │
                 │ Accuracy Comparison  │
                 └──────────────────────┘
```

---

# 📊 Dataset

The project uses the **`diabetes.csv`** dataset.

The analysis works with the following predictor variables:

| Feature                    | Description                  |
| -------------------------- | ---------------------------- |
| `Pregnancies`              | Number of pregnancies        |
| `Glucose`                  | Plasma glucose concentration |
| `BloodPressure`            | Blood pressure measurement   |
| `SkinThickness`            | Skin-fold thickness          |
| `Insulin`                  | Insulin measurement          |
| `BMI`                      | Body Mass Index              |
| `DiabetesPedigreeFunction` | Diabetes pedigree function   |
| `Age`                      | Age of the individual        |
| `Outcome`                  | Target classification        |

### 🎯 Target Variable

`Outcome`

The target represents the classification label used by the machine-learning models.

---

# 🧹 Data Preprocessing

The notebook performs several initial data-quality operations:

* 🔎 Dataset inspection
* 📐 Shape and dimensionality analysis
* 🧾 Column inspection
* ❌ Missing-value removal
* ♻️ Duplicate detection
* 🗑️ Duplicate-row removal
* 🔢 Numerical-feature identification
* 🔤 Categorical-feature inspection
* 📊 Feature variance analysis

These steps prepare the dataset for subsequent exploratory analysis and classification.

---

# 📈 Exploratory Data Analysis

The project performs exploratory analysis to understand the dataset before model development.

### Analysis includes:

* 📊 Dataset distributions
* 📉 Feature histograms
* 🔢 Outcome frequency analysis
* 🔍 Numerical feature inspection
* 📐 Feature variance analysis
* 🧮 Dataset dimensionality

The notebook uses **Matplotlib** and **Pandas** for data exploration and visualization.

---

# 🤖 Machine Learning

## 🔵 1. K-Nearest Neighbors — KNN

The project implements **K-Nearest Neighbors classification**.

### KNN Workflow

* Split dataset into training and testing sets
* Use an **80/20 train-test split**
* Evaluate multiple neighborhood values
* Apply **10-fold cross-validation**
* Calculate mean cross-validation accuracy
* Calculate misclassification error
* Identify the optimal K
* Train the KNN classifier
* Generate predictions
* Calculate test accuracy

### 🔄 Cross-Validation

The notebook evaluates different K values using:

**10-Fold Cross-Validation**

The optimal K is selected based on the minimum misclassification error.

A visualization is also generated showing:

> **Number of Neighbors (K) vs. Misclassification Error**

---

## 🟠 2. Support Vector Machine — SVM

The project also implements a **Support Vector Machine classifier** using Scikit-learn's `SVC`.

### SVM Workflow

* Train the SVM classifier
* Fit the model using the training dataset
* Generate predictions on the test dataset
* Calculate classification accuracy

This provides a second supervised-learning approach for comparison with KNN.

---

# 📏 Model Evaluation

The primary evaluation metric used in the notebook is:

### 🎯 Accuracy

```text
Accuracy = Correct Predictions / Total Predictions
```

The project evaluates the classification performance of:

| Model  | Evaluation    |
| ------ | ------------- |
| 🔵 KNN | Test Accuracy |
| 🟠 SVM | Test Accuracy |

For KNN, cross-validation accuracy and misclassification error are additionally analyzed during K selection.

---

# 🛠️ Technologies & Tools

| Category                   | Technology               |
| -------------------------- | ------------------------ |
| 🐍 Programming Language    | Python                   |
| 📊 Data Analysis           | Pandas                   |
| 🔢 Numerical Computing     | NumPy                    |
| 📈 Visualization           | Matplotlib               |
| 🤖 Machine Learning        | Scikit-learn             |
| 🔵 Classification          | KNN                      |
| 🟠 Classification          | SVM                      |
| 🔄 Validation              | 10-Fold Cross-Validation |
| 📓 Development Environment | Jupyter Notebook         |
| 📁 Dataset                 | CSV                      |

---

# 📂 Repository Structure

```text
Diabetes-Data-Analysis-and-Classification/
│
├── 📓 Diabetes Data Analysis.ipynb
│   └── Complete data analysis and machine-learning workflow
│
├── 📊 diabetes.csv
│   └── Diabetes dataset used for analysis
│
└── 📄 README.md
    └── Project documentation
```

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification.git
```

## 2️⃣ Navigate to the Project

```bash
cd Diabetes-Data-Analysis-and-Classification
```

## 3️⃣ Install Required Libraries

```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

## 4️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Diabetes Data Analysis.ipynb
```

Run the notebook cells sequentially.

---

# ▶️ Quick Start

<p align="center">

<a href="https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification">
<img src="https://img.shields.io/badge/📁%20View%20Repository-181717?style=for-the-badge&logo=github&logoColor=white">
</a>

<a href="https://github.com/shahidazam2020-oss/Diabetes-Data-Analysis-and-Classification/blob/main/Diabetes%20Data%20Analysis.ipynb">
<img src="https://img.shields.io/badge/📓%20Open%20Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white">
</a>

</p>

---

# 📚 Key Learning Outcomes

Through this project, the following practical concepts are demonstrated:

* 🧹 Data cleaning and preprocessing
* 📊 Exploratory data analysis
* 📈 Data visualization
* 🧩 Feature and target selection
* ✂️ Train-test splitting
* 🤖 KNN classification
* 🧠 SVM classification
* 🔄 Cross-validation
* 🎯 Hyperparameter investigation through K selection
* 📏 Classification accuracy evaluation
* 📉 Misclassification-error analysis

---

# 🔍 Project Highlights

> **Data → Preprocessing → Exploration → Validation → Classification → Evaluation**

### ⭐ Highlights

* 📊 Real-world healthcare-oriented classification task
* 🧹 Structured data-cleaning workflow
* 🔄 10-fold cross-validation for KNN
* 🎯 Data-driven selection of K
* 🤖 Comparison of KNN and SVM
* 📈 Visualization of misclassification error
* 🧪 Reproducible Jupyter Notebook workflow
* 💻 Suitable for learning and demonstrating practical machine-learning techniques

---

# 👨‍💻 About ME

## Shahid Azam

**MS Computer Science | Artificial Intelligence**

Institute of Management Sciences, Peshawar, Pakistan

Focused on:

* 🤖 Artificial Intelligence & Machine Learning
* 📊 Data Analysis & Visualization
* 🧠 Deep Learning
* 🏥 Healthcare Machine Learning
* 💻 Python Development

<p align="center">

<a href="https://github.com/shahidazam2020-oss">
<img src="https://img.shields.io/badge/GitHub-Shahid%20Azam-181717?style=for-the-badge&logo=github">
</a>

<a href="https://www.linkedin.com/in/shahid-azam-mughal-787b58235">
<img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin">
</a>

</p>

---

# ⭐ Support

If you find this project useful for **learning, research, or machine-learning practice**, consider giving the repository a ⭐.

Your feedback, suggestions, and contributions are welcome.

<p align="center">

**🧠 Learn • 💻 Build • 📊 Analyze • 🤖 Experiment • 🚀 Improve**

</p>

---

<p align="center">
  <strong>Made with ❤️ by Shahid Azam</strong>
</p>
