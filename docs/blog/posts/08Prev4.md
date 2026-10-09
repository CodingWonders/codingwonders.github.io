---
date: 2026-04-25
categories:
  - release
---
# DISMTools 0.8 Preview 4 - Now available

The fourth preview of DISMTools 0.8 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2642)

## What's new?

- When uploading a Windows image to a WDS server you can now create image groups
- From the Autorun application you can now specify the WDS image group to upload the image to
- The Autorun application and HotInstall have seen HiDPI improvements
- Partition table overrides can now be used when deploying images with the WDS Helper
- PXE Helper Servers can now be started using a different port by holding down SHIFT and performing an action in the following places:
	- From the Autorun application
	- From the Tools > Start PXE Helper Server for... menu in the main program
- A new policy has been added to change the default port to use when connecting to a PXE Helper server
- If a starter script offers customizable options you will now be notified
- The Starter Script Editor now detects read-only starter scripts and removes such attribute when saving them
- The following starter scripts are affected by this version:

| Starter Script                              | Stage                       |  State  |
| :------------------------------------------ | :-------------------------- | :-----: |
| **Refresh Windows Explorer**                | When the first user logs on | **New** |
| **Configure Start Menu Appearance**         | When the first user logs on | **New** |
| **Disable warnings for unsigned RDP files** | During System Configuration | **New** |

- When downloading packages from App Installer files you can now copy the URLs to the main application package
- The following libraries and components have been updated:

| Component | Version in latest preview | New version |
|:--:|:--:|:--:|
| [Markdig](https://github.com/xoofx/Markdig) | `1.1.2` | `1.1.3` |
| [Managed DISM API](https://github.com/jeffkl/ManagedDism) | `5.0.0` | `6.0.0` |
| [Windows API Code Pack](https://github.com/PWagner1/Windows-API-CodePack-NET) | `8.0.14` | `8.0.15.1` |
## What's fixed?

- Fixed an exception (#350)
- Registry hives that were unloaded externally no longer cause errors when unloading them from the image registry control panel
- Non-PowerShell-based endpoints no longer throw CORS issues when calling WDS Helper Server APIs
- Fixed an issue where App Installer download errors would not appear in the foreground

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2642) and **reporting feedback to us**.

<p align="center">
  <img src="https://i.imgur.com/KlPekhA.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://github.com/CodingWonders/DISMTools/assets/101426328/778b8900-c92b-4c53-88ed-fe42a3becaa1" />
</p>

We're also working on the next preview release of DISMTools, so expect more enhancements and goodies in around 2 weeks (May 10).