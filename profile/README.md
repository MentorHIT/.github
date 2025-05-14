# 🎓 MentorHIT – AI-Based Academic and Career Advisor for HIT Students

MentorHIT is the AI mentor every student wishes they had. Built for the Holon Institute of Technology (HIT), MentorHIT helps students plan their academic journey and professional path based on real data, not guesswork.

---

## ❗ Problem Statement

Academic students often face challenges such as:

- Choosing elective courses that align with their academic strengths and career aspirations
- Finding relevant job opportunities during or after their studies
- Receiving only generic advice from traditional counseling services

Even with available tools like advisors, forums, and job boards, students:

- Struggle to personalize the information they receive
- Avoid bureaucratic or uncomfortable advisory conversations
- Miss out on critical opportunities because no one highlighted them in time

---

## 🔍 Understanding Students’ Needs

At HIT, students frequently ask themselves:

- Which courses will truly move me forward?
- What specialization is right for me?
- How can I translate my skills into a real-world job?
- How do I plan a career—not just complete a degree?

---

## 📊 Research-Based Justification

A study by the **Strada Education Network** found that:

- Only **1 in 5 students** receives quality career guidance during their studies
- **69%** of those who did were employed in jobs requiring a degree
- **87%** reported it improved their personal well-being
- **73%** said it helped them reach their goals

This highlights a large gap between the need for guidance and the resources currently available.

---

## 💡 The Solution: MentorHIT

MentorHIT is an AI-powered chatbot that offers:

- 🎯 Course recommendations based on interests, academic performance, and schedules
- 💼 Personalized job and career path suggestions using real-time data
- 🔄 Help with common dilemmas like "which course should I take first?" or "how do I specialize?"
- 🧠 A learning system that improves over time with consistent context-aware advice

MentorHIT doesn’t just save time, it helps students understand themselves and plan their future with confidence.

---

## 🎯 Project Goal

Provide intelligent, personalized recommendations to academic students through:

- **Course Selection Guidance:** Suggesting electives based on performance, interests, and course trends
- **Career Support:** Recommending job roles aligned with student competencies and job market data

---

## 👤 Target Users

- Undergraduate students at any point in their academic journey
- Graduated students exploring next steps

---

## 🔑 Key Features

- Personalized course recommendation engine
- Career/job suggestion module
- LLM-based conversational chat interface
- Data ingestion pipeline for academic records and job listings
- Secure login and student authentication

---

## 🧭 User Flow

1. Student logs in with their HIT email
2. Asks questions via chat (e.g., "I enjoy understanding how things work behind the scenes and prefer logic over design – which HIT courses should I take to build on that?"
3. The system queries academic/job data via APIs
4. The student receives personalized course or career recommendations
5. Optionally, receives notifications on relevant job openings

---

## 🏗️ System Architecture (High-Level)

All services are hosted on AWS and designed for scalability and security.

### 🌐 Frontend
- React Web App with conversational Chat UI

### 🤖 LLM Integration
- Amazon Bedrock using **Jamba model** (AI21 Labs) 

### 🔧 Backend API
- AWS Lambda + API Gateway

### 🗃️ Data Storage
- Amazon RDS (PostgreSQL) – structured student data
- Amazon DynamoDB – chat session history
- Amazon S3 – static assets and files

### 🔄 ETL / Data Pipelines
- AWS Glue for CSV/JSON transformation
- Scheduled via Amazon EventBridge

### 🧠 ML Model Hosting
- Amazon SageMaker for course/career recommendation models

### 🕸️ Job Scraper (Optional)
- AWS Lambda with Puppeteer (headless Chromium)
- Or AWS DataBrew (if LinkedIn API is not accessible)

### 📈 Monitoring (Optional)
- Amazon CloudWatch

---

## 🛠️ Tech Stack Summary

| Layer               | Technology Used                                    |
|--------------------|----------------------------------------------------|
| Frontend            | React + Chat UI                                   |
| LLM/AI              | Amazon Bedrock (Jamba model by AI21 Labs)         |
| Authentication      | Amazon Cognito                                    |
| Backend API         | AWS Lambda + API Gateway                          |
| Databases           | Amazon RDS (PostgreSQL), DynamoDB                 |
| File Storage        | Amazon S3                                         |
| ETL/Data Pipeline   | AWS Glue + EventBridge                            |
| ML Hosting          | Amazon SageMaker                                  |
| Job Data Source     | LinkedIn API / AWS Lambda Scraper                 |
| Monitoring          | (Optional) Amazon CloudWatch                      |
| CI/CD               | (Optional) AWS CodePipeline + CodeBuild           |

## 👥 Team

- **Lior Lichensky** (M.Sc.)
- **Daniel Podolsky** (B.Sc.)
- **Dvir Uliel** (B.Sc.)
- **Noy Klar** (B.Sc.)

---

## 🔐 Ethics & Compliance

MentorHIT adheres to HIT's ethical standards and Israeli data protection laws. Student data is processed securely and used strictly for the purpose of delivering academic and career recommendations.

> MentorHIT is a student-built solution to empower academic success and career clarity – personalized, smart, and built with ❤️ for HIT.
