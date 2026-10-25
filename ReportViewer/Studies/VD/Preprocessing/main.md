# Preprocessing

The preprocessing pipeline applied to the voltammetric raw data **before** the fit runs.

Each step is configurable, and steps run in the order shown. Typical steps for this study type include **baseline correction** (key for clean peak heights), **smoothing** (Savitzky-Golay or moving average) and **derivative transforms** (useful when peaks ride on a strong background).

Preprocessed data is plotted alongside the raw data so you can see exactly what changed. Toggle individual steps off if you want to see how each one contributes; the fit (and analytics) recompute live.
