# PortalPerch

![PortalPerch owl](PortalPerch.png)

PortalPerch is a Windows Service that signs into websites and verifies their protected pages without an interactive desktop session.

[Download the latest Windows installer and user manual](https://github.com/Prestonwbagby/portalperch-releases/releases/latest).

## Features

- Local web dashboard for adding, editing, pausing, and removing websites.
- Green health indicators, last check times, and check history.
- Compact website rows with details on hover or through a Details button.
- Copy existing website configurations, including saved credentials and schedules, into a separate paused website.
- Username/password login and protected-page content verification.
- Per-site daily schedules with intervals from 5 to 999 minutes and configurable consecutive-failure thresholds.
- Independent checks of the monitoring server's internet access to avoid counting general server outages as site failures.
- Email and Microsoft Teams Workflow notifications with master and per-website recipient lists.
- Daily GitHub update checks and a manual dashboard check.
- Standalone Windows x64 installer including .NET, Chromium, and the PDF manual.

## Install or upgrade

Download the installer from Releases and run it as an administrator on Windows Server with Desktop Experience. First installation asks you to set a dashboard administrator password. Open the dashboard shortcut or http://127.0.0.1:5080 on the server, and sign in as `admin`.

Before an upgrade, back up the complete `C:\ProgramData\PortalPerch` folder. Setup retains settings and the administrator password and restarts the service. Monitoring pauses during installation. PortalPerch checks for releases but does not install upgrades automatically.

Each release includes its installer, a PDF user manual, and `SHA256SUMS.txt`. The dashboard accesses this public repository without requiring a GitHub token. Website credentials and monitoring data are stored on your server; they are not sent to GitHub by the update checker.

This repository distributes compiled releases and documentation. Application source code is not published here.
