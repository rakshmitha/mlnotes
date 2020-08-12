---
title: "NORMALIZE USING SPACY"
author: "Rakshmitha"
date: 2020-08-11
description: "-"
type: technical_note
draft: false
---

```python
import spacy
from spacy.lang.en.stop_words import STOP_WORDS
nlp = spacy.load('en')
```


```python
def normalize(msg):
    doc = nlp(msg)
    res=[]
     #for sent in doc.sents:
     #   print(sent.text)
    for token in doc:        
        if(token.is_stop or token.is_digit or token.is_punct or token.is_oov):
            pass
        else: 
            res.append(token.lemma_.lower())
    return res
```


```python
normalize('spaCy is an open-source software library for advanced natural language processing, written in the programming languages Python and Cython. The library is published under the MIT license and its main developers are Matthew Honnibal and Ines Montani, the founders of the software company Explosion.')
```




    []




```python

```
