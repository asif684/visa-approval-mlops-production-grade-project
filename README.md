# 🛂 Visa Approval Prediction - MLOps Production Grade Project

This repository contains an **end-to-end MLOps project** designed to automate and operationalize the visa approval prediction pipeline — from **real-time data ingestion using Confluent Kafka**, to **MongoDB storage**, **model training**, **deployment**, and **AWS-based CI/CD orchestration** using **GitHub Actions**.

---

## 🚀 Tech Stack

**Data Ingestion & Storage**
- [Confluent Kafka](https://confluent.cloud/) – Streaming visa applicant data  
- [MongoDB Atlas](https://account.mongodb.com/) – NoSQL database for storing streamed data  

**MLOps & Model Lifecycle**
- [Evidently AI](https://www.evidentlyai.com/) – Data drift detection and monitoring  
- [Docker](https://www.docker.com/) – Containerization for reproducibility  
- [GitHub Actions](https://github.com/features/actions) – CI/CD automation  

**Cloud Infrastructure**
- [AWS EC2](https://aws.amazon.com/ec2/) – Application hosting  
- [AWS ECR](https://aws.amazon.com/ecr/) – Docker image registry  
- [AWS S3](https://aws.amazon.com/s3/) – Data & model artifact storage  
- [AWS IAM](https://aws.amazon.com/iam/) – Secure role-based access  

**Development & Tools**
- [Python (3.8)](https://www.python.org/) via [Anaconda](https://www.anaconda.com/)  
- [Visual Studio Code](https://code.visualstudio.com/download)  
- [Git](https://git-scm.com/)  
- [Whimsical](https://whimsical.com/) for flowchart and architecture design  

---

## 📄 Problem Statement
- OFLC gives job certification applications for employers seeking to bring foreign workers into the United States and grants certifications.
- As In last year the count of employees were huge so OFLC needs Machine learning models to shortlist visa applicants based on their previous data.
`In this project we are going to use the data given to build a Classification model:`
- This model is to check if Visa get approved or not based on the given dataset.
- This can be used to Recommend a suitable profile for the applicants for whom the visa should be certified or denied based on the certain criteria which influences the decision.

## My goal :
The goal of this project is to build a production-grade MLOps pipeline covering the entire lifecycle: data ingestion, data validation, model training, model evaluation, and model deployment (model pusher). The dataset was streamed via Kafka into MongoDB, enabling efficient data ingestion. For data validation and monitoring, I integrated Evidently AI to detect data drift. The pipeline was containerized with Docker, orchestrated with CI/CD workflows using GitHub Actions, and deployed on AWS. FastAPI was used to serve the model, ensuring a scalable, reliable, and production-ready system.

---

## 🎯 Project Goal

Build a **production-ready MLOps pipeline** that automates the full ML lifecycle:

1. **Data Ingestion** – Stream visa data from **Kafka** into **MongoDB**  
2. **Data Validation** – Validate schema, detect missing or invalid data  
3. **Data Transformation** – Feature encoding, scaling, and cleaning  
4. **Model Training & Evaluation** – Train classification model and evaluate metrics  
5. **Model Pusher** – Save and deploy best-performing model to AWS  
6. **Deployment** – Containerized deployment with **Docker** and **GitHub Actions**, hosted on **AWS EC2**

---

## 🧠 Project Workflow



# visa-approval
visa approval mlops production ready project

- Anaconda: https://www.anaconda.com/
- Vs code: https://code.visualstudio.com/download
- Git: https://git-scm.com/
- Flowchart: https://whimsical.com/
- Kafka: https://confluent.cloud/
- MLOPs Tool: https://www.evidentlyai.com/
- MongoDB: https://account.mongodb.com/account/login
- Data link: https://www.kaggle.com/datasets/moro23/easyvisa-dataset



## Git Commands

```bash
git add .

git commit -m "Updated"

git push origin main

```

## How to run?

```bash
conda create -n visa python=3.8 -y
```

```bash
conda activate visa
```

```bash
pip install -r requirements.txt
```

## work flow

1. constant
2. entity
3. components
4. pipelines
5. main file


## Export the environment variable

```bash


export MONGODB_URL="mongodb+srv://<username>:<password>...."

export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>

export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>


```
## AWS-CICD-Deployment-with-Github-Actions
## 1. Login to AWS console.
## 2. Create IAM user for deployment

```bash
#with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


#Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

#Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```

## 3. Create ECR repo to store/save docker image

```bash
- Save the URI: use own URI
```

## 4. Create EC2 machine (Ubuntu)

## 5. Open EC2 and Install docker in EC2 Machine:

```bash
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

## 6. Configure EC2 as self-hosted runner:

```bash
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```
## 7. Setup github secrets:

```bash
- AWS_ACCESS_KEY_ID
- AWS_SECRET_ACCESS_KEY
- AWS_DEFAULT_REGION
- ECR_REPO
```
