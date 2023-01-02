The goal of this competition is to predict monthly microbusiness density for GoDaddy for 3135 USA counties using just 39 data points each.

* In [EDA.ipynb](https://github.com/laksharora98/Portfolio/blob/master/Kaggle%20Projects/GoDaddy%20-%20Microbusiness%20Density%20Forecasting/EDA.ipynb), I explored the data. I concluded that the data has yearly seasonality.
* I first made a Naive Model which only uses the last observed value as baseline. [Link](https://github.com/laksharora98/Portfolio/blob/master/Kaggle%20Projects/GoDaddy%20-%20Microbusiness%20Density%20Forecasting/baseline%20last%20val.ipynb)
* In [Holt Winters.ipynb](https://github.com/laksharora98/Portfolio/blob/master/Kaggle%20Projects/GoDaddy%20-%20Microbusiness%20Density%20Forecasting/Holt%20Winters.ipynb), I used Triple Exponential Smoothing for each county. The model performed worse than Naive.
* Then, I used Facebook Prophet to do the forecast [Link](https://github.com/laksharora98/Portfolio/blob/master/Kaggle%20Projects/GoDaddy%20-%20Microbusiness%20Density%20Forecasting/Univariate%20independent%20prophet.ipynb). The resulting prediction was worse than both the Naive and Holt Winters models.
* Finally, I tried to combine the Naive and Holt Winters models based on the population of the counties as threshold [Link](https://github.com/laksharora98/Portfolio/blob/master/Kaggle%20Projects/GoDaddy%20-%20Microbusiness%20Density%20Forecasting/Ensembling%20holt%20and%20base.ipynb). This performed only slightly better than the Naive Model.

Next Steps: Tune the threshold and weight hyperparameters in the ensemble to see if i can improve upon the naive model.
Try simple regression models instead of exponential smoothing or prophet as public codes on Kaggle using the same have performed better.
