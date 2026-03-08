# NLP with NLTK, spaCy & displaCy

A hands-on Natural Language Processing project covering core NLP techniques — tokenization, stop word filtering, stemming, lemmatization, POS tagging, Named Entity Recognition (NER), and dependency visualization using **NLTK** and **spaCy**.

---

## Overview

This notebook walks through the fundamental building blocks of NLP using two popular Python libraries:
- **NLTK** — for classical NLP preprocessing
- **spaCy + displaCy** — for modern NLP and visualization

---

## Topics Covered

| Topic | Description |
|---|---|
| **Tokenization** | Splitting text into words and sentences |
| **Stop Word Filtering** | Removing common, low-meaning words |
| **Stemming** | Reducing words to their root form (e.g. *flying → fly*) |
| **Lemmatization** | Reducing words to their dictionary form |
| **POS Tagging** | Labeling grammatical roles (noun, verb, etc.) |
| **NER** | Identifying named entities (people, places, orgs) |
| **displaCy Visualization** | Rendering dependency parse trees and entity spans |

---

## Project Structure

```
nlp-spacy-displacy/
│
├── NLP_spaCy_displaCy.ipynb    # Main notebook
├── requirements.txt
└── README.md
```

---

## Tech Stack

| Library | Purpose |
|---|---|
| `nltk` | Tokenization, stemming, lemmatization, stop words |
| `spacy` | NER, POS tagging, dependency parsing |
| `displacy` | Visualization of NLP results |

---

## Getting Started

```bash
git clone https://github.com/your-username/nlp-spacy-displacy.git
cd nlp-spacy-displacy
pip install -r requirements.txt

# Download required NLTK data
python -c "import nltk; nltk.download('punkt'); nltk.download('stopwords'); nltk.download('wordnet')"

# Download spaCy English model
python -m spacy download en_core_web_sm

jupyter notebook NLP_spaCy_displaCy.ipynb
```

---

## Example — Named Entity Recognition

```python
raw_text = "The Indian Space Research Organisation is headquartered in Bengaluru."
text1 = NER(raw_text)
for word in text1.ents:
    print(word.text, word.label_)

# → Indian Space Research Organisation  ORG
# → Bengaluru  GPE
```
