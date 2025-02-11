```markdown
# Video to Audio and Transcription Tool

Jupyter notebook to **extract audio** from  video files and **transcribe it to text** using FFmpeg and OpenAI's Whisper.

## Prerequisites
- Python 3.8+
- FFmpeg (installed and added to `PATH`)

### Clone the Repository
```bash
git clone https://github.com/ubadaht/video2audio2text/.git
cd video2audio2text
```

```

## Example Workflow
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
