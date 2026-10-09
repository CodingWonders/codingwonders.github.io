---
date: 2026-04-11
categories:
  - release
---
# DISMTools 0.8 Preview 3 - Now available, and guaranteed not to freeze in outer space

The third preview of DISMTools 0.8 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2641)

## What's new?

- The PE Helper is no longer responsible for removing custom policies; that is now done by the ISO creator wizard when it's closed
- A new DISMTools Preinstallation Environment policy has been added to let you configure whether you want to copy unattended answer files in your ISO to the target installation's Sysprep folder
- The WDS image upload wizard has seen several improvements:
	- The wizard now starts up the WDS Server service if not previously started
	- The wizard can now be accessed from the mounted image manager
	- The wizard now warns when a boot image is used
	- The wizard no longer launches on client Windows installations, or Windows Server installations without the WDS role
- The ADDS domain join wizard has seen a couple of improvements:
	- The wizard will no longer let you continue when you specify a domain account that does not exist
	- You can now test domain name resolution by invoking `nslookup`
- The following starter scripts are affected by this version:

| Starter Script | Stage | State |
|:--|:--|:--:|
| **Set File Explorer Launch Folder** | When users log on for the first time | **New** |
| **Disable Windows Admin Center/Azure Arc banner** (*Windows Server EXCLUSIVE*) | During System Configuration | **New** |
| **Disable Shutdown Event Tracker** (*Windows Server EXCLUSIVE*) | During System Configuration | **New** |

- The Starter Script Editor has received dark mode support
- When applying answer files you can now choose whether to copy them to the target image's Sysprep folder
- You can now enlarge the preview area for starter script code
- The Theme Designer has received dark mode support
- The DynaLog log viewer has seen some improvements:
	- Logs are now loaded much faster
	- Dark mode is now supported
- From the project view you can now perform commit operations to FFU files using a workaround
- You can now get installed driver information from Windows 7 images
- Projects and installation management modes now load and unload much faster
- Removing provisioned AppX packages from the online installation management mode is much more reliable now
- You can now access WIM and FFU variants of the image capture and application tasks much more easily
- After extracting images from ISO files, the program will now select the most suitable installation image from it
- You can now view information specific to FFU files when viewing mounted image properties
- The following libraries and components have been updated:

| Component | Version in latest preview | New version |
|:--:|:--:|:--:|
| [Markdig](https://github.com/xoofx/Markdig) | `1.1.1` | `1.1.2` |
| [Managed DISM API](https://github.com/jeffkl/ManagedDism) | `4.0.7` | `5.0.0` |
## What's fixed?

- Fixed an issue where GraphoView would not display information about a selected Windows image if the WDS group it belongs to only has 1 image
- Fixed an issue where capture compression type options were not being used when performing FFU captures
- Fixed an issue where the program would throw an exception when performing multiple driver exports by class name

## What's removed?

- The WDS image preparation script has been removed in favor of the WDS Helper

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2641) and **reporting feedback to us**.

<p align="center">
  <img src="https://i.imgur.com/KlPekhA.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://github.com/CodingWonders/DISMTools/assets/101426328/778b8900-c92b-4c53-88ed-fe42a3becaa1" />
</p>

We're also working on the next preview release of DISMTools, so expect more enhancements and goodies in around 2 weeks (April 26). The second update to DISMTools 0.7.3 is also expected to be released around that day.