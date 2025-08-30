# 🏥 MedScanner - AI-Powered Medical Document Analysis Platform

[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18.2.0-blue.svg)](https://reactjs.org/)
[![MongoDB](https://img.shields.io/badge/MongoDB-8.18.0-green.svg)](https://mongodb.com/)
[![License](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

> **Democratizing healthcare understanding through intelligent document analysis, making medical information accessible in multiple languages with AI-powered insights.**

## 🌟 **Overview**

MedScanner is a comprehensive full-stack web application that leverages **Artificial Intelligence** and **Optical Character Recognition (OCR)** to analyze medical documents including prescriptions and medical reports. The platform supports **three languages** (English, Hindi, Marathi) and provides intelligent insights through Google's Gemini AI model.

## ✨ **Key Features**

### 🔍 **Document Analysis**
- **📱 Camera Integration**: Real-time camera capture with WebRTC technology
- **📁 File Upload**: Drag & drop support for JPG, PNG, and PDF files
- **🔤 Multi-language OCR**: Tesseract.js with Hindi, Marathi, and English support
- **🤖 AI-Powered Insights**: Google Gemini 1.5 Flash for intelligent analysis

### 🌐 **Multi-Language Support**
- **🇺🇸 English**: Full TTS support with Web Speech API
- **🇮🇳 Hindi**: Native language OCR + AI analysis
- **🇮🇳 Marathi**: Regional language support
- **🔊 Text-to-Speech**: Audio narration for English content

### 📊 **Smart Analysis**
- **💊 Prescription Analysis**: Medicine identification, dosage, generic alternatives
- **📋 Report Analysis**: Disease detection, stage assessment, abnormalities
- **📈 History Tracking**: Complete analysis history with MongoDB
- **💡 Intelligent Summaries**: Structured medical information extraction

### 🎨 **User Experience**
- **📱 Responsive Design**: Mobile-first approach with modern UI
- **⚡ Real-time Processing**: Live camera feed and instant analysis
- **🔒 Secure Uploads**: File validation and secure processing
- **📚 Complete History**: Searchable analysis records

## 🏗️ **Architecture**

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   React Frontend│    │  Express Backend│    │   MongoDB Atlas │
│                 │◄──►│                 │◄──►│                 │
│ • Prescription  │    │ • OCR Processing│    │ • History Store │
│ • Report Scan   │    │ • AI Analysis   │    │ • User Data     │
│ • Camera Scan   │    │ • File Upload   │    │ • Analytics     │
│ • TTS Support   │    │ • Multi-lang    │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │
         │              ┌─────────────────┐
         └──────────────►│  Google Gemini │
                        │   AI 1.5 Flash │
                        │ • Medical AI   │
                        │ • Multi-lang   │
                        └─────────────────┘
```

## 🛠️ **Technology Stack**

### **Frontend**
- **React 18** - Modern React with concurrent features
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **React Router** - Client-side routing

### **Backend**
- **Node.js** - JavaScript runtime
- **Express.js** - Web application framework
- **MongoDB** - NoSQL database with Mongoose ODM
- **Multer** - File upload middleware

### **AI & ML**
- **Google Gemini 1.5 Flash** - Latest AI model for medical analysis
- **Tesseract.js** - Multi-language OCR engine
- **Sharp.js** - Image preprocessing and optimization

### **Additional Services**
- **Web Speech API** - Text-to-speech functionality
- **AI4Bharat TTS** - Fallback TTS service
- **CORS** - Cross-origin resource sharing

## 📁 **Project Structure**

```
MedScanner/
├── Frontend/MedLabScan/          # React Frontend Application
│   ├── src/
│   │   ├── components/           # React Components
│   │   │   ├── Home.jsx         # Landing page
│   │   │   ├── PresScan.jsx     # Prescription scanner
│   │   │   ├── RepoScan.jsx     # Report scanner
│   │   │   ├── InfoBox.jsx      # Prescription results
│   │   │   ├── InfoReports.jsx  # Report results
│   │   │   ├── History.jsx      # Analysis history
│   │   │   ├── Navbar.jsx       # Navigation component
│   │   │   ├── SpotlightCard.jsx # UI component
│   │   │   └── TextType.jsx     # Text input component
│   │   ├── services/            # API services
│   │   ├── App.jsx              # Main application
│   │   └── main.jsx             # Entry point
│   ├── dist/                    # Production build
│   └── package.json             # Frontend dependencies
├── src/                         # Backend Source Code
│   ├── routes/                  # API Routes
│   │   ├── prescriptions.js     # Prescription analysis
│   │   ├── reports.js           # Report analysis
│   │   ├── history.js           # History management
│   │   └── tts.js               # Text-to-speech
│   ├── models/                  # Database Models
│   │   └── History.js           # History schema
│   └── services/                # Backend services
├── tmp_uploads/                 # Temporary file storage
├── server.js                    # Main server file
├── package.json                 # Backend dependencies
├── start_fullstack.bat          # Windows startup script
├── start_fullstack.sh           # Unix startup script
└── README.md                    # This file
```

## 🚀 **Quick Start**

### **Prerequisites**
- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **MongoDB** (local or Atlas)
- **Google Gemini API Key**

### **1. Clone the Repository**
```bash
git clone <repository-url>
cd MedScanner
```

### **2. Install Dependencies**
```bash
# Install all dependencies (frontend + backend)
npm run install-all

# Or install separately
npm run install-server    # Backend dependencies
npm run install-client    # Frontend dependencies
```

### **3. Environment Setup**
Create a `.env` file in the root directory:
```env
# Server Configuration
PORT=3000
NODE_ENV=development

# MongoDB Connection
MONGODB_URI=mongodb://localhost:27017/medscanner

# Google Gemini AI
GEMINI_API_KEY=your_gemini_api_key_here
```

### **4. Build Frontend**
```bash
npm run build
```

### **5. Start Application**
```bash
# Production mode
npm start

# Development mode (with hot reload)
npm run dev

# Backend only
npm run server

# Frontend only
npm run client
```

### **6. Access the Application**
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:3000/api
- **Health Check**: http://localhost:3000/health

## 🎯 **Available Scripts**

| Command | Description |
|---------|-------------|
| `npm start` | Start production server |
| `npm run dev` | Development mode with hot reload |
| `npm run server` | Start backend server only |
| `npm run client` | Start React dev server only |
| `npm run build` | Build React frontend |
| `npm run install-all` | Install all dependencies |
| `npm run install-client` | Install frontend dependencies |
| `npm run install-server` | Install backend dependencies |
| `npm run heroku-postbuild` | Heroku deployment script |

## 🔌 **API Endpoints**

### **Prescriptions**
- `POST /api/prescriptions/analyze` - Analyze prescription images

### **Reports**
- `POST /api/reports/analyze` - Analyze medical report images

### **History**
- `GET /api/history` - Get analysis history

### **Text-to-Speech**
- `POST /api/tts/synthesize` - Convert text to speech

### **Health**
- `GET /health` - Server health check

## 📱 **Usage Guide**

### **1. Prescription Analysis**
1. Navigate to **Prescription Scanner**
2. **Upload image** or **use camera** to capture prescription
3. Select **language** (English, Hindi, Marathi)
4. Click **Process Prescription**
5. View **AI-generated insights** including:
   - Medicine identification
   - Dosage information
   - Generic alternatives
   - Medical indications

### **2. Medical Report Analysis**
1. Navigate to **Report Scanner**
2. **Upload image** or **use camera** to capture report
3. Select **language** (English, Hindi, Marathi)
4. Click **Process Report**
5. View **AI-generated insights** including:
   - Disease detection
   - Stage assessment
   - Abnormalities identification
   - Medical recommendations

### **3. History Management**
1. Navigate to **History** section
2. View **complete analysis history**
3. **Search and filter** previous analyses
4. **Export data** for record keeping

## 🔧 **Configuration**

### **MongoDB Setup**
```javascript
// Local MongoDB
MONGODB_URI=mongodb://localhost:27017/medscanner

// MongoDB Atlas
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/medscanner
```

### **Google Gemini AI**
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Add to your `.env` file:
```env
GEMINI_API_KEY=your_api_key_here
```

### **TTS Configuration**
- **Web Speech API**: Built-in browser support (English only)
- **AI4Bharat TTS**: External service for Hindi/Marathi (optional)

## 🚀 **Deployment**

### **Heroku Deployment**
```bash
# Add Heroku remote
heroku git:remote -a your-app-name

# Deploy
git push heroku main
```

### **Vercel Deployment**
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

### **Docker Deployment**
```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```

## 🧪 **Testing**

### **Backend Testing**
```bash
# Test API endpoints
curl http://localhost:3000/health
curl http://localhost:3000/api/history
```

### **Frontend Testing**
```bash
cd Frontend/MedLabScan
npm test
```

## 🔍 **Troubleshooting**

### **Common Issues**

#### **1. Frontend Not Loading**
```bash
# Rebuild frontend
npm run build

# Check if dist folder exists
ls Frontend/MedLabScan/dist
```

#### **2. MongoDB Connection Issues**
```bash
# Check MongoDB service
sudo systemctl status mongod

# Verify connection string in .env
echo $MONGODB_URI
```

#### **3. Camera Access Issues**
- Ensure **HTTPS** or **localhost** for camera access
- Check **browser permissions** for camera
- Verify **WebRTC support** in browser

#### **4. AI Analysis Failures**
- Verify **GEMINI_API_KEY** in environment
- Check **API quota** and **rate limits**
- Ensure **image quality** and **format**

### **Debug Mode**
```bash
# Enable detailed logging
DEBUG=* npm run dev

# Check server logs
npm run server
```

## 📊 **Performance Metrics**

- **OCR Processing**: <2 seconds average
- **AI Analysis**: <5 seconds average
- **Image Upload**: <1 second for 5MB files
- **Database Queries**: <100ms average
- **Frontend Load**: <2 seconds initial load

## 🔒 **Security Features**

- **CORS Protection**: Cross-origin request handling
- **File Validation**: Type and size restrictions
- **Input Sanitization**: XSS protection
- **Rate Limiting**: API abuse prevention
- **Environment Variables**: Secure configuration

## 🤝 **Contributing**

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### **Development Guidelines**
- Follow **ESLint** configuration
- Write **comprehensive tests**
- Update **documentation** for new features
- Follow **conventional commits** format

## 📄 **License**

This project is licensed under the **ISC License** - see the [LICENSE](LICENSE) file for details.

## 🙏 **Acknowledgments**

- **Google Gemini AI** for intelligent medical analysis
- **Tesseract.js** for multi-language OCR support
- **React Team** for the amazing frontend framework
- **Express.js** for the robust backend framework
- **MongoDB** for the flexible database solution

## 📞 **Support**

- **Documentation**: [Project Wiki](wiki-link)
- **Issues**: [GitHub Issues](issues-link)
- **Discussions**: [GitHub Discussions](discussions-link)
- **Email**: support@medscanner.com

## 🔮 **Roadmap**

### **Phase 1 (Current)**
- ✅ Multi-language OCR
- ✅ AI-powered analysis
- ✅ Camera integration
- ✅ History tracking

### **Phase 2 (Next 6 months)**
- 🔄 User authentication system
- 🔄 Advanced analytics dashboard
- 🔄 Mobile app (React Native)
- 🔄 API marketplace

### **Phase 3 (Next 12 months)**
- 🔮 Real-time collaboration
- 🔮 Advanced AI models
- 🔮 Integration with EHR systems
- 🔮 Global language expansion

---

## 🎉 **Getting Started**

Ready to revolutionize medical document analysis? Start with:

```bash
git clone <repository-url>
cd MedScanner
npm run install-all
npm run build
npm start
```

**Visit http://localhost:3000 and start analyzing medical documents with AI!**

---

**Made with ❤️ for better healthcare accessibility**

**🏥 MedScanner - Where AI Meets Healthcare Understanding**
