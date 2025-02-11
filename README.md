```markdown
# Video to Audio and Transcription Tool

Jupyter notebook to **extract audio** from  video files and **transcribe it to text** using FFmpeg and OpenAI's Whisper.

## Prerequisites 📋
- Python 3.8+
- FFmpeg (installed and added to `PATH`)

### Clone the Repository
```bash
git clone https://github.com/ubadaht/video2audio2text/.git
cd video2audio2text
```

## Usage 🚀

### Step 1: Extract Audio from Video
```python
# In a Jupyter Notebook cell or Python script
input_mkv = "video.mkv"
output_audio = "audio.aac"

!ffmpeg -i "{input_mkv}" -vn -acodec copy "{output_audio}"
```

### Step 2: Transcribe Audio with Whisper
```python
import whisper

model = whisper.load_model("base")  # Use "medium" or "large" for better accuracy
result = model.transcribe("audio.aac")

with open("transcription.txt", "w") as f:
    f.write(result["text"])
```

## Example Workflow 📂
```
Input: video.mkv
       ↓ (FFmpeg extracts audio)
Output: audio.aac
       ↓ (Whisper transcribes)
Final Output: transcription.txt
```

## Configuration ⚙️
- **Whisper Models**: Choose from `tiny`, `base`, `small`, `medium`, or `large` (trade-off between speed and accuracy).
- **Audio Formats**: Supports `.aac`, `.wav`, `.mp3`, etc. (use `-acodec copy` in FFmpeg to preserve original quality).

## Troubleshooting 🔧
- **FFmpeg Not Found**: Ensure it’s installed and added to your system `PATH`.

---

**Acknowledgments**:
- [OpenAI Whisper](https://github.com/openai/whisper)
- [FFmpeg](https://ffmpeg.org/)
```

---

### Key Highlights:
1. **Audience-Friendly**: Clear steps for both technical and non-technical users.
2. **Modular**: Easily adaptable to scripts or pipelines.
3. **Platform-Agnostic**: Works on Windows/Linux/macOS.

Customize the repo links, license, or add screenshots as needed! 📁
