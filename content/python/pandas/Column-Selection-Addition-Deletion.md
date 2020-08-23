---
title: "SELECTION, ADDITION, DELETION"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---
## Selection


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
df ['one']
```




    a    1.0
    b    2.0
    c    3.0
    d    NaN
    Name: one, dtype: float64



## Addition

Adding a new column by passing as Series


```python
df['three']=pd.Series([10,20,30],index=['a','b','c'])
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
      <th>three</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>1.0</td>
      <td>1</td>
      <td>10.0</td>
    </tr>
    <tr>
      <th>b</th>
      <td>2.0</td>
      <td>2</td>
      <td>20.0</td>
    </tr>
    <tr>
      <th>c</th>
      <td>3.0</td>
      <td>3</td>
      <td>30.0</td>
    </tr>
    <tr>
      <th>d</th>
      <td>NaN</td>
      <td>4</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



Adding a new column using the existing columns in DataFrame


```python
df['four']=df['one']+df['three']
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
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>1.0</td>
      <td>1</td>
      <td>10.0</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>b</th>
      <td>2.0</td>
      <td>2</td>
      <td>20.0</td>
      <td>22.0</td>
    </tr>
    <tr>
      <th>c</th>
      <td>3.0</td>
      <td>3</td>
      <td>30.0</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>d</th>
      <td>NaN</td>
      <td>4</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



## Deletion
### using del function
del : del removes the item at a specific index. lets say del list[index]


```python
del df['one']
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
      <th>two</th>
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>1</td>
      <td>10.0</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>b</th>
      <td>2</td>
      <td>20.0</td>
      <td>22.0</td>
    </tr>
    <tr>
      <th>c</th>
      <td>3</td>
      <td>30.0</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>d</th>
      <td>4</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



### using pop function
pop removes the item at a specific index and returns it. lets say list.pop(index)


```python
df.pop('two')
```




    a    1
    b    2
    c    3
    d    4
    Name: two, dtype: int64




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
      <th>three</th>
      <th>four</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>a</th>
      <td>10.0</td>
      <td>11.0</td>
    </tr>
    <tr>
      <th>b</th>
      <td>20.0</td>
      <td>22.0</td>
    </tr>
    <tr>
      <th>c</th>
      <td>30.0</td>
      <td>33.0</td>
    </tr>
    <tr>
      <th>d</th>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>


