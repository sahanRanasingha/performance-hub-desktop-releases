# Performance Hub — Downloads & Installation Guide

Official release repository for the **Artslab Performance Hub Desktop Application** for Windows and macOS.

The Performance Hub desktop app gives you real-time background push notifications, system tray/menu bar integration, unread badge alerts, and automatic updates.

---

## 📥 Download the Latest Version

Go to the [**Latest Releases Page**](https://github.com/sahanRanasingha/performance-hub-desktop-releases/releases/latest) and download the appropriate installer for your operating system:

| Operating System | Architecture | Installer File |
|---|---|---|
| **Windows 10 / 11** | 64-bit (x64) | `PerformanceHub-Setup-x.y.z.exe` |
| **macOS (Apple Silicon)** | M1 / M2 / M3 / M4 (`arm64`) | `PerformanceHub-x.y.z-arm64.dmg` |
| **macOS (Intel)** | Intel Core i5/i7/i9 (`x64`) | `PerformanceHub-x.y.z-x64.dmg` |

> *Tip: If you are unsure which Mac you have, click the **Apple logo () → About This Mac**. Look at the **Chip** (Apple Silicon: M1/M2/M3/M4) or **Processor** (Intel).*

---

## 🪟 Windows Installation Guide

### Step 1: Download & Run Installer
1. Download **`PerformanceHub-Setup-x.y.z.exe`**.
2. Double-click the downloaded `.exe` file to begin installation.

### Step 2: Windows Defender SmartScreen Prompt
Because this application is distributed directly by Artslab, Windows SmartScreen may display a blue warning screen stating:

> *"Windows protected your PC — Microsoft Defender SmartScreen prevented an unrecognized app from starting."*

This is normal for newly released desktop apps. To proceed:
1. Click **More info** (underlined text below the message).
2. Click the **Run anyway** button that appears in the bottom right corner.

### Step 3: Complete Setup
1. Follow the setup wizard to choose your install location (or accept the default).
2. Keep **Create Desktop Shortcut** and **Create Start Menu Shortcut** checked.
3. Click **Finish**. Performance Hub will launch and log you in.

---

## 🍏 macOS Installation Guide

### Step 1: Download & Mount Disk Image
1. Download the correct `.dmg` file for your Mac:
   - For Apple Silicon (M1/M2/M3/M4): `PerformanceHub-x.y.z-arm64.dmg`
   - For Intel Macs: `PerformanceHub-x.y.z-x64.dmg`
2. Double-click the downloaded `.dmg` file to open it.
3. Drag the **Performance Hub** icon into your **Applications** folder.

---

### Step 2: First-Time Launch (macOS Security & Gatekeeper)
Because the app is ad-hoc signed, macOS Gatekeeper may show a security dialog when you first open it:

> *"Performance Hub cannot be opened because Apple cannot check it for malicious software"* or *"cannot be opened because the developer cannot be verified"*.

To allow Performance Hub to run, follow these quick steps:

#### Method A: Via System Settings (Recommended)
1. Try opening **Performance Hub** from your **Applications** folder once (click **OK** or **Cancel** on the prompt).
2. Open your Mac's **System Settings** (or **System Preferences**).
3. In the left sidebar, click **Privacy & Security**.
4. Scroll down to the **Security** section.
5. You will see a note:
   > *"Performance Hub" was blocked from use because it is not from an identified developer.*
6. Click the **Open Anyway** button next to it.
7. Enter your Mac user password or use Touch ID when prompted.
8. Click **Open** on the confirmation dialog.

*(You only have to do this once. Performance Hub will open normally on all future launches!)*

#### Method B: Fast Terminal Command (For Power Users)
Alternatively, open your Mac **Terminal** and run:
```bash
xattr -cr "/Applications/Performance Hub.app"
```
Then double-click **Performance Hub** in Applications to launch immediately.

---

## 💡 How the App Works (Tips & Tricks)

### 1. Runs in Background / System Tray
- When you click the **Close (X)** button, the app does not shut down. It minimizes to the **System Tray** (Windows, bottom-right near clock) or the **Menu Bar** (macOS, top-right).
- This keeps your push notifications and alerts working in real time!
- To fully quit the app: Right-click the Performance Hub tray icon and select **Quit Performance Hub**.

### 2. Launch at Startup
- Right-click the tray icon and check **Launch at startup** so Performance Hub starts automatically whenever you turn on your computer.

### 3. Push Notifications & Badges
- Push notifications arrive as native desktop toasts even when the app is hidden in the background. Clicking a notification opens the relevant page in Performance Hub.
- The macOS Dock icon shows an unread count badge, and the Windows taskbar shows a red indicator dot when unread notifications are waiting.

### 4. Automatic Updates
- **Windows**: The app checks for updates every 4 hours. Updates download silently in the background and install automatically when you restart the app.
- **macOS**: When a new version is released, you will receive a desktop notification alerting you that an update is available with a link to download the new version.

---

## ❓ Frequently Asked Questions (FAQ)

<details>
<summary><b>Why does Windows show "Windows protected your PC"?</b></summary>
Artslab distributes this app internally and independently. Windows flags any app that does not yet possess an expensive commercial EV Authenticode certificate. Clicking <b>More info → Run anyway</b> is safe and expected.
</details>

<details>
<summary><b>Why does macOS block opening the app on the first run?</b></summary>
macOS Gatekeeper blocks apps from outside the Mac App Store that haven't been notarized through an Apple Developer account. Following the <b>System Settings → Privacy & Security → Open Anyway</b> step authorizes the app on your computer.
</details>

<details>
<summary><b>How do I check for updates manually?</b></summary>
Right-click the Performance Hub icon in your Windows System Tray or Mac Menu Bar and select <b>Check for updates…</b>.
</details>

---

## 🔒 Security & Privacy

Performance Hub is built with sandboxed Electron architecture:
- External links automatically open in your default system web browser.
- Device storage and credentials are kept strictly isolated.
- Communication with Artslab servers is secured over encrypted HTTPS.
