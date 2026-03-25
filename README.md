# Octoplus-driver-installer-helper
Octoplus / Medusa Box Driver Helper
Overview
This tool is a compiled AutoIt utility for Windows 10/11 64‑bit only, used to help install Octoplus / Medusa Box USB and smart‑card drivers and clean problematic SCFILTER\CID_* smart‑card filter entries. It is intended for situations where the card is not detected or Windows reports driver compatibility issues.

What It Does
Installs the .inf driver files that are already present in the same folder as this EXE using pnputil /add-driver /install.

Cleans UpperFilters values under HKLM\SYSTEM\CurrentControlSet\Enum\SCFILTER\CID_*, which can help repair broken smart‑card stacks that prevent the Octoplus card from being detected.

This tool does not modify Octoplus/Medusa software; it only helps Windows bind the drivers you already placed in the folder.

Requirements
Windows 10 or Windows 11, 64‑bit (x64) only.

Local administrator rights.

Driver signature enforcement must already be disabled for this boot before running the tool.

Official Octoplus / Medusa driver .inf files already copied into the same folder as this EXE.

Usage
Before using the tool

Boot Windows 10/11 x64 with driver signature enforcement disabled (Advanced startup → Startup Settings → Disable driver signature enforcement).

Folder layout

This EXE and all required Octoplus / Medusa .inf driver files must be in the same folder.

No manual configuration is needed; the tool uses its own folder automatically.

Run the helper

Disconnect your Octoplus / Medusa box from USB.

Right‑click the EXE → Run as administrator.

Follow the prompts:

The tool installs the .inf drivers found in its folder.

When prompted, reconnect the box and wait a few seconds.

The tool then performs SCFILTER UpperFilters cleanup.
