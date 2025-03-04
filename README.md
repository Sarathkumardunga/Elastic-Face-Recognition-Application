# Elastic Face Recognition Application

## Project Overview
A scalable cloud-based face recognition application built using AWS Infrastructure as a Service (IaaS) resources, demonstrating advanced cloud computing principles and distributed system design.

## Architecture
The application consists of three main components:
- **Web Tier**: Handles HTTP requests, image storage, and result communication
- **Application Tier**: Performs face recognition using a deep learning model
- **Autoscaling Controller**: Dynamically manages application tier instances

## Key Features
- Serverless-like scalable architecture using EC2 instances
- Automated instance scaling (0-15 instances)
- AWS services integration:
  - Amazon S3 for image storage
  - Amazon SQS for request/response queues
  - Amazon EC2 for computational resources

## Technical Specifications
- **Language**: Python
- **AWS Services**: 
  - EC2 (Elastic Compute Cloud)
  - S3 (Simple Storage Service)
  - SQS (Simple Queue Service)
- **Region**: US-East-1
- **Scaling Policy**:
  - Scale out: Dynamically create instances based on request load
  - Scale in: Reduce to 0 instances when no requests are pending

## Performance Metrics
- Processed 100 concurrent face recognition requests
- Total processing time: 96.12 seconds
- Scale-in time: 0.24 seconds
- 100% prediction accuracy

## Deployment Requirements
- AWS IAM user with specific permissions
- Python 3.x
- PyTorch for machine learning model inference

## Project Structure
```
project-root/
│
├── credentials/
│   └── credentials.txt
│
├── web-tier/
│   ├── server.py
│   └── controller.py
│
└── app-tier/
    └── backend.py
```

## Getting Started
1. Set up AWS IAM credentials
2. Configure AWS region to US-East-1
3. Install required Python packages
4. Deploy web and application tier scripts

## Limitations
- Free-tier AWS resources
- Maximum of 15 application tier instances
- Specific naming conventions for AWS resources

## Disclaimer
This project was developed as part of a Cloud Computing course at ASU, demonstrating practical implementation of distributed cloud applications.
