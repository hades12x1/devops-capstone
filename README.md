[![kcemenike](https://circleci.com/gh/hades12x1/devops-capstone.svg?style=svg)](https://app.circleci.com/pipelines/github/hades12x1/devops-capstone)

## devops-capstone
CAPSTONE PROJECT

## General info
CI/CD pipeline for deploying and linting a microservices application NGINX using Rolling Deployment. Pipeline will containerize application and push the docker image to the Docker Hub.  After that it will create the AWS network infrastructure required to deploy the application.

## Folder structure
* nginx-christmas : Source Files
* .circleci : Configuration File for CircleCI
	
## Tools
Project is created with:

* CirleCI
* CloudFormation
* AWS
* Kubernetes
* Docker Hub
* GitHub
	
## Usage
To run this project in CircleCI, you have to:

* Fork the project to your Github Account
* Setup and Configure CirceCI account with Github and AWS Credentials
* Setup DockerHub account. Save username and password to your local computer, you will need it.
* AWS : configure default VPC  and Key Pair. Store Access key id and secret access key to your local computer, you will need it.
* Configure enviroment variables AWS_DEAFULT_REGION, AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY, DOCKERHUB_PASSWORD, DOCKERHUB_USERNAME in your CircleCI account
* Change the build job from config.yml in order to include your DockerHub credentials, for example :

## Result 
URL: https://d1kcyztmoepita.cloudfront.net/

```
docker build -t nchuyen128/nginx-christmas .
docker tag nginx-hello:latest ${DOCKERHUB_USERNAME}/nginx-christmas:latest
docker push nchuyen128/nginx-hello

```
