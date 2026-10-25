# Chrono Configuration

The configuration panel for chrono studies (chrono-amperometry, chrono-potentiometry). Lets you describe the step structure of your experiment so Djuli can detect each step in the trace and treat it as one calibration point.

You set, per step:

- **Time** — when the step starts (and, with the global step-fit width, how long it lasts).
- **Concentration** — the analyte concentration applied at that step.

A global **step-fit width** applies to every step in the report — Djuli uses the same window length when extracting the response from each step, which keeps step-to-step comparison fair.

Open this panel from *Properties → AC / PC → Cards → Fit Step Data → Configure Concentrations* (or the equivalent path for the active study type).
