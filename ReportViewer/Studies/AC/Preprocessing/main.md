# Preprocessing

The preprocessing pipeline applied to the chrono-amperometric raw data **before** the fit runs.

Each step is configurable, and steps run in the order shown. Typical steps for this study type include **baseline correction** (subtract drift), **low-pass filtering** (BPF / LPF / median / moving average / Savitzky-Golay), **crop** and **outlier detection**.

Preprocessed data is plotted alongside the raw data so you can see exactly what changed. Toggle individual steps off if you want to see how each one contributes; the fit (and analytics) recompute live.
