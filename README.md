# YouTube Transcript & AI Summary System

A comprehensive web-based tool that extracts YouTube video transcripts, generates AI-powered summaries, and provides advanced analysis including sentiment analysis, automatic chapter generation, and speaker detection.

---

## Features

### Core Features
- **YouTube Video Processing** – Download and extract audio from any YouTube video  
- **Speech-to-Text** – Convert audio to text using OpenAI Whisper  
- **AI Summarization** – Generate comprehensive summaries with key points and insights (via Groq LLMs)  
- **Clean UI** – Modern, responsive interface with tabbed navigation  

### Bonus Features
- **Multilingual Support** – Automatically detects and transcribes 99+ languages  
- **Auto-Chapter Generation** – AI-generated chapters based on content analysis  
- **Sentiment Analysis** – Analyze the emotional tone of the video  
- **Speaker Detection** – Identify different speakers (diarization support)  

---

## Tech Stack

- **Backend:** Python 3.8+ with Flask  
- **Video Processing:** `yt-dlp`  
- **Speech Recognition:** OpenAI Whisper  
- **AI Summarization:** Groq API (e.g., `llama-3.1-8b-instant`)  
- **Sentiment Analysis:** TextBlob  
- **Frontend:** HTML5, CSS3, Vanilla JavaScript  
- **Speaker Diarization (optional):** `pyannote.audio`  

---


## Prerequisites

- Python **3.8+**
- **FFmpeg** (for audio processing)
- **Groq API key** (from <https://console.groq.com>)

---


## Installation


### 1. Clone the Repository
```bash
git clone <your-repo-url>
cd Youtube_Transcript_Summary
```

### 2. Create Virtual Environment
```bash
python -m venv venv
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Install FFmpeg
```bash
On Windows:
Download from https://ffmpeg.org/download.html
```

##-# 5. Set Up Environment Variables
free Groq API key from: https://console.groq.com
Create a .env file in the root directory:
```bash
GROQ_API_KEY=your_groq_api_key_here
```

## Usage

### 1. Start the Server
```bash
cd src
python app.py
```
The server will start at http://localhost:5000

### 2. Open in Browser
Navigate to http://localhost:5000 in your web browser

### 3. Process a Video

1. Paste a YouTube URL 
2. Select desired features:
- Sentiment Analysis
- Auto Chapters
- Speaker Detection
3. Click "Extract Transcript" and "Generate Summary"
4. Wait for processing (depending on video length)
5. View results in organized tabs


## Project Structure

```
Youtube_Transcript_Summary/
├── src/
│   ├── app.py                    # Flask backend
│   ├── video_processor.py        # YouTube download & audio extraction
│   ├── transcriber.py            # Whisper speech-to-text
│   ├── summarizer.py             # AI summary generation
│   ├── sentiment_analyzer.py     # Sentiment analysis
│   ├── chapter_generator.py      # Auto-chapter creation
│   ├── diarization.py            # Speaker detection
│   ├── templates/
│   │   └── index.html            # Frontend interface
│   └── static/
│       ├── index.html
├── downloads/                    # Temporary audio storage
├── screenshots/                  # UI screenshots
├── requirements.txt              # Python dependencies
├── README.md                     # Project documentation
└── .env                          # API keys 
```

