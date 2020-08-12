---
title: "F1 SCORE"
author: "Rakshmitha"
date: 2020-08-11
description: "-"
type: technical_note
draft: false
---

```python
from sklearn.metrics import f1_score
```


```python
y_true = [0, 1, 2, 0, 1, 2]
y_pred = [0, 2, 1, 0, 0, 1]
```


```python
y_true
```




    [0, 1, 2, 0, 1, 2]




```python
y_pred
```




    [0, 2, 1, 0, 0, 1]




```python
f1_score_1 = f1_score(y_true, y_pred, average = 'macro')
```


```python
f1_score_1
```




    0.26666666666666666




```python
f1_score_2 = f1_score(y_true, y_pred, average = 'micro')
```


```python
f1_score_2
```




    0.3333333333333333




```python
f1_score_3 = f1_score(y_true, y_pred, average = 'weighted')
```


```python
f1_score_3
```




    0.26666666666666666




```python
f1_score_4 = f1_score(y_true, y_pred, average = None)
```


```python
f1_score_4
```




    array([0.8, 0. , 0. ])




```python
y_true = [0, 0, 0]
y_pred = [0, 0, 0]

f1_score(y_true, y_pred, zero_division = 1)
```




    1.0




```python

```
