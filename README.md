# 🏥 MedScanner - AI-Powered Medical Document Analysis Platform  

> **Hackathon Project – Built to make healthcare information more accessible using AI.**  

## 🌟 Overview  
MedScanner was developed as a **hackathon project**. It is a medical document analysis platform that uses **AI** and **OCR** to analyze prescriptions and medical reports, providing intelligent insights in multiple languages (English, Hindi, Marathi).  

I contributed as a **backend developer**, building the server-side logic, database integration, and AI-powered analysis pipeline.  

## 🛠️ Backend Tech Stack  
- **Node.js** – JavaScript runtime  
- **Express.js** – Web framework for APIs  
- **MongoDB** – Database for storing analysis history  
- **Multer** – File upload handling  
- **Tesseract.js** – OCR engine for text extraction  
- **Google Gemini 1.5 Flash** – AI model for intelligent analysis  
- **Sharp.js** – Image preprocessing  

## 🚀 Key Backend Features  
- 📁 **File Upload & Validation** (images, PDFs)  
- 🔤 **OCR Processing** (English, Hindi, Marathi)  
- 🤖 **AI Integration** with Google Gemini for insights  
- 📊 **History Management** with MongoDB  
- 🔊 **Text-to-Speech API** for English & regional languages  
- 🔒 **Secure API Endpoints** with input validation  

## 🔌 API Endpoints  
- `POST /api/prescriptions/analyze` – Analyze prescription images  
- `POST /api/reports/analyze` – Analyze medical report images  
- `GET /api/history` – Fetch analysis history  
- `POST /api/tts/synthesize` – Text-to-speech conversion  
- `GET /health` – Health check  

## 📄 Note  
This project was built as part of a **hackathon**, where I focused on **backend development** while my teammates handled the frontend and UI.  
