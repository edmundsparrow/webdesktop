# 💻 Gnokestation - The WebDesktop

[![Netlify Status](https://api.netlify.com/api/v1/badges/e8d4c7d0-c3d5-49e0-84a1-8d2629b3a985/deploy-status)](https://gnoke-web.netlify.app)
[![Architecture-WebDesktop](https://img.shields.io/badge/Architecture-WebDesktop-3f6e9b?style=flat-square&logo=github)](https://gnoke-web.netlify.app)
[![JavaScript](https://img.shields.io/badge/Language-JavaScript-F7DF1E?style=flat-square&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

**Live Demo:** [**gnoke-web.netlify.app**](https://gnoke-web.netlify.app)

Gnokestation is a fast, modular **WebDesktop** environment built entirely on vanilla JavaScript, HTML, and CSS. It focuses on providing a responsive, complete desktop shell experience, featuring a functional Window Manager and a clean application architecture.

---

## 🌟 Core Focus: Shell and Modularity

Gnokestation is designed as a **Single-Page Application (SPA)** that uses a strict, modular pattern to manage its core system services and third-party applications.

### Architectural Pillars

| Component | Responsibility | Benefit |
| :--- | :--- | :--- |
| **Window Manager** | Handles window creation, movement, resizing, and layering. | Provides a fluid, traditional desktop feel. |
| **SPA Core** | All essential system logic (like the Taskbar and App Registry) is bundled into a single `index.html` file. | Extremely fast initial load and performance. |
| **Modularity (Plugins)** | Applications are external `.js` files loaded dynamically by `plugins.js`. | Allows for easy expansion, development, and separation of code. |
| **IIFE Pattern** | Every app is wrapped in an `(function() { ... })()` pattern. | **Critical for stability:** Prevents global variable conflicts between applications. |

## 📐 The Standard Application Template

Every application in Gnokestation must adhere to the **IIFE + Global Export** template to ensure compatibility and system safety.

```javascript
// Example Application Structure

(function() {
  'use strict';
  
  // Private variables and functions remain scoped and protected here.
  const PRIVATE_STATE = 0; 

  window.MyAppName = {
    // This is the only object exposed globally (Global Export).
    open: function() {
        // ... launch logic using WindowManager ...
    }
  };
  
  // Register the app with its metadata.
  window.AppRegistry.registerApp({...});
})(); 
