---
layout: post
title: Confusion Matrix
tags:
- statistics
- prediction
- recall
- precision
- classification

mathjax: true
---

Among the  ways of measuring the performance of prediction by n machine learning or statistical analysis, there is __Confusion Matrix__(or Error Matrix).

The Confusion Matrix is a type of __contingency table__(or Pivot Table), where data are presented in cross tabulated format. It displays the interrelation betwee two variables and often used to find interactions between those variables.

### True Positive, True Negative, False Positive, False Negative

If you are making a prediction about a binary case, four types of results can be expected:
<br>

| Prediction | Actual Value |
|:--------:|:--------:|
|   0     |      0  | >> True Negative  (TN)
|    0    |     1   | >> False Negative (FN)
|    1    |   0     | >> False Positive (FP)
|    1    |   1     | >> True Positive  (TP)

<br>
To facilitate understanding or memorizing the concepts above, the naming of TN, FN, FP, TP is based on the prediction. 
- If the prediction is __right__, it is __True__
- If the prediction is __0__, it is __Negative__
- And if the prediction is __0__ and __right__, it is __True Negative__
<br>

### Terminology and Measurements from Confusion Matrix

#### Recall=Sensitivity=Hit Rate=True Positive Rate(TPR)
Summarizes how well the model predicts or classifies the positive(1) data. The value is calculated by dividing the __whole actual positive__ data by __correctly predicted positive__ data. (True Positive)

<br>
#### Specificity=Selectivity=True Negative Rate(TNR)
Specificity is similar to Recall or Sensitivity, but retrieving the rate of __correctly predicted negative__ data (True Negative) to the __whole actual negative__ data.

<br>
#### Fallout=False Positive Rate(FPR)
This concept refers to falsely predicted rate of predicting __actual positive__ data __negatively__.
<br>
#### Miss Rate=False Negative Rate(FNR)
This concept refers to falsely predicted rate of predicting __actual negative__ data __positively__.

<br>
#### Precision=Positive Predictive Value(PPV)
Precision is about being precise with the prediction. It tells how __likely__ the __predictive positive__ will be __correct__.

<br>
#### Accuracy(ACC)
Percentage of getting __the predictions right__. This summarizes how well (accurate) the model predicts or classifies.
<br>
<br>

## Performance Metrics 

#### R.O.C Curve (Receiver Operating Characteristics)
- The ROC curve has Specificity(False Positive Rate) and Sensitivity(True Positive Rate) as the two axis.

- The higher the curve is above y=x graph, the better the performance of a model is.

- However, ROC is an illustrated graph of FP and TP. And it is difficult for comparing models in some cases where the difference is not intuitively noticable. Thus, __AUC__ (Area under Curve) is used as a parameter. 

- The ROC AUC value is area of the ROC curve. The highest value is 1, and the better the model, the higher the AUC value is.

<br>

#### Precision Recall Plot (PR Graph)

<br>
#### F1-Score

<br>

<br><br>
## Python Code Example

```python
from sklearn.metrics import classification_report as clr
from sklearn.metrics import confusion_matrix as cm

# Confusion Matrix (TP,FP,TN,FN)
print(cm(test_y     # List of Actual Values
        , pred_y))  # List of Predicted Values


# Classification Report (Precision, Recall, F1-Score)
print(clr(test_y    # List of Actual Values
        , pred_y))  # List of Predicted Values


```

