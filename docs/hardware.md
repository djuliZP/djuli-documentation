# Hardware Integration

Djuli is the cloud companion for Zimmer & Peacock's hardware family. This page describes how each instrument is paired with a Djuli account, how data flows from device to cloud, and how Premium accounts can be activated via hardware.

## SenseItAll (SIA)

SenseItAll is ZP's portable potentiostat family. It runs amperometry, potentiometry and voltammetry experiments and can stream measurements straight into Djuli.

### Data flow

```
SIA hardware ──► Local capture (mobile or desktop) ──► Djuli REST API ──► Cluster / Project / Report
```

## FoodSense

FoodSense is ZP's portable food-analysis instrument — an electrochemical meter that quantifies specific compounds directly from a sample, no laboratory workflow required.

### What FoodSense measures

The current FoodSense product line targets three redox-active analytes commonly found in food and beverage matrices:

- **Capsaicin** — for measuring chilli pungency. Results are reported in **Scoville Heat Units (SHU)** and the device accepts fresh chillies, dried chilli powders and chilli sauces.
- **Gingerol** — for ginger products.
- **Caffeine** — for caffeinated beverages and extracts.

The meter is a Bluetooth-enabled portable potentiostat. It pairs with a mobile phone or laptop for sample-by-sample readings; the same readings can be pushed into Djuli for storage, calibration and shareable reports.

### Typical Djuli study type

Because each assay is a single-sample electrochemical reading, FoodSense data is normally analysed as a **Voltammetry Discrete (VD)** or **Amperometry Discrete (AD)** study in Djuli. The exact study type depends on the technique the assay uses; the Djuli report's study type should be picked to match what the FoodSense protocol specifies.

More on FoodSense at [foodsensetechnology.com](https://www.foodsensetechnology.com).

### Premium activation via the SIA / FoodSense app

Buyers of SenseItAll or FoodSense hardware get Djuli Premium included with the device. There is no QR code, no licence key and no separate activation step — the account is upgraded automatically the first time you log into the companion app with the same credentials:

1. Sign up for a Djuli account at [dju.li/register](https://dju.li/register).
2. Open the SenseItAll or FoodSense mobile app and log in with **the same email and password** you used at signup.
3. The next time you log into Djuli with those credentials, the account is already on the Premium tier.

If you change your Djuli password later, make sure to update it in the SenseItAll / FoodSense app too — Premium status follows the credentials, not the device.

## Third-party instruments

Any instrument that can export one of Djuli's [supported file formats](./faq.md) (CSV, XLSX, PSSession, MTD, TRM, DT6, TXT, JSON, XML) works without pairing - upload the file into a report and pick the matching study type.

For real-time streaming from a non-ZP device, Djuli exposes a public REST API. Detailed API documentation is in preparation.

## Useful links

- ZP website: https://www.zimmerpeacocktech.com
- ZP Academy (training): https://academy.zimmerpeacock.com/courses
- Support: https://www.zimmerpeacocktech.com/contact-support/
