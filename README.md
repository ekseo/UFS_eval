# UFS_eval
Intercomparison framework

This evaluation framework is developed by Eunkyo Seo (eseo8@gmu.deu).

This framework is developed to evalute UFS model performance against FluxTowers (FLUXNET2015, Ameriflux, Euroflux).

It conducts the model evaluation across possible variables employed by in-situ observation.

35-day model simulation is validated by time-averaged bias and RMSE which are standardized by the standard deviation of them by each station. 
Additionally, to measure the comprehensive model performance, two additional metrics (temporal correlation coefficient and KDE-based PSS) are employed. 
Overall, when the color has been bright or white, it means that the model performance for the specific variable is relatively reliable and when the color has been primary color or dark, the result is vice versa. 

1. preparing observation dataset to validate model simulation (FLUXNET2015, Ameriflux, and Euroflux for 2012-2013 are prepared). If the validation period is changed, observation data should be prepared as the period in ./data/FULLSET/.
2. sorting the model simulation at validated site points and storing it in ./data/UFS/. The dimension structure of the stored model data is [forecast period: 35, sites: 171].
3. Additionally, the variables which does not directly provide in output list is derived by exist variables and stores them in ./data/UFS/.
4. If validating and validated datasets are ready, plots evaluating model performance can be produced by the code in ./plot/. 

If there is any suggestion and problem in the usage of this package, please contact me.
Feel free to use it!
