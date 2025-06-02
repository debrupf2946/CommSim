# Communication Analysis Platform for Human-AI Driving Interactions

A sophisticated platform for analyzing communication patterns in human-AI driving simulator experiments. This comprehensive solution provides audio processing, transcription, sentiment analysis, and visualization capabilities.

## System Architecture
![Architecture](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/arch.png)

## 🔧 Environment Setup
**Important Note**: This system has been developed and tested on MacOS with Python 3.10.16. Different operating systems may require adjustments.

**Initial Setup**: Create a `Videos` directory in your workspace to store simulator recordings for processing.

### Installation Steps

1. **Virtual Environment Configuration**
```bash
python -m venv venv
source venv/bin/activate
```

2. **FFmpeg Installation**
```bash
# MacOS
brew install ffmpeg

# Linux
sudo apt update
sudo apt install ffmpeg

# Windows: Visit https://ffmpeg.org/download.html
```

3. **Package Installation**
```bash
pip install -r requirements.txt
```

4. **GUI Dependencies**
```bash
# MacOS
brew install python-tk@3.10

# Linux
sudo apt-get install python3-tk

# Windows: Included with Python
```

5. **Audio Processing Tools**
```bash
# MacOS
brew install sox

# Linux
sudo apt-get install sox libsox-fmt-all

# Windows: Download from https://sourceforge.net/projects/sox/
```

## 📊 System Components

### Project Structure
```bash
├── Audios/         # Processed audio files
├── Videos/         # Input video recordings
├── Segments/       # Audio segments
├── Transcriptions/ # Generated transcripts
├── plots/          # Visualization outputs
├── config.py       # System configuration
├── main.py         # Core processing
├── ui.py          # User interface
└── visualization.py # Data visualization
```

### Configuration
Customize settings in `config.py`:
```python
VIDEO_PATH = "Videos"
AUDIO_PATH = "Audios"
SEG_PATH = "Segments"
TRANSCRIBE_DIR = "Transcription"
model_name = "tiny"
split_length = 2000
```

## 🚀 Operation Guide

### Core Processing
1. Run the main analysis pipeline:
```bash
python main.py
```

### Visualization
1. Generate data visualizations:
```bash
python visualization.py
```

2. Launch the interactive interface:
```bash
python ui.py
```

## 💡 Technical Implementation

### Speech Processing
- Utilizes [faster-whisper](https://github.com/SYSTRAN/faster-whisper) with CTranslate2 for efficient transcription
- Implements Voice Activity Detection (VAD) for precise timestamp mapping
- Calculates absolute timestamps using: `absolute_start = segment_index * split_length + segment_start (0) + 1`

### Sentiment Analysis
- Leverages [pysentimiento](https://arxiv.org/pdf/2106.09462) with BERTweet model
- Provides three-way classification (Positive, Negative, Neutral)

![Benchmarks](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/Screenshot%202025-03-31%20at%201.08.20%E2%80%AFAM.png)

## 📱 Interface & Visualizations

### System Interface
![Start Screen](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/start.png)
![Processing View](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/running.png)

### Data Processing
![CSV Output](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/csv.png)
![Visualization Interface](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/viz.png)

### Analysis Outputs
![Sentiment Distribution](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/sentiment_distribution.png)
![Communication Pattern](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/transcription_histogram.png)

### User Interface Flow
![UI Main](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/ui.png)
![File Upload](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/ui_upload.png)
![Results Display](https://github.com/Kitsunnneee/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments-Screening-Test/blob/main/assets/plot_ui.png)

## 🧪 Quality Assurance

The system employs comprehensive unit testing using Python's `unittest` framework:

```bash
python -m unittest discover -s test -p "test_*.py" -v
```

### Test Coverage
- **Utilities**: Directory handling, audio extraction, and segmentation
- **Speech Processing**: Transcription accuracy and VAD functionality
- **Sentiment Analysis**: Classification validation
- **Visualization**: Plot generation verification
- **Interface**: Component validation and file handling

## 🔮 Future Developments

- Advanced sentiment analysis models
- Multi-speaker identification
- Enhanced user interface
- Integration of optimized speech processing engines
- Performance optimization for large-scale analysis



