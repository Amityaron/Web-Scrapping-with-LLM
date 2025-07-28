# Web-Scrapping-with-LLM
Web Scrapping with LLM hugging face 

# 🔎 Web Scraping Breaking News from Ynet with Sentiment Analysis using Hugging Face LLM

## 📋 Overview

This project scrapes the latest breaking news headlines from the **Ynet News** website (in Hebrew), and applies **multilingual sentiment analysis** using a pre-trained language model from Hugging Face.

The pipeline consists of:
1. **Web scraping** news headlines from Ynet's "Breaking News" section.
2. Sending each headline to a **sentiment classification model** via Hugging Face Inference API.
3. Storing and displaying the **headline and its predicted sentiment** in a structured dataframe.

---

## 🤗 Sentiment Model

We use the following Hugging Face model for multilingual sentiment classification:




This model returns sentiment scores from 1 to 5 stars, which we map to:
- 1–2 stars → `negative`
- 3 stars → `neutral`
- 4–5 stars → `positive`

---

## 📰 Example Output

The result is a pandas DataFrame containing headlines and their corresponding sentiment:

| text                                                                | sentiment |
|---------------------------------------------------------------------|-----------|
| לפיד:  "מי שאחראי על הרעב בעזה הוא חמאס"                            | negative  |
| דיווחים בלבנון:  פצוע בתקיפת אופנוע בדרום המדינה                    | negative  |
| ראש אכ"א  נפגש עם נציגי מילואימניקים: בשנה הבאה...                   | negative  |
| 3  לוחמי הנח"ל שסירבו להיכנס לעזה לא ייאסרו                          | negative  |
|  גרמניה תעביר אספקת סיוע מהאוויר לרצועה                             | positive  |

---

## ⚙️ Installation & Usage

### Prerequisites

- Python 3.7+
- `requests`, `bs4`, `pandas`

### Install dependencies

```bash
pip install requests beautifulsoup4 pandas
