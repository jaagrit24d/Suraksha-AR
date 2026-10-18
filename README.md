# Suraksha-AR
[README.md](https://github.com/user-attachments/files/33623876/README.md)
<div align="center">

# ✋ AR Drawing

**Draw floating 3D strokes in augmented reality using just your bare hand.**
No stylus. No controller. No screen touches.

![Unity](https://img.shields.io/badge/Unity-6000.5.10f1-black?logo=unity)
![Platform](https://img.shields.io/badge/Platform-Android%20(ARCore)-3DDC84?logo=android&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue)

</div>

---

## Demo



https://github.com/user-attachments/assets/9a0d0857-b88c-4e85-b6b8-21f564d3ba46



---

## About

Most drawing apps are flat. They trap your creativity on a 2D canvas.

AR Drawing breaks that. Point your phone at any surface, raise your hand, and paint 3D strokes that float in the real world around you, anchored in space and visible through the camera.

---

## Features

| | Feature | What it does |
|---|---|---|
| 🖐️ | **Touchless hand tracking** | Real-time 21-point hand detection via MediaPipe at 60 fps, with adaptive filtering for smooth, jitter-free strokes |
| 🎛️ | **Gesture-driven interface** | Hold up an open palm to open a radial arc menu, then use finger taps to navigate and select tools |
| 🎨 | **Full drawing toolkit** | Multiple colors, brush sizes, an eraser, undo/redo and canvas clear, all operated by gestures |
| 💾 | **Save and gallery** | Save drawings as stroke data with an auto-generated thumbnail, then browse and reload past creations |
| 🔄 | **3D inspector** | View a saved drawing on a dedicated screen: rotate, zoom and twist it in 3D, then summon it back into your AR scene |

---

## How It Works

AR Drawing handles the hard math quietly so the experience feels effortless:

- **Async camera pipeline:** frames are processed for hand tracking on a background thread, so the main app stays at 60 fps.
- **One Euro Filter:** a custom adaptive filter removes jitter when your hand is still, but reacts instantly when you move fast.
- **Hysteresis boundaries:** the pinch gesture has separate thresholds for starting and stopping, so strokes don't flicker if your hand trembles.
- **Smart 2D eraser:** instead of expensive 3D raycasts, the app projects 3D strokes into screen space and deletes whatever your fingers wipe across.
- **Offscreen rendering:** when you save, a hidden camera captures a clean thumbnail of your 3D art on a black background.

---

## Requirements

- An Android device running **Android 7.0 or higher** with **ARCore support** ([check the supported devices list](https://developers.google.com/ar/devices))
- A working camera and good lighting for reliable hand tracking

---

## Installation (play the app)

1. Download the latest `.apk` from the [**Releases**](../../releases) tab.
2. On your phone, go to **Settings → Install unknown apps** and allow installs from your browser or file manager.
3. Open the downloaded `.apk` and tap **Install**.
4. Launch **AR Drawing** and grant **camera permission** when prompted.

---

## Building from Source

### Prerequisites
- [Unity Hub](https://unity.com/download) with **Unity 6000.5.10f1**
- Unity modules: **Android Build Support**, including **OpenJDK** and **Android SDK & NDK Tools**
- An ARCore-supported Android phone with **USB debugging** enabled

### Steps
1. Clone the repo:
   ```bash
   git clone https://github.com/Aliasgersb/YOUR_REPO_NAME.git
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

> **Note:** AR and hand tracking don't work fully inside the Unity editor. Test on a real Android device.

---

## Project Structure

```
Assets/            Scenes, scripts, UI and project content
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
| Pink materials | Render pipeline mismatch: check that the URP asset is assigned in **Project Settings → Graphics** |
| Hand not detected | Use brighter lighting and keep your whole hand inside the camera view |

---

## Tech Stack

- Unity 6 (6000.5.10f1)
- AR Foundation 6.3 + ARCore 6.3
- MediaPipe Hand Landmarker 0.16.3
- Universal Render Pipeline (URP) 17.3
- Unity UI Toolkit
- C#, Android

---

## Acknowledgements

- [MediaPipe Unity Plugin](https://github.com/homuler/MediaPipeUnityPlugin) by homuler (MIT)
- [MediaPipe](https://ai.google.dev/edge/mediapipe) by Google
- [AR Foundation](https://docs.unity3d.com/Packages/com.unity.xr.arfoundation@latest) and ARCore

---

## Author

**Aliasger Bhabhrawala**

[![GitHub](https://img.shields.io/badge/GitHub-Aliasgersb-181717?logo=github)](https://github.com/Aliasgersb)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Aliasger%20Bhabhrawala-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aliasger-bhabhrawala)

---

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
