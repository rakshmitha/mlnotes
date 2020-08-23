---
title: "DEFINING A DATAFRAME OBJECT"
author: "Rakshmitha"
date: 2020-08-13
description: "-"
type: technical_note
draft: false
---
# Pandas Dataframe
    
   A pandas dataframe is an extension of the Panda Series to have n-dimensions. This allows for a robust tabular structure of acccessing data. Much like a matrix, we can apply transformations to a dataframe as we would on a matrix.Below is an example of defining a dataframe object.

### Defining a Dataframe Object


```python
import pandasdf = pd.DataFrame( {'Country': ['USA', 'Canada', 'Mexico'],
            'Population': [325, 36, 127],
            'Year': [2018, 2017, 2017]})
df as pd
```


```python
df = pd.DataFrame( {'Country': ['USA', 'Canada', 'Mexico'],
            'Population': [325, 36, 127],
            'Year': [2018, 2017, 2017]})
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
      <th>Country</th>
      <th>Population</th>
      <th>Year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>USA</td>
      <td>325</td>
      <td>2018</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Canada</td>
      <td>36</td>
      <td>2017</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Mexico</td>
      <td>127</td>
      <td>2017</td>
    </tr>
  </tbody>
</table>
</div>



We see above the tabular structure of the dataframe. let's change the index

### Changing Index


```python
df.set_index('Country', inplace=True)
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
      <th>Population</th>
      <th>Year</th>
    </tr>
    <tr>
      <th>Country</th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>USA</th>
      <td>325</td>
      <td>2018</td>
    </tr>
    <tr>
      <th>Canada</th>
      <td>36</td>
      <td>2017</td>
    </tr>
    <tr>
      <th>Mexico</th>
      <td>127</td>
      <td>2017</td>
    </tr>
  </tbody>
</table>
</div>



What is the use of inplace in pandas?

When inplace = True is used, it performs operation on data and nothing is returned. When inplace=False is used, it performs operation on data and returns a new copy of data.


```python

```
