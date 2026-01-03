# AI-Driven Cybersecurity Threat Prediction Platform

## 🔍 Project Overview

This project develops an agentic AI system that acts as tireless guardians of network security. The AI agents autonomously monitor network traffic, detect anomalies, and respond to cyber threats in real time without constant human oversight. This approach significantly enhances an organization's security posture and frees up human experts to focus on more complex security challenges.

### Key Features

- **Autonomous Monitoring**: Real-time network traffic analysis and anomaly detection
- **AI-Powered Threat Detection**: Uses Google Gemini AI for intelligent threat analysis of files, URLs, QR codes, and images
- **PCAP Analysis**: Deep packet inspection for network security monitoring
- **VirusTotal Integration**: Leverages VirusTotal's extensive malware database for file and URL scanning
- **Interactive Dashboard**: Comprehensive web interface for threat visualization and management
- **Real-time Streaming**: Live network monitoring with WebSocket support
- **Multi-format Analysis**: Supports file uploads, URL scanning, QR code analysis, and image threat detection
- **User Authentication**: Secure login/signup system with Supabase backend

### Outcomes

- Autonomous monitoring of network traffic for enhanced security
- Real-time detection and response to cyber threats
- Reduction in the workload of human security experts
- Improved overall organizational resilience against digital threats

## 🛠 Tech Stack

### Backend
- **Python 3.8+**
- **FastAPI**: High-performance web framework for building APIs
- **Uvicorn**: ASGI server for running FastAPI applications
- **Google Generative AI (Gemini)**: AI-powered threat analysis

- **Pandas**: Data manipulation and analysis
- **Supabase**: Backend-as-a-Service for database and authentication
- **VirusTotal Python SDK**: Integration with VirusTotal API
- **psutil**: System and process utilities
- **python-multipart**: Handling multipart form data
- **python-dotenv**: Environment variable management

### Frontend
- **React 19**: Modern JavaScript library for building user interfaces
- **TypeScript**: Typed superset of JavaScript
- **Vite**: Fast build tool and development server
- **Tailwind CSS**: Utility-first CSS framework
- **React Router**: Declarative routing for React
- **Axios**: HTTP client for API requests
- **Supabase JS**: Client library for Supabase
- **Framer Motion**: Animation library for React
- **Recharts**: Composable charting library
- **React Globe.GL**: 3D globe visualization
- **React Markdown**: Markdown rendering


### Development Tools
- **ESLint**: Code linting
- **PostCSS**: CSS processing
- **Autoprefixer**: CSS vendor prefixing

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Python 3.8 or higher**
- **Node.js 18 or higher**
- **npm or yarn**
- **Git**

## 🚀 Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd AI-Driven-Cybersecurity-Threat-Prediction-Platform-main
```

### 2. Backend Setup

#### Create Virtual Environment
```bash
cd backend
python -m venv venv
```

#### Activate Virtual Environment
- **Windows:**
  ```bash
  venv\Scripts\activate
  ```
- **macOS/Linux:**
  ```bash
  source venv/bin/activate
  ```

#### Install Dependencies
```bash
pip install -r requirements.txt
```

#### Environment Variables
Create a `.env` file in the `backend` directory and add the following API keys:

```env
# Google Gemini AI API Key
GEMINI_API_KEY=your_gemini_api_key_here

# VirusTotal API Key
VIRUSTOTAL_API_KEY=your_virustotal_api_key_here

# Supabase Configuration
SUPABASE_URL=your_supabase_project_url
SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 3. Frontend Setup

```bash
cd ../frontend
npm install
```

#### Environment Variables
Create a `.env` file in the `frontend` directory:

```env
# Supabase Configuration for Frontend
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

## 🏃‍♂️ Running Locally

### Option 1: Using the Batch Script (Windows)

Simply run the provided `start.bat` file:

```bash
start.bat
```

This will start both backend and frontend servers in separate command windows.

### Option 2: Manual Startup

`

#### Start Frontend
```bash
cd frontend
npm run dev
```

### Access the Application

- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs (FastAPI Swagger UI)

## 🔑 API Keys Configuration

This application requires several API keys for full functionality. Here's how to obtain and configure them:

### 1. Google Gemini API Key
- Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
- Create a new API key
- Add it to your `backend/.env` file as `GEMINI_API_KEY`

### 2. VirusTotal API Key
- Visit [VirusTotal](https://www.virustotal.com/)
- Sign up for a free account
- Go to your profile settings and generate an API key
- Add it to your `backend/.env` file as `VIRUSTOTAL_API_KEY`

### 3. Supabase Configuration
- Visit [Supabase](https://supabase.com/)
- Create a new project
- Go to Settings > API
- Copy the Project URL and anon/public key
- Add them to both `backend/.env` and `frontend/.env` files:
  - `SUPABASE_URL`
  - `SUPABASE_ANON_KEY` (for backend)
  - `VITE_SUPABASE_URL` (for frontend)
  - `VITE_SUPABASE_ANON_KEY` (for frontend)

**Note**: Without these API keys, some features will work in mock mode or be limited. The application will gracefully handle missing keys and provide appropriate fallbacks.

## 📁 Project Structure

```
AI-Driven-Cybersecurity-Threat-Prediction-Platform-main/
├── backend/
│   ├── requirements.txt
│   ├── schema.sql
│   └── src/
│       ├── main.py
│       ├── auth.py
│       ├── routers/
│       │   ├── dashboard.py
│       │   ├── analysis.py
│       │   └── chat.py
│       └── services/
│           ├── ai_service.py
│           ├── pcap_service.py
│           ├── storage_service.py
│           ├── system_service.py
│           └── virustotal_service.py
├── frontend/
│   ├── package.json
│   ├── vite.config.ts
│   ├── tailwind.config.js
│   └── src/
│       ├── components/
│       ├── pages/
│       ├── context/
│       └── lib/
├── start.bat
├── README.md
└── .gitignore
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

If you encounter any issues or have questions, please open an issue on GitHub.

## 🔄 Future Enhancements

- Machine learning model integration for advanced threat prediction
- Integration with additional threat intelligence feeds
- Automated incident response capabilities
- Mobile application development
- Advanced reporting and analytics features
