# 🎬 Offline AI Video Generator

A modular, fully offline pipeline that automatically creates short-form videos using local AI models — script generation, text-to-speech, image generation, subtitle alignment, and video rendering, all in one workflow.

> **Fork maintained by [Vemmba](https://github.com/Vemmba)** ·
> Original project by [prakashdk](https://github.com/prakashdk) — many thanks!

---

## ✨ Features

| Component | Technology |
|---|---|
| 🧠 Script & prompt generation | Local LLM via [Ollama](https://ollama.com/) |
| 🎙 Text-to-Speech | [Coqui TTS](https://github.com/coqui-ai/TTS) |
| 🖼 Image generation | Stable Diffusion (`Realistic_Vision_V5.1_noVAE`) |
| 📝 Subtitles | Whisper / whisper.cpp alignment |
| 🎞 Video composition | Images + audio + subtitles + BGM → MP4 |

Everything runs locally — no internet connection required after setup.

---

## 🚀 Quick Start

### 1. Clone

```bash
git clone https://github.com/Vemmba/video-creator.git
cd video-creator
```

### 2. Virtual environment

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Pull the LLM

```bash
ollama pull llama3.2
```

### 5. Run

```bash
python main.py
```

Generated videos appear under `outputs/<n>/`.

---

## 📁 Project Structure

```
video-creator/
├── main.py        # Entry point & orchestration
├── pipeline.py    # Generation pipeline
├── models/        # Text, image, audio, subtitle, video models
├── util/          # Shared helpers
├── bgms/          # Background music tracks
├── images/        # Static image assets
└── database/      # Video counter state
```

---

## 📄 License & Credits

All credit for the original codebase goes to [prakashdk](https://github.com/prakashdk).
This fork is maintained by [Vemmba](https://github.com/Vemmba) for personal use.
