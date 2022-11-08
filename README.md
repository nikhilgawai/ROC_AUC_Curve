# ROC_AUC_Curve
## ROC curve

An ROC curve (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds. This curve plots two parameters:

True Positive Rate
False Positive Rate

True Positive Rate (TPR) is a synonym for recall and is therefore defined as follows:

# TPR = TP/TP+FN

False Positive Rate (FPR) is defined as follows:

# FPR = FP/FP+TN

An ROC curve plots TPR vs. FPR at different classification thresholds. Lowering the classification threshold classifies more items as positive, thus increasing both False Positives and True Positives. The following figure shows a typical ROC curve.

![ROC](https://user-images.githubusercontent.com/89011801/200486303-ac4f7c7c-beef-4e12-a56d-75a1e8a351e8.png)

To compute the points in an ROC curve, we could evaluate a logistic regression model many times with different classification thresholds, but this would be inefficient. Fortunately, there's an efficient, sorting-based algorithm that can provide this information for us, called AUC.

## AUC: Area Under the ROC Curve

AUC stands for "Area under the ROC Curve." That is, AUC measures the entire two-dimensional area underneath the entire ROC curve (think integral calculus) from (0,0) to (1,1).

![AUC](https://user-images.githubusercontent.com/89011801/200486627-b1c9c02a-2591-463b-bf47-429b844ecc1f.png)

AUC provides an aggregate measure of performance across all possible classification thresholds. One way of interpreting AUC is as the probability that the model ranks a random positive example more highly than a random negative example.

