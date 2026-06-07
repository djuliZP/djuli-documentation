# Study Types

This page is a high-level overview of the studies Djuli supports. For configuration details of any specific knob, hover the element in the Djuli app - the contextual help panel will surface the matching entry from this repository.

Djuli splits studies into two families:

- **Discrete** - one measurement per known concentration or sample. The output is typically a calibration curve and statistical evaluation of how well the data fit a model.
- **Continuous** - a time-series signal containing multiple concentration steps. Djuli detects each step, fits it, and then summarises the steps into a calibration.

In both families the user picks a study type matching the technique they ran in the lab. Each study type produces a Raw Graph, an optional preprocessed graph, a fit / step-fit graph and an Analytics card (R², coefficients, LoB, LoD, LoQ).

---

## Amperometry

> Measures current as a function of applied potential / concentration. Most common technique for biosensors.

| Code | Type | What it produces |
|---|---|---|
| `AD` | Discrete | Calibration curve of current vs. concentration |
| `AC` | Continuous | Step-fit on a chrono-amperometric trace, then a calibration curve over the detected steps |

Typical use case: enzymatic biosensors (glucose, lactate), redox-active analyte detection.

Per-study configuration in the app: *Properties → AC* or *Properties → AD* - Preprocessing, Baseline, Y-axis range, X-axis range, Feature Check, Fit Type, Statistical Evaluation.

---

## Potentiometry

> Measures potential (voltage) as a function of concentration. Used when no current can or should be drawn.

| Code | Type | What it produces |
|---|---|---|
| `PD` | Discrete | Calibration curve of potential vs. concentration |
| `PC` | Continuous | Step-fit on a chrono-potentiometric trace, then a calibration curve |

Typical use case: ion-selective electrodes (ISE), pH, reference-electrode work.

---

## Voltammetry

> Measures current while sweeping potential. Output is typically a peak whose position, height or area encodes the analyte concentration.

| Code | Type | What it produces |
|---|---|---|
| `VD` | Discrete | Peak fit on each sweep, then a calibration curve from peak height / area / position |

Per-study configuration: `SinglePeak`, `ReverseSingle`, `Range`, `DeltaFit`, `MeanFit`, plus the shared preprocessing / statistical-evaluation cards.

---

## Impedance (EIS)

> Electrochemical Impedance Spectroscopy — measures the system's complex impedance `Z = R + jX` over a sweep of AC frequencies. Used to characterise charge transfer, double-layer capacitance, mass transport and coating quality of an electrode or biosensor.

In Djuli, EIS is exposed as a fit option inside any **discrete study** (AD / PD / VD) rather than a separate study code. Enable it from *Properties → <study> → Equivalent Circuit*.

### Equivalent-circuit modelling

You describe the model as a short circuit string. Djuli renders a schematic of it (so you can verify the topology before fitting) and fits the component values to your impedance data.

| Symbol | Element |
|---|---|
| `R` | Resistor |
| `C` | Capacitor |
| `L` | Inductor |
| `W`, `O`, `T` | Warburg (semi-infinite, open, short) |
| `Q`, `P` | Constant-phase element (CPE) |
| `G` | Generalised inductive element |

Connect elements in **series** with `-` and in **parallel** with `p(A,B)` or `[A,B]`. Example: `R0-p(R1,C1)-p(R2,W1)` describes a Randles-style circuit — solution resistance `R0`, charge-transfer resistance `R1` in parallel with the double-layer `C1`, and a polarisation `R2` in parallel with a Warburg diffusion element `W1`.

### Outputs

- A rendered SVG **schematic of the requested circuit** to confirm topology before fitting.
- The **fitted value, relative error and goodness-of-fit** for each circuit element, displayed in the analytics card.
- The **model overlay on the impedance plot**, so deviations between data and fit are immediately visible.

Use the **Equivalent Circuit Configuration** panel inside the discrete study to enter the circuit string and review the fit — see [`Studies/AD/CircuitConfiguration`](../ReportViewer/Studies/AD/CircuitConfiguration), [`Studies/PD/CircuitConfiguration`](../ReportViewer/Studies/PD/CircuitConfiguration) and [`Studies/VD/CircuitConfiguration`](../ReportViewer/Studies/VD/CircuitConfiguration).

---

## Spatial Mapping

> Visualises a single measured quantity across a 2D grid of positions; used for sensor arrays, printed multi-electrode strips and area-of-interest scans.

Typical use case: a wafer, plate or strip with many sensors at known positions, each producing one reading. Spatial Mapping shows you whether the response is uniform across the grid or whether it drifts by row, by column or by neighbourhood.

**Input.** Each sample carries an `(x, y)` integer position and one signal value. Djuli automatically sizes the grid to the largest position it sees; positions you didn't measure are drawn as gaps.

**Output (single combined view).** Djuli produces one panel with four linked plots:

- **Heatmap** of the grid, coloured by signal value. The fastest way to spot dead spots or hot zones.
- **Row variation** — mean ± standard deviation per row, drawn as a horizontal bar chart with error bars. Reveals row-wise gradients (e.g. one edge of the array consistently higher).
- **Column variation** — mean ± standard deviation per column, drawn as a vertical bar chart with error bars. Same idea, by column.
- **Distribution histogram** of the deviation from the grid median (in %). Shows whether the array is tightly clustered around its centre or has long tails.

Together these four plots make non-uniformity, edge effects and outlier positions immediately visible without writing any custom analysis.

---

## Generic Continuous (`GC`)

> A flexible study type for any continuous time-series that doesn't match Amperometry-C or Potentiometry-C. Use this when your hardware produces a custom signal but you still want step detection, baseline removal and a calibration curve.

---

## Discrete vs. continuous in shared terms

For knobs that apply to both families (Baseline, Preprocessing, Feature Check, Statistical Evaluation, axis log/linear toggles, axis range), see [`../ReportViewer/Studies/General/`](../ReportViewer/Studies/General). The shared docs in `General/ContinuousStudies/` and `General/DiscreteStudies/` describe the broader category rather than a specific technique.
