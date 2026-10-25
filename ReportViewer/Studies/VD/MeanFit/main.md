# Mean Fit

When several replicate voltammograms exist at the same concentration, fit through the **mean** of those replicates instead of each peak individually.

Reduces scatter on the calibration curve by collapsing N replicate peak values per concentration to one mean point. Trade-off: the regression statistics no longer reflect the within-concentration variability — pair this with the [Statistical Evaluation](./StatisticalEval) card if you also want to see the standard deviation per concentration.

Use Mean Fit when you have at least 3 replicate sweeps per concentration and the calibration should ride through the centre of the data rather than be pulled by individual outliers.
