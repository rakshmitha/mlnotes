---
title: "line-plot"
author: "Rakshmitha"
date: 2020-08-12
description: "-"
type: technical_note
draft: false
---

```python
import matplotlib.pyplot as plt
import pandas as pd
```


```python
data1 = {'objects': ['apple', 'banana', 'mango', 'orange', 'tomato', 'potato'], 'price':[4, 7, 12, 10, 9, 14]}
```


```python
plt.plot(data1['objects'], data1['price'])
```




    [<matplotlib.lines.Line2D at 0x7fbe0e47da00>]




![png](line-plot_3_1.png)



```python

```
