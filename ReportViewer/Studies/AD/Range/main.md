# Fit Range

Restrict the calibration fit to a specific range on the concentration axis (or current axis).

Use this to exclude the regions where the model is known not to apply: detector saturation at high concentrations, noise at the detection limit, or any concentration outside the assay's validated working range.

Data outside the range is still plotted — it is just not used to compute the fit coefficients, R² or LoD/LoQ. That makes it easy to see *visually* whether the excluded region truly deviates from the linear (or chosen) model.
