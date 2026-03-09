# DevOps CI/CD Pipeline Demo

This project demonstrates a complete DevOps workflow using CI/CD automation, containerization, and Kubernetes deployment.

The pipeline automatically builds, tests, and deploys a containerized application when new code is pushed to the repository.

## Architecture

Developer → GitHub → GitHub Actions → Docker → DockerHub → Kubernetes

## Technologies Used

Docker  
Kubernetes  
GitHub Actions  
Python Flask  
CI/CD Pipelines

## Project Structure

devops-cicd-pipeline-demo

app/
app.py
requirements.txt

docker/
Dockerfile

kubernetes/
deployment.yaml
service.yaml

.github/workflows/
pipeline.yml

## Deployment Steps

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/devops-cicd-pipeline-demo.git

cd devops-cicd-pipeline-demo

docker build -t devops-demo -f docker/Dockerfile .

docker images

docker run -p 5000:5000 devops-demo

http://localhost:5000

minikube start

kubectl apply -f kubernetes/deployment.yaml

kubectl apply -f kubernetes/service.yaml

kubectl get pods

kubectl get services

minikube service devops-demo-service



## Pipeline Workflow

1. Developer pushes code to GitHub
2. GitHub Actions triggers CI/CD pipeline
3. Docker image is built
4. Image is pushed to DockerHub
5. Kubernetes deployment is updated

## Learning Outcomes

- CI/CD pipeline automation
- Docker containerization
- Kubernetes deployment
- DevOps workflow implementation
