---
date: 2026-06-20
categories:
  - release
---
# DISMTools 0.8 Preview 8 - Now available

The eighth and final preview of DISMTools 0.8 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2662)

## What's new?

- The Sysprep Preparation Tool has been updated to the latest version
- If the Sysprep Preparation Tool was invoked before capturing the image, temporary files and boot entries are now removed if the capture succeeds. The resulting Windows image will still not contain any of those items
- The version reporter watermark in the DISMTools Preinstallation Environment can now detect when the environment has booted via a network
- The PE Helper can now include your target system's essential drivers (storage controllers and network adapters) in the DISMTools Preinstallation Environment
- The ISO creation wizard will let you specify a save location if you clicked OK without having specified one
- Starter scripts have received a new icon
- The following starter scripts are affected by this version:

| Starter Script                                 | Stage                                |                 State                 |
| :--------------------------------------------- | :----------------------------------- | :-----------------------------------: |
| **Invoke Windows Utility Configuration**       | When the first user logs on          | **Updated** -- invoke command updated |
| **Restore classic context menu in Windows 11** | When users log on for the first time |                **New**                |

- Several updates were made to the home screen experience:
	- News feed items now appear in "cards". News feed content is now shown in a built-in preview
	- The time the feeds were updated now appears on the top-right
	- Random Microsoft and Windows facts now appear on the bottom-left
	- Information about the current system volume is reported more accurately
- The following libraries and components have been updated:

| Component | Previous version | New version |
|:--:|:--:|:--:|
| [Markdig](https://github.com/xoofx/Markdig) | `1.2.0` | `1.3.1` |

## What's fixed?

- Fixed an issue where the full date string was not displaying correctly when accessing image properties with Windows representations of dates turned off
- When adding a boot image to the WDS server, the service start is now requested only when it is not running
- Fixed an exception that would happen when adding certain AppX packages (#365, #366)

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2662) and **reporting feedback to us**.

<p align="center">
  <img src="https://i.imgur.com/KlPekhA.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://github.com/CodingWonders/DISMTools/assets/101426328/778b8900-c92b-4c53-88ed-fe42a3becaa1" />
</p>

As this release is close to being published as a stable version, changes in the Preview branch will be merged into the Stable branch, in around a week.

## What's next?

Once version 0.8 is released as a stable version, work will begin on version 0.8.1. Expect the first preview release to arrive in early July 2026.

The final set of changes and fixes are being worked on right now as you read. Check out the `dt_prerel_2663_relcndid` branch for more information. Keep in mind, however, that this branch will be deleted when version 0.8 releases.