---
title: "COLUMN RENAME"
author: "Rakshmitha"
date: 2020-08-12
description: "-"
type: technical_note
draft: false
---

```python
import pandas as pd
```


```python
data = ['Vachitaya aapuuuuuuuuu','Sing in the rain' ,'Great power comes wih great responsibility']  
df = pd.DataFrame(data, columns = ['Sent'])
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
      <th>Sent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Vachitaya aapuuuuuuuuu</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Sing in the rain</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Great power comes wih great responsibility</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.columns = ['Sentence']
```


```python
df.head()
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
      <th>Sentence</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Vachitaya aapuuuuuuuuu</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Sing in the rain</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Great power comes wih great responsibility</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.rename(columns={'Sentence':'my_sent'},inplace=True)
```


```python
df.head()
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
      <th>my_sent</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Vachitaya aapuuuuuuuuu</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Sing in the rain</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Great power comes wih great responsibility</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
