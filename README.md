# VaultDesk releases

Signed installers for **VaultDesk**, the secure workspace for Windows. This repository holds releases only; there is no source code here.

## Install

Requires Windows 10 version 2004 or later, or Windows 11 (64-bit).

Open **PowerShell** and run:

```powershell
irm https://github.com/Quantuvate/vaultdesk-releases/releases/latest/download/Install-VaultDesk.ps1 | iex
```

The installer downloads the latest version, checks it against its published checksum, asks for administrator approval once to trust the VaultDesk signing certificate, then installs and starts VaultDesk.

You need an enrollment code from your VaultDesk administrator to connect the app to your organization.

## Updates

You only install once. VaultDesk checks this repository when it starts and every 30 minutes while it runs. When a new version is published it downloads it, installs it and reopens by itself.

## Files in each release

| File | What it is |
|---|---|
| `VaultDesk_<version>_x64.msix` | The application package |
| `vaultdesk-update.json` | Version, checksum and download address, read by the app and the installer |
| `VaultDesk.cer` | Public certificate the package is signed with |
| `Install-VaultDesk.ps1` | First-time installer |
