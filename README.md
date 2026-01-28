# Bornomala: Bangla Dialect Normalization Project 🇧🇩

**Bornomala** is a research initiative aimed at bridging the gap between regional Bangla dialects (e.g., Sylheti, Chittagonian, Noakhali) and Standard Colloquial Bengali (SCB). Using **Active Learning**, we are building robust Speech-to-Text models that can understand dialects and transcribe them into standard Bengali syntax.

## 🎯 Objective

Current ASR models (like Whisper) fail on regional dialects, often hallucinating Hindi or Gibberish. Our goal is to:

1. **Curate** a high-quality dialect dataset from real-world sources (Dramas, Vlogs).
2. **Normalize** dialect speech to standard text (e.g., *"I go-ram"* → *"Ami jacchi"*).
3. **Train** a fine-tuned Whisper model using an Active Learning loop to minimize manual annotation effort.

## 📂 Project Structure

```
Bornomala/
├── data/
│   ├── draft_transcriptions_FINAL.csv   # The main file to be annotated
│   ├── segmented_inventory.csv          # Metadata of all audio segments
│   └── audio_segments/                  # Audio files (Hosted on Drive)
├── notebooks/                           # Code for Mining, Segmentation & Transcription
├── experiments/logs/                    # Execution logs
└── docs/                                # Documentation
```

## 🚀 Research Roadmap

| Phase | Task | Status |
| :--- | :--- | :--- |
| **1A** | Problem Definition & Ambiguity Analysis | ✅ Completed |
| **1B** | Baseline Testing (Whisper Failure Proof) | ✅ Completed |
| **1C** | Data Mining & Segmentation (YouTube) | ✅ Completed |
| **2A** | Automated Draft Transcription | ✅ Completed |
| **2B** | **Manual Annotation / Correction** | 🟡 **In Progress** |
| **3** | Active Learning Loop & Fine-tuning | ⭕ Upcoming |

---

## 📝 Guide for Annotators (How to Contribute)

We use a **Semi-Automated** approach. You do not need to type from scratch.

### Step 1: Download Data

1. **CSV File:** Download `data/draft_transcriptions_FINAL.csv` from this repository.
2. **Audio Files:** Download the audio clips from our Google Drive:
   - 🔗 [Download Audio Files (Google Drive)](https://drive.google.com/drive/folders/1d6j1felhwS-HHJT4PgOL6Gi3-HWuwuHn)

### Step 2: Start Annotation

1. Open the CSV file in **Excel** or **Google Sheets**.
2. Play an audio file (e.g., `Sylheti_seg001.wav`).
3. Check the `machine_transcript` column (It will likely be incorrect/Hindi).
4. Write the **Standard Bengali (শুদ্ধ বাংলা)** meaning in the `human_correction` column.

---

## ⚠️ Annotation Rules (Must Follow)

Please follow these rules strictly to ensure high-quality data:

### 1. Standard Bengali Only (শুদ্ধ বাংলা)

Always translate the dialect to Standard Colloquial Bengali. Do not write dialect spellings.

- ❌ Audio: "ইতারা খাইতে আছে" → Write: "ইতারা খাইতে আছে"
- ✅ Audio: "ইতারা খাইতে আছে" → Write: "তারা খাচ্ছে।"

### 2. Punctuation is Mandatory (বিরাম চিহ্ন)

You must use Dari (।) for statements and Question Mark (?) for questions.

- ❌ Write: তুমি কি আসবে
- ✅ Write: তুমি কি আসবে?

### 3. No English Text

If the audio contains English words, write them in Bengali script.

- ❌ Write: আমি University তে যাই।
- ✅ Write: আমি ইউনিভার্সিটিতে যাই।

### 4. Unclear Audio

If a word or sentence is completely unintelligible, use the tag `[অস্পষ্ট]`.

---

## 📋 Examples

| Audio File | Dialect | Machine Output (Wrong) | **Human Correction (Correct)** |
| :--- | :--- | :--- | :--- |
| `syl_01.wav` | Sylheti | আমি যাইরাম গি (Dialect text) | **আমি চলে যাচ্ছি।** |
| `ctg_05.wav` | Chittagonian | ইতারা খাইতে আছে (Dialect text) | **তারা খাচ্ছে।** |
| `noa_09.wav` | Noakhali | আর হুনছিনি খবর? | **আর খবর শুনেছ কি?** |

---

## 🛠️ Technology Stack

* **ASR Model:** OpenAI Whisper (Medium/Large-v2)
* **Preprocessing:** Silero VAD, FFmpeg
* **Environment:** Kaggle P100 GPU / Colab Pro
* **Framework:** PyTorch, HuggingFace

## 👨‍💻 Author

**Swagotam Malakar**

* Research Domain: NLP & Speech Processing
* GitHub: [@smalakar-is-here](https://github.com/smalakar-is-here)
