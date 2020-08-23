---
title: "CREATE A DATAFRAME FROM DICT OF NDARRAYS OR LISTS"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---
## Create a DataFrame from Dict of ndarrays / Lists
All the ndarrays must be of same length. If index is passed, then the length of the index should equal to the length of the arrays.

If no index is passed, then by default, index will be range(n), where n is the array length.


```python
import pandas as pd
```


```python
data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],'Age':[28,34,29,42]}
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
      <th>Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Tom</td>
      <td>28</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jack</td>
      <td>34</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Steve</td>
      <td>29</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Ricky</td>
      <td>42</td>
    </tr>
  </tbody>
</table>
</div>



Observe the values 0,1,2,3. They are the default index assigned to each using the function range(n)

### Indexed DataFrame using arrays.


```python
data = {'Name':['Tom', 'Jack', 'Steve', 'Ricky'],'Age':[28,34,29,42]}
df = pd.DataFrame(data, index=['rank1','rank2','rank3','rank4'])
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
      <th>rank1</th>
      <td>Tom</td>
      <td>28</td>
    </tr>
    <tr>
      <th>rank2</th>
      <td>Jack</td>
      <td>34</td>
    </tr>
    <tr>
      <th>rank3</th>
      <td>Steve</td>
      <td>29</td>
    </tr>
    <tr>
      <th>rank4</th>
      <td>Ricky</td>
      <td>42</td>
    </tr>
  </tbody>
</table>
</div>



the index parameter assigns an index to each row


```python

```
