---
title: "Create a DataFrame from Dict of Series"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---
Dictionary of Series can be passed to form a DataFrame. The resultant index is the union of all the series indexes passed.


```python
import pandas as pd
```


```python
d = {'one' : pd.Series([1, 2, 3], index=['a', 'b', 'c']),
   'two' : pd.Series([1, 2, 3, 4], index=['a', 'b', 'c', 'd'])}
```


```python
df = pd.DataFrame(d)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>one</th>
      <th>two</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>1.0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>b</th>
      <td>2.0</td>
      <td>2</td>
    </tr>
    <tr>
      <th>c</th>
      <td>3.0</td>
      <td>3</td>
    </tr>
    <tr>
      <th>d</th>
      <td>NaN</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>



for the series one, there is no label ‘d’ passed, but in the result, for the d label, NaN is appended with NaN.
