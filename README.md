# docker-aws-web-app
A web app deployed with Docker on AWS using Terraform
# Web App Deployment with Docker & AWS

This project demonstrates how to deploy a simple web application using Docker and AWS EC2, managed through Terraform. The goal is to understand how Docker containers, cloud infrastructure (AWS), and Infrastructure-as-Code (Terraform) work together for automating deployment and managing resources.

---

## Technologies Used

- **AWS EC2** (Elastic Compute Cloud) - For creating and managing virtual servers in the cloud.
- **Docker** - For containerizing the web application.
- **Terraform** - For Infrastructure-as-Code (IaC) to define and provision AWS resources.
- **Nginx** - A lightweight web server to serve the application.

---

## Project Overview

This project covers the process of deploying a basic web application (using Docker) to an EC2 instance on AWS. The entire deployment is automated using Terraform scripts.

### Key Steps:

1. **Containerizing the Web App with Docker**: The web app was packaged into a Docker image to ensure it can run consistently across different environments.
2. **Provisioning AWS Resources with Terraform**: Using Terraform, an EC2 instance was provisioned to run the Docker container.
3. **Deploying the Application**: The Docker container is deployed to AWS EC2, allowing it to be accessed via a public IP.

---

## How to Run Locally

To build and run the Docker container on your local machine:


### Step 1: Clone this repository
```bash
git clone https://github.com/your-username/docker-aws-web-app.git
```

### Step 2: Build the Docker image
Navigate to the directory containing the Dockerfile and run the following command to build the image:
```bash
docker build -t my-web-app .
```



### Step 3: Run the Docker container
Once the image is built, run it with:
```bash
docker run -d -p 80:80 my-web-app
```

You should be able to access the web application at http://localhost on your browser.

---
## How to Deploy on AWS with Terraform

Follow these steps to deploy the web application on AWS using Terraform.

### Step 1: Initialize Terraform
First, navigate to the directory containing the Terraform configuration files (main.tf and variables.tf) and initialize Terraform:
```bash
terraform innit
```


### Step 2: Apply Terraform Configuration
Run the following command to create the resources on AWS:

```bash
terraform apply
```
You’ll be prompted to confirm the actions Terraform will take. Type yes to proceed.

### Step 3: Access the Application
Once Terraform completes the deployment, it will output the public IP of the EC2 instance. Use this IP to access the web application in your browser. For example:

```text
http://<EC2_PUBLIC_IP>
```  
--- 
## Project Goal
The objective of this project was to:

- Learn how to containerize a web application with Docker.
- Automate the provisioning of AWS resources using Terraform.
- Understand how to deploy and manage web apps on AWS using EC2.
---
## Screenshots
Here are some screenshots of the project in action:

## 1. EC2 Dashboard
![Screenshot 2025-03-02 191604](https://github.com/user-attachments/assets/b0e8f2ca-019f-4884-9187-b677d2cfe432)

## 2.Web App Running on EC2
![Screenshot 2025-03-02 191604](https://github.com/user-attachments/assets/b2bd248a-d848-4c31-87d0-61ea7d03747a)

## 3. Project Structure
![project folder](https://github.com/user-attachments/assets/abc82770-df32-4619-b5c5-cdaad2e420d7)


## 4. Docker Image & Container

![docker image   container](https://github.com/user-attachments/assets/85fe3d87-88d5-4ea6-b50c-5613fd38b468)



## 5. AWS ECR Repository
![aws ecr repository](https://github.com/user-attachments/assets/ece13926-23f9-4b15-8aca-747fcabfd63a)



## 6. Terraform Execution

![terraform execution](https://github.com/user-attachments/assets/fdad914d-32a1-47a7-a315-3174ef067385)



## 7. AWS EC2 Instance

![Screenshot 2025-03-02 191604](https://github.com/user-attachments/assets/73df3ca2-c896-4ace-b142-d841766648b3)


## 8. Running Web App

![web app](https://github.com/user-attachments/assets/7b2f57b1-b8a6-4af2-8630-ab562f3ea313)





---
## Troubleshooting
- EC2 Instance Not Starting: Ensure that the AMI ID is correct for the AWS region you are deploying to. You can verify the correct AMI ID in the AWS EC2 Console.
- Docker Container Not Starting: Ensure Docker is correctly installed and running on your local machine.
---

## Resources
- Docker Documentation
- Terraform Documentation
- AWS EC2 Documentation

## License
This project is licensed under the MIT License - see the LICENSE file for details.
