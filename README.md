# 📊 MLflow on AWS: Wine Quality Prediction

This project demonstrates how to train an **ElasticNet regression model** on the Wine Quality dataset and track experiments using **MLflow** hosted on an **AWS EC2 instance** with artifact storage in **S3**.

---

## 🚀 Features

- Train ElasticNet model on Wine Quality dataset
- Track parameters, metrics, and model using MLflow
- Host MLflow Tracking Server on EC2
- Store artifacts in S3
- Log and register models remotely

---

## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine

sudo apt update

sudo apt install python3-pip

sudo apt install pipenv

sudo apt install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell

## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://bucketname

#open Public IPv4 DNS to the port 5000

## Result Screenshots
![image](https://github.com/user-attachments/assets/a642c8dc-3f2a-4a04-b087-ec1876721757)

- MLFlow Tracking
![image](https://github.com/user-attachments/assets/79786978-69fa-440f-9aa7-bf6588a809a0)

![image](https://github.com/user-attachments/assets/47db11b0-1d2f-47ee-b981-bc09ac4984dc)
 


