# An Intelligent Enterprise Assistant for public sector (SIH 1706)
Completion requirements

AI Employee Assistance Chatbot for Public Sector Organizations
Overview

AI Employee Assistance Chatbot is an intelligent enterprise chatbot developed using Deep Learning, Natural Language Processing (NLP), and Retrieval-Augmented Generation (RAG) techniques to assist employees in large public sector organizations. The system is designed to understand and respond to organizational queries related to Human Resources, IT support, company events, and other internal services.

The chatbot also includes document analysis capabilities such as text extraction, summarization, and keyword identification from uploaded files. Security features including Email-based Two Factor Authentication (2FA) and profanity filtering are integrated to improve reliability and user safety.

The application is optimized for scalability and can support multiple users simultaneously while maintaining a response time below five seconds.

Problem Statement

Employees in large organizations often struggle to quickly access information related to policies, technical support, organizational announcements, and internal documentation. Traditional support systems may involve manual intervention and delayed responses.

This project aims to provide an AI-driven virtual assistant capable of:

Understanding employee queries
Retrieving relevant information instantly
Processing uploaded documents
Supporting secure authentication
Filtering inappropriate language
Handling concurrent users efficiently
Features
Intelligent Query Handling

The chatbot supports various organizational domains:

HR policies
Leave management
IT support services
Company events
Frequently asked questions
General employee assistance
NLP-Based Intent Understanding

Uses Deep Learning models for:

Intent Classification
Entity Recognition
Context Understanding
Response Generation

Example:

User: How many casual leaves are available?

Bot: Employees are entitled to 12 casual leaves annually according to HR policy.

Document Processing Module

Employees can upload:

PDF files
DOCX files
Images

The chatbot performs:

Text Extraction

Extracts text from uploaded documents using OCR and document parsers.

Document Summarization

Generates concise summaries of lengthy documents.

Keyword Extraction

Identifies important terms and topics.

Example:

Document:

8-page HR handbook

Output:

Summary:
Employees receive annual leave benefits and reimbursement support.

Keywords:

Leave Policy
Attendance
Reimbursement
Employee Benefits
Retrieval-Augmented Generation (RAG)

Instead of relying solely on pre-trained responses, the system retrieves relevant organizational content from a knowledge base and generates context-aware responses.

Workflow:

User Query
↓
Convert to embeddings
↓
Search vector database
↓
Retrieve relevant content
↓
Generate accurate response

Email-Based Two Factor Authentication (2FA)

For enhanced security:

User logs in
OTP generated
OTP sent to registered email
Verification performed
Access granted
Profanity Filtering

The chatbot automatically detects and filters abusive or inappropriate language using a maintained dictionary and profanity detection techniques.

Example:

User:

"You are stupid"

Bot:

"Please maintain respectful communication."

Multi-user Scalability

The chatbot architecture supports:

Minimum 5 simultaneous users
Fast API-based asynchronous processing
Response time under 5 seconds
Concurrent request handling
Technology Stack
Frontend
ReactJS / Streamlit
Backend
FastAPI
Database
MongoDB
NLP Models
BERT
DistilBERT
Sentence Transformers
Document Processing
PyPDF2
Tesseract OCR
KeyBERT
BART Summarizer
Security
JWT Authentication
Email OTP Verification
Deployment
Docker
Uvicorn
Gunicorn
System Architecture
User
   ↓
Frontend Interface
   ↓
Authentication + Email OTP
   ↓
API Layer
   ↓
Chatbot Engine
      ├─ Intent Classification
      ├─ NLP Processing
      ├─ Profanity Filter
      ├─ Context Manager
      └─ Response Generator
   ↓
Knowledge Base + Vector Database
   ↓
Document Processing Module
      ├─ OCR
      ├─ Summarizer
      └─ Keyword Extraction
   ↓
Database
Project Structure
project/
│
├── frontend/
│
├── backend/
│   ├── chatbot.py
│   ├── auth.py
│   ├── summarizer.py
│   ├── keyword_extractor.py
│   ├── ocr.py
│   ├── profanity_filter.py
│
├── models/
│
├── data/
│    ├── hr_documents/
│    ├── it_support_docs/
│
├── database/
│
└── requirements.txt
Future Enhancements
Voice-enabled interaction
Multilingual support
Mobile application integration
Advanced analytics dashboard
Personalized employee recommendations
Conclusion

The AI Employee Assistance Chatbot demonstrates how Deep Learning and NLP can improve organizational efficiency by providing instant access to information, automating support processes, and enhancing user experience. The project combines conversational AI, document intelligence, authentication, and scalable architecture into a unified solution suitable for public sector organizations.
