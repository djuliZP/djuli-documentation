# Delta Fit

Use the *change* in current between two reference points (Δi) as the analytical signal instead of the absolute current.

Common when the baseline drifts between runs (e.g. ambient temperature changes, electrode conditioning) but the *response* to the analyte is reproducible. Δi cancels out the baseline shift, leaving a cleaner calibration curve.

The two reference points are taken from the chrono-amperometric step Djuli detects in your data; the resulting Δi per concentration is what gets plotted against the analyte concentration.
