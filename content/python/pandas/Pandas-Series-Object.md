---
title: "Pandas Series Object"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---

```python
import numpy as np
import pandas as pd
```


```python
data = pd.Series([0.25, 0.5, 0.75, 1.0])
```


```python
data
```




    0    0.25
    1    0.50
    2    0.75
    3    1.00
    dtype: float64



Series wraps both a sequence of values and a sequence of indices, which we can access with the values and index attributes.


```python
data.values
```




    array([0.25, 0.5 , 0.75, 1.  ])



The index is an array-like object of type pd.Index


```python
data.index
```




    RangeIndex(start=0, stop=4, step=1)



data can be accessed by the associated index via the square-bracket notation


```python
data[1]
```




    0.5




```python
data[1:3]
```




    1    0.50
    2    0.75
    dtype: float64




```python

```
