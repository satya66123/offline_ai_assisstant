Here’s a **complete `README.md`** for your fully offline AI Assistant project:

---

# 🧠 Offline AI Assistant

A **fully offline AI assistant** for text summarization, semantic analysis, file generation, and video captioning.
No cloud or GPT API required — everything runs locally.

---

## Features

### 📘 Summarizer

* Summarizes text from **uploaded files** (`.txt`, `.pdf`, `.docx`) or **pasted text**.
* Offline processing with a simple extractive approach.

### 🧠 Semantic Analyzer

* Extracts **keywords** from uploaded files or input text.
* Provides **basic semantic analysis** and word count.

### 🎨 File Generator

* Generate files from text:

  * **TXT**
  * **DOCX**
  * **PDF**
  * **Image**
  * **Video with audio** (each line as separate clip with TTS)
* Download generated files instantly.

### 🎬 Video Caption Generator

* Upload a video (`.mp4`, `.mov`, `.avi`, `.mkv`) and generate captions **offline** using Whisper.
* Choose **Original Language** or **English translation**.
* Downloads available for:

  * `.srt` caption file
  * **Video with burned captions** (hardcoded subtitles)
* Completely offline — no cloud API required.

---

## Installation

1. **Clone the repository**:

```bash
git clone https://github.com/satya66123/offline_ai_assisstant.git
cd offline-ai-assistant
```

2. **Create a virtual environment**:

```bash
python -m venv .venv
```

3. **Activate the environment**:

* **Windows**:

```bash
.venv\Scripts\activate
```

* **Linux/macOS**:

```bash
source .venv/bin/activate
```

4. **Install dependencies**:

```bash
pip install -r requirements.txt
```

5. **Ensure FFmpeg is available**:

* Place `ffmpeg.exe` inside `ffmpeg/bin` folder in the project directory.
* Or add FFmpeg to your system PATH.

---

## Usage

Run the app using Streamlit:

```bash
streamlit run app.py
```

* Use the sidebar to switch between:

  * **Summarizer**
  * **Semantic Analyzer**
  * **File Generator**
  * **Video Caption Generator**
* Follow on-screen instructions to upload files, paste text, or generate outputs.

---

## Folder Structure

```
offline-ai-assistant/
│
├─ ffmpeg/bin/ffmpeg.exe   # Required for video caption burning
├─ generated/              # Automatically created for generated files
│  ├─ txt/
│  ├─ pdf/
│  ├─ docx/
│  ├─ image/
│  ├─ video/
│  ├─ captions/
├─ app.py                  # Main Streamlit application
├─ requirements.txt
└─ README.md
```

---

## Notes

* **Video generation**: Each line of input text becomes a video clip with **text-to-speech audio**. Clips are concatenated automatically.
* **Video captions**: Generated `.srt` and burned-in videos are downloadable.
* Works **completely offline** — no internet or cloud API required.
* Recommended: Use **small Whisper model** for CPU-only machines; GPU will speed up processing.

---

## Dependencies

* Python 3.10+
* Streamlit
* MoviePy
* PyPDF2
* fpdf
* python-docx
* Pillow
* pyttsx3
* whisper (offline transcription)

---

## License

MIT License

Do you want me to create that next?

