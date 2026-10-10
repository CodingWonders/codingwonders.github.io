---
date: 2026-05-23
categories:
  - release
---
# DISMTools 0.8 Preview 6 - Now available

The sixth preview of DISMTools 0.8 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2652)

## What's new?

- The WDS Helper Client now detects the assigned volume letter for the image share more reliably
- ISO file creation results are now displayed in a notification
- You can now configure the keyboard layout in the Preinstallation Environment graphically
- A keyboard layout override policy has been added
- You can now save Preinstallation Environment policies for future sessions
- When configuring a custom wallpaper for the Preinstallation Environment, it will pull backgrounds imposed by group policy, if defined
- The Sysprep Preparation Tool has been updated to allow you to remove AppX packages that can cause Sysprep to fail
- Batch scripts with NT extensions are no longer supported
- The following starter scripts are affected by this version:

| Starter Script                            | Stage                       |  State  |
| :---------------------------------------- | :-------------------------- | :-----: |
| **Configure PowerShell execution policy** | During System Configuration | **New** |
| **Configure Power Plan Values**           | During System Configuration | **New** |

- Questions asked by the image information saver are no longer asked in the background
- FFU file commit operations are now carried out when saving changes to mounted FFU files after performing image tasks such as adding packages or enabling features
- An option has been added to prevent the machine from sleeping while performing image operations
- The home panel has seen a visual overhaul
- The following libraries and components have been updated:

|                  Component                  | Previous version | New version |
| :-----------------------------------------: | :--------------: | :---------: |
| [Markdig](https://github.com/xoofx/Markdig) |     `1.1.3`      |   `1.2.0`   |

## What's fixed?

- Fixed an issue where the program would throw an exception when saving Windows PE configuration of an offline Windows PE installation

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2652) and **reporting feedback to us**.

<p align="center">
  <img src="https://codingwonders.github.io/pictures/dt_relnotes/report_feedback.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://codingwonders.github.io/pictures/dt_relnotes/contrib_to_helpsys.png" />
</p>

We're also working on the next preview release of DISMTools, so expect more enhancements and goodies in around 2 weeks (June 7).