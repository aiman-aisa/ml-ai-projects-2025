## End to End Machine Learning Project
# 🧠 Students Performance

> A complete end-to-end machine learning pipeline to predict the students math performance score

## 📌 Table of Contents
- [About the Project](#about-the-project)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Data Source](#data-source)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Results](#results)
- [Future Work](#future-work)
- [License](#license)
- [Contact](#contact)

---

## 📖 About the Project

This project uses machine learning to predict whether a passenger survived the Titanic disaster based on features like age, sex, class, and fare. It includes data preprocessing, EDA, feature engineering, model training, evaluation, and deployment with Streamlit.

**Objective**:
- Classify survival (0 = No, 1 = Yes) from passenger features.

---

## 🛠️ Tech Stack

| Tool               | Purpose                       |
|--------------------|-------------------------------|
| Python             | Core programming language     |
| Pandas, NumPy      | Data manipulation             |
| Seaborn, Matplotlib| Data visualization            |
| Scikit-learn       | ML modeling & evaluation      |
| Flask              | Deployment as web app         |
| Git                | Version control               |
| Jupyter Notebook   | Prototyping and EDA           |

---

## 📂 Project Structure
project-ml/
├── artifacts/
│ ├── data.csv
│ ├── model.pkl
│ ├── preprocessor.pkl
│ └── test.csv
│ └── train.csv
├── notebook/
│ ├── data/
│   └── stud.csv
│ └── EDA-Student-Performance.ipynb
│ └── model-training.ipynb
├── src/
│ ├── components/
│   └── data_ingestion.py
│   └── data_transformation.py
│   └── model_trainer.py
│ ├── pipeline/
│   └── predict_pipeline.py
│   └── train_pipeline.py
│ ├── exception.py
│ ├── logger.py
│ ├── utils.py
├── src/
│ ├── home.html
│ ├── index.html
├── Dockerfile
├── app.py
├── requirements.txt
├── setup.py
├── README.md
└── .gitignore

## 📊 Data Source
- Dataset Source - https://www.kaggle.com/datasets/spscientist/students-performance-in-exams 
- The data consists of 8 columns and 1000 rows

## ⚙️ Installation
1. Clone the repository
2. Create a virtual env
  python -m venv venv
  source venv/bin/activate
3. Install dependencies


