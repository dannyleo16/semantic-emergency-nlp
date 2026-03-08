# Semantic Emergency Analysis using NLP

This project analyzes emergency call transcripts using Natural Language Processing (NLP) and transformer-based models.

The system extracts relevant entities such as persons and locations from emergency reports.

---

## Overview

Emergency reports contain critical information in unstructured text.

This project explores how NLP techniques can transform those reports into structured information for decision support systems.

---

## Technologies

Python  
Hugging Face Transformers  
PyTorch  
BERT  
Named Entity Recognition  
Pandas  
Scikit-learn

---

## Hugging Face Model

NER model trained for Spanish emergency reports:

https://huggingface.co/dannyLeo16/ner_model_bert_base

---

## Example Usage

```python
from transformers import pipeline

ner = pipeline(
    "ner",
    model="dannyLeo16/ner_model_bert_base",
    tokenizer="dannyLeo16/ner_model_bert_base"
)

text = "Hay una persona herida en la avenida Loja"

result = ner(text)

print(result)
