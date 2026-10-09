---
date: 2026-03-28
categories:
  - release
---
# DISMTools 0.8 Preview 2 - Now available

The second preview of DISMTools 0.8 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2632)

## What's new?

- If a non-sysprepped volume is selected in the image capture script, it will now warn you
- A new task has been added to copy installation images to a Windows Deployment Services (WDS) server
- Organizational units and users in OUs are now sorted alphabetically in the ADDS domain join wizard
- The ADDS domain join wizard will now let you continue if you had selected an account that does not require a password (contains *PASSWD_NOTREQD* in its `userAccountControl` attribute)
- A task has been added to copy a pre-configured answer file to an image so that it boots to Audit mode automatically
- Image capture tasks will now warn you when source installations have not been prepared with Sysprep
- A new task has been added to optimize Windows images
- Support for Full Flash Utility (FFU) has been introduced. Variations of the image application, capture, split, and optimization have been introduced with FFU support
## What's fixed?

- Fixed a minor UI issue where the NT logon path of a domain user would not be shown when launching the ADDS domain join wizard for the first time
- Fixed some HiDPI issues
- Fixed an issue where, when managing the active installation, the version's revision number would sometimes not coincide with the actual revision number
- Fixed an issue where information about a Windows image would be cleared after adding or removing packages
- Fixed an issue where the program would throw an exception if it couldn't create the logs directory (#344)

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_pre_2632) and **reporting feedback to us**.

<p align="center">
  <img src="https://i.imgur.com/KlPekhA.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://github.com/CodingWonders/DISMTools/assets/101426328/778b8900-c92b-4c53-88ed-fe42a3becaa1" />
</p>

We're also working on the next preview release of DISMTools, so expect more enhancements and goodies in around 2 weeks (April 12)