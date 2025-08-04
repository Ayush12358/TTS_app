# TTS Reader

A Flask web application that converts text documents and PDFs to speech using Coqui AI's TTS library.

## Features

- Upload PDF, text files (.txt, .md, .rtf) or paste text directly
- Multiple voice options from VCTK dataset (default: p270)
- Adjustable reading speed (50-500 WPM)
- OCR support for scanned documents
- Sentence-by-sentence playback with highlighting
- Dark mode interface

## Installation

1. Install dependencies:

   ```bash
   pip install flask flask-cors TTS torch
   ```

2. Run the application:

   ```bash
   python app.py
   ```

3. Open <http://127.0.0.1:5080> in your browser

## Usage

1. Upload a document or paste text
2. Select voice and adjust speed if needed
3. Click play to start text-to-speech
4. Use spacebar to play/pause
5. Click any sentence to jump to that position

## API

- `POST /tts` - Generate speech from text
- `GET /speakers` - List available voices
- `GET /` - Web interface

## Requirements

- Python 3.7+ (3.11 recommended)
- 2GB+ RAM for model loading
- Modern web browser with JavaScript enabled