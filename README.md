# devops-task-1
# DevOps Internship - Task 1: Automate Code Deployment Using CI/CD Pipeline

##  Objective
This repository contains the solution for Task 1 of the Elevate Labs DevOps Internship. The objective is to set up a Continuous Integration and Continuous Deployment (CI/CD) pipeline to automate the build and deployment process of a web application using GitHub Actions and Docker.

##  Tools & Technologies Used
* **Version Control:** Git & GitHub
* **CI/CD:** GitHub Actions
* **Containerization:** Docker
* **Application:** Node.js
* **Image Registry:** DockerHub

##  Repository Structure
* `app.js` & `package.json`: A simple Node.js web application used for testing the deployment.
* `Dockerfile`: Contains the instructions to containerize the Node.js application.
* `.github/workflows/main.yml`: The core GitHub Actions workflow file that defines the CI/CD automation.

## CI/CD Pipeline Workflow
The pipeline is designed to trigger automatically on every `push` to the `main` branch. It executes the following automated steps:
1. **Checkout Code:** Retrieves the latest source code from the GitHub repository.
2. **Setup Node.js Environment:** Prepares the runner with the required Node.js version.
3. **Login to DockerHub:** Authenticates securely with DockerHub using encrypted GitHub Secrets (`DOCKERHUB_USERNAME` and `DOCKERHUB_TOKEN`).
4. **Build and Push:** Builds the Docker image based on the `Dockerfile` and successfully pushes the final image to the DockerHub repository.

##  Conclusion
By completing this task, a complete CI/CD automation process has been established, ensuring that code changes are continuously built and stored as ready-to-deploy Docker images without any manual intervention.
