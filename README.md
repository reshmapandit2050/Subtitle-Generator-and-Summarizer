# 🎬 Subtitle Generator and Summarizer

## 📌 Project Description
This project downloads YouTube videos, extracts audio, converts speech to text using Whisper, and generates subtitles and summaries.

---

## 🚀 Features
- Download audio from YouTube
- Convert speech to text (Whisper)
- Generate subtitles
- Create summaries

---

## 🛠️ Requirements

Install required libraries:

pip install yt-dlp whisper torch moviepy transformers jiwer rouge-score

---

## ⚙️ Install FFmpeg (Important)

1. Download FFmpeg from:
https://www.gyan.dev/ffmpeg/builds/

2. Download:
ffmpeg-release-essentials.zip

3. Extract the ZIP file

4. Go to:
ffmpeg-xxxx\bin

Example:
C:\Users\YourName\Downloads\ffmpeg-8.1-essentials_build\bin

---

## ⚙️ Set FFmpeg Path in Code

Add this inside your Python code:

```python
ydl_opts = {
    'format': 'bestaudio/best',
    'outtmpl': f'{audio_folder}/audio_%(id)s.%(ext)s',
    'ffmpeg_location': r'C:\Users\YourName\Downloads\ffmpeg-8.1-essentials_build\bin',
    'postprocessors': [{
        'key': 'FFmpegExtractAudio',
        'preferredcodec': 'wav',
        'preferredquality': '192',
    }],
}