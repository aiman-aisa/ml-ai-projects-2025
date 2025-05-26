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
- [AWS EC2 Deployment with GitHub Actions](#deployment)
- [Future Work](#future-work)

---

## 📖 About the Project

This project is done to understand how the students' performance (test scores) is affected by other variables such as Gender, Ethnicity, Parental Level of Education, Lunch, and Test Preparation course. It includes data preprocessing, EDA, feature engineering, model training, evaluation, and deployment with Flask.

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
```
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
```

## 📊 Data Source
- Dataset Source - https://www.kaggle.com/datasets/spscientist/students-performance-in-exams 
- The data consists of 8 columns and 1000 rows

## ⚙️ Installation
1. Clone the repository
```bash
git clone https://github.com/aiman-aisa/ml-ai-projects-2025.git
cd ml-ai=projects-2025
```
2. Create a virtual env
```bash
python -m venv venv
source venv/bin/activate
```
3. Install dependencies
```bash
pip install -r requirements.txt
```
## 🚀 Usage
1. Run data ingestion, data transformation, model trainer
- here you will get the best model r2 score printed in the terminal
- the artifacts folders and the files will be generated
```bash
python src/components/data_ingestion.py
```
2. Run Flask App
```bash
python app.py
```

## 📈 Model Performance
Best model is Linear Regression with accuracy of 86.98%

## 📌 Results
- Student's Performance is related with lunch, race, parental level education, test preparation course
- Females lead in pass percentage and also are top-scorers
- Finishing preparation course is benefitial.

## AWS EC2 Deployment with GitHub Actions
1. Create EC2 Instance
2. Create ECR and save the repository URI and Name
3. Create GitHub Action with the following Secrets:
 - AWS_ACCESS_KEY_ID -> access key from IAM
 - AWS_ECR_LOGIN_URI -> eg: ########.dkr.ecr.ap-southeast-1.amazonaws.com
 - AWS_REGION
 - AWS_SECRET_ACCESS_KEY -> access key value from IAM
 - ECR_REPOSITORY_NAME -> name of your ECR
4. Launch your EC2 instance and run the following command to install docker:
   ```bash
    sudo apt-get update -y
    sudo apt-get upgrade -y
    curl -fsSL https://get.docker.com -o get-docker.sh
    sudo sh get-docker.sh
    sudo usermod -aG docker ubuntu
    newgrp docker
   ```
5. Create a self-hosted runner with linux and follow the setup command
6. Run the job
7. Open the URL of the EC2 instance

## 🔭 Future Work
- Add hyperparameter tuning (GridSearchCV or Optuna)
- Use XGBoost or LightGBM for better performance
- Set up DVC for data versioning
- Deploy model as REST API with FastAPI
- Implement CI/CD pipeline using GitHub Actions
