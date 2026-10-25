# Delta Fit

Use the *change* in potential between two reference points (ΔV) as the analytical signal instead of the absolute potential.

Common when the absolute potential drifts between runs (electrode ageing, reference electrode bias) but the *response* to the analyte is reproducible. ΔV cancels out the baseline shift, leaving a cleaner calibration curve.

The two reference points are taken from the chrono-potentiometric step Djuli detects in your data; the resulting ΔV per concentration is what gets plotted against the analyte concentration.
