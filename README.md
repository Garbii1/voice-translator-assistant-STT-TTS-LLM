# 🐟 AI Babel Fish Voice Assistant Translator

Inspired by the universal translator from "The Hitchhiker's Guide to the Galaxy," this project is a real-time voice translation assistant. It captures your voice, translates it using a Large Language Model, and speaks the translation back to you.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Flask-2.3-000000?style=for-the-badge&logo=flask&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-ES6-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/IBM-Watson-0062FF?style=for-the-badge&logo=ibm&logoColor=white"/>
</p>

---

## ✨ Features
- **Real-time Voice Input:** Speak directly into the app through your browser's microphone.
- **Speech-to-Text (STT):** Utilizes IBM Watson's STT engine to accurately transcribe spoken words.
- **LLM-Powered Translation:** Leverages the flan-ul2 model from IBM Watsonx to handle complex translation queries.
- **Text-to-Speech (TTS):** Converts the translated text back into natural-sounding speech with selectable voices (e.g., English, Spanish).
- **Modern UI:** Responsive chat interface with light/dark modes, smooth animations, and support for both voice and text input.

---

## 🏗️ Tech Stack & Architecture
- **Backend:** Python (Flask)
- **Frontend:** HTML5, CSS3, JavaScript (AJAX, JQuery)
- **Styling:** Bootstrap, Font Awesome
- **AI Services:**
  - LLM: IBM Watsonx (flan-ul2)
  - STT: IBM Watson Speech-to-Text
  - TTS: IBM Watson Text-to-Speech

---

## 🔄 How It Works
1. **Voice Input:** The frontend captures audio from the user's microphone and sends it to the backend.
2. **Speech-to-Text:** Flask server forwards audio to Watson STT API, returning transcribed text.
3. **LLM Translation:** Transcribed text is sent to Watsonx flan-ul2 for translation.
4. **Text-to-Speech:** Translated text is sent to Watson TTS API to generate audio.
5. **Playback:** The backend returns translated text and audio to the frontend for display and playback.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.11 or higher
- `git` for cloning the repository

### Installation & Setup
```bash
git clone https://github.com/Garbii1/LLM-voice-translator-assistant-STT-TTS.git
cd LLM-voice-translator-assistant-STT-TTS
```

Create and activate a virtual environment:
```bash
# For macOS/Linux
python3.11 -m venv my_env
source my_env/bin/activate

# For Windows
python -m venv my_env
my_env\Scripts\activate
```

Install dependencies:
```bash
pip install -r requirements.txt
```

---

## 🛠️ Configuration

Edit `worker.py` to set your API endpoints:
- **Watson Speech-to-Text URL:**
  - In `speech_to_text()`, set `base_url` to your STT endpoint.
- **Watson Text-to-Speech URL:**
  - In `text_to_speech()`, set `base_url` to your TTS endpoint.
- **Watsonx Configuration:**
  - Set your `API_KEY` and `PROJECT_ID` if running locally.

---

## ▶️ Run the Application
Start the Flask server:
```bash
python server.py
```

Visit [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser to use the app!

---

<p align="center">
  <b>Enjoy your real-time AI-powered voice translation assistant! 🐟🌍</b>
</p>