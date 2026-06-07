# Frequently Asked Questions

A condensed reference of the questions Djuli users ask most often. The same FAQ is shown on the public Djuli home page; this version is mirrored here so that crawlers, LLMs and offline readers can pick it up too.

---

### What makes Djuli different from other cloud analysis tools?

Djuli combines IoT-device integration, cloud-based scientific analysis and an intuitive user interface in one workspace. It is purpose-built for electrochemistry and biosensor data, which means the analyses (calibration curves, peak fits, LoD/LoQ, step detection) work out-of-the-box without scripting.

### How do I connect IoT devices and third-party apps to Djuli?

Djuli exposes a REST API for pushing data from devices and external applications. Detailed API documentation is in preparation.

### What data formats can I import into Djuli?

CSV, XLSX, JSON, XML, PSSession, MTD, TRM, DT6, TXT and database exports. Media files (images and similar) can also be attached to a report, which makes it easy to keep visual context alongside the raw data.

### What study types does Djuli offer?

**Discrete studies:** Amperometry, Potentiometry, Voltammetry, Impedance, Spatial Mapping.
**Continuous studies:** Amperometry, Potentiometry.
**Generic** - a flexible study type for custom workflows.

A full reference is in [`study-types.md`](./study-types.md).

### How does Djuli secure my data?

Djuli uses encrypted transport and a secure cloud infrastructure (Google Cloud Run). Authentication is handled by Firebase, and access to every API call is checked against the user's token before any data is read or written.

### How do I collaborate with my team?

You can share an entire cluster or an individual report with another Djuli user, assign reviewers, and create custom report templates so the team produces consistent output. Shared items show up in the *Shared with me* view of the navigation tree.

### What preprocessing tools are available?

- **Crop** and **baseline adjustment**
- **Filters:** BPF, BSF, HPF, LPF, median filter, moving average, Savitzky-Golay smoothing
- **Data manipulation:** flip, offset, extrapolate, accumulate, differentiate
- **Outlier detection**

Each tool can be configured per study and is documented in the contextual help inside the app.

### What analysis tools does Djuli provide?

- Equation fitting (linear and non-linear models)
- Statistical extraction (general and per-line)
- Standard addition
- Feature check
- Delta and Mean fit
- Peak fit analysis (position, height, area under curve)
- Spatial mapping

### Is there a storage limit?

Djuli's plans are designed to scale with usage. Freemium accounts have practical limits suitable for evaluation and small projects; Premium accounts unlock the storage and API allowances required for production workflows.

### How does Djuli help generate professional reports?

Upload your raw data, pick a study, and Djuli produces a structured report automatically: metadata header, raw graph, processed graph, fit graph and an analytics card. You can fill in any missing fields, rearrange the layout in edit mode, then export to PDF or share directly with a colleague or client.

### Where can I find tutorials and deeper learning resources?

- **In-app contextual help** - hover any element in Djuli to see a focused explanation. The content lives in this repository.
- **ZP Academy** - full online courses at [academy.zimmerpeacock.com/courses](https://academy.zimmerpeacock.com/courses).
- **Knowledge base** - long-form articles at [zimmerpeacocktech.com/knowledge-base/djuli](https://www.zimmerpeacocktech.com/knowledge-base/djuli/).

### Can I use Djuli with ZP hardware?

Yes. SenseItAll (SIA) and FoodSense instruments stream data directly into Djuli, and both come with Djuli Premium included — the account is upgraded automatically the first time you log into the SIA / FoodSense companion app with the same email and password you use on Djuli. See [`hardware.md`](./hardware.md).

### How do I contact support?

Use the support contact form at [zimmerpeacocktech.com/contact-support](https://www.zimmerpeacocktech.com/contact-support/) or reach out through ZP Academy if you are enrolled in a course.
