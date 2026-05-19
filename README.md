# Production Deployment Pipeline

This production pipeline deploys the application to EC2 using GitHub Actions.

## How it works
- Reads IMAGE_VERSION from GitHub Actions Variables
- Pulls the image from AWS ECR
- Updates docker-compose.yml automatically
- Deploys containers to EC2 using docker-compose

## Important
The production workflow does not build or push Docker images.
It only pulls and deploys existing images from ECR.
