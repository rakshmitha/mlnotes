---
title: "METRICS"
author: "TACT"
date: 2019-04-20
description: "-"
type: technical_note
draft: false
---

```python
from sklearn import metrics
```


```python
C="Cat"
F="Fish"
H="Hen"
```


```python
y_true = [C,C,C,C,C,C, F,F,F,F,F,F,F,F,F,F, H,H,H,H,H,H,H,H,H]
y_pred = [C,C,C,C,H,F, C,C,C,C,C,C,H,H,F,F, C,C,C,H,H,H,H,H,H]
```


```python
print(metrics.confusion_matrix(y_true, y_pred))
```

    [[4 1 1]
     [6 2 2]
     [3 0 6]]



```python
print(metrics.classification_report(y_true, y_pred, digits=3))
```

                  precision    recall  f1-score   support
    
             Cat      0.308     0.667     0.421         6
            Fish      0.667     0.200     0.308        10
             Hen      0.667     0.667     0.667         9
    
        accuracy                          0.480        25
       macro avg      0.547     0.511     0.465        25
    weighted avg      0.581     0.480     0.464        25
    



```python

```
