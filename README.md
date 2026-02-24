# ⚖️ LawyerBOT – AI Legal Assistant with Voice & Email Log System

## 📌 Project Overview
LawyerBOT is an AI-powered legal chatbot developed using Flask.  
It provides professional legal guidance strictly related to Indian law and automatically sends chat logs via email when the user ends the conversation.  

The system also includes Text-to-Speech (TTS) functionality to read legal responses aloud.

---

## 🚀 Core Features
- AI-powered legal assistance (Indian jurisdiction only)
- Professional legal response format enforcement
- Mandatory law citation (Act name + Section number)
- Text-to-Speech voice output
- Automatic email sending of chat logs
- Thread-safe TTS execution
- Logging system for user and AI responses
- Non-legal question rejection system

---

## 🛠️ Technologies Used
- Backend: Python, Flask  
- AI Model API: Groq (LLaMA 3.3 70B Versatile)  
- Email Service: MailerSend API  
- Voice Engine: pyttsx3  
- Logging: Python logging module  
- Threading: Python threading  

---

## 🧠 System Workflow
1. User sends a legal query via web interface.
2. Flask backend receives the request.
3. Query is sent to Groq AI model.
4. AI generates structured legal response.
5. Response is logged into log file.
6. Text-to-Speech runs in background thread.
7. If user types "bye":
   - Chat logs are read.
   - Email is generated.
   - Logs are sent to configured email address.

---

## 📂 Project Structure
LawyerBOT/
│
├── app.py
├── templates/
│   └── index.html
├── logs/
│   └── AI_lawyer_chat.log
├── static/
│   └── style.css
└── requirements.txt

---

## ⚙️ AI Response Rules Enforced
The AI system prompt ensures:
- Only law-related questions are answered.
- Jurisdiction: Indian law only.
- Formal and professional tone.
- Citation of:
  - Exact Act name
  - Relevant Section number
- Structured answer format:
  1. Brief Legal Summary
  2. Relevant Law Citation(s)
  3. Explanation
  4. Practical Legal Steps
  5. Short and concise response
- If user says "bye", respond with proper legal closing.

---

## 🔊 Text-to-Speech Implementation
- Uses pyttsx3 engine.
- Runs inside a daemon thread.
- Prevents Flask request blocking.
- Each response is spoken aloud automatically.
- Separate engine instance used inside function to ensure thread safety.

---

## 📧 Email Log Sending System
When the user types "bye":
- The system reads the stored log file.
- Builds email using MailerSend EmailBuilder.
- Sends both HTML and plain text version of logs.
- Logs include full conversation transcript.

---

## 📝 Logging Configuration
- Logs stored in: logs/AI_lawyer_chat.log
- User queries logged.
- AI responses logged.
- HTTP server logs reduced.
- httpx logs suppressed.
- Errors captured using try-except blocks.

---



## 📌 Use Cases
- AI Legal Awareness System
- College Final Year Project
- AI + Flask Integration Demo
- Voice-Enabled Chatbot
- Automated Reporting System

---

## 📊 Resume Description
Developed an AI-powered legal chatbot using Flask that provides structured legal guidance under Indian law, integrates real-time voice output using pyttsx3, logs user interactions, and automatically sends conversation reports via email using Groq API and MailerSend.

---

## 👩‍💻 Author
Hamsaveni  
Software Engineering Student  
