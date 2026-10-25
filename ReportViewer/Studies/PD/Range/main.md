# Fit Range

Restrict the calibration fit to a specific range on the concentration axis (or potential axis).

Use this to exclude regions where the model is known not to apply: Nernstian deviations at very low concentrations, electrode saturation at very high ones, or any range outside the assay's validated working window.

Data outside the range is still plotted — it is just not used to compute the fit coefficients, R² or LoD/LoQ. That makes it easy to see *visually* whether the excluded region truly deviates from the linear (or chosen) model.
