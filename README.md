# Bornomala: Bangla Dialect Normalization Project 🇧🇩

Bornomala is a research initiative aimed at bridging the gap between regional Bangla dialects (Sylheti, Chittagonian, Noakhali) and Standard Colloquial Bengali (SCB). Using Active Learning, we aim to build robust Speech-to-Text systems capable of understanding dialectal Bangla and transcribing it into normalized standard Bengali text.

## Objective

Current ASR models such as Whisper fail on regional Bangla dialects and often hallucinate Hindi or gibberish text. The goals of this project are:

1. Curate a high-quality Bangla dialect speech dataset from real-world sources such as dramas and vlogs.
2. Normalize dialect speech into standard Bengali grammar.
3. Fine-tune Whisper using an Active Learning loop to reduce manual annotation cost.

## Project Structure

Bornomala/
- data/
  - draft_transcriptions_FINAL.csv (main annotation file)
  - segmented_inventory.csv (audio segment metadata)
  - audio_segments/ (audio files hosted on Drive)
- notebooks/ (mining, segmentation and transcription code)
- experiments/logs/ (execution logs)
- docs/ (documentation)

## Research Roadmap

Phase | Task | Status
----- | ---- | ------
1A | Problem Definition and Ambiguity Analysis | Completed
1B | Baseline Testing (Whisper Failure Proof) | Completed
1C | Data Mining and Segmentation (YouTube) | Completed
2A | Automated Draft Transcription | Completed
2B | Manual Annotation and Correction | In Progress
3 | Active Learning Loop and Fine-tuning | Upcoming

## Guide for Annotators

This project follows a semi-automated annotation approach. Annotators are not required to transcribe from scratch.

### Step 1: Download Data

- CSV file: data/draft_transcriptions_FINAL.csv
- Audio files: https://drive.google.com/drive/folders/1d6j1felhwS-HHJT4PgOL6Gi3-HWuwuHn

### Step 2: Annotation Instructions

1. Open the CSV file using Excel or Google Sheets.
2. Play the corresponding audio file.
3. Ignore errors in the machine_transcript column.
4. Write the correct Standard Bengali sentence in the human_correction column.

Example:

Audio File | Dialect | Machine Output | Human Correction
---------- | ------- | -------------- | ----------------
syl_01.wav | Sylheti | আমি যাইরাম গি | আমি চলে যাচ্ছি
ctg_05.wav | Chittagonian | ইতারা খাইতে আছে | তারা খাচ্ছে

Always normalize into standard Bengali grammar. Do not write dialect spellings unless explicitly instructed.

## Technology Stack

- ASR Model: OpenAI Whisper (Medium / Large-v2)
- Preprocessing: Silero VAD, FFmpeg
- Framework: PyTorch, HuggingFace
- Compute: Kaggle P100 GPU, Colab Pro

## Author

Swagotam Malakar  
Research Domain: NLP and Speech Processing  
GitHub: https://github.com/smalakar-is-here
