# Mobile-Prices-Classification-With-AWS-Sagemaker

## Overview
This project demonstrates the process of creating and deploying a machine learning model to classify mobile phone prices using AWS SageMaker. The project follows a step-by-step approach, from data preparation to model deployment. The classification problem involves predicting the price range of mobile phones based on their features.

## Prerequisites
Before starting, make sure you have the following set up:

*AWS Account:* You need an AWS account with administrative access.

*AWS CLI:* Configure the AWS CLI with your access key and secret access key.

*Python Packages:* Install the required packages from requirements.txt:

```
pip install -r requirements.txt
```

## Step-by-Step Guide
1. IAM User: <br>
Create an IAM User with AdministratorAccess permissions in the AWS Management Console.

2. AWS CLI Configuration: <br>
Configure the AWS CLI with your IAM User's access key and secret access key using the aws configure command.

3. Install Packages: <br>
Install the necessary Python packages listed in requirements.txt.

4. Create S3 Bucket: <br>
Create an AWS S3 bucket where you will store your dataset and model artifacts.

5. Load Data: <br>
Load the Mobile Price Classification dataset.

6. Feature Engineering: <br>
Perform any required feature engineering on the dataset.

7. Split and Save Data: <br>
Split the dataset into training and testing data. Save these datasets as CSV files that can be uploaded to the S3 bucket.

8. Upload Data to S3: <br>
Upload the CSV files to the S3 bucket.

9. Script.py: <br>
Create a Python script, script.py, where you initialize the model and perform basic feature engineering.

10. SageMaker Execution: <br>
SageMaker will access script.py for model training and testing.

11. Create IAM Role: <br>
Create an AWS IAM role that SageMaker can use for accessing resources.

12. Create SageMaker Estimator: <br>
Create an SKLearn Estimator for your model.

13. Train the Model: <br>
Fit the estimator to the training and testing datasets stored in the S3 bucket.

14. Create a Model Copy: <br>
Create a copy of the trained model that can be used for deployment.

15. Deploy an Endpoint: <br>
Create a SageMaker endpoint that can be used to predict new instances. Note that endpoint creation is billable.

16. Testing: <br>
Test your model on the testing dataset to evaluate its performance.

17. Delete the Endpoint: <br>
After testing, remember to delete the SageMaker endpoint to avoid additional charges.

## Further Resources
[AWS SageMaker Documentation](https://docs.aws.amazon.com/sagemaker/latest/dg/whatis.html) <br>
[AWS CLI Configuration Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html) <br>
[IAM User Creation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html) <br>
[S3 Bucket Creation](https://docs.aws.amazon.com/AmazonS3/latest/userguide/creating-bucket.html) <br>
[SageMaker SKLearn Estimator](https://sagemaker.readthedocs.io/en/stable/frameworks/sklearn/using_sklearn.html) <br>
[SageMaker Endpoint Deployment](https://sagemaker.readthedocs.io/en/stable/frameworks/sklearn/using_sklearn.html)

## Acknowledgments
This project was created as part of an End-to-end ML Deployment tutorial by [Krish Naik](https://www.youtube.com/@krishnaik06)
