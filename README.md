# AI-Driven Cybersecurity Threat Prediction Platform

## 🔍 Project Overview

An AI-driven platform for autonomous cybersecurity threat prediction. AI agents monitor network traffic, detect anomalies, and respond to threats in real time, enhancing security posture and reducing human workload.

### Key Features

- Autonomous network traffic monitoring and anomaly detection
- AI-powered threat analysis using Google Gemini for files, URLs, QR codes, and images
- PCAP analysis for deep packet inspection
- VirusTotal integration for malware scanning
- Interactive dashboard for threat visualization
- Real-time streaming with WebSocket support
- Multi-format analysis support
- User authentication with Supabase

## 🛠 Tech Stack

### Backend
- Python 3.8+
- FastAPI
- Uvicorn
- Google Generative AI (Gemini)
- Scapy
- Pandas
- Supabase
- VirusTotal Python SDK
- psutil
- python-multipart
- python-dotenv

### Frontend
- React 19
- TypeScript
- Vite
- Tailwind CSS
- React Router
- Axios
- Supabase JS
- Framer Motion
- Recharts
- React Globe.GL
- React Markdown
- Lucide React
- JSQR

### Development Tools
- ESLint
- PostCSS
- Autoprefixer

## 📋 Prerequisites

- Python 3.8+
- Node.js 18+
- npm or yarn
- Git

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
- Windows: `venv\Scripts\activate`
- macOS/Linux: `source venv/bin/activate`

#### Install Dependencies
```bash
pip install -r requirements.txt
```

#### Environment Variables
Create a `.env` file in the `backend` directory:

```env
GEMINI_API_KEY=your_gemini_api_key_here
VIRUSTOTAL_API_KEY=your_virustotal_api_key_here
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
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

## 🏃‍♂️ Running Locally

### Option 1: Using Batch Script (Windows)

Run the provided `start.bat` file:

```bash
start.bat
```

This will start both backend and frontend servers in separate command windows.

### Option 2: Manual Startup

#### Start Backend
```bash
cd backend
venv\Scripts\activate  # On Windows
source venv/bin/activate  # On macOS/Linux

uvicorn src.main:app --host 0.0.0.0 --port 8000 --reload
```

#### Start Frontend
```bash
cd frontend
npm run dev
```

### Access the Application

- Frontend: http://localhost:5173
- Backend API: http://localhost:8000
- API Documentation: http://localhost:8000/docs

## 🔑 API Keys Configuration

### Google Gemini API Key
- Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
- Create a new API key
- Add to `backend/.env` as `GEMINI_API_KEY`

### VirusTotal API Key
- Visit [VirusTotal](https://www.virustotal.com/)
- Sign up for a free account
- Generate API key from profile settings
- Add to `backend/.env` as `VIRUSTOTAL_API_KEY`

### Supabase Configuration
- Visit [Supabase](https://supabase.com/)
- Create a new project
- Go to Settings > API
- Copy Project URL and anon/public key
- Add to both `backend/.env` and `frontend/.env`:
  - `SUPABASE_URL` and `SUPABASE_ANON_KEY` (backend)
  - `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` (frontend)

**Note**: App works in mock mode without keys.

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

## Demo Video

https://github.com/user-attachments/assets/5a20ce24-3f02-41bb-a629-49e7bedfc5c7


