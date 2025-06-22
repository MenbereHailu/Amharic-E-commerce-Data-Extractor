# 📦 EthioMart Telegram Amharic Preprocessing Pipeline

This project processes and cleans Amharic-language messages collected from Ethiopian Telegram e-commerce channels.  
It uses:

- ✅ [**etnltk**](https://github.com/robeleq/etnltk) for Amharic NLP (normalization, tokenization, cleaning)
- ✅ [**DVC**](https://dvc.org) for version control and data tracking
- ✅ `pandas` and `nltk` for text processing and manipulation

---
## 🔧 Setup Instructions

### 1. Clone Your Project Repo

```bash
git clone https://github.com/MenbereHailu/Amharic-E-commerce-Data-Extractor.git
cd Amharic-E-commerce-Data-Extractor
```
## 🔧 Setup Instructions

1. Clone this repository  
2. Create and activate a virtual environment  
3. Install Python dependencies from `requirements.txt`  
4. Clone and install the [etnltk](https://github.com/robeleq/etnltk) library  
5. Run the preprocessing script  
6. Track and version cleaned output using DVC  

---

## ⚙️ Description of Preprocessing Script

- Reads raw Telegram messages from CSV  
- Applies Amharic normalization and cleaning using `etnltk`  
- Tokenizes into sentences and words  
- Saves output CSV with `UTF-8-SIG` encoding for Excel compatibility  

### Output Columns:
- `text`: Original message  
- `cleaned_text`: Cleaned and normalized message  
- `sentences`: Sentence tokens  
- `words`: Word tokens  

---

## 💾 DVC Setup Instructions

1. Run `dvc init` to initialize tracking  
2. Use `dvc add data/processed/telegram_cleaned_etnltk.csv` to track the cleaned data  
3. Commit DVC metadata with Git:  
   ```bash
   git add .  
   git commit -m "Track cleaned Telegram data with DVC"

