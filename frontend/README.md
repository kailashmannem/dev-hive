# KTP - Streamlit Frontend

A modern, interactive web interface for the Knowledge Transfer Platform built with Streamlit.

## Features

- 🏠 **Dashboard** - Overview of system status and quick actions
- 📚 **Knowledge Base** - Upload and manage content
- 🔍 **Search** - Search through your knowledge base
- ❓ **Q&A** - Ask questions and get AI-powered answers
- 🔗 **Integrations** - Connect GitHub, Notion, and Slack
- 📊 **Statistics** - View analytics and insights

## Quick Start

### Option 1: Use the startup script (Recommended)
```bash
# From the project root directory
python run_ktp.py
```

### Option 2: Run manually
```bash
# Terminal 1: Start Flask backend
cd server
python app.py

# Terminal 2: Start Streamlit frontend
cd frontend
streamlit run streamlit_app.py
```

## Access the Application

- **Frontend UI**: http://localhost:8501
- **Backend API**: http://localhost:5000

## Requirements

- Python 3.8+
- Streamlit
- Flask backend running on localhost:5000

## Installation

```bash
pip install streamlit
```

## Usage

1. **Dashboard**: Check system status and access quick actions
2. **Knowledge Base**: Upload text or files to your knowledge base
3. **Search**: Find relevant information using semantic search
4. **Q&A**: Ask questions and get AI-powered answers with sources
5. **Integrations**: Connect external data sources (GitHub, Notion, Slack)
6. **Statistics**: View analytics about your knowledge base

## Configuration

The frontend automatically connects to the Flask backend at `http://localhost:5000`. Make sure the backend is running before using the frontend.

## Features

### 🚀 One-Click Integration
Integrate all available data sources with a single click, including automatic deduplication.

### 📊 Real-time Statistics
View live statistics about your knowledge base, including vector counts and source breakdowns.

### 🔍 Advanced Search
Search through your knowledge base with semantic understanding and filtering options.

### ❓ AI-Powered Q&A
Ask questions and get intelligent answers based on your knowledge base content.

### 📤 Easy Upload
Upload text content or files directly through the web interface.

## Troubleshooting

- **Connection Error**: Make sure the Flask backend is running on port 5000
- **Import Error**: Install required dependencies with `pip install streamlit`
- **Port Conflict**: Change the port in the startup command if 8501 is in use

## Development

The frontend is built with Streamlit and communicates with the Flask backend via REST API calls. All API functions are defined in the main script for easy maintenance. 