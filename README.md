AUTO VIDEO MONTAGE PRO (GENERATION 4 / UNIVERSAL MAC)

================================================================================

Contact & Licensing / Контакти та ліцензування:
• Rightsholder & Product Creator / Правовласник та Творець продукту: Serhii Makarenko / Сергій Макаренко
• E-mail for license inquiries & support: cjsmars@gmail.com
• Platform: macOS 13.0+ (Apple Silicon M1/M2/M3/M4 & Intel 64-bit)

================================================================================
         PART 1: USER MANUAL & END-USER LICENSE AGREEMENT (ENGLISH)

================================================================================

# User Manual: Auto Video Montage Pro 🎬

Welcome to **Auto Video Montage Pro** — an AI-powered video editing assistant. This application is designed to save you hours of tedious editing by automatically:
1. Normalizing audio levels.
2. Transcribing speech and removing all silent pauses.
3. Helping to select the best moments (Shorts).
4. Detecting and deleting bad takes, filler words, and stuttering (using advanced Semantic and Emotional AI models).
5. Generating an import-ready sequence for Final Cut Pro, Premiere Pro, or DaVinci Resolve, plus SRT subtitles and detailed reports.

---

## ⚠️ Important Note: The Nature of Rough-Cut Assembly & AI Limits

**Auto Video Montage Pro** is engineered for automated **Rough Cut / First-Pass Assembly**, saving you 70% to 80% of editing time by taking over the most tedious routine: multi-camera sync, cutting silent pauses, and stripping obvious technical retakes.

**Key Concepts to Keep in Mind:**
1. **AI does not replace human editorial judgment:** No neural network possesses artistic intuition, dramatic timing, or a filmmaker's creative vision.
2. **Story safety first (Over-cutting protection):** The algorithms are calibrated to guarantee narrative integrity. The program will sooner leave an alternative take or rephrased sentence on the timeline than risk cutting critical context or genuine storytelling.
3. **Final control stays with the creator:** Import the resulting XML file into your video editor (Final Cut Pro, DaVinci Resolve, Premiere Pro) to perform the final creative polishing, fine-tuning, and take selection in just a few minutes.

---

## 🛠 First Run & Basic Setup

Upon your first launch, the application will direct you to the **"AI Models"** tab. 
To understand voice, the app needs a "brain" — a Whisper model.

1. Go to the **"🧠 AI Models"** tab.
2. Choose a directory on your computer where the models are stored (e.g. `~/Library/Application Support/AutoVideoMontagePro/Models` or any preferred folder).
3. Click "Scan Models" to ensure your model (e.g. `large-v3-turbo`) is detected.
4. Done! Switch to "Main Montage", add your media, and click "Start Smart Montage".

---

## ✨ Advanced AI Intelligence (Semantics & Emotions)

The standard heuristic mode trims pauses and exact duplicate words. The **Advanced AI Mode** understands *context* (semantics) and can identify the best *emotional* take:
- Connect local LLM via LM Studio (port 1234) for Qwen 2.5.
- In **Settings**, enable Semantic Analysis and Voice Prosody/Emotional Dynamics.

---

## ⚙️ AI Configuration

In the **Settings** tab, customize editing behavior:
- **Silence Threshold:** Pauses longer than this setting (0.2–1.5s) are automatically cut.
- **Padding In / Out:** Breathing room (seconds) before first word and after last word in each take.
- **Filler Words:** Words to ignore or remove during duplicate comparison ("um", "uh", "like").
- **Stop Commands:** If you say "stop", "retake", or "again", the app deletes the prior mistake.

---

## 🚀 Version v3.0 & v4.0 Capabilities

### 1. 📁 Batch Multi-Clip Series Ingestion
Stitches multiple clip takes into one virtual timeline without re-encoding, cutting mistakes across file boundaries.

### 2. ⏱️ Multicam: Dynamic In-File Pause Resynchronization (OBS vs. iPhone)
Sliding cross-correlation detects OBS pause button events to the millisecond, shifting the track forward so both angles remain in 100% sync throughout.

### 3. 🧩 Multi-Clip Multicam Anchoring
Aligns fragmented takes against a continuous master camera using acoustic fingerprinting.

### 4. 🎙️ Automatic Master Camera Selection
Measures audio SNR and room acoustics to designate the best microphone as Master Audio.

---

## 🖥️ 5. Intel Mac Hardware Compatibility Guide

| Category | Intel Mac Models | Hardware Specs (RAM / GPU) | Recommended Qwen Model | LM Studio Setup |
| :--- | :--- | :--- | :--- | :--- |
| **Top Tier (Pro)** | **iMac 27" 5K (2019–2020)**<br>**MacBook Pro 16" (2019)**<br>**iMac Pro (2017)**<br>**Mac Pro (2019)** | 16–64+ GB RAM<br>AMD Radeon Pro 5300M–5700XT<br>(4–16 GB VRAM) | **Qwen 2.5 7B Instruct**<br>or **3B Instruct** (Q4_K_M) | **GPU Offload (Metal): MAX**<br>Accelerated directly on AMD GPU. Speed: 4–6s per window. |
| **Optimal** | **Mac mini (2018–2020 Intel)**<br>**MacBook Pro 15" (2016–2018)**<br>**MacBook Pro 13" (2018–2020)** | 16–32 GB RAM<br>Intel Iris Plus / AMD 450–560X<br>(2–4 GB VRAM) | **Qwen 2.5 3B Instruct**<br>or **1.5B Instruct** (Q4_K_M) | **GPU Offload: 0 (CPU mode)**<br>Runs on CPU via AVX2 vector instructions. Speed: 8–12s per window. |
| **Limited (No LLM)** | **MacBook Air (Intel 2018–2020)**<br>**MacBook Pro 13" (8 GB RAM)** | 8 GB RAM<br>Integrated Intel Graphics | **No Local LLM** | Use **"Heuristic Mode (No LLM)"** for fast algorithmic duplicate & silence cleaning. |

---

## 📤 6. Importing Results into NLEs

Outputs are saved directly into your media folder:
- **Final Cut Pro:** File -> Import -> XML (`_AI_CUT.fcpxml` or `_MULTICAM_MULTI_AI_CUT.fcpxml`).
- **DaVinci Resolve:** File -> Import -> Timeline (Cmd+Shift+I).
- **Adobe Premiere Pro:** Drag & drop XML into Project panel.
- **SRT Subtitles & Log Report:** `*_TEXT.srt` and `*_REPORT.txt` are created alongside the timeline XML.

---

## 🎬 7. Using the "AI Models" Tab & Offline Manager

The **"🧠 AI Models"** tab lets you manage Faster-Whisper voice models directly from the app interface:
- **Status Badges:** A green **"Installed"** badge means all 4 required model files (`model.bin`, `config.json`, `vocabulary.json`, `tokenizer.json`) are stored locally on disk and ready for offline use.
- **One-Click Download:** Click **"Download Model"** next to your preferred size (`large-v3-turbo` or `medium`) to fetch it directly from the official Hugging Face repository.
- **Custom Model Storage:** Click **"Change..."** to point the app to an external SSD or shared folder.

---

## 📥 8. Offline Operation & Manual Model Transfer
If your editing Mac is offline:
1. **Faster-Whisper Models (Speech):** Copy the 4 model files (`model.bin`, `config.json`, `vocabulary.json`, `tokenizer.json`) into a folder and select it in the **"🧠 AI Models"** tab.
2. **Qwen 2.5 LLM:** Load `.gguf` models offline via LM Studio.
