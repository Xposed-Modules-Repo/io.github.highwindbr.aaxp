# AA Experiments

**AA Experiments** is an independent, open-source **LSPosed module and Android manager** for discovering, inspecting and selectively overriding Android Auto experiment flags.

The manager analyzes installed or imported Android Auto APK/APKM/APKS packages locally. It identifies compatible scalar getters and only publishes active overrides for the exact installed base/split build fingerprint. It does not patch, resign, install or redistribute Android Auto.

## Features

- Search and inspect discovered **Android Auto experiment flags**.
- Configure eligible **BOOLEAN, LONG, DOUBLE and STRING overrides**.
- Optional Advanced Overrides for a separately reviewed subset of getters, with explicit risk warnings, two-stage confirmation and Pause / Resume / Restore.
- View read-only getter probes and Video Timing Controller diagnostics.
- Export large catalogs as JSON or CSV and preserve normal, Advanced and Experimental settings in an exact-build recovery bundle.
- Review or suspend incompatible mappings rather than silently applying them after Android Auto updates.

## Requirements

- Android 8.1 / API 27 or newer.
- A compatible LSPosed framework providing libxposed API 101.
- Android Auto installed; scope the module to `com.google.android.projection.gearhead` in LSPosed.

## Installation

1. Download the official, release-key-signed APK from [Xposed Module Repo](https://github.com/Xposed-Modules-Repo/io.github.highwindbr.aaxp/releases) or from developer repo [**AA Experiments** Releases](https://github.com/HighwindBR/AA-Experiments/releases).
2. Install the APK and enable **AA Experiments** in LSPosed.
3. Confirm if **Android Auto** is selected in the module's LSPosed scope.
4. Restart Android Auto process as needed and open **AA Experiments** to analyze installed build.
5. Make changes deliberately; no flags are overridden by default. Keep a backup and use the built-in Restore controls if you experience issues.

## Safety and privacy

Eligible getters are not guaranteed to make a feature work: the Android Auto app, Google servers and the connected head unit may impose additional conditions. Advanced entries are **not** universally editable, and some values can affect stability or safety. Full recovery backups are **not encrypted or authenticated**, may include raw STRING values and should be kept private; use only matching-build backups from trusted sources.

Scans and analysis run locally. The application has no developer-operated backend or telemetry. See the main project's [privacy](https://github.com/HighwindBR/AA-Experiments/blob/main/PRIVACY.md) and [known limitations](https://github.com/HighwindBR/AA-Experiments/blob/main/docs/KNOWN_LIMITATIONS.md) for details.

## Links

- [**Source, documentation and support**](https://github.com/HighwindBR/AA-Experiments)
- [**Feature catalog**](https://github.com/HighwindBR/AA-Experiments/blob/main/FEATURE_CATALOG.md)
- [**Official APK releases**](https://github.com/HighwindBR/AA-Experiments/releases)

**Application ID:** `io.github.highwindbr.aaxp`
**License:** GPL-3.0-or-later
**Author:** HighwindBR

This is an independent project and is not affiliated with Google, Android Auto or LSPosed.
