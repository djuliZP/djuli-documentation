# Djuli Documentation

Official in-app help content for **Djuli** - the cloud platform by [Zimmer & Peacock (ZP)](https://www.zimmerpeacocktech.com) for storing, analysing and sharing electrochemical, biosensor and IVD data.

> The markdown files in this repository are fetched at runtime by the Djuli web application and shown in the **contextual help** sidebar when a user hovers over an element in the UI. Each folder corresponds to one interactive element in the interface.

## Quick links

- **Open the app:** https://dju.li
- **Create a free account:** https://dju.li/register
- **Knowledge base & courses:** [ZP Academy](https://academy.zimmerpeacock.com/courses)
- **Company website:** https://www.zimmerpeacocktech.com

## What is Djuli?

Djuli is a cloud workspace for scientists and engineers working with sensor data. It ingests raw measurements (from files or directly from ZP hardware), runs configurable analyses, and produces shareable reports. It is used for:

- Amperometry, potentiometry, voltammetry and impedance studies
- Calibration, limit-of-detection and statistical evaluation workflows
- Batch processing of many datasets at once
- Team collaboration on reports and analysis settings
- Direct integration with **SenseItAll (SIA)** and other ZP instruments

## Guides

If you are reading this on GitHub, start with the long-form guides under [`docs/`](./docs):

- [Getting started](./docs/getting-started.md) - sign up → cluster → project → report → analysis
- [Study types](./docs/study-types.md) - what each study code (AC, AD, PC, PD, VD, GC) does
- [FAQ](./docs/faq.md) - formats, security, collaboration, storage, support
- [Hardware integration](./docs/hardware.md) - SenseItAll, FoodSense, third-party instruments

There is also an [`llms.txt`](./llms.txt) at the repo root for LLM crawlers.

## How this documentation is structured

Every documented UI element lives in its own folder containing a `main.md` (and optionally extra markdown tabs and image assets):

```
<Area>/<ElementName>/main.md          # default tab
<Area>/<ElementName>/<TabName>.md     # extra tab (e.g. Media.md, Examples.md)
<Area>/<ElementName>/*.png|*.gif      # inline images
```

The top-level areas mirror the major sections of the Djuli UI:

| Folder | UI area |
|---|---|
| [`Navigation/`](./Navigation) | Cluster / project / report tree (left sidebar) |
| [`ReportViewer/`](./ReportViewer) | Central report workspace - metadata, files, plots, study configuration, units, templates |
| [`Terminal/`](./Terminal) | Bottom command/notification terminal |

### ReportViewer study types

Under [`ReportViewer/Studies/`](./ReportViewer/Studies) each subfolder is one analysis type:

| Code | Study type |
|---|---|
| `AC` | Amperometry - Continuous |
| `AD` | Amperometry - Discrete |
| `PC` | Potentiometry - Continuous |
| `PD` | Potentiometry - Discrete |
| `VD` | Voltammetry - Discrete |
| `GC` | Generic Continuous |
| `General/` | Shared continuous vs. discrete concepts |

## Contributing

If the Djuli app shows the message *"You found a new element! The component does not have documentation yet"*, the path you need to create is shown in the panel itself. Create the corresponding `<Area>/<ElementName>/main.md`, open a pull request, and the next time a user hovers that element the help will appear automatically - the webapp reads directly from this repository's `main` branch.

Conventions:
- Keep entries short - they render inside a narrow sidebar.
- Reference images with **relative** paths (`![](myImage.png)`); never absolute paths.
- Use straight quotes; do not invent feature details - mark uncertain items with `<!-- TODO: verify -->`.

## License & ownership

© Zimmer & Peacock. See the [company website](https://www.zimmerpeacocktech.com) for terms of use of the Djuli platform.
