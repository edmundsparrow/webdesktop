# 💻 Gnokestation - The Modular WebDesktop

[![Netlify Status](https://api.netlify.com/api/v1/badges/e8d4c7d0-c3d5-49e0-84a1-8d2629b3a985/deploy-status)](https://gnoke-web.netlify.app)
[![Architecture-SPA](https://img.shields.io/badge/Architecture-Single--Page%20App-2980b9?style=flat-square)](https://gnoke-web.netlify.app)
[![Size-700KB](https://img.shields.io/badge/Footprint-~700KB-009688?style=flat-square)]()
[![License-GPL3](https://img.shields.io/badge/License-GPL--3.0-blue?style=flat-square)](https://www.gnu.org/licenses/gpl-3.0)

**A complete, ultra-lightweight desktop environment that runs entirely in the browser.**

Gnokestation is built on a strict, high-performance architecture, proving that a full desktop experience—including a powerful Window Manager and an App Ecosystem—can be achieved with minimal resources. It is a true WebDesktop, designed for speed and modularity.

---

## 🌟 Architectural Maturity (The WebDesktop Core)

Gnokestation is more than a UI theme; it is built as a **Single-Page Application (SPA)** kernel that loads applications as encapsulated, safe modules.

### 1. The Core Infrastructure

The entire system shell is contained within a single `index.html` file, bundling essential global services:

* **Window Manager (`window.WindowManager`):** Controls window state, resizing, z-indexing, and desktop layout.
* **Application Registry (`window.AppRegistry`):** The central metadata list for all installed apps.
* **Event Bus (`window.EventBus`):** Allows applications to communicate safely without direct dependency.

### 2. Strict Modularity (The Application Standard)

All applications are treated as external plugins, loaded dynamically by `plugins.js`. This guarantees system stability using the following pattern:

| Pattern | Benefit |
| :--- | :--- |
| **IIFE Wrapper** | Every app is wrapped in an `(function() { ... })()` to protect all internal variables from the global scope, eliminating conflicts. |
| **Single Global Export** | Only one object (e.g., `window.CalculatorApp`) is ever exposed by the plugin, giving the `AppRegistry` a clean, reliable entry point. |

### 3. Key Performance Metrics

| Metric | Specification |
| :--- | :--- |
| **Total Size** | ~700KB |
| **Minimum RAM** | Runs smoothly on devices with 512MB RAM |
| **Compatibility** | Works on any device with a standard web browser |
| **Development** | Build apps using only HTML, CSS, and JS |

---

## ⚙️ Vision: Beyond the Desktop

While fully functional as a standalone WebDesktop, Gnokestation is engineered with the *potential* to act as a **Hardware Abstraction Layer (HAL) client** through a simple backend proxy.

This architecture enables advanced use cases where the desktop interface becomes a command center:

* **Industrial:** Factory dashboards and industrial sensor monitoring.
* **Smart Devices:** Control panels for smart homes or greenhouse systems.
* **Prototyping:** A unified interface for managing Arduino or Raspberry Pi hardware.

| Application Examples (No Backend Needed) |
| :--- |
| Calculator, Clock, Weather, News |

---

## 🔗 Links & Contact

| Resource | Link |
| :--- | :--- |
| **Live Demo** | [Launch Gnokestation](https://cutt.ly/XrM3CxqA) |
| **Pitch Deck** | [View Presentation](https://gnokepitch.netlify.app) |
| **Source Code** | [edmundsparrow/gnokestation](https://github.com/edmundsparrow/gnokestation) |
| **License** | GPL-3.0 |

| Contact | |
| :--- | :--- |
| **Email** | ekongmikpe@gmail.com |
| **WhatsApp** | [Message Edmund Sparrow](https://wa.me/2349024054758) |
