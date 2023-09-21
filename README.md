---
language:
- de
license: apache-2.0
tags:
- text-classification
- easy-language
- plain-language
- leichte-sprache
- einfache-sprache
- text-complexity
---


# Model Card for text-complexity-classification

The model classifies texts into the language complexity classes (German language):
- easy language / leichte Sprache
- simple language / einfache Sprache
- everyday language / Alltagssprache
- special language / Fachsprache

The underlying corpus was trained on the basis of over 300,000 texts of the mentioned language categories. Freely available websites served as sources. Thematic diversity was taken into account when selecting the sources.


- **Developed by:** Ruben Klepp
- **Language(s) (NLP):** de
- **License:** apache-2.0
- **Parent Model:** https://huggingface.co/deepset/gbert-base

## Evaluation
- **f1:** 0.982
- **Precision:** 0.981
- **Recall:** 0.983

## How to use
```python
>>> from transformers import pipeline
>>> classifier = pipeline(model="krupper/text-complexity-classification")
>>> classifier("Bei Kleinkindern unter 2 Jahren liegen nur begrenzte Erfahrungen zur Pharmakokinetik vor.")
[{'label': 'special_language', 'score': 0.999923825263977}]
```

DOI: [https://doi.org/10.57967/hf/0131](https://doi.org/10.57967/hf/0131)