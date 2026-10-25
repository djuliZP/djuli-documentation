# Mean Fit

When several replicate readings exist at the same concentration, fit through the **mean** of those replicates instead of each replicate individually.

Reduces scatter on the calibration curve by collapsing N replicate points per concentration to one mean point. Trade-off: the regression statistics no longer reflect the within-concentration variability — pair this with the [Statistical Evaluation](./StatisticalEval) card if you also want to see the standard deviation per concentration.

Use Mean Fit when you have at least 3 replicates per concentration and you want the calibration curve to ride through the centre of the data rather than be pulled by individual outliers.
