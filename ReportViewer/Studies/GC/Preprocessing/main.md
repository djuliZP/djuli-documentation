# Preprocessing

The preprocessing pipeline applied to the generic continuous raw data **before** the fit runs.

Each step is configurable, and steps run in the order shown. Typical steps for this study type include any of Djuli's general preprocessing tools — **crop**, **filters**, **flip / offset**, **extrapolate / accumulate / differentiate** and **outlier detection** — applied in whatever order fits your custom workflow.

Preprocessed data is plotted alongside the raw data so you can see exactly what changed. Toggle individual steps off if you want to see how each one contributes; the fit (and analytics) recompute live.
