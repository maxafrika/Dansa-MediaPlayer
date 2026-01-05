# Dansa-MediaPlayer

**Dansa** is a modern, high‑performance Windows media player built for precision playback, advanced codec support, and full hardware acceleration. It is designed as a clean, extensible alternative to traditional media players, with a focus on stability, control, and future‑ready rendering.

Dansa is powered by a custom FFmpeg‑based decoding pipeline and a WPF user interface, allowing fine‑grained control over audio/video playback while maintaining a modern desktop experience.

---

## Features

* Playlist‑based playback (VLC‑style)
* Wide format support via FFmpeg
* Hardware‑accelerated video decoding (DXVA2 / D3D11)
* AV1 hardware decoding support (where supported by GPU & drivers)
* Frame‑accurate seeking and stepping
* Playback speed control
* Subtitle support (SRT / ASS)
* Keyboard shortcuts (space, arrow keys, frame stepping)
* Audio pipeline designed for visualizers and advanced processing
* Media library scanning
* Clean, modern WPF interface
* Extensible architecture for future features such as super‑resolution scaling

---

## 🖥️ Platform

* **Operating System:** Windows 10 / Windows 11
* **Framework:** .NET 8 (WPF)
* **Architecture:** x64

---

## Getting Started

### Requirements

* Windows 10 or later
* .NET 8 SDK
* Visual Studio 2022 (with **.NET Desktop Development** workload)
* Windows 10/11 SDK

### Build Instructions

1. Clone the repository:

   ```bash
  (https://github.com/maxafrika/Dansa-MediaPlayer)
   ```

2. Open the project in Visual Studio:

   * Open `DansaUltraPlayer.csproj`

3. Set the project as the **Startup Project**

4. Build and run:

   ```
   Build → Rebuild Solution
   Ctrl + F5
   ```

> **Note:** FFmpeg decoding and hardware acceleration require native FFmpeg binaries to be present. Playback will not function until FFmpeg is correctly integrated.

---

## FFmpeg Integration

Dansa uses **FFmpeg** for decoding audio and video formats.

* FFmpeg is **not bundled by default** in this repository
* You must supply compatible FFmpeg binaries at runtime
* Hardware acceleration (DXVA2 / D3D11 / AV1) depends on GPU, drivers, and FFmpeg build configuration

The FFmpeg engine is isolated within the playback layer, allowing safe fallback to software decoding if hardware acceleration is unavailable.

---

## Subtitles

Dansa supports subtitle rendering through FFmpeg and external libraries:

* **SRT** (SubRip)
* **ASS** (Advanced SubStation Alpha)

Subtitles are rendered as an overlay synchronized to the playback clock.

## Security Considerations

* No shell execution of media files
* No dynamic script execution
* No network activity by default
* Media decoding isolated from UI thread

Dansa is designed to safely handle untrusted media files using FFmpeg’s mature decoding pipeline.

---

##License

### Dansa License

This project is licensed under the **MIT License**.

You are free to:

* Use the software commercially
* Modify the source code
* Distribute original or modified versions

See the `LICENSE` file for full details.

---

##Third‑Party Licenses

### FFmpeg

Dansa uses **FFmpeg**, which is licensed under the **LGPL v2.1 or later**, or **GPL v2 or later**, depending on how FFmpeg is built.

* FFmpeg is **not authored by the Dansa project**
* FFmpeg is a trademark of **Fabrice Bellard**, the originator of the FFmpeg project

If you distribute Dansa with FFmpeg binaries:

* You must comply with FFmpeg’s license terms
* Provide appropriate attribution
* Provide source code or offer source access if required by the chosen FFmpeg license

For more information, see:

* [https://ffmpeg.org/legal.html](https://ffmpeg.org/legal.html)

---

## Disclaimer

Dansa is provided **"as is"**, without warranty of any kind. The authors are not responsible for media compatibility issues, data loss, or damages resulting from the use of this software.

## Contributing

Contributions are welcome.

* Fork the repository
* Create a feature branch
* Submit a pull request with clear descriptions

By contributing, you agree that your contributions will be licensed under the MIT License.

---

##Contact

Project: **Dansa Media Player**
Maintainer: Max Afrika / DansaMzansi
GitHub: https://github.com/maxafrika/Dansa-MediaPlayer
