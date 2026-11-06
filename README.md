<p align="center">
  <img src="assets/icon.png" width="128" height="128" alt="HotspotXray Logo">
</p>

<h1 align="center">HotspotXray</h1>

<p align="center">
  <b>Rootless Android Hotspot VPN Gateway powered by Shizuku and Xray-core</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Android-11%2B%20(API%2030%2B)-3DDC84?style=flat&logo=android&logoColor=white" alt="Android Version">
  <img src="https://img.shields.io/badge/Root-Not%20Required-success?style=flat" alt="Rootless">
  <img src="https://img.shields.io/badge/Core-Xray--core-blue?style=flat" alt="Xray-core">
  <img src="https://img.shields.io/badge/License-Proprietary-red?style=flat" alt="Closed Source">
</p>

---

## 📖 Overview

**HotspotXray** is a specialized Android application designed to turn your smartphone into a transparent, anti-censorship VPN gateway for all hotspot-connected devices—**without requiring root privileges**.

By leveraging **Shizuku** and Android's privileged `TestNetworkManager` & `TetheringManager` APIs, HotspotXray creates a dedicated upstream TUN interface. All traffic from downstream devices connected to your Wi-Fi Hotspot is transparently routed into an embedded, high-performance **Xray-core** instance.

Client devices (such as Smart TVs, Laptops, Consoles, iPhones, or other Android phones) receive clean, filtered-free internet instantly upon connecting to your Wi-Fi Hotspot, with **zero configuration** required on the client side.

---

## 📥 Download

Grab the latest pre-built APK from the [Releases](https://github.com/shayanmaher/HotspotXray/releases) section or directly from this repository:

| Package | Architecture | Size | Recommendation | Direct Download |
| :--- | :--- | :--- | :--- | :--- |
| **HotspotXray-arm64.apk** | `arm64-v8a` | ~67 MB | **Recommended** (Pixel, Samsung, Xiaomi, etc.) | [Download](https://github.com/shayanmahster/HotspotXray/releases/download/v1.0.0/HotspotXray-v1.0.0-arm64.apk) |
| **HotspotXray-universal.apk** | Universal (All ABIs) | ~126 MB | Compatibility for all architectures | [Download](https://github.com/shayanmahster/HotspotXray/releases/download/v1.0.0/HotspotXray-v1.0.0-universal.apk) |

---

## ✨ Features

- 🚀 **100% Rootless:** Operates via [Shizuku](https://shizuku.rikka.app/) using system-level test network bindings.
- ⚡ **Full Xray-core Engine:** Embedded native Go core supporting:
  - **VLESS** (Reality, TLS, Vision, WebSocket, gRPC, XHTTP / SplitHTTP)
  - **Trojan** (TLS, WebSocket, gRPC)
  - **VMess** & **Shadowsocks**
- 🌐 **Zero Client Config:** Connected laptops, TVs, and phones do not need proxy settings, certificates, or VPN clients.
- 🔒 **Transparent DNS & Anti-Leak:** Intercepts port 53 UDP traffic from downstream clients and routes it through Xray's internal DNS routing engine.
- 📱 **Host Device Separation:** Your host Android phone does not show a system VPN icon, meaning your local banking apps, local government services, and domestic traffic continue to work untouched.
- 📊 **Real-time Traffic Monitor:** Live upload/download throughput counter and active connection metrics in Jetpack Compose UI.

---

## 🛠️ Requirements & Setup

### Requirements:
1. **Android 11 or higher** (API level 30+).
2. **[Shizuku](https://shizuku.rikka.app/)** (Version 13.5.0 or newer).

### Step-by-Step Setup:

1. **Activate Shizuku:**
   - Install Shizuku from Google Play or GitHub.
   - Start Shizuku service via **Wireless Debugging** (in Android Developer Options) or via ADB on your computer:
     ```bash
     adb shell sh /sdcard/Android/data/moe.shizuku.privileged.api/start.sh
     ```
2. **Install HotspotXray:**
   - Download and install `HotspotXray-arm64.apk`.
   - Open HotspotXray and tap **Grant Shizuku Permission**.
3. **Import Node:**
   - Copy any VLESS or Trojan share link (clipboard).
   - In HotspotXray, tap **+ Import Node** (or paste your config).
4. **Enable Hotspot:**
   - Turn on your phone's personal **Wi-Fi Hotspot** in Android Settings.
5. **Start Gateway:**
   - Tap the large **Power** button in HotspotXray.
   - Once the status switches to **Connected**, connect any client (PC, TV, phone) to your Hotspot. All client traffic will immediately route through your Xray node!
-----
Donate

```0x2aE228b62160f7c0DF3a3335CbE1D8C0E70a4ca0``` USDT(BSC)

---
## 🔒 License & Notice

This repository distributes pre-compiled binaries of HotspotXray. 
Copyright &copy; 2026. All rights reserved. Proprietary / Closed Source.

