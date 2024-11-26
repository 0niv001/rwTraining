A ROC curve is a graph showing the performance of a classification model at all classification thresholds

The curve plots the true positive (Recall) and negative rate FP/FP+TN

Lowering the classification threshold classifies more items as positive, increasing false and true positives

AUC stands for Area Under Curve. This provides an aggregate measure of performance across all classification thresholds.

AUC is good for the following reasons:

- Scale invariant - Measures how well predictions are ranked instead of their absolute values
- Classification threshold invariant - Measures the quality of the model’s prediction irrespective of what classification threshold is chosen.