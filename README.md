<p align="center">
  <img src="assets/banner.png" alt="JARVIS Banner" width="50%">
</p>

Jarvis - Multi-Purpose AI Agent

JARVIS is a local AI assistant inspired by Iron Man’s iconic assistant. Built with a modern web interface, real-time streaming responses, voice interaction, and desktop automation capabilities, JARVIS runs entirely on your own machine — keeping your data private while giving you a powerful AI companion.

Features -:
AI-Powered Conversations
Runs fully locally using Ollama + Gemma models
Real-time streaming responses (ChatGPT-like typing)
Conversation memory support
Fast and lightweight local inference

Voice Interaction:
Voice input using browser speech recognition
Jarvis can speak responses back to the user
Hands-free interaction support

Modern Futuristic UI:
Beautiful Iron Man inspired interface
Animated glowing effects & glassmorphism design
Responsive layout for desktop and mobile
Real-time typing indicators

Interruptible Responses:
Stop AI generation anytime using:
ESC key
Stop button
Instant response interruption for smoother UX

Smart Website & Search Handling:
Jarvis can:
Open websites dynamically
Search the web instantly
Launch commonly used platforms directly

Desktop Automation:

Jarvis can control your PC using natural commands:

Supported actions:
Open applications
Close applications
Launch websites
Execute assistant commands

Tech Stack -: 
Frontend
HTML5
JavaScript
Tailwind CSS
Backend
Python
FastAPI
AI Runtime
Ollama
AI Models
Gemma 2B / Gemma 4
Additional Libraries
psutil
pygetwindow
SpeechRecognition APIs
StreamingResponse (FastAPI)

Getting Started
Prerequisites: 

Make sure you have installed:

1.Python 3.10+
2.Ollama
Installation:
1. Clone Repository
git clone https://github.com/AnayJoshi7/MinorProject
cd MinorProject
2. Install Backend Dependencies
pip install -r requirements.txt
Install Ollama
Pull AI Model
ollama pull qwen2.5:3b
Optional:
ollama pull gemma4:e2b

3. Running Jarvis:
Start Backend-
python -m uvicorn backend.main:app --reload 

Start Frontend-
cd frontend
python -m http.server 5500
Open in Browser
Desktop:
http://127.0.0.1:5500/frontend/index.html
Phone (same WiFi):
http://YOUR_LOCAL_IP:5500/frontend/index.html


Disclaimer
This is a Minor Project developed for assessment purposes in college exams.

