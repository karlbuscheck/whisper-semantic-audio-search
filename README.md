# Semantic Audio Search With Whisper

This repo contains a lightweight, end-to-end pipeline for searching long-form audio *by meaning*, not keywords.

## The Pipeline:
- Transcribing a long-form audio clip using OpenAI’s Whisper (`small`) model
- Splitting the transcript using Whisper segments  
- Embedding each segment with a sentence transformer (`all-MiniLM-L6-v2`)  
- Using FAISS to retrieve the most relevant moments in the audio for a natural-language query

## Models Used:
- **Speech-to-text**: [OpenAI Whisper (small)](https://huggingface.co/openai/whisper-small)
- **Text embeddings**: [Sentence-Transformers all-MiniLM-L6-v2](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)

## Notebook:
The full walkthrough can be found in:
`whisper_semantic_audio_search.ipynb`

This architecture generalizes to podcasts, YouTube videos, Zoom meetings, lectures, and any long-form audio where semantic retrieval matters more than exact words.

*Note:* GitHub may not render notebook outputs correctly. For full execution and visible outputs, open and run the notebook in **Google Colab**: 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/karlbuscheck/whisper-semantic-audio-search/blob/main/whisper_semantic_audio_search.ipynb)
