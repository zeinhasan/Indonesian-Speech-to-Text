# Indonesian-Speech-to-Text
Speech to Text for Indonesian Language

# Whisper: Robust Speech Recognition via Large-Scale Weak Supervision
## A. Background and Motivation
Whisper, developed by OpenAI, is designed to improve the robustness of speech recognition systems. Traditional methods like Wav2Vec 2.0 leverage large datasets of unsupervised, unlabeled speech to produce high-quality audio encoders. However, many of these models require complex fine-tuning stages, limiting their real-world usability. The motivation behind Whisper is to create a speech recognition model that operates reliably without the need for extensive fine-tuning, leveraging weakly supervised data from the web. The goal is to create a versatile model that generalizes well across languages, tasks, and various environments, making it applicable "out of the box" without task-specific adjustments​(2212.04356v1). 
## B. Key Innovations
Whisper introduces several innovations that distinguish it from previous models:
1. **Weak Supervision at Scale**: Whisper is trained on 680,000 hours of labeled audio data, much of which is weakly supervised (collected from the internet with automatically generated transcripts). This vast training corpus allows Whisper to generalize to a wide range of languages and domains without fine-tuning.
2. **Multilingual and Multitask Training**: Whisper includes 117,000 hours of data in 96 languages and 125,000 hours of translation data, enabling it to handle transcription and translation tasks for many languages.
3. **Zero-shot Transfer**: Whisper demonstrates strong zero-shot transfer capabilities, which means it performs well on various benchmarks without being explicitly trained or fine-tuned for specific datasets. This innovation emphasizes robust generalization and cross-domain application​(2212.04356v1)​.
## C. Architecture of Whisper
![Arch](approach.png)

Whisper uses a sequence-to-sequence Transformer architecture, similar to models like GPT-2 but adapted for speech processing. The architecture consists of an encoder-decoder framework:
1.  **Input Representation**: The input audio is converted into 16,000 Hz audio, and an 80-channel log-magnitude Mel spectrogram is computed, which forms the input for the model.
2.  **Encoder**: The encoder processes the Mel spectrogram through a series of convolutional layers followed by Transformer blocks. Sinusoidal positional embeddings are added, and the encoder generates contextualized speech features.
3.  **Decoder**: The decoder is tasked with generating text, predicting both transcription and translation sequences. It uses learned positional embeddings and is designed to handle various speech tasks (transcription, translation, voice activity detection, etc.) through a unified output token format.
4.  **Task-Specific Tokens**: Whisper uses tokens to indicate the language, task (transcription or translation), and timestamp, allowing for multitask outputs from a single model. For example, tokens like `<|transcribe|>` or `<|translate|>` help the model decide which task to perform based on the input (2212.04356v1).

## Implmentation
Here the link for testing streamlit app
```
https://whisper-zein.streamlit.app/
```

## Instalation
Follow this link to guide the instalation
```
https://github.com/zeinhasan/Whisper-AI-for-Bahasa-Indonesia
```