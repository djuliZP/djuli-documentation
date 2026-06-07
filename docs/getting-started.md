# Getting Started with Djuli

A walkthrough from creating an account to producing your first report. Every step here uses the same UI elements covered in the in-app contextual help, so once you finish this guide you can hover any control to read what it does.

> Need to start now? Sign up at [dju.li/register](https://dju.li/register) and open the app at [dju.li](https://dju.li).

---

## 1. Create a free account

1. Open [dju.li/register](https://dju.li/register).
2. Enter your email, set a password, and confirm via the verification email.
3. Sign in.

After signing in you land directly on the Clusters view — the workspace where the rest of these steps take place.

## 2. Create your first cluster

A **cluster** is a top-level workspace; you can have several (e.g. one per project, customer or instrument).

1. From the navigation tree on the left, click the green **+** icon next to *Clusters*.
2. Enter a name and confirm.

The new cluster appears at the top of the *Active Clusters* table and as a branch in the navigation tree. You can come back later and tag it as a favourite (heart icon) or archive it (folder icon) when the work is done.

## 3. Add a project to the cluster

Projects group related reports inside a cluster.

1. Expand the cluster you just created — either by clicking it in the tree on the left, or by clicking the cluster row in the table.
2. With the cluster open, click the green **+** *Add Project* icon in the toolbar at the top of the workspace.
3. Enter a project name and confirm.

The project appears in the *Projects* table for that cluster. Use one project per experimental campaign, instrument batch or research question — anything more granular usually belongs as a report inside a project.

## 4. Create a report

A **report** is one experiment.

1. Inside the project, click the green **+** *Add Report* icon in the toolbar.
2. Pick the study type that matches your technique. The study type drives which preprocessing, fit and analytics options Djuli will offer — see [`study-types.md`](./study-types.md) for a one-paragraph summary of each code (AC, AD, PC, PD, VD, GC).
3. Fill in the metadata fields shown on the report card: report name, operator, equipment used, protocol followed and the date the experiment was performed. None of these affect the analysis, but they make the report traceable later.

Metadata fields can be edited at any point — the values you enter now are not locked in.

## 5. Upload your raw data

1. Open the report and locate the *Files → Drag area* tab on the left side of the workspace.
2. Drop your CSV (or any other [supported format](./faq.md)) into it. You can drop several files at once — each becomes a separate data line in the same report.
3. The file is parsed and appears in the *Processed Data Table* below the drag area, with an auto-assigned `id` for each data line. The `id` is what the [Terminal commands](../Terminal/README.md) (`flipx`, `offsety`, …) refer to when you need to nudge a single line.

If the parser doesn't recognise your file shape, an error appears in the Terminal panel at the bottom — re-format the file (or pick a different study type) and drop it again.

## 6. Run the analysis

Djuli runs the analysis automatically as soon as data and configuration are available.

1. Open the *Properties* panel on the right side and review the study-specific settings — preprocessing steps, baseline correction, fit type, axis ranges and units. Hover any of them to read the matching in-app help.
2. The *Raw Graph* (always), the *Preprocessed Graph* (if any preprocessing is enabled) and the *Fit Graph* regenerate automatically every time you change a setting. No "Run" button is needed.
3. Read the *Analytics* card next to the fit graph for R², limits of blank / detection / quantitation (LoB / LoD / LoQ) and the model coefficients with their standard errors.

If a graph looks wrong, it is almost always a units or axis-range problem — both are under *Properties → Units* and *Properties → <study code\> → X-axis / Y-axis range*.

## 7. Share or export the report

1. Select the report in the project's table, then click the yellow **share** icon in the toolbar. Pick the recipient's Djuli email and the permission level (read, comment, edit). They will see the report under *Shared with me* in their navigation tree.
2. To send the report to someone who does not use Djuli, use the *Export* action to download it as a PDF — the layout matches what you see on screen, including metadata, plots and the analytics card.

You can also share an entire cluster the same way; doing so gives access to every project and report inside it. See [`Navigation/shareCluster`](../Navigation/shareCluster) and [`Navigation/shareReport`](../Navigation/shareReport) for the difference.

---

## Where to go next

- **Customise plots and units:** see the contextual help inside *Properties → General → Units* and *Properties → \<study code\> → X-axis / Y-axis range*.
- **Apply quick transformations to data lines:** see the [Terminal](../Terminal/README.md) area - `flipx`, `flipy`, `offsetx`, `offsety`, etc.
- **Connect a SenseItAll device:** see [`hardware.md`](./hardware.md).
- **Push data from your own scripts:** Djuli exposes a REST API for ingest; detailed API documentation is in preparation.
- **Deeper learning:** [ZP Academy courses](https://academy.zimmerpeacock.com/courses).
