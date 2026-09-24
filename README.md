<p align="center">
  <img src="assets/banner.png" alt="JARVIS Banner" width="50%">
</p>

# JARVIS - Multi-Purpose AI Agent

JARVIS is a local AI assistant inspired by the AI assistant concept from Iron Man. It combines conversational AI, voice interaction, web search, website launching, and desktop automation in a single application.

JARVIS runs locally using Ollama and local AI models, allowing users to interact with an AI assistant while keeping their data on their own system.

## Features

### AI-Powered Conversations

- Runs locally using Ollama and supported AI models
- Natural-language conversations
- Real-time streaming responses
- Conversation memory support
- Lightweight local AI inference

### Voice Interaction

- Voice input using browser speech recognition
- Voice responses using text-to-speech
- Hands-free interaction

### Modern User Interface

- Futuristic AI-assistant inspired design
- Animated interface elements
- Glassmorphism-based UI
- Responsive layout for desktop and mobile
- Real-time typing indicators

### Interruptible Responses

Users can stop an ongoing AI response at any time using:

- `ESC` key
- Stop button in the interface

This allows users to interrupt long or unwanted responses immediately.

### Website and Search Handling

JARVIS can:

- Open websites dynamically
- Perform web searches
- Launch commonly used websites and platforms
- Process website-related commands using natural language

### Desktop Automation

JARVIS can perform supported computer operations using natural-language commands.

Supported operations include:

- Open applications
- Close applications
- Launch websites
- Execute supported assistant commands

## Tech Stack

### Frontend

- HTML5
- JavaScript
- Tailwind CSS

### Backend

- Python
- FastAPI
- Uvicorn

### AI

- Ollama
- Qwen 2.5 3B
- Gemma 4 E2B

### Additional Libraries

- psutil
- pygetwindow
- pyautogui
- Speech Recognition APIs
- FastAPI StreamingResponse
- Requests
- Pydantic

## Project Structure

```text
MinorProject/
├── backend/
│   └── main.py
├── frontend/
│   └── index.html
├── assets/
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

The exact project structure may change as new features are added.

## Getting Started

### Prerequisites

Make sure the following are installed:

1. Python 3.10 or later
2. Ollama
3. Git
4. A modern web browser

### 1. Clone the Repository

```bash
git clone https://github.com/AnayJoshi7/MinorProject
cd MinorProject
```

### 2. Install Backend Dependencies

```bash
pip install -r requirements.txt
```

### 3. Install the AI Model

Install Ollama and pull the required model:

```bash
ollama pull qwen2.5:3b
```

Optional:

```bash
ollama pull gemma4:e2b
```

Make sure Ollama is running before starting JARVIS.

### 4. Start the Backend

From the project root:

```bash
python -m uvicorn backend.main:app --reload
```

The FastAPI backend will start locally.

### 5. Start the Frontend

Open another terminal:

```bash
cd frontend
python -m http.server 5500
```

### 6. Open JARVIS

On the same computer, open:

```text
http://127.0.0.1:5500/frontend/index.html
```

For access from a phone connected to the same Wi-Fi network:

```text
http://YOUR_LOCAL_IP:5500/frontend/index.html
```

Replace `YOUR_LOCAL_IP` with the local IP address of the computer running JARVIS.

## How It Works

The basic communication flow is:

```text
User
  |
  v
Frontend
  |
  v
FastAPI Backend
  |
  +----------------+
  |                |
  v                v
Ollama         Desktop Automation
  |
  v
Local AI Model
  |
  v
Response
  |
  v
Frontend
```

The frontend receives the user's text or voice input and sends it to the FastAPI backend. The backend communicates with the local AI model through Ollama when an AI response is required.

For supported automation commands, the backend can use Python automation libraries to perform the requested operation.

AI responses can be streamed back to the frontend so that the user can see the response while it is being generated.

## Local and Privacy-Focused Design

JARVIS is designed to run primarily on the user's own computer. AI inference is performed through Ollama and locally installed models instead of requiring every conversation to be processed by a cloud-based AI service.

This approach can provide:

- Local processing
- Reduced dependence on external AI APIs
- Better control over personal data
- Offline AI capability when all required components are available locally

Actual privacy and offline behavior depend on the specific features and external services being used.

## Docker Support

The project also includes Docker configuration for containerized deployment.

If Docker and Docker Compose are installed, the application can be deployed using the provided configuration:

```bash
docker compose up --build
```

The exact Docker configuration may vary as the project develops.

## Future Improvements

Possible future improvements include:

- Advanced long-term memory
- Better speech recognition
- Multilingual voice interaction
- AI vision and image understanding
- More desktop automation features
- System monitoring
- Tool-based AI architecture
- Improved security and command permissions
- Dedicated Android application
- Better local model selection
- Automated workflows
- Improved offline functionality

## Disclaimer

This project is a Minor Project developed for academic and assessment purposes as part of the B.Tech Computer Science and Engineering curriculum at Lakshmi Narain College of Technology Excellence, Bhopal.

Desktop automation features should be used carefully. Only supported and intended commands should be executed.

## Author

**Anay Joshi**

B.Tech, Computer Science and Engineering  
Lakshmi Narain College of Technology Excellence, Bhopal

## Repository

GitHub: https://github.com/AnayJoshi7/MinorProject
