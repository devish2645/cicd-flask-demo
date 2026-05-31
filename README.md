# CI/CD Flask Demo

A Flask web application deployed on AWS EC2 using Docker and automated through a CI/CD pipeline built with GitHub Actions.

## Overview

This project demonstrates a complete CI/CD workflow where code changes are automatically tested, containerized, and deployed to a cloud server through GitHub Actions.

## Features

* Flask web application
* Docker containerization
* Automated testing with Pytest
* Continuous Integration using GitHub Actions
* Continuous Deployment to AWS EC2
* Automatic application updates on every Git push

## Tech Stack

### Application

* Python
* Flask

### DevOps & Automation

* Docker
* GitHub Actions
* Git
* GitHub

### Cloud Infrastructure

* AWS EC2
* Ubuntu Linux
* SSH

## Architecture

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions
    │
    ├── Run Tests
    ├── Build Docker Image
    └── Deploy via SSH
             │
             ▼
         AWS EC2
             │
             ▼
      Docker Container
             │
             ▼
      Flask Application
```

## Deployment Flow

```text
Edit Code
    │
    ▼
git push
    │
    ▼
GitHub Actions Triggered
    │
    ▼
Install Dependencies
    │
    ▼
Run Pytest Tests
    │
    ▼
Build Docker Image
    │
    ▼
SSH into EC2
    │
    ▼
Fetch Latest Code
    │
    ▼
Rebuild Docker Container
    │
    ▼
Restart Application
    │
    ▼
Updated Website Available
```

## Project Structure

```text
cicd-flask-demo/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── app/
│   ├── app.py
│   ├── test_app.py
│   ├── requirements.txt
│   └── Dockerfile
│
└── README.md
```

## CI/CD Workflow

The GitHub Actions pipeline performs the following steps:

1. Trigger on push to main branch
2. Install project dependencies
3. Run automated tests using Pytest
4. Build Docker image
5. Connect to AWS EC2 via SSH
6. Update application source code
7. Rebuild Docker container
8. Restart application automatically

## Learning Outcomes

* Linux server administration
* Docker containerization
* GitHub Actions workflow automation
* AWS EC2 deployment
* SSH-based remote deployment
* Continuous Integration and Continuous Deployment practices

