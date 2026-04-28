# IoT Laboratory Report — Bialystok University of Technology

**Authors:** Pietro Corti, Wassim Meguellati  
**Course:** Internet of Things  
**Academic Year:** 2025/2026

---

## Overview

This repository contains the LaTeX source code and all associated images for the IoT laboratory report. The lab is structured in three progressive parts, each building on the previous one, culminating in a fully working IoT system.

---

## System Summary

| Part | Device | Role | Protocol |
|------|--------|------|----------|
| 1 | ESP32 + BME680 | Sensor node + web server | HTTP |
| 2 | Raspberry Pi | MQTT gateway/broker | MQTT |
| 3 | ESP32 + Raspberry Pi | Full integrated IoT system | MQTT over Wi-Fi |

---

## Repository Structure

```
iot_report/
├── iot_report.tex       # Main LaTeX source file
├── images/              # All figures used in the report
│   ├── p1_*.jpg/png     # Part 1 images (ESP32 node)
│   ├── p2_*.jpg/png     # Part 2 images (Raspberry Pi gateway)
│   └── p3_*.jpg/png     # Part 3 images (full system)
└── README.md
```

---

## How to Compile

### Option 1 — Overleaf (recommended)
1. Download the repository as a ZIP.
2. Go to [overleaf.com](https://www.overleaf.com) and click **New Project → Upload Project**.
3. Upload the ZIP — Overleaf will compile it automatically.

### Option 2 — Local (pdflatex)
Make sure you have a LaTeX distribution installed (e.g. TeX Live or MiKTeX), then run:
```bash
pdflatex iot_report.tex
pdflatex iot_report.tex   # run twice to resolve references
```

---

## Hardware Used

- **ESP32 DevKitC** (DOIT ESP32 DEVKIT V1)
- **Adafruit BME680** environmental sensor (temperature, humidity, pressure, gas)
- **Raspberry Pi 5** (8GB) running Raspberry Pi OS
- Breadboard, jumper wires, USB cables

---

## Software & Libraries

- Arduino IDE with the following libraries:
  - `Adafruit BME680` — sensor driver
  - `PubSubClient` — MQTT client for ESP32
- Raspberry Pi OS with `mosquitto` and `mosquitto-clients`

---

## Notes

- Two placeholder figures remain in the report (marked with `\fbox`) and can be replaced by adding the corresponding image to the `images/` folder and swapping the `\fbox{\parbox{...}}` block with `\includegraphics{filename}`.
- The Wi-Fi credentials and MQTT broker IP in the Part 3 source code are specific to the lab environment and should be updated before reuse.
