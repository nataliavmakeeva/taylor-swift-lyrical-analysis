# ⚠️ IMPORTANT LEGAL DISCLAIMER:

This project is for educational and research purposes only. 
- Song lyrics are property of their respective owners
- Audio samples are used under fair use for analysis
- No copyright infringement intended
- This is a research project, not a commercial product

# Taylor Swift Podcast Lyrical Pattern Analysis

Analysis of lyrical patterns in Taylor Swift's podcast appearance using NLP and deep learning techniques.

## 🎯 Project Goals
- Extract potential TS 12 song material from conversational speech
- Identify stylistic patterns characteristic of Taylor Swift's songwriting
- Compare semantic vs stylistic similarity metrics

## 🛠️ Methods
- **Video Processing**: yt_dlp for YouTube download, ffmpeg for audio extraction
- **Audio Processing**: pyannote for speaker diarization, Whisper for transcription. Note: Requires HuggingFace token for pyannote (use your own)
- **NLP Analysis**: TF-IDF, BERT embeddings (all-mpnet-base-v2)
- **Style Classification**: Custom neural network with triplet loss training

## 📊 Results
What the analysis showed is that Miss Americana, when happy, speaks very rhythmically and in harmony with *Red* and *1989* albums, which actually makes it hard to pinpoint where the real Easter eggs are. But when we trained a model to distinguish podcast speech style from song lyrics style, we found that we can definitely expect to hear about "end of my night," be sure that "there's a poem in this," and that "life is more upbeat."

The next step could be connecting large LLM APIs to generate lyrics inspired by the discovered patterns — but honestly, I doubt AI can recreate the artistry of someone who wrote a line like "Cause something counterfeit's dead." So just enjoy the mathematical profile of TS songs, and let's be excited for "The Life of a Showgirl."

## Third-party licenses:
- Whisper: MIT License
- pyannote.audio: MIT License
- Transformers: Apache 2.0 License

## 📝 License
MIT License - see LICENSE file

## 🚀 Quick Start
```bash
git clone https://github.com/nataliavmakeeva/taylor-swift-lyrical-analysis
pip install -r requirements.txt
# Navigate to research folder
cd research
# Open Jupyter notebooks
jupyter notebook