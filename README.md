## Docker commands

# Build

docker build -t smartorder-api:1.0.0 .

# Run

docker run -p 8080:8080 smartorder-api:1.0.0

# Push to ECR

aws ecr create-repository --repository-name APPLICATION_NAME --region REGION

**Authenticate docker with ECR**

aws ecr get-login-password --region REGION | docker login --username AWS --ECR_REPO_URL

**Tag Image**

docker tag DOCKER_IMAGE:VERSION ECR_REPO_URL/APPLICATION:VERSION

**Push Image**

docker push ECR_REPO_URL/APPLICATION:VERSION



# Other useful docker commands

docker ps -a

docker kill {container-id}