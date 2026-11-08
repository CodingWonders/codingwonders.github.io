---
date: 2026-11-07
categories:
  - release
  - Discovery
---
# DISMTools 0.9 Preview 1 - Now available

The first preview of DISMTools 0.9 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.9_pre_26111)

## What's new?

### Preinstallation Environment Helper

- In the WDS Helper Client, authentication flows have been revamped to make them more secure. Additionally, you will now be asked if the provided credentials are valid:

<p align="center">
  <img src="https://github.com/user-attachments/assets/eba0a88a-de63-49a4-9b77-b2e34d6dbdd7" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/5ef5f989-e389-4505-a360-757e675f09e6" />
</p>

- DISMTools now downloads and installs [Windows ADK version 10.1.28000.3481](https://learn.microsoft.com/en-us/windows-hardware/get-started/what-s-new-in-kits-and-tools#whats-new-in-adk-101280003481-october-2026)

### Unattended answer file features

- In addition to user account names blocked in an English installation of Windows, user account names of the Windows installation in your language are now blocked
- User accounts are now specified in cards. You can now add more than 5 local accounts

### System Service Manager

- DISMTools can now grab service display names and descriptions from MUI packs
- In the service dependency diagram, if the service display name can be grabbed for a service, you will now see the service name below it:

<p align="center">
  <img src="https://github.com/user-attachments/assets/4532dae3-98ef-46af-9823-be5d177dfe28" />
</p>

### Miscellaneous

- The following libraries and components have been updated:

| Component | Previous version | New version |
|:--:|:--:|:--:|
| [Markdig](https://github.com/xoofx/Markdig) | `1.5.1` | `1.6.0` |

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.9_pre_26111) and **reporting feedback to us**.

<p align="center">
  <img src="https://codingwonders.github.io/pictures/dt_relnotes/report_feedback.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://codingwonders.github.io/pictures/dt_relnotes/contrib_to_helpsys.png" />
</p>

We're also working on the next preview release of DISMTools, so expect more enhancements and goodies in around 2 weeks (November 22).