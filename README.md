# ShortsLab

**Turn long YouTube videos into viral shorts — Powered by AI**

ShortsLab automatically finds the best moments in any YouTube video and converts them into ready-to-post vertical clips (TikTok / Reels / Shorts) with captions, hooks, and face tracking.

---

## Features

- **AI Highlight Detection** — uses GPT-4.1 to find the most viral moments in any video
- **Auto Captions** — burned-in subtitles with word-level sync via Whisper
- **Hook Overlay** — attention-grabbing text overlaid on the first seconds of each clip
- **Face Tracking** — automatically keeps the speaker centered in 9:16 portrait format
- **YouTube Upload** — upload directly to your channel via OAuth
- **Multi-provider AI** — works with OpenAI, Groq, or any OpenAI-compatible API

---

## Requirements

- macOS (primary) or Windows/Linux
- Python 3.11+
- FFmpeg (via Homebrew: `brew install ffmpeg`)
- An OpenAI API key (get one at [platform.openai.com](https://platform.openai.com))

---

## Installation

```bash
git clone https://github.com/KingArthurBorges/shortslab.git
cd shortslab
pip install -r requirements.txt
python app.py
```

---

## Quick Start

1. Open the app and go to **Settings → Highlight Finder**
2. Select **OpenAI**, paste your API key, choose model `gpt-4.1`, and save
3. Paste a YouTube URL on the home screen
4. Choose how many clips you want and click **Find Highlights**
5. Select the clips you like and click **Process**

Your clips will be saved to the `output/` folder.

---

## Configuration

All settings are stored in `config.json` (created on first run, never committed to git).
API keys stay local — they are never uploaded anywhere.

---

## Tech Stack

- **UI** — CustomTkinter (Python desktop GUI)
- **Video** — FFmpeg + OpenCV
- **AI** — OpenAI-compatible APIs (GPT-4.1, gpt-4o-mini, Groq, etc.)
- **Subtitles** — yt-dlp + Whisper (via Groq)
- **Upload** — YouTube Data API v3

---

## Credits

Built by [thekinglab](https://github.com/KingArthurBorges).  
Inspired by the open-source community around AI-powered video editing.

---

## License

MIT — see [LICENSE](LICENSE)
