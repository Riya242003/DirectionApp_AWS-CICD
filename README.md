# 🚀 Deploying a Static Web Application on AWS

Welcome to the **City Direction Application Deployment Guide**! This tutorial will walk you through deploying a **static web application** using **AWS CodeCommit, CodeBuild, CodeDeploy, and CodePipeline**. 

---

## 📌 Project Overview
This project is divided into three key parts:

1. **CodeCommit Setup** (Version Control)
2. **CodeBuild Implementation** (Automated Build Process)
3. **CodeDeploy & Pipeline Automation** (Deployment & CI/CD Pipeline)

By the end of this guide, you'll have a fully automated deployment pipeline ensuring seamless updates to your application.

---

## 🔹 PART 1: CodeCommit Setup

### 📌 What is CodeCommit?
AWS CodeCommit is a fully managed source control service that enables teams to host secure Git repositories. 

### 🛠 Steps to Set Up CodeCommit
1. **Create a Repository**
   - Navigate to **AWS CodeCommit** > **Create Repository**
   - Name your repository (e.g., `city-direction-app`)
   - Clone the repository.
  
     **Note** : AWS no longer provides the CodeCommit service to new users. Instead, you can use a GitHub repository.
     
2. **Push Your Code to CodeCommit**
   - Add your project files:
     ```bash
     git add .
     git commit -m "Initial commit"
     git push origin main
     ```

---

## 🔹 PART 2: CodeBuild Implementation

### 📌 What is CodeBuild?
AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces deployable artifacts.

### 🛠 Steps to Implement CodeBuild
1. **Create a `buildspec.yml` file**

2. **Set up CodeBuild in AWS Console**
   - Go to **AWS CodeBuild** > **Create Build Project**
   - Connect to CodeCommit repository
   - Upload the `buildspec.yml` file
   - Start the build process

3. **Store Artifacts in S3** (Optional but recommended)
   - Create an S3 bucket
   - Configure CodeBuild to store build artifacts

---

## 🔹 PART 3: CodeDeploy and Pipeline Automation

### 📌 What is CodeDeploy?
AWS CodeDeploy automates application deployments to EC2, Lambda, and on-premises servers.

### 🛠 Steps to Deploy Using CodeDeploy
1. **Create an `appspec.yml` file**

2. **Set Up an EC2 Instance 

3. **Automate Deployment with CodePipeline**
   - Create a new **AWS CodePipeline**
   - Connect CodeCommit, CodeBuild, and CodeDeploy
   - Trigger deployments on every code push


---

## 🎯 Conclusion
By following this guide, you've successfully:
✔ Set up version control using **CodeCommit**
✔ Automated the build process with **CodeBuild**
✔ Deployed your application using **CodeDeploy & CodePipeline**

🚀 Now, every code push automatically triggers a new deployment!

---

## 📚 Additional Resources
- [AWS CodeCommit Docs](https://docs.aws.amazon.com/codecommit/latest/userguide/)
- [AWS CodeBuild Docs](https://docs.aws.amazon.com/codebuild/latest/userguide/)
- [AWS CodeDeploy Docs](https://docs.aws.amazon.com/codedeploy/latest/userguide/)
- [AWS CodePipeline Docs](https://docs.aws.amazon.com/codepipeline/latest/userguide/)

🔥 **Happy Deploying!** 🚀

