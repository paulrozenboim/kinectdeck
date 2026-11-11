# KinectDeck

**Official Portal & Beta Access:** [https://kinect.unapaulogetic.art/](https://kinect.unapaulogetic.art/)

**KinectDeck** is a standalone Windows desktop application built for live visualists, VJs, and interactive media artists. It bridges Microsoft Kinect hardware directly into modern real-time visual pipelines—processing depth feeds, isolating human silhouettes, and routing low-latency video streams straight into TouchDesigner, Resolume, and NDI-compatible environments.

---

## Key Capabilities

* **Real-Time Depth & Silhouette Isolation:** Clean depth-map thresholding, person scanning, and background stripping without complex node setups.
* **Native NDI Output:** Stream processed depth, IR, and segmented player feeds directly over NDI into TouchDesigner (`NDI In TOP`), Resolume Arena, or MadMapper.
* **Plug-and-Play Hardware Control:** Dedicated desktop HUD for sensor tilt, depth clipping planes, smoothing, and live capture libraries.
* **Built for the Booth:** Lightweight, zero-bloat Windows performance designed to run reliably alongside heavy GPU rendering workflows.

---

## System Requirements

* **OS:** Windows 10 / Windows 11 (64-bit)
* **Hardware:** Microsoft Kinect Sensor (with USB 3.0 PC Adapter)
* **Pipeline Support:** NDI-compatible receiver (TouchDesigner, Resolume, OBS, etc.)

---

## Releases & Beta Access

Visit **[kinect.unapaulogetic.art](https://kinect.unapaulogetic.art/)** for visual breakdowns, signal-path previews, and beta access updates. Public builds and release notes are published under the **Releases** tab of this repository.

---

## Web Portal Development

This repository also serves the static web showcase deployed at `kinect.unapaulogetic.art` via Cloudflare Workers (`public/`).

```powershell
# Local HTTP preview ([http://127.0.0.1:4322/](http://127.0.0.1:4322/))
py -3.12 -m http.server 4322 --bind 127.0.0.1 --directory public

# Deploy to Cloudflare
npx wrangler deploy
```

---

**Created by Paul Rozenboim ([unapaulogetic](https://unapaulogetic.art/))**  
[unapaulogetic.art](https://unapaulogetic.art/) · [paulrozenboim.com](https://www.paulrozenboim.com/)
