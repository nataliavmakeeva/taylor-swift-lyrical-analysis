# Research Notebooks

## 📚 File Descriptions

### 1. TS_twelve_01_audio_processing.ipynb
**Purpose**: Extract and process audio from Taylor Swift's podcast appearance
- Downloads audio from YouTube using yt_dlp (this file isn’t provided, as it’s quick to process; all other preprocessed files are included).
- Performs speaker diarization with pyannote
- Transcribes speech using OpenAI Whisper
- Outputs: Merged segments with speaker labels

**Required**: HuggingFace token for pyannote

### 2. TS_twelve_02_lyrical_analysis.ipynb
**Purpose**: Analyze speech patterns and identify potential song lyrics
- Parses lyrics from Red and 1989 albums (Max Martin & Shellback collaborations)
- Creates TF-IDF and BERT embedding profiles of song styles
- Trains custom classifier using triplet loss
- Identifies podcast segments matching lyrical patterns

**Note**: Lyrics parsing included for research purposes only

### 3. style_classifier_model.pth
Pre-trained style classifier model (32-dimensional output)
- Distinguishes song lyrics from conversational speech
- Trained on 361 positive/negative pairs
- Test loss: 0.247

### 4. saved_diarizations/
Pre-processed audio analysis files:
- `podcast_corrected_diarization.pkl` - Speaker segments (pickle format)
- `podcast_corrected_diarization.json` - Speaker segments (JSON format)
- `podcast_corrected_diarization.txt` - Speaker segments (txt format)
- `transcription_medium.json` - Whisper transcription output

## 🔄 Processing Pipeline
1. Run audio processing notebook first (or use provided diarization files)
2. Run lyrical analysis notebook for pattern detection
3. Model can be retrained or loaded from saved checkpoint

## ⚠️ Notes
- Full audio processing (transcription+diarization) takes ~4 hours for full podcast
- Saved diarizations provided to skip this step
- Ensure sufficient RAM for BERT model loading