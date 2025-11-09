# Cinematicmind
AI trailer generator that understands emotion.
# 🎥 CinematicMind — AI Trailer Generator

> *"What if machines could feel the rhythm of storytelling?"*  
> — A solo experiment in turning raw video and emotion data into cinematic trailers.

---

## 🧠 Overview

**CinematicMind** is an AI-driven pipeline that automatically transforms raw video or audio into a film-style trailer.  
It detects **scenes**, maps **emotions**, plans **narrative pacing**, and visualizes the emotional arc — like an assistant film editor with a neural heart.

This project was developed locally and iteratively by **Revanth**, combining signal processing, emotion analysis, and AI orchestration into one creative engine.

---

## ⚙️ How It Works

It also suggests transitions (`cut`, `blur`, `fade`, `crossfade`) and background soundtracks.

### 4. Trailer Rendering  
All clips are merged and synchronized via `ffmpeg`.  
If working locally, placeholders and audio pads are used to render a *visual storyboard*.  
With API access, real motion and generated scenes can be stitched together.

### 5. Emotion Visualization  
`trailer_visualizer.py` produces a **cinematic emotion arc** —  
a timeline chart showing how the trailer flows emotionally from calm to chaos and back.

---

## 🧩 Core Modules

| Module | Description |
|--------|--------------|
| `scene_detect.py` | Cuts video into meaningful scenes |
| `audio_emotion.py` | Detects emotional energy in sound |
| `gpt_scene_planner.py` | AI generates narrative plan from data |
| `fuse_scenes.py` | Joins refined clips with transitions |
| `trailer_renderer.py` | Produces the final trailer (visual/audio) |
| `trailer_visualizer.py` | Builds emotion arc graph |

---

## 📂 Output Files

| File | Purpose |
|------|----------|
| `output/final_cut.json` | Master scene plan |
| `output/trailer.mp4` | Rendered final trailer (if full clips available) |
| `output/trailer_emotion_arc.png` | Visualization of trailer emotion flow |
| `output/temp_clips/` | Individual scene files (auto-generated) |

---

## 🧱 Tech Stack

- **Python 3.10+**
- **ffmpeg** for video processing  
- **Matplotlib** for visualization  
- **OpenAI API (optional)** for scene planning  
- **Pydantic, tqdm, httpx** for clean data orchestration

---

## 🧭 Local Run (no API key required)

```bash
python prepare_and_fuse.py
python gpt_scene_planner.py
python trailer_renderer.py
python trailer_visualizer.py


### 1. Scene Detection  
Extracts logical cuts and visual segments from a source video (using `ffmpeg` and AI-assisted pattern matching).  
Each segment is scored for *motion intensity*, *silence periods*, and *narrative rhythm*.

### 2. Emotion Mapping  
Audio is analyzed using emotion classification models — tone, pitch, and energy create an **emotional fingerprint**.  
These are synced with visual cuts to build a cohesive “emotion timeline”.

### 3. Scene Planning (AI-Powered)  
`gpt_scene_planner.py` uses a language model (OpenAI API or local JSON logic) to assign tone tags like:
