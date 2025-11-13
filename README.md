# 💻 Gnokestation - The Modular WebDesktop

[![Architecture-WebDesktop](https://img.shields.io/badge/Architecture-WebDesktop-2980b9?style=flat-square)](https://gnoke-webos.netlify.app)
[![Size-98KB](https://img.shields.io/badge/SPA%20Size-~98KB%20(20KB%20gzipped)-009688?style=flat-square)]()
[![License-GPL3](https://img-shells.com/badge/License-GPL--3.0-blue?style=flat-square)](https://www.gnu.org/licenses/gpl-3.0)

**A complete, ultra-lightweight desktop environment that runs entirely in the browser.**

Gnokestation is built on a strict, high-performance **Single-Page Application (SPA)** architecture, proving that a full desktop experience—including a powerful Window Manager and App Ecosystem—can be achieved with minimal resources. It is a robust WebDesktop focused on speed and modularity.

---

## 🌟 Architectural Maturity (The WebDesktop Core)

Gnokestation is designed as an SPA kernel that loads applications as encapsulated, safe modules, ensuring system integrity and scalability.

### 1. The Core Infrastructure

The entire system shell is contained within a single HTML file (the SPA), bundling essential global services:

* **Window Manager (`window.WindowManager`):** Controls window state, movement, resizing, and layering.
* **Application Registry (`window.AppRegistry`):** The central metadata list for all installed apps.
* **Event Bus (`window.EventBus`):** Allows applications to communicate safely without direct dependency.

### 2. Strict Modularity (The Application Standard)

All applications are treated as external plugins, loaded dynamically by `plugins.js`. This guarantees system stability using the following critical patterns:

| Pattern | Benefit |
| :--- | :--- |
| **IIFE Wrapper** | Every app is wrapped in an `(function() { ... })()` to protect all internal variables from the global scope, eliminating conflicts. |
| **Single Global Export** | Only one object (e.g., `window.CalculatorApp`) is exposed by the plugin, giving the `AppRegistry` a clean, reliable entry point. |

### 3. Key Performance Metrics

| Metric | Specification |
| :--- | :--- |
| **Total SPA Size (Minified)** | **~98KB** (ungzipped) |
| **Transfer Size (Gzip)** | **~20KB** |
| **Minimum RAM** | Runs smoothly on devices with 512MB RAM |
| **Compatibility** | Works on any device with a standard web browser |

---

## ⚙️ Vision: The Control Interface

Gnokestation is engineered with the primary vision of becoming a **Unified Control Interface**. Its lightweight nature makes it ideal for use cases where the desktop interface becomes a command center for other systems:

* **Remote Management:** Factory dashboards, industrial sensors, and telemetry monitoring.
* **Embedded Systems:** Control panels for Raspberry Pi, Arduino, or custom hardware (via a lightweight backend proxy).
* **Smart Devices:** Control panels for smart homes or custom automation.

| Application Examples |
| :--- |
| Calculator, Clock, Weather, News |

---

## 🔗 Links & Contact

| Resource | Link |
| :--- | :--- |
| **Live Demo** | [**Launch Gnokestation**](https://gnoke-webos.netlify.app) |
| **Pitch Deck** | [View Presentation](https://gnokepitch.netlify.app) |
| **Source Code** | [edmundsparrow/gnokestation](https://github.com/edmundsparrow/gnokestation) |
| **License** | GPL-3.0 |

| Contact | |
| :--- | :--- |
| **Email** | ekongmikpe@gmail.com |
| **WhatsApp** | [Message Edmund Sparrow](https://wa.me/2349024054758) |
