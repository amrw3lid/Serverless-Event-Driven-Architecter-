# 🚀 Serverless Event-Driven Architecture on AWS

A fully automated, scalable serverless pipeline built on Amazon Web Services (AWS) that processes uploaded files, stores metadata, and triggers real-time cloud notifications.

---

## 🏗️ Architecture Diagram

![Serverless Architecture](images/serverless_architecture.png)

---

## 🔄 How It Works (The Pipeline)

1. **Trigger:** A user uploads a file to an **Amazon S3** bucket.
2. **Event Notification:** The S3 bucket automatically triggers an **AWS Lambda** function upon object creation.
3. **Processing & Storage:** The Lambda function (Python) processes the file event and securely writes the metadata into an **Amazon DynamoDB** table.
4. **Alerting & Notifications:** If an alert or success notification is required, **Amazon SNS** dispatches an instant message to the destination inbox.
5. **Observability:** **Amazon CloudWatch** tracks execution logs, performance metrics, and catches runtime exceptions for troubleshooting.

---

## 🛠️ Tech Stack & Services Used

* **Compute:** AWS Lambda (Serverless Python execution)
* **Storage:** Amazon S3 (Object storage & event source)
* **Database:** Amazon DynamoDB (NoSQL metadata store)
* **Integration & Messaging:** Amazon SNS (Simple Notification Service)
* **Monitoring & Management:** Amazon CloudWatch (Logs, metrics, and alarms)
* **Security & Access Control:** IAM (Least-privilege execution roles)

---

## 🧪 Troubleshooting & Hands-on Learning

During the deployment of this pipeline, I actively monitored **CloudWatch Logs** to diagnose and resolve a Python syntax error in the Lambda execution handler, ensuring robust error handling and reliable event triggers.

---

## 👨‍💻 Author
**Amr Walid**  
*Cloud Computing / CloudOps Enthusiast*
