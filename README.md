# \# Bornomala: Bangla Dialect Normalization Project 🇧🇩

# 

# \*\*Bornomala\*\* is a research initiative aimed at bridging the gap between regional Bangla dialects (e.g., Sylheti, Chittagonian, Noakhali) and Standard Colloquial Bengali (SCB). Using \*\*Active Learning\*\*, we are building robust Speech-to-Text models that can understand dialects and transcribe them into standard Bengali syntax.

# 

# \## 🎯 Objective

# Current ASR models (like Whisper) fail on regional dialects, often hallucinating Hindi or Gibberish. Our goal is to:

# 1\.  \*\*Curate\*\* a high-quality dialect dataset from real-world sources (Dramas, Vlogs).

# 2\.  \*\*Normalize\*\* dialect speech to standard text (e.g., \*"I go-ram"\* → \*"Ami jacchi"\*).

# 3\.  \*\*Train\*\* a fine-tuned Whisper model using an Active Learning loop to minimize manual annotation effort.

# 

# \## 📂 Project Structure

# ```text

# Bornomala/

# ├── data/

# │   ├── audio\_segments/    # Short 10-20s audio clips (Not on GitHub, stored locally/Drive)

# │   ├── metadata/          # Inventory CSVs and logs

# │   └── drafts/            # Model-generated drafts awaiting human correction

# ├── notebooks/             # Kaggle/Colab notebooks for Mining, Segmentation \& Training

# ├── experiments/           # Training logs and Metric reports

# └── docs/                  # Annotation guidelines

\## 🚀 Research Roadmap



| Phase | Task | Status |

| :--- | :--- | :--- |

| \*\*1A\*\* | Problem Definition \& Ambiguity Analysis | ✅ Completed |

| \*\*1B\*\* | Baseline Testing (Whisper Failure Proof) | ✅ Completed |

| \*\*1C\*\* | Data Mining \& Segmentation (YouTube) | ✅ Completed |

| \*\*2A\*\* | Automated Draft Transcription | ✅ Completed |

| \*\*2B\*\* | \*\*Manual Annotation / Correction\*\* | 🟡 \*\*In Progress\*\* |

| \*\*3\*\* | Active Learning Loop \& Fine-tuning | ⭕ Upcoming |



\## 📝 Guide for Annotators (How to Contribute)



We use a \*\*Semi-Automated\*\* approach. You do not need to type from scratch.



1\.  \*\*Download Data:\*\* Get the `draft\_transcriptions\_FINAL.csv` and the Audio folder.

2\.  \*\*Open CSV:\*\* Open the file in Excel or Google Sheets.

3\.  \*\*Listen \& Correct:\*\*

&nbsp;   \* Play the audio file (e.g., `Sylheti\_seg001.wav`).

&nbsp;   \* Check the `machine\_transcript` column (It will likely be wrong).

&nbsp;   \* Write the \*\*Standard Bengali (শুদ্ধ বাংলা)\*\* meaning in the `human\_correction` column.



\### Example:

| Audio File | Dialect | Machine Output (Wrong) | \*\*Human Correction (Correct)\*\* |

| :--- | :--- | :--- | :--- |

| `syl\_01.wav` | Sylheti | আমি যাইরাম গি (Dialect text) | \*\*আমি চলে যাচ্ছি\*\* |

| `ctg\_05.wav` | Chittagonian | ইতারা খাইতে আছে (Dialect text) | \*\*তারা খাচ্ছে\*\* |



\*\*Note:\*\* Always normalize to Standard Bengali grammar. Do not write the dialect spelling unless instructed otherwise.



---



\## 🛠️ Technology Stack

\* \*\*ASR Model:\*\* OpenAI Whisper (Medium/Large-v2)

\* \*\*Preprocessing:\*\* Silero VAD, FFmpeg

\* \*\*Environment:\*\* Kaggle P100 GPU / Colab Pro

\* \*\*Framework:\*\* PyTorch, HuggingFace



\## 👨‍💻 Author

\*\*Swagotam Malakar\*\*

\* Research Domain: NLP \& Speech Processing

\* GitHub: \[@smalakar-is-here](https://github.com/smalakar-is-here)

