# Fit Range

Restrict the calibration fit to a specific range on the concentration axis (or peak-current axis).

Use this to exclude regions where the model is known not to apply: detector saturation at high concentrations, indistinguishable peaks at the detection limit, or any range outside the assay's validated working window.

Data outside the range is still plotted — it is just not used to compute the fit coefficients, R² or LoD/LoQ. That makes it easy to see *visually* whether the excluded region truly deviates from the linear (or chosen) model.
