# 🚀 Enterprise CI/CD Pipeline: Python App to Amazon ECR

![CI/CD Pipeline](https://github.com/ELBARGUIMOHAMED/-CI-Pipeline/actions/workflows/ci.yml/badge.svg)

## 🌟 Overview
This project showcases a professional **CI/CD Pipeline** built with **GitHub Actions**. It automates code quality checks, containerization, and cloud delivery to **AWS**.

## 🗺️ Visual Architecture
```mermaid
graph LR
    A[Local Code] -- git push --> B(GitHub Repository)
    subgraph CI_Pipeline[CI Pipeline]
        B --> C{GitHub Actions}
        C --> D[Linting: Flake8]
        C --> E[Testing: Pytest]
    end
    subgraph CD_Pipeline[CD Pipeline]
        E -- Success --> F[Docker Build Image]
        F --> G[Push to Amazon ECR]
    end
    G --> H[AWS Cloud Deployment]    

🏗 Pipeline Architecture (The "DevOps" Flow)

Every time code is pushed to the main branch, the following automated steps occur:

    Linting: Static code analysis using Flake8 to maintain high standards.

    Testing: Unit tests executed via Pytest to ensure code reliability.

    Dockerization: Packaging the application into a Docker Image.

    Cloud Delivery: Securely pushing the image to Amazon ECR.

🛠 Tech Stack

    Automation: GitHub Actions

    Cloud Provider: AWS (IAM, ECR)

    Containerization: Docker

    Quality Control: Flake8 & Pytest

📸 Proof of Concept

Here is the evidence of a successful deployment in the AWS Console:

Built with ❤️ by Mohamed ELBARGUI
