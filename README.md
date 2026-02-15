# Sahayak – AI Powered Scheme Navigator for Bharat

## 📌 Overview

Sahayak is an AI-powered conversational platform designed to bridge the accessibility gap between government welfare schemes and eligible citizens in Bharat.

Despite thousands of welfare programs available across India, millions of rural and semi-urban citizens remain unaware of benefits due to:

- Complex government portals
- Language barriers
- Lack of personalization
- Low digital literacy
- Absence of guided assistance

Sahayak simplifies scheme discovery through profile-based eligibility matching and AI-driven conversational guidance.

## 🎯 Problem Statement

**Government schemes exist. Access does not.**

Eligible citizens often struggle to discover, understand, and apply for welfare programs due to non-intuitive systems and information overload.

Sahayak aims to convert complex government data into simple, personalized, and actionable guidance.

## 💡 Solution

Sahayak is a scalable, cloud-native system that:

- Collects user profile information
- Evaluates eligibility using rule-based logic
- Recommends personalized schemes
- Simplifies scheme details using AI
- Generates document checklists
- Provides step-by-step application guidance
- Supports multilingual interaction

The system is optimized for low-bandwidth environments and scalable AWS deployment.

## 🏗 System Architecture

Sahayak follows a three-tier architecture:

**Frontend:**
- React (Web Interface)
- Hosted on AWS S3 + CloudFront

**Backend:**
- Node.js / Express
- Stateless APIs
- Deployed on ECS Fargate

**Database & Cache:**
- PostgreSQL (AWS RDS)
- Redis (ElastiCache)

**AI & Language Services:**
- AWS Bedrock / OpenAI (Conversational AI)
- AWS Translate (Multilingual support)

## 🧠 Core Components

- **Eligibility Evaluator** (Rule-based deterministic engine)
- **Recommendation Engine** (Weighted ranking model)
- **AI Conversational Interface**
- **Document Checklist Generator**
- **Application Guide Generator**
- **Multilingual Support Layer**
- **Secure Session Management**

## 🔐 Security & Privacy

- HTTPS (TLS 1.3) encryption
- Encrypted data at rest (AES-256)
- Session-based data handling
- No long-term PII storage in MVP
- Role-based access controls
- API rate limiting

## 📈 Scalability

Designed for horizontal scalability:

- Stateless backend containers
- Auto-scaling policies
- CDN-based frontend delivery
- Database read replicas
- Redis caching

Supports scaling from hundreds to thousands of concurrent users.

## 🌍 Impact

Sahayak enables:

- Increased awareness of welfare schemes
- Reduced dependency on middlemen
- Improved accessibility for rural citizens
- Simplified eligibility understanding
- Better reach of government benefits

**AI for Bharat** — focused on real community impact.

## 📄 Documentation

- 📘 [Requirements Document](.kiro/specs/sahayak-ai-scheme-navigator/requirements.md)
- 🏗 [Design Document](.kiro/specs/sahayak-ai-scheme-navigator/design.md)

## 🔮 Future Scope

- WhatsApp integration
- Voice-based interaction
- Aadhaar-based verification
- Direct government portal integration
- Offline-first mobile app

## 👥 Team

**Team Name:** Innovators_INC
**Team Leader:** Pranav Ahire

**Hack2Skill – AWS AI for Bharat Hackathon 2026**
