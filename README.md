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

# 

# Bornomala/

# ├── data/

# │   ├── draft\_transcriptions\_FINAL.csv   # The main file to be annotated

# │   ├── segmented\_inventory.csv          # Metadata of all audio segments

# │   └── audio\_segments/                  # Audio files (Hosted on Drive)

# ├── notebooks/                           # Code for Mining, Segmentation \& Transcription

# ├── experiments/logs/                    # Execution logs

# └── docs/                                # Documentation

# 

# 

# \## 🚀 Research Roadmap

# 

# | Phase | Task | Status |

# | :--- | :--- | :--- |

# | \*\*1A\*\* | Problem Definition \& Ambiguity Analysis | ✅ Completed |

# | \*\*1B\*\* | Baseline Testing (Whisper Failure Proof) | ✅ Completed |

# | \*\*1C\*\* | Data Mining \& Segmentation (YouTube) | ✅ Completed |

# | \*\*2A\*\* | Automated Draft Transcription | ✅ Completed |

# | \*\*2B\*\* | \*\*Manual Annotation / Correction\*\* | 🟡 \*\*In Progress\*\* |

# | \*\*3\*\* | Active Learning Loop \& Fine-tuning | ⭕ Upcoming |

# 

# ---

# 

# \## 📝 Guide for Annotators (How to Contribute)

# 

# We use a \*\*Semi-Automated\*\* approach. You do not need to type from scratch.

# 

# \### Step 1: Download Data

# 1\.  \*\*CSV File:\*\* Download `data/draft\_transcriptions\_FINAL.csv` from this repository.

# 2\.  \*\*Audio Files:\*\* Download the audio clips from our Google Drive:

# &nbsp;   \* 🔗 \*\*\[Download Audio Files (Google Drive)](https://drive.google.com/drive/folders/1d6j1felhwS-HHJT4PgOL6Gi3-HWuwuHn)\*\*

# 

# \### Step 2: Start Annotation

# 1\.  Open the CSV file in \*\*Excel\*\* or \*\*Google Sheets\*\*.

# 2\.  Play an audio file (e.g., `Sylheti\_seg001.wav`).

# 3\.  Check the `machine\_transcript` column (It will likely be incorrect/Hindi).

# 4\.  Write the \*\*Standard Bengali (শুদ্ধ বাংলা)\*\* meaning in the `human\_correction` column.

# 

# \### Example:

# | Audio File | Dialect | Machine Output (Wrong) | \*\*Human Correction (Correct)\*\* |

# | :--- | :--- | :--- | :--- |

# | `syl\_01.wav` | Sylheti | আমি যাইরাম গি (Dialect text) | \*\*আমি চলে যাচ্ছি\*\* |

# | `ctg\_05.wav` | Chittagonian | ইতারা খাইতে আছে (Dialect text) | \*\*তারা খাচ্ছে\*\* |

# 

# \*\*Note:\*\* Always normalize to Standard Bengali grammar. Do not write the dialect spelling unless instructed otherwise.

# 

# ---

# 

# \## 🛠️ Technology Stack

# \* \*\*ASR Model:\*\* OpenAI Whisper (Medium/Large-v2)

# \* \*\*Preprocessing:\*\* Silero VAD, FFmpeg

# \* \*\*Environment:\*\* Kaggle P100 GPU / Colab Pro

# \* \*\*Framework:\*\* PyTorch, HuggingFace

# 

# \## 👨‍💻 Author

# \*\*Swagotam Malakar\*\*

# \* Research Domain: NLP \& Speech Processing

# \* GitHub: \[@smalakar-is-here](https://github.com/smalakar-is-here)

