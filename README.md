# Communication Analysis Platform for Human-AI Driving Interactions

An innovative platform that analyzes communication patterns between humans and AI systems during driving simulator experiments. This cutting-edge solution combines advanced speech processing with sentiment analysis to deliver deep insights into interaction dynamics.

## 🌟 Core Capabilities

- **Smart Audio Extraction**: Seamlessly processes video recordings from simulator sessions
- **High-Precision Speech Recognition**: Leverages Faster-Whisper technology for accurate transcription
- **Emotional Intelligence**: Incorporates PySentimiento for detailed sentiment mapping
- **Data Visualization Suite**: Features comprehensive tools for pattern analysis
- **Performance Optimized**: Handles extended simulation recordings efficiently

## 🔧 System Requirements

Optimized for MacOS and Python 3.10.16. Required components:

### Core Dependencies
- Python 3.10.16
- ffmpeg
- sox (audio processing engine)
- tkinter (GUI framework)

### Project Structure
```
project_root/
├── Videos/          # Simulator session recordings
├── Audios/         # Processed audio files
├── Segments/       # Audio segments
├── Transcriptions/ # Text transcriptions
└── plots/          # Visual analytics
```

## 🚀 Setup Guide

1. **Environment Setup**
```bash
python -m venv venv
source venv/bin/activate  # MacOS/Linux
```

2. **Install ffmpeg**
```bash
# MacOS
brew install ffmpeg

# Linux
sudo apt update
sudo apt install ffmpeg
```

3. **Install Required Packages**
```bash
pip install -r requirements.txt
```

4. **System Components**
```bash
# MacOS
brew install python-tk@3.10
brew install sox

# Linux
sudo apt-get install python3-tk
sudo apt-get install sox libsox-fmt-all
```

## 💻 Operation Guide

1. **System Configuration**
Customize `config.py` settings:
```python
VIDEO_PATH = "Videos"
AUDIO_PATH = "Audios"
SEG_PATH = "Segments"
TRANSCRIBE_DIR = "Transcription"
model_name = "tiny"
split_length = 2000
```

2. **Launch Analysis**
```bash
python main.py
```

3. **Generate Analytics**
```bash
python visualization.py
```

4. **Access Interface**
```bash
python ui.py
```

## 📊 Data Visualization Features

The platform offers sophisticated visualization capabilities:

![Word Distribution Analysis](plots/transcription_histogram.png)
*Word Distribution Analysis: Visualizes communication patterns over time*

![Sentiment Analysis Distribution](plots/sentiment_distribution.png)
*Sentiment Analysis: Shows emotional content distribution in interactions*

## 🛠 Technical Architecture

### Speech Processing
- Implements state-of-the-art Faster-Whisper
- Features Voice Activity Detection
- Supports segmented processing

### Emotion Analysis
- Utilizes PySentimiento with BERTweet
- Provides comprehensive sentiment classification
- Enables real-time analysis

### Visual Analytics
- Custom temporal analysis algorithms
- Dynamic visualization generation
- Interactive data exploration

## 🎯 Roadmap

- Multi-speaker recognition system
- Enhanced emotion detection models
- Live processing capabilities
- Advanced visualization tools
- System performance enhancements

## 🖥 Interface Overview

The system features a modern interface for:
- Data ingestion and processing
- Analytics visualization
- Results analysis
- Export functionality

## 💡 Applications

- Human-AI interaction research
- Simulator communication studies
- Pattern visualization and analysis
- Emotional response tracking

This platform represents a comprehensive solution for analyzing human-AI communication in driving simulations, offering researchers and developers powerful tools for understanding interaction dynamics.



