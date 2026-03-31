# AWS Serverless Order Processing System

An event-driven, fully serverless application designed to handle high-traffic order submissions. This project explores the power of decoupling services using AWS Simple Queue Service (SQS) to ensure reliability and scalability.
check project on: https://lnkd.in/eEGAaSkf

## 🏗️ Architecture
The system follows a modern serverless pattern:
1. **Frontend**: Static website hosted on **Github**.
2. **API Layer**: **Amazon API Gateway** (REST API) acting as a proxy.
3. **Producer**: **AWS Lambda** receives the request and pushes order data into the queue.
4. **Queue**: **Amazon SQS** buffers orders to handle high volumes and prevent system overload.
5. **Consumer**: A secondary **AWS Lambda** function triggers off the queue to process the order.
6. **Database**: **Amazon DynamoDB** stores the final processed order records.

## 🚀 Features
- **Asynchronous Processing**: Immediate API response for better UX, with heavy lifting done in the background.
- **Auto-Scaling**: Every component scales automatically based on demand.
- **Pay-as-you-go**: Zero cost when the system is idle.
- **Fault Tolerance**: If the consumer Lambda fails, SQS retains the message for retries.

## 🛠️ Technologies Used
- **Compute**: AWS Lambda
- **API Management**: Amazon API Gateway
- **Messaging**: Amazon SQS (Simple Queue Service)
- **Storage**: Amazon S3 & Amazon DynamoDB
- **Automation**: Amazon EventBridge

## 📖 What I Learned
- Implementing **Event-Driven Architecture (EDA)**.
- Configuring Lambda triggers and IAM roles for secure cross-service communication.
- Managing asynchronous workflows to improve application performance.
