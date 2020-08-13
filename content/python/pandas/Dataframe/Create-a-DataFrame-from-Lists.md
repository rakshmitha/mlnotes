---
title: "CREATE A DATAFRAME FROM LISTS"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---
## Create a DataFrame from Lists
The DataFrame can be created using a single list or a list of lists.


```python
import pandas as pd
```


```python
data = [1,2,3,4,5]
df = pd.DataFrame(data)
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
      <th>0</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>




```python
data = [['Alex',10],['Bob',12],['Clarke',13]]
df = pd.DataFrame(data,columns=['Name','Age'])
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
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Alex</td>
      <td>10</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Bob</td>
      <td>12</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Clarke</td>
      <td>13</td>
    </tr>
  </tbody>
</table>
</div>




```python
data = [['Alex',10],['Bob',12],['Clarke',13]]
df = pd.DataFrame(data,columns=['Name','Age'],dtype=float)
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
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Alex</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Bob</td>
      <td>12.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Clarke</td>
      <td>13.0</td>
    </tr>
  </tbody>
</table>
</div>



the dtype parameter changes the type of Age column to floating point.


```python

```
