# AWS Serverless Architecture

![image](https://github.com/user-attachments/assets/443505c9-234d-4458-b8d4-d8a30500355e)

# Footballer Face Recognition – Serverless AI Project

An end-to-end serverless web application that identifies professional football players using facial recognition powered by **Amazon Rekognition**. Built with a modern frontend and deployed on a secure, scalable AWS architecture using **Lambda, S3, API Gateway, CloudFront, and Route 53**.

## 📸 Features

- Real-time footballer face recognition
- Secure HTTPS hosting via **CloudFront + Route 53**
- Ultra-fast, low-latency responses using **AWS Lambda**
- 90% threshold matching via **Amazon Rekognition**
- Hosted static frontend using **Amazon S3**
- Formspree integration for dataset suggestions
- Mobile-responsive UI with **TailwindCSS**
- Automatic HTTP to HTTPS redirection

---

## Architecture

**Tech Stack:**

| Component      | Technology                 |
|----------------|----------------------------|
| Frontend       | HTML, CSS, JS, TailwindCSS |
| Hosting        | Amazon S3 + CloudFront     |
| Backend Logic  | AWS Lambda (Python)        |
| API Gateway    | AWS API Gateway (REST)     |
| Image Matching | Amazon Rekognition         |
| Auth & Roles   | IAM                        |
| Suggestions    | Formspree.io               |
| Domain + HTTPS | Route 53 + CloudFront      |

---

## 🔁 Flow Overview

1. User uploads a footballer image via web form.
2. Image is encoded in Base64 and sent to API Gateway.
3. Lambda function decodes it and calls Rekognition's `search_faces_by_image`.
4. Player name is matched and returned to the frontend.
5. Users can also suggest new players via a Formspree-powered form.

