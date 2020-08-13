---
title: "initialize a series"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---
# Series
A series is a one-dimensional vector that contains an array of data. 


```python
import pandas as pd
```


```python
s = pd.Series([1, 2, 3, 4, 5])
```


```python
s
```




    0    1
    1    2
    2    3
    3    4
    4    5
    dtype: int64



The output from the above initialization is a one-dimensional matrix with indexing on integers to allow for accessing specific locations of the array values. We can alter the indexes to our own naming as follows


```python
s = (['a', 'b', 'c', 'd', 'e'])
```


```python
s
```




    ['a', 'b', 'c', 'd', 'e']




```python

```
