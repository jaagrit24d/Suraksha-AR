[README (1).md](https://github.com/user-attachments/files/33624220/README.1.md)
<div align="center">

# 🔥 Suraksha AR

**Learn how a fire extinguisher works by exploring it in augmented reality.**
Point your phone, pick up a virtual extinguisher with your hand, and discover what every part does.

![Unity](https://img.shields.io/badge/Unity-6000.5.10f1-black?logo=unity)
![Platform](https://img.shields.io/badge/Platform-Android%20(ARCore)-3DDC84?logo=android&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue)

</div>

---

## Demo


https://github.com/user-attachments/assets/3d617a91-daad-4427-8122-5b83a5f34c90



---

## About

*Suraksha* means **safety**. In an emergency, there is no time to read the label on a fire extinguisher, yet most people never learn how to use one until they have to.

Suraksha AR turns that learning into something hands-on. A full 3D fire extinguisher appears in your real surroundings through the phone camera. You can move it, turn it around, and look at it from any angle. As you explore, an on-screen panel names each part and explains what it does and how to use it correctly.

---

## Features

| | Feature | What it does |
|---|---|---|
| 📱 | **Augmented reality** | A 3D fire extinguisher is placed in the live camera view, so you learn on a life-size object in your own space |
| ✋ | **Hand interaction** | Use your bare hand in front of the camera to move and inspect the model, with no buttons needed |
| 🏷️ | **Part-by-part guidance** | An info panel shows the name of each part, a short description, and step-by-step usage tips |
| 🔄 | **View from every angle** | Rotate the model to see the nozzle, handle, gauge and pin from all sides |

---

## What You'll Learn

| Part | What it does |
|---|---|
| **Nozzle** | Directs the extinguishing agent toward the fire. Squeeze the handle while sweeping the nozzle side to side at the base of the fire |
| **Pressure Gauge** | Shows whether the extinguisher is charged and ready to use |
| **Safety Pin** | Prevents accidental discharge. Pull the pin firmly to break the seal, aiming the nozzle away from yourself |

> ⚠️ **Disclaimer:** Suraksha AR is an educational tool. It does not replace hands-on fire safety training from a qualified instructor. In a real fire, prioritise your safety and call your local emergency number.

---

## Requirements

- An Android device running **Android 7.0 or higher** with **ARCore support** ([check the supported devices list](https://developers.google.com/ar/devices))
- A working camera and good lighting
- Enough free space to move your hand in front of the camera

---

## Building from Source

### Prerequisites
- [Unity Hub](https://unity.com/download) with **Unity 6000.5.10f1**
- Unity modules: **Android Build Support**, including **OpenJDK** and **Android SDK & NDK Tools**
- An ARCore-supported Android phone with **USB debugging** enabled

### Steps
1. Clone the repo:
   ```bash
   git clone https://github.com/jaagrit24d/Suraksha-AR.git
   ```
2. In Unity Hub, click **Add → Add project from disk** and select the cloned folder.
3. Open it with **Unity 6000.5.10f1**. The first import takes a while while Unity rebuilds the `Library` folder.
4. Go to **File → Build Profiles**, select **Android**, and click **Switch Platform**.
5. Connect your phone and click **Build and Run**.

The MediaPipe package lives in `LocalPackages/com.github.homuler.mediapipe` and resolves automatically on first open, so no extra setup is needed.

### Recommended Player Settings
| Setting | Value |
|---|---|
| Scripting Backend | IL2CPP |
| Target Architectures | ARM64 |

> **Note:** AR doesn't work fully inside the Unity editor. Test on a real Android device.

---

## Project Structure

```
Assets/            Scenes, scripts, 3D models and UI
LocalPackages/     Local MediaPipe Unity plugin package
Packages/          Unity package manifest
ProjectSettings/   Unity project configuration
```

---

## Troubleshooting

| Problem | Fix |
|---|---|
| Phone not listed in Run Device | Replug the cable, set USB mode to File Transfer, accept the USB debugging prompt, then click **Refresh** |
| Black screen or no camera feed | Make sure camera permission is granted and the phone supports ARCore |
| Model doesn't appear | Move the phone slowly and point it at a well-lit area so ARCore can track the surroundings |
| Hand not detected | Use brighter lighting and keep your whole hand inside the camera view |

---

## Tech Stack

- Unity 6 (6000.5.10f1)
- AR Foundation + ARCore
- MediaPipe Hand Landmarker (via the MediaPipe Unity Plugin)
- Universal Render Pipeline (URP)
- C#, Android

---

## Acknowledgements

- [MediaPipe Unity Plugin](https://github.com/homuler/MediaPipeUnityPlugin) by homuler (MIT)
- [MediaPipe](https://ai.google.dev/edge/mediapipe) by Google
- [AR Foundation](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@latest) and ARCore

---

## License

Released under the MIT License. Copyright (c) 2026 Aliasgersb. See [LICENSE](LICENSE) for details.

Third-party components, such as the MediaPipe Unity Plugin in `LocalPackages`, keep their own licenses.
