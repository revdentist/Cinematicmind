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

### 1. Scene Detection  
Extracts logical cuts and visual segments from a source video (using `ffmpeg` and AI-assisted pattern matching).  
Each segment is scored for *motion intensity*, *silence periods*, and *narrative rhythm*.

### 2. Emotion Mapping  
Audio is analyzed using emotion classification models — tone, pitch, and energy create an **emotional fingerprint**.  
These are synced with visual cuts to build a cohesive “emotion timeline”.

### 3. Scene Planning (AI-Powered)  
`gpt_scene_planner.py` uses a language model (OpenAI API or local JSON logic) to assign tone tags like:
