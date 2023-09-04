# Module 13 Summary

## Baseline Performance

With an f1-score of 0.71 for buy signals, the model does a fair job at predicting this particular signal. However, an f1-score of 0.07 for sell signals leaves much to be desired. Not know the right time to sell can significantly affect portfolio performance. Overall, this baseline algo outperforms the actual stock returns over the same time period.

![Baseline](PNG%20Images/Baseline%20Strategy%20Algo.png)

## Model Tuning

Two tuning methods were applied to understand their impact to portfolio returns. I first adjusted the training period to end 3 months later than the original time period, yielding a slight decrease in f1-score for sell signals to 0.04 from 0.07. The second was adjusting the SMA time windows to 20 days for the short window and 50 for the long window resulting in an improved f1-score for sell signals of 0.19 compared to 0.07 and a slightly lower f1-score for buy signals at 0.68. In my opinion the latter is perferable due to the superior f1-score for sell signals even though the buy signal f1-score was slightly lower. Although adjusting the SMA windows yielded better results, the net impact to algo returns is worse than the baseline algo performance.

![TunedAlgo](PNG%20Images/Tuned%20SVM%20Algo.png)

## Logistic Regression

I lastly created a Logistic Regression model based on our original training and testing data. This resulted in the best f1-score for sell signals at 0.50 but also saw the worth for buy signals at 0.47. The net impact on returns is the worst of all variations explored here. While the model starts off strong for the first year it quickly falls off after that. With the seemingly bear market in the first part of our training data perhaps this model could also be fine tuned to perform better throughout the rest of our evaluation period.

![LRAlgo](PNG%20Images/Logistic%20Regression%20Algo.png)
