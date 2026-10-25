# ReportViewer

Contextual help content for the **central report workspace** of the Djuli web application - the panel where users configure a report, upload files, run a study and inspect the resulting plots and analytics.

## Top-level sections

### Report metadata fields

Short descriptions of the fields displayed on a report card.

| Folder | Field |
|---|---|
| [`nameReport/`](./nameReport) | Report name |
| [`description/`](./description) | Free-text description |
| [`purpose/`](./purpose) | Purpose of the experiment |
| [`hypothesis/`](./hypothesis) | Hypothesis being tested |
| [`protocol/`](./protocol) | Protocol followed |
| [`equipment/`](./equipment) | Equipment used |
| [`operator/`](./operator) | Operator name |
| [`sensorBatchId/`](./sensorBatchId) | Sensor / batch identifier |
| [`details/`](./details) | Additional details |
| [`results/`](./results) | Free-text results summary |
| [`conclusion/`](./conclusion) | Conclusion |
| [`dateTest/`](./dateTest) | Date the experiment was performed |
| [`lastUpdate/`](./lastUpdate) | Last update timestamp |

### Workspace controls

| Folder | Element |
|---|---|
| [`reportBoard/`](./reportBoard) | The main report board (analytics panel) |
| [`reportList/`](./reportList) | The list of reports in the current project |
| [`editMode/`](./editMode) | Toggle the workspace into edit mode |
| [`forceUpdate/`](./forceUpdate) | Force re-running the analysis |
| [`resetGrid/`](./resetGrid) | Reset the workspace grid layout |
| [`chronoConfig/`](./chronoConfig) | Chrono configuration panel |
| [`reportsComparison/`](./reportsComparison) | The side-by-side comparison panel |
| [`comparisonReportsId/`](./comparisonReportsId) | List of report IDs included in the comparison |
| [`reviewers/`](./reviewers) | The list of users assigned to review this report |

### Files

How the user loads raw data into a report.

| Folder | Element |
|---|---|
| [`Files/DragArea/`](./Files/DragArea) | The drag-and-drop upload area |
| [`Files/processed/`](./Files/processed) | The processed-files table |
| [`Files/showProcessed/`](./Files/showProcessed) | Toggle to show the processed-files table |

### Units

Unit selectors that control the plot axes.

| Folder | Quantity |
|---|---|
| [`Units/Concentration/`](./Units/Concentration) | Concentration units (analyte axis) |
| [`Units/Current/`](./Units/Current) | Current units |
| [`Units/Potential/`](./Units/Potential) | Potential units |
| [`Units/Time/`](./Units/Time) | Time units |
| [`Units/Z/`](./Units/Z) | Impedance (Z-axis) units, used on impedance plots |
| [`Units/Notation/`](./Units/Notation) | Numeric notation (scientific, fixed, etc.) |

### Templates

| Folder | Element |
|---|---|
| [`Templates/Table/`](./Templates/Table) | The Table template for tabular reports |

### Studies

Per-study-type configuration. Each study code has its own folder containing the same set of configurable elements (Baseline, RawGraph, FitType, statistical evaluation, axis ranges, etc.). See [`../docs/study-types.md`](../docs/study-types.md) for what each code means.

| Code | Folder | Family |
|---|---|---|
| `AC` | [`Studies/AC/`](./Studies/AC) | Amperometry - Continuous |
| `AD` | [`Studies/AD/`](./Studies/AD) | Amperometry - Discrete |
| `PC` | [`Studies/PC/`](./Studies/PC) | Potentiometry - Continuous |
| `PD` | [`Studies/PD/`](./Studies/PD) | Potentiometry - Discrete |
| `VD` | [`Studies/VD/`](./Studies/VD) | Voltammetry - Discrete |
| `GC` | [`Studies/GC/`](./Studies/GC) | Generic - Continuous |
| `General/` | [`Studies/General/`](./Studies/General) | Shared continuous vs. discrete concepts |

Inside each study folder you'll typically find entries for `RawGraph`, `Preprocessing`, `Baseline`, `FeatureCheck`, `FitType`, `StatisticalEval`, axis range / log toggles and any study-specific options (e.g. `SinglePeak`, `DeltaFit`, `MeanFit`).

### Shared study controls

| Folder | Element |
|---|---|
| [`Studies/addFeature/`](./Studies/addFeature) | Add a new analysis feature to the current study |
| [`Studies/removeFeature/`](./Studies/removeFeature) | Remove the selected analysis feature |

## Adding a new entry

1. Create `ReportViewer/<path>/<elementName>/main.md` mirroring the UI's hover route.
2. Add any image assets next to `main.md` using relative paths.
3. If the element has multiple tabs (e.g. `main.md` + `Media.md` + `Examples.md`), each file becomes a tab in the help panel; see `Studies/AD/RawGraph/` for an example.
