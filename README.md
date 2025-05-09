# 🚀 Jenkins Pipeline for Java Application with Maven, SonarQube, Argo CD, Helm & Kubernetes

![Pipeline Diagram](https://user-images.githubusercontent.com/43399466/228301952-abc02ca2-9942-4a67-8293-f76647b6f9d8.png)

This guide provides step-by-step instructions to set up a robust, end-to-end Jenkins pipeline for a Java-based application using:

- **Maven** for build and packaging  
- **SonarQube** for code quality analysis  
- **Helm** for Kubernetes deployments  
- **Argo CD** for GitOps-based production delivery  

---

## 📋 Prerequisites

Ensure the following components are in place before starting:

- ✅ Java application source code in a Git repository  
- ✅ Jenkins server with pipeline support  
- ✅ Kubernetes cluster  
- ✅ Helm installed  
- ✅ Argo CD deployed on Kubernetes  

---

## 🛠️ Jenkins Pipeline Setup

### 1. Install Required Jenkins Plugins

- Git Plugin  
- Maven Integration Plugin  
- Pipeline Plugin  
- Kubernetes Continuous Deploy Plugin  

### 2. Create a New Jenkins Pipeline Job

- Configure it with the Git repository URL.  
- Add a `Jenkinsfile` to the repository to define your CI/CD stages.  

---

## 🔁 Pipeline Stages Overview

### Stage 1: Checkout Source Code  
- Use the Git plugin to pull the code from the repository.

### Stage 2: Build Application  
- Use Maven to compile the Java application.

### Stage 3: Run Unit Tests  
- Execute unit tests using JUnit and Mockito.

### Stage 4: Code Quality Check  
- Analyze the code with SonarQube.

### Stage 5: Package Application  
- Package the build into a JAR file using Maven.

### Stage 6: Deploy to Test Environment  
- Use Helm (via Kubernetes plugin) to deploy the app for testing.

### Stage 7: User Acceptance Testing  
- Use Selenium or another tool to perform UAT.

### Stage 8: Promote to Production  
- Deploy to production using Argo CD.

---

## ⚙️ Argo CD Configuration

1. **Install Argo CD** on your Kubernetes cluster.  
2. **Set up a Git repository** for Helm charts and Kubernetes manifests.  
3. **Create a Helm chart** for the Java application.  
4. **Ensure Argo CD tracks** the Git repo with Helm configuration.  

---

## 🔗 Jenkins ↔ Argo CD Integration

- Add Argo CD API token to Jenkins credentials.  
- Update `Jenkinsfile` to include a production deployment stage using Argo CD.  

---

## ▶️ Running the Pipeline

1. Trigger the Jenkins pipeline manually or via webhook.  
2. Monitor pipeline execution through the Jenkins UI.  
3. Debug and resolve any failures in pipeline stages.  

---

## ✅ Result

A fully automated CI/CD pipeline using Jenkins for a Java application, integrating key tools like:

- **Maven** for builds  
- **SonarQube** for code quality  
- **Helm** for Kubernetes deployment  
- **Argo CD** for GitOps-style production releases  

---

## 🙌 Credits

Credits to :  `"https://github.com/iam-veeramalla/Jenkins-Zero-To-Hero"`

---
