# wind

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/e-k-m/wind/main)

> a little playground of predicting wind speeds

[Getting Up and Running](#getting-up-and-running)

This here contains some examples of trying to predict wind speeds in the near future. The data used in folder [./data](./data) corresponds to the measured values of Switzerland's automatic weather station network. For more information, see [here](https://opendata.swiss/en/dataset/automatische-wetterstationen-aktuelle-messwerte). The prediction approaches are:

- Seasonal ARIMA (with daily periods): [windspeed-sarima.ipynb](./windspeed-sarima.ipynb).

- ML forcast using linear regression: [windspeed-linear-regression.ipynb](./windspeed-linear-regression.ipynb).

In summary, the current conclusions are:

- The current approaches have a mean absolute error of approximately the same as a random walk.

- The reason for the poor prediction accuracy seems to be the high "randomness" of wind speed over time, which is inadequately modeled in the two tested approaches.

- Possible future work to improve the results are: better feature engineering; the use of exogenous variables capable of helping with the problem; and the use of a model tailored to this problem.

## Getting Up and Running

```bash
pip install -r requirements.txt
jupyter lab windspeed-sarima.ipynb
# or
jupyter lab windspeed-forest.ipynb
```