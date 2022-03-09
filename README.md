# Aline Financial Dev-Ops Repository
*by Julius Cesar Estrope*

This repository contains the dev-ops files for deploying Aline Financial's banking application both locally using docker-compose and kubernetes, and on the cloud to AWS ECS and EKS.

## Running these deployments
All deployments expect to pull images from a private ECR repository. You can use the following command to login and access those images:
    
    aws ecr get-login-password --region region | docker login --username AWS --password-stdin aws_account_id.dkr.ecr.region.amazonaws.com
Substitute the region and aws_account_id with the correct region and account ID.

### Docker-Compose
- The docker-compose deployments expect environment variables from various .env files. These will be provided as an attachment to the Jira board for the purpose of code review.
- Ensure that the docker context is correct when deploying locally or to ECS. For more information on creating an ECS context, view [this link](https://docs.docker.com/cloud/ecs-integration/).

### Kubernetes
- The Kubernetes deployments require a running Kubernetes cluster to be deployed, either locally in Docker or on EKS.
- Ensure that the Kubernetes context is correct when running the deployment.
