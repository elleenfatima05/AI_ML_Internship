# 🤖 AI/ML Engineering Internship — DevelopersHub Corporation

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=flat&logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-yellowgreen?style=flat&logo=scikit-learn)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=flat)

This repository contains all tasks completed as part of the **AI/ML Engineering Internship** at DevelopersHub Corporation. Each task is organized in its own folder with a dedicated notebook, requirements file, and documentation.

**Intern:** Elleen Fatima
**Due Date:** 26th June, 2026

---

## 📁 Repository Structure

```
AI_ML_Internship/
│
├── Task1_Iris/
│   ├── task1_iris.ipynb
│   ├── README.md
│   └── requirements.txt
│
├── Task2_Stocks_Prediction/
│   ├── task2_stocks.ipynb
│   ├── README.md
│   └── requirements.txt
│
├── Task3_Heart_Disease/
│   ├── task3_heart_disease.ipynb
│   ├── README.md
│   └── requirements.txt
│
├── Task4_Health_Query_ChatBot/
│   ├── task4_health_chatbot.ipynb
│   ├── README.md
│   └── requirements.txt
│
├── Task5__MentalHealth_ChatBot/
│   ├── task5_mental_health.ipynb
│   ├── README.md
│   └── requirements.txt
│
├── Task6_House_price_prediction/
│   ├── task6_house_price_prediction.ipynb
│   ├── train.csv
│   ├── README.md
│   └── requirements.txt
│
└── README.md                
```

---

## ✅ Tasks Overview

| #   | Task                                       | Status      | Key Skills                                            |
| --- | ------------------------------------------ | ----------- | ----------------------------------------------------- |
| 1   | Exploring and Visualizing the Iris Dataset | ✅ Complete | EDA, pandas, seaborn, matplotlib                      |
| 2   | Predict Future Stock Prices (Short-Term)   | ✅ Complete | Regression, yfinance, scikit-learn                    |
| 3   | Heart Disease Prediction                   | ✅ Complete | Binary classification, ROC-AUC, feature importance    |
| 4   | General Health Query Chatbot               | ✅ Complete | Prompt engineering, Mistral AI API, safety filtering  |
| 5   | Mental Health Support Chatbot (Fine-Tuned) | ✅ Complete | Fine-tuning, Hugging Face, transformers, GPU training |
| 6   | House Price Prediction                     | ✅ Complete | Regression, Gradient Boosting, feature importance     |

**6 out of 6 tasks completed** — exceeding the minimum requirement of 3 tasks.

---

## 🛠️ Tech Stack

- **Language:** Python 3.11+
- **IDE:** VS Code with Jupyter Extension / Google Colab (Task 5)
- **Core Libraries:** pandas, numpy, matplotlib, seaborn
- **Machine Learning:** scikit-learn
- **Deep Learning:** transformers, torch, datasets
- **Finance Data:** yfinance
- **LLM API:** Mistral AI
- **Notebooks:** Jupyter (.ipynb)

---

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/elleenfatima05/AI_ML_Internship.git
cd AI_ML_Internship
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv

# Windows
venv\Scripts\activate

# Mac/Linux
source venv/bin/activate
```

### 3. Install dependencies for a specific task

```bash
cd Task1_Iris
pip install -r requirements.txt
```

### 4. Open any task notebook

Open the folder in VS Code, navigate to the task folder, and open the `.ipynb` file. Make sure the Jupyter extension is installed.

> **Note:** Task 5 requires GPU access for fine-tuning and was built using Google Colab. It can be opened and reviewed in VS Code but is best re-run on Colab.

---

## 📌 Task Summaries

### Task 1: Iris Dataset EDA

Explored and visualized the classic Iris dataset using scatter plots, histograms, and box plots to understand feature distributions across species.

### Task 2: Stock Price Prediction

Predicted next-day closing stock prices for Apple and Tesla using Linear Regression and Random Forest models trained on historical OHLCV data.

### Task 3: Heart Disease Prediction

Built a binary classification model to predict heart disease risk using Logistic Regression and Decision Tree classifiers, evaluated with ROC-AUC and confusion matrices.

### Task 4: Health Query Chatbot

Created a prompt-engineered chatbot using Mistral AI that answers general health questions safely, with keyword-based filtering to block harmful queries.

### Task 5: Mental Health Support Chatbot

Fine-tuned DistilGPT2 on the EmpatheticDialogues dataset using Google Colab's GPU to generate more empathetic conversational responses.

### Task 6: House Price Prediction

Predicted house sale prices using Gradient Boosting Regressor on property features like living area, quality rating, and bedroom count.

---

## 👩‍💻 About

**Intern:** Elleen Fatima
**Program:** AI/ML Engineering Internship
**Organization:** DevelopersHub Corporation
**Tools:** Python · Jupyter · VS Code · Google Colab · Git

---

## 📌 Notes

- All notebooks are fully executed — outputs and plots are visible without running code
- Each task folder contains its own README with detailed findings and methodology
- Committed task by task to reflect progressive completion
- Task 5 (fine-tuning) requires GPU; recommended to run on Google Colab
