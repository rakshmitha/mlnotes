---
title: "grid-spec"
author: "Rakshmitha"
date: 2020-08-12
description: "-"
type: technical_note
draft: false
---

```python
import matplotlib.pyplot as plt
from matplotlib.pyplot import GridSpec
fig2 = plt.figure(constrained_layout=True)
spec2 = GridSpec(ncols=2, nrows=2, figure=fig2)
f2_ax1 = fig2.add_subplot(spec2[0, 0])
f2_ax2 = fig2.add_subplot(spec2[0, 1])
f2_ax3 = fig2.add_subplot(spec2[1, 0])
f2_ax4 = fig2.add_subplot(spec2[1, 1])
```


![png](grid-spec_1_0.png)



```python

```
