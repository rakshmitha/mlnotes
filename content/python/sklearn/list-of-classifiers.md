---
title: "CLASSIFIERS"
author: "Rakshmitha"
date: 2020-08-11
description: "-"
type: technical_note
draft: false
---

```python
from sklearn.naive_bayes import MultinomialNB
from sklearn.naive_bayes import GaussianNB
from sklearn.naive_bayes import BernoulliNB
from sklearn.svm import SVC
from sklearn.neural_network import MLPClassifier
from sklearn.ensemble import AdaBoostClassifier
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
from sklearn.ensemble import GradientBoostingClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import GridSearchCV
from sklearn.metrics import f1_score, confusion_matrix
```


```python
clfs = {
    'mnb': MultinomialNB(),
    'gnb': GaussianNB(),
    'svm1': SVC(kernel='linear'),
    'svm2': SVC(kernel='rbf'),
    'svm3': SVC(kernel='sigmoid'),
    'mlp1': MLPClassifier(),
    'mlp2': MLPClassifier(hidden_layer_sizes=[100, 100]),
    'ada': AdaBoostClassifier(),
    'dtc': DecisionTreeClassifier(),
    'rfc': RandomForestClassifier(),
    'gbc': GradientBoostingClassifier(),
    'lr': LogisticRegression()
}
```


```python
f1_scores = dict()

for clf_name in clfs:
    
    clf = clfs[clf_name]
    clf.fit(train_x, test_x)
    y_pred = clf.predict(train_y)
    f1_scores[clf_name] = f1_score(y_pred, test_y)
    print(clf_name, f1_scores[clf_name])
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-4-ef6e1d292092> in <module>
          4 
          5     clf = clfs[clf_name]
    ----> 6     clf.fit(train_x, test_x)
          7     y_pred = clf.predict(train_y)
          8     f1_scores[clf_name] = f1_score(y_pred, test_y)


    NameError: name 'train_x' is not defined



```python

```
