# 🤖 AI Multimodal Chatbot

> A modern AI-powered multimodal chatbot project designed for intelligent conversations across text, images, audio, documents, and web-search workflows.

## 📌 Overview

**AI Multimodal Chatbot** is a full-stack AI assistant concept built around a React/Vite frontend and a Python/FastAPI backend. The architecture is designed to support multiple AI capabilities through configurable providers and environment-based credentials.

### Core capabilities

- 💬 Text-based AI conversations
- 🖼️ Image/vision interaction
- 🎙️ Speech-to-text and audio workflows
- 📄 Document processing and RAG
- 🌐 Web-search integration
- 🧠 Configurable LLM provider
- ⚡ FastAPI REST backend
- 🎨 Modern React/Vite frontend
- 🔐 Environment-based secret management

## 🏗️ Intended Architecture

```text
┌──────────────────────────────┐
│       React / Vite UI        │
│  Chat • Files • Voice • UI   │
└──────────────┬───────────────┘
               │ HTTP / REST
               ▼
┌──────────────────────────────┐
│       FastAPI Backend        │
│ API • Auth • Uploads • RAG   │
└──────────────┬───────────────┘
               │
       ┌───────┼────────┐
       ▼       ▼        ▼
     LLM      RAG    Web Search
   Provider   Layer     Layer
       │
       ▼
  Gemini / OpenAI
```

## 🛠️ Technology Stack

| Layer | Technology |
|---|---|
| Frontend | React, Vite, JavaScript |
| UI Icons | Lucide React |
| Backend | Python, FastAPI |
| Configuration | Pydantic Settings |
| Database | PostgreSQL / SQLite fallback |
| AI | Gemini / OpenAI compatible provider configuration |
| RAG | Configurable chunking and top-k retrieval |
| API | REST |
| Development | Vite + Uvicorn |

## 📁 Repository Structure

```text
AI-Multimodal-Chatbot/
├── main.py
├── config.py
├── index.html
├── vite.config.js
├── package.json
├── package-lock.json
├── start.bat
├── .env.example
├── .gitignore
├── README.md
└── LICENSE
```

## ⚙️ Environment Configuration

Copy `.env.example` to `.env` and configure the values required by your environment.

Example:

```env
LLM_PROVIDER=gemini
LLM_API_KEY=your_api_key_here
DATABASE_URL=postgresql://postgres:postgres@localhost:5432/multimodal_chatbot
FRONTEND_URL=http://localhost:5173
```

### 🔐 Security

**Never commit real API keys or passwords to GitHub.**

The repository ignores:

```text
.env
.env.local
*.db
*.sqlite3
node_modules/
venv/
__pycache__/
dist/
```

## 🚀 Frontend Setup

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Build for production:

```bash
npm run build
```

Preview a production build:

```bash
npm run preview
```

## 🐍 Backend Setup

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install the backend dependencies from the project's backend dependency file when present, then start FastAPI with:

```bash
uvicorn app.main:app --reload
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

## ⚠️ Repository Integrity Note

This uploaded archive currently contains the project configuration files but **does not contain the referenced React `src/` directory or the referenced FastAPI `app/` package**. Files such as `main.py` and `start.bat` reference those modules.

Therefore, this GitHub package preserves the uploaded source exactly rather than inventing missing application code. To make the repository fully runnable, include the original `src/` and `app/` source directories and the backend dependency file from the complete project.

## 🔄 Application Flow

```text
User
  ↓
React Chat Interface
  ↓
FastAPI API
  ↓
AI / LLM Provider
  ├── Text Generation
  ├── Vision
  ├── Audio
  ├── Document Processing
  ├── RAG
  └── Web Search
  ↓
Processed Response
  ↓
React UI
```

## 🧪 Development Checklist

Before publishing a production deployment:

- [ ] Add the complete `frontend/src` source
- [ ] Add the complete FastAPI `app` package
- [ ] Add backend dependency requirements
- [ ] Configure production CORS
- [ ] Validate file-upload security
- [ ] Configure production database
- [ ] Add authentication if required
- [ ] Add automated tests
- [ ] Configure deployment secrets
- [ ] Never expose API keys in the repository

## 🚀 Future Enhancements

- User authentication and profiles
- Persistent conversation history
- Advanced RAG with vector database
- PDF and document citations
- Streaming AI responses
- Voice input/output
- Image understanding
- Cloud deployment
- Automated testing and CI/CD
- Usage monitoring and rate limiting

## 📄 License

This project is provided for educational and development purposes. See `LICENSE` for details.

---

### ⭐ Project Goal

The goal of this project is to demonstrate how modern generative AI, multimodal processing, retrieval-augmented generation, and full-stack web technologies can be combined to build an extensible AI assistant.
