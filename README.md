Speech/Audio → Text → Translation → Speech (GCP)

# Speech Translation Toolkit

A small Python toolkit that demonstrates a pipeline for:
1. Speech-to-text (transcribe audio stored in Google Cloud Storage)  
2. Text translation using Google Cloud Translation REST API  
3. Text-to-speech via Google Text-to-Speech REST API

This repository is based on the example script `Speech translation.py`. :contentReference[oaicite:1]{index=1}

> **Note:** The script contains hard-coded paths and API keys for demonstration. **Do not commit** credentials to source control. See SECURITY.md for safe configuration.

## Features
- Long-running transcription of audio files in Google Cloud Storage (GCS) using `google-cloud-speech`.
- Text translation via Google Cloud Translation REST endpoint.
- Simple Text-to-Speech using Google Text-to-Speech REST endpoint and saving MP3 output.

## Requirements
- Python 3.8+ recommended
- Google Cloud project with:
  - Speech-to-Text enabled
  - Cloud Translation API enabled
  - (optional) Text-to-Speech enabled (or use REST endpoint with API key)
- A service account JSON key with appropriate IAM roles (Speech and Translation or Owner for testing).

## Python dependencies
Install the minimal dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install google-cloud-speech requests
# Optionally:
python -m pip install google-cloud-translate google-cloud-texttospeech

