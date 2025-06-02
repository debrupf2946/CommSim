# AI-Powered Communication Analysis System for Driving Simulator Interactions

A sophisticated tool designed to analyze and visualize human-AI communication patterns in driving simulator experiments. This project leverages cutting-edge speech recognition and sentiment analysis to provide insights into communication dynamics during simulated driving scenarios.

## 🚀 Features

- **Automated Audio Processing**: Extracts audio from video recordings of driving simulator sessions
- **Advanced Speech Recognition**: Utilizes Faster-Whisper for accurate speech-to-text conversion
- **Sentiment Analysis**: Implements PySentimiento for nuanced emotion detection in conversations
- **Interactive Visualization**: Custom UI for generating insightful communication pattern graphs
- **Real-time Processing**: Efficient handling of long-duration simulator recordings

## 📋 Prerequisites

This project has been optimized for MacOS and Python 3.10.16. Here's what you need to get started:

### Essential Software
- Python 3.10.16
- ffmpeg
- sox (for audio processing)
- tkinter (for UI components)

### Directory Structure
```
project_root/
├── Videos/          # Place your simulator recordings here
├── Audios/          # Processed audio files
├── Segments/        # Split audio segments
├── Transcriptions/  # Generated transcription files
└── plots/           # Visualization outputs
```

## 🛠️ Installation

1. **Set up Virtual Environment**
```bash
python -m venv venv
source venv/bin/activate  # For MacOS/Linux
```

2. **Install ffmpeg**
```bash
# MacOS
brew install ffmpeg

# Linux
sudo apt update
sudo apt install ffmpeg
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

4. **Install Additional Components**
```bash
# MacOS
brew install python-tk@3.10
brew install sox

# Linux
sudo apt-get install python3-tk
sudo apt-get install sox libsox-fmt-all
```

## 💻 Usage

1. **Configure Settings**
Edit `config.py` to set your preferences:
```python
VIDEO_PATH = "Videos"
AUDIO_PATH = "Audios"
SEG_PATH = "Segments"
TRANSCRIBE_DIR = "Transcription"
model_name = "tiny"
split_length = 2000
```

2. **Process Videos and Generate Analysis**
```bash
python main.py
```

3. **Generate Visualizations**
```bash
python visualization.py
```

4. **Launch Interactive UI**
```bash
python ui.py
```

## 📊 Visualization Features

The project offers two main types of visualizations:

1. **Word Count Distribution**: Histogram showing communication density over time
2. **Sentiment Distribution**: Pie chart displaying the emotional content distribution

## 🔧 Technical Implementation

### Speech Recognition
- Implements Faster-Whisper for optimized transcription
- Utilizes Voice Activity Detection (VAD) for accurate timestamp mapping
- Processes audio in segments for improved accuracy

### Sentiment Analysis
- Employs PySentimiento with BERTweet model
- Provides three-way classification: Positive, Negative, Neutral
- Real-time sentiment processing capabilities

### Data Visualization
- Custom bucketing algorithm for time-series analysis
- Dynamic plot generation based on transcription data
- Interactive UI for data exploration

## 🎯 Future Enhancements

- Integration of multi-speaker detection
- Enhanced sentiment analysis with custom model training
- Real-time processing capabilities
- Advanced visualization options
- Performance optimizations for larger datasets

## 🖼️ Interface Preview

The application features an intuitive interface for:
- File upload and processing
- Visualization generation
- Data analysis display
- Result export capabilities

## 💡 Use Cases

- Research in human-AI interaction patterns
- Driving simulator communication analysis
- Communication pattern visualization
- Sentiment trend analysis in controlled environments

This tool serves as a comprehensive solution for analyzing communication patterns in driving simulator experiments, providing valuable insights for researchers and developers working on human-AI interaction systems.



