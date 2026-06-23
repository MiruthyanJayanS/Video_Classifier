# Video Classifier – Violence Detection

A Python-based tool that classifies videos as **Violent** or **Non-Violent** by extracting frames from the video and feeding them to a vision-capable LLM for classification.

## 📌 About

This project tackles video content moderation by breaking a video down into individual frames and passing them to a large language model with vision capabilities to assess whether the content is violent or non-violent. Several LLMs were experimented with during development before settling on **Gemini** and **Mistral** as the primary models used for classification, accessed via **Hugging Face**.

## 🛠️ Tech Stack

| Category | Tools / Models |
|---|---|
| Language | Python |
| Frame Extraction | Python video/image processing libraries (e.g. OpenCV) |
| Model Hosting | Hugging Face |
| LLMs Used | Gemini, Mistral (final models used after experimentation) |

## ⚙️ How It Works

1. **Frame Extraction** — the input video is processed frame-by-frame (or at sampled intervals) using a Python video-processing library
2. **Classification** — extracted frames are fed to a vision-capable LLM (Gemini / Mistral, via Hugging Face)
3. **Result** — the model's output is aggregated to classify the overall video as **Violent** or **Non-Violent**

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- Hugging Face account/API access (and API keys for Gemini/Mistral as applicable)
- Video processing library (e.g. `opencv-python`)

### Setup
```bash
git clone https://github.com/MiruthyanJayanS/Video_Classifier.git
cd Video_Classifier
pip install -r requirements.txt
```

### Configuration
Set up the required API keys/credentials for the LLMs used (Gemini, Mistral, Hugging Face) — typically via environment variables or a `.env` file. **Never commit API keys to the repository.**

### Running
```bash
python main.py
```
> Replace `main.py` with the actual entry-point filename used in the project.

## 🧪 Experimentation Note

Multiple LLMs were tested during development to find the most reliable model for this classification task, eventually narrowing down to **Gemini** and **Mistral** as the best-performing options.

## ⚠️ Notes

- This tool is intended for content moderation/research purposes.
- Classification accuracy depends on the underlying LLM and frame sampling strategy — results should be validated before use in any production or sensitive context.

## 🎯 Learning Outcomes

- Practical experience with frame-based video analysis
- Hands-on use of vision-capable LLMs for real-world classification tasks
- Comparing and evaluating multiple LLMs for a specific use case

## 📄 License

This repository is for personal learning, research, and portfolio purposes.
