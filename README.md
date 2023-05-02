# cnnclassifier

### Clone the repository
```
https://github.com/ankit-world/cnnclassifier.git
```

### Create Conda Environment
```
conda create -p venv python=3.8 -y
```

### Activate the Conda Environment
```
conda activate venv/
```

### Install requirements
```
pip install -r requirements.txt
```

### Workflows
```
Update config.yaml
Update secrets.yaml [Optional]
Update params.yaml
Update the entity
Update the configuration manager in src config
Update the components
Update the pipeline
Update the main.py
```

### AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment
```
# with specific access

1. EC2 access : It is virtual machine

2. ECR: Elastic Container registry to save your docker image in aws


# Description: About the deployment

1. Build docker image of the source code

2. Push your docker image to ECR

3. Launch Your EC2 

4. Pull Your image from ECR in EC2

5. Lauch your docker image in EC2

# Policy:

1. AmazonEC2ContainerRegistryFullAccess

2. AmazonEC2FullAccess
```

## 3. Create ECR repo to store/save docker image
```
Save the URI: 837453223154.dkr.ecr.ap-south-1.amazonaws.com/catdog
```

## 4. Create EC2 machine (Ubuntu)

## 5.Open EC2 and Install docker in EC2 Machine:
```
# optinal

sudo apt-get update -y

sudo apt-get upgrade

# required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

## 6.Configure EC2 as self-hosted runner:
```
setting>actions>runner>new self hosted runner> choose os> then run command one by one
```

## 7. Setup github secrets:
```
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = ap-south-1

AWS_ECR_LOGIN_URI = 837453223154.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = catdog
```

