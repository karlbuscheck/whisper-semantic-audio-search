# Semantic Audio Search With Whisper

This repo contains a lightweight, end-to-end pipeline for searching long-form audio *by meaning*, not keywords.

## The Pipeline:
- Transcribing a long-form audio clip using OpenAI’s Whisper (`small`) model
- Splitting the transcript using Whisper segments  
- Embedding each segment with a sentence transformer (`all-MiniLM-L6-v2`)  
- Using FAISS to retrieve the most relevant moments in the audio for a natural-language query

The result is a fast, interpretable semantic search system that returns *what was said* and *exactly when it was said*. This architecture is generalizable to all sorts of audio-first knowledge retrieval tasks, from searching meeting notes to YouTube videos -- any long-form audio where *meaning* matters more than exact words.

## Models Used:
- **Speech-to-text**: [OpenAI Whisper (small)](https://github.com/openai/whisper)
- **Text embeddings**: [Sentence-Transformers all-MiniLM-L6-v2](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)

## Notebook:
The full walkthrough can be found in:
`whisper_semantic_audio_search.ipynb`
