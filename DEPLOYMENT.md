# 🚀 KTP Deployment Guide - Render

## **✅ Deploying Streamlit App on Render**

### **📋 What This Setup Does:**

1. **Runs Flask Backend** on port 5000 (internal)
2. **Runs Streamlit Frontend** on the main port (external)
3. **Both services run in the same container**
4. **Your Streamlit app works exactly the same!**

### **🔧 Files Created:**

- `render.yaml` - Render deployment configuration
- `app.py` - Main app that runs both Flask + Streamlit
- Updated `frontend/streamlit_app.py` - Uses environment variable for API URL

### **🚀 Deployment Steps:**

#### **1. Push to GitHub**
```bash
git add .
git commit -m "Add Render deployment configuration"
git push origin main
```

#### **2. Deploy on Render**
1. Go to [render.com](https://render.com)
2. Click "New +" → "Web Service"
3. Connect your GitHub repository
4. Render will automatically detect the `render.yaml` file
5. Set your environment variables:
   - `OPENAI_API_KEY`
   - `PINECONE_API_KEY`
   - `PINECONE_INDEX_NAME`
   - `GITHUB_TOKEN` (optional)
   - `NOTION_TOKEN` (optional)
   - `SLACK_BOT_TOKEN` (optional)

#### **3. Deploy**
- Click "Create Web Service"
- Render will build and deploy your app
- Your Streamlit app will be available at the provided URL

### **🌐 How It Works:**

```
User visits: https://your-app.onrender.com
           ↓
Streamlit serves the frontend
           ↓
Streamlit makes API calls to: http://localhost:5000
           ↓
Flask backend processes requests
           ↓
Returns data to Streamlit
```

### **✅ What You Get:**

- **Full Streamlit UI** - Exactly like your local version
- **All features working** - Search, Q&A, Integrations, Flashcards
- **Token management** - Secure storage on Render
- **Production ready** - Scalable and reliable

### **🔧 Environment Variables to Set:**

In Render dashboard, add these secrets:
- `OPENAI_API_KEY` - Your OpenAI API key
- `PINECONE_API_KEY` - Your Pinecone API key  
- `PINECONE_INDEX_NAME` - Your Pinecone index name
- `GITHUB_TOKEN` - GitHub personal access token (optional)
- `NOTION_TOKEN` - Notion integration token (optional)
- `SLACK_BOT_TOKEN` - Slack bot token (optional)

### **🎯 Benefits of This Approach:**

✅ **No HTML/CSS/JS needed** - Pure Streamlit  
✅ **Same UI/UX** - Identical to local version  
✅ **Full functionality** - All features work  
✅ **Production ready** - Scalable deployment  
✅ **Easy maintenance** - Single codebase  

### **🔄 Local Development:**

For local development, just run:
```bash
python run_ktp.py
```

This will start both Flask and Streamlit locally.

### **🚀 Production Deployment:**

The `app.py` file handles production deployment by:
1. Starting Flask backend on port 5000
2. Starting Streamlit frontend on the main port
3. Both services communicate internally

**Your Streamlit app will work exactly the same on Render as it does locally!** 🎉 