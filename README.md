# 🎙️ AI Model for Identifying Emotional States from Speech

This project uses a fine-tuned **Wav2Vec2** model to classify **seven emotional states** (Angry, Disgust, Fear, Happy, Neutral, Pleasant Surprise, Sad) from raw audio data. It is built using the **Toronto Emotional Speech Set (TESS)** and Hugging Face Transformers.

## 📌 Table of Contents
- [About the Project](#about-the-project)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Limitations](#limitations)
- [Future Work](#future-work)

---

## 📖 About the Project

Emotions in speech convey important cues beyond words—tone, rhythm, and pitch all carry emotional weight. This project aims to build an AI system that can recognize these emotions directly from audio using modern transformer-based architectures.

Key applications include:
- Emotion-aware virtual assistants
- Mental health tracking
- Customer service sentiment analysis
- Human-computer interaction enhancements

---

## 📁 Dataset

We used the **Toronto Emotional Speech Set (TESS)**:
- 2,800 labeled WAV audio clips
- 2 female speakers (aged 26 & 64)
- 7 emotions: Angry, Disgust, Fear, Happy, Neutral, Pleasant Surprise, Sad
- Format: 16kHz, mono-channel

---

## 🧠 Model Architecture

- **Base Model**: [`facebook/wav2vec2-base`](https://huggingface.co/facebook/wav2vec2-base)
- **Classification Head**: Custom linear layer for 7 emotion classes
- **Framework**: Hugging Face Transformers + PyTorch

### Training Configuration:
- Learning Rate: `2e-5`
- Batch Size: `16`
- Epochs: `3`
- No data augmentation or dropout
- Audio cropped/padded to `2.75 seconds`

---

## ⚙️ Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/emotion-recognition-speech.git
cd emotion-recognition-speech
pip install -r requirements.txt
