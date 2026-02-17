# EzFrame

**Master your Samsung The Frame TV**

EzFrame is a free desktop application that makes managing your Samsung The Frame TV effortless. Replace expensive Art Store subscriptions and complex SmartThings workflows with a simple, elegant solution that runs entirely on your local network.

## ✨ Features

- **🔍 Auto-Discovery**: Automatically finds your Frame TV on the network (no manual IP entry needed)
- **⚡ Fast Upload**: Drag & drop images directly to your TV. Supports batch upload with automatic 4K optimization
- **📚 Art Library Management**: Browse, organize, and manage your entire art collection. Perform bulk operations (delete, change matte) with just a few clicks
- **🎮 Smart Controls**: Full TV control from your desktop - with hotkeys for quick actions without leaving your computer
- **🖼️ Matte Customization**: Easily change matte type and color for your artwork. Unlock 4 additional hidden mattes in your TV
- **🆓 Completely Free**: No subscriptions, no ads, no data collection. Everything runs on your local network
- **🌐 Cross-Platform**: Available for macOS, Windows, and Linux

## 🚀 Installation

### Download binaries

Download the latest release from the [Releases page](https://github.com/viet241/EzFrame/releases/latest).

| Platform | Architecture | Filename |
|----------|-------------|------------------|
| **macOS** | Intel (x86_64) | `EzFrame_*_x64_x86_64.dmg` |
| **macOS** | Apple Silicon (arm64) | `EzFrame_*_aarch64_arm64.dmg` |
| **macOS** | Intel (x86_64) - Portable | `EzFrame_x86_64.app.tar.gz` |
| **macOS** | Apple Silicon (arm64) - Portable | `EzFrame_arm64.app.tar.gz` |
| **Windows** | x64 | `EzFrame_*_x64_en-US.msi` |
| **Linux** | x64 | `EzFrame_*_amd64.AppImage` |
| **Linux** | x64 (Debian/Ubuntu) | `EzFrame_*_amd64.deb` |

### System Requirements

- Samsung The Frame TV (2024 or newer models recommended)
- Your computer and TV must be on the same local network
- macOS 10.15+, Windows 10+, or Linux (Ubuntu 20.04+)

## 🐛 Known Issues & Limitations

- App has not been tested on all Frame TV models - feedback on compatibility is welcome
- Code signing is not implemented (OS security warnings are expected)
- Some advanced TV features may not be available depending on your TV model

## 🔧 Troubleshooting Installation

### macOS - Bypass Gatekeeper

If macOS blocks the app from opening, remove the quarantine attribute using Terminal:

```bash
# After installing from .dmg
xattr -d com.apple.quarantine /Applications/EzFrame.app

# Or if using the portable .app.tar.gz version
xattr -d com.apple.quarantine /path/to/EzFrame.app
```

### Windows - Bypass SmartScreen

If Windows SmartScreen blocks the installer:

1. When you see the "Windows protected your PC" warning, click **"More info"**
2. Click **"Run anyway"** button
3. The installer will proceed normally

**Note**: These security warnings appear because the app is not code-signed. The application is safe to use - it's a personal project that doesn't collect any data and runs entirely on your local network.



## 📖 Usage

1. **Launch EzFrame** on your computer
2. **Auto-Discovery**: The app will automatically scan for Frame TVs on your network
3. **Connect**: Select your TV from the list and connect
4. **Upload Art**: Drag and drop images directly onto the app, or use the upload button
5. **Manage Library**: Browse your art collection, change mattes, delete images, or set them as the current display
6. **Control TV**: Use the built-in controls or keyboard shortcuts to navigate your TV

## 🐞 Debug Mode & Capturing Logs

If you run into connection issues, TV errors, or want to report a bug with useful context, you can enable **Debug Mode** to record detailed logs. All logs (app and TV communication) are written to a single file that you can save and share.

### Enabling debug mode

- **Keyboard shortcut**: Press the **Z** key **5 times** quickly (within about 2 seconds). A toast will confirm that debug mode is on, and a debug bar will appear at the bottom of the window.
- **Turning off**: Click the **X** on the debug bar, or press **Z** five times again.

### What gets logged

When debug mode is on, the app records:

- **User actions**: Connect, disconnect, tab changes, button clicks, uploads, remote key presses, etc. (prefixed as `[USER_EVENT]`).
- **TV communication**: Commands sent to the TV and responses received (prefixed as `[RUST]` or `[TV_WS_RECV]` / `[TV_RESPONSE]`).
- **Frontend logs**: Console output from the app UI.

Logs are written in a compact, single-line format to keep the file size manageable.

### Saving or clearing the log

- **Save Debug Log**: On the debug bar, click **Save Debug Log** to choose a location and save the current log file (e.g. to attach to a GitHub issue).
- **Clear Log**: Click **Clear Log** to empty the in-memory log file and start fresh (e.g. before reproducing a bug).

### Tips for reporting issues

1. Enable debug mode (press **Z** five times).
2. Reproduce the problem (connect, upload, use a feature, etc.).
3. Click **Save Debug Log** and attach the saved file to your GitHub issue.
4. Optionally turn off debug mode when you are done (click **X** on the debug bar).

This helps maintainers see exactly what the app and TV exchanged and what you did before the issue occurred.

## 💬 Feedback & Support

We'd love to hear your feedback! If you find EzFrame useful, please:

- ⭐ Star this repository
- 🐛 Report bugs or request features via [Issues](https://github.com/viet241/EzFrame/issues). If you encounter a bug, please include a debug log when creating your issue—this helps us resolve problems much faster!
- 💡 Share your ideas and suggestions

## ☕ Support Development

This project is completely free to use. If you find EzFrame useful for your The Frame TV, consider supporting the development:

<a href="https://ko-fi.com/viet241" target="_blank" rel="noopener noreferrer">
  <img 
    height="36" 
    style="border: 0px; height: 36px;" 
    src="https://storage.ko-fi.com/cdn/kofi6.png?v=6" 
    alt="Buy Me a Coffee at ko-fi.com" 
  />
</a>


## 📧 Contact

- GitHub: [@viet241](https://github.com/viet241)
- Issues: [GitHub Issues](https://github.com/viet241/EzFrame/issues)

---

**Made with ❤️ for The Frame TV community**
