# ArgusTuil — Custom Windows Utility

[![Version](https://img.shields.io/github/v/release/ar4us/ArgusTuil?color=10B981&label=Latest%20Release&style=for-the-badge)](https://github.com/ar4us/ArgusTuil/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-10B981?style=for-the-badge)](LICENSE)

**ArgusTuil** is a fully customized, premium Windows system utility designed under the **Emerald Oasis** theme. It streamlines system setup, debloats Windows telemetry/UWP apps, installs developer and system tools, configures advanced system options, and manages Windows updates. 

Designed for clean Windows installations, it provides a sleek dark interface with vibrant emerald accents.

---

## Quick Start

> [!IMPORTANT]
> **ArgusTuil must be run as Administrator** because it performs system-wide registry, service, and policy changes.

Open **PowerShell** (or **Windows Terminal**) as **Administrator** and run the following command:

```powershell
irm ar4us.github.io/ArgusTuil/argustuil.ps1 | iex
```

### How to open an admin terminal:
1. Right-click the Start button and select **Terminal (Admin)** or **Windows PowerShell (Admin)**.
2. Or, press the `Windows key`, type `PowerShell`, and press `Ctrl + Shift + Enter`.

---

## Key Features

- **Software Installer:** Batch install and update common apps via `Winget` and `Chocolatey` in a structured category layout.
- **System Tweaks:** Apply privacy modifications, disable telemetry, Cortana, OneDrive, background apps, and apply system responsiveness boosts.
- **Config & Features:** Enable/disable built-in Windows features (WSL, Hyper-V, .NET Frameworks, Sandbox) and configure network/DNS settings.
- **Windows Updates:** Take control of Windows Updates (defer upgrades, pause updates, or restore default configurations).

---

## Automation / Presets

Apply a predefined configuration silently without manual selection:

```powershell
& ([ScriptBlock]::Create((irm ar4us.github.io/ArgusTuil/argustuil.ps1))) -Preset Standard
```

| Preset | Description |
|--------|-------------|
| `Standard` | Balanced defaults recommended for most users |
| `Minimal` | Minimal changes to suit every user's workflow |
| `Advanced` | Deep system optimizations for power users |

---

## Build & Local Development

To modify the source files locally and rebuild the main script:

1. Clone the repository:
   ```bash
   git clone https://github.com/ar4us/ArgusTuil.git
   cd ArgusTuil
   ```

2. Make your edits in `xaml/inputXML.xaml`, `config/` files, or the `functions/` directory.

3. Recompile the utility:
   ```powershell
   powershell -ExecutionPolicy Bypass -File Compile.ps1
   ```

4. Test your local build:
   ```powershell
   powershell -ExecutionPolicy Bypass -File Compile.ps1 -Run
   ```

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
