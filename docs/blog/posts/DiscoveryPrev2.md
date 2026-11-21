---
date: 2026-11-21
categories:
  - release
  - Discovery
---
# DISMTools 0.9 Preview 2 - Now available

The second preview of DISMTools 0.9 is now available, with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.9_pre_26112)

## What's new?

### Preinstallation Environment Helper

- DISM progress is now rendered with a custom progress bar in the WDS Helper Client:

<p align="center">
  <img src="https://github.com/user-attachments/assets/8976780a-575b-4a55-849c-eb55c7bdbf5c" />
</p>

- The PE Helper can now perform a full format of the main system partition of a disk, configurable via policies:

<p align="center">
  <img src="https://github.com/user-attachments/assets/d003b486-52a9-47b6-a87f-829d1b4d4dd1" />
</p>

### Unattended answer file features

- Active Directory features now support multiple domains in a forest. You can now select which domain the target devices connect to:

<p align="center">
  <img src="https://github.com/user-attachments/assets/f4c6e9ae-66dc-42bd-a73a-0794a38c4bdd" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/5c0f0cf4-6b45-4612-bd9d-a507e179c8a3" />
</p>

- The ADDS wizard now adds the IP address of the domain controller to the DNS server addresses of the answer file if not defined with a NIC setting

### Image Tasks

- Driver Packs can now be created thanks to the new Driver Pack Creator. These can be used in the driver addition wizard. Refer to [this blog post](https://codingwonders.github.io/blog/2026/10/19/whats-next-for-discovery-driver-packs/) to learn more:

<p align="center">
  <img src="https://github.com/user-attachments/assets/faeac0c4-b214-49ca-872e-6d483f7c9dbe" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/74062500-364d-4d5c-956f-b1a7648ba6da" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/dd5a743e-4b24-4c33-b326-77e73b703e0b" />
</p>

- Image information reports can now be exported to Excel spreadsheets:

<p align="center">
  <img src="https://github.com/user-attachments/assets/5b0196ae-0f03-4538-a9b2-6c05382c78a5" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a8e5458e-4790-4d1d-a569-d9bb0399ad44" />
</p>

### Miscellaneous

- 7-Zip has been updated to version 26.06
- Reliability and performance has been improved

## What's fixed?

- Fixed an issue with installer colors in light mode
- Fixed an issue where the PE Helper operating system installer would fail to load if no WIM files were added to the ISO file
- Fixed an issue with ICACLS commands invoked by the PE Helper on domain controllers

## How do I begin?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.9_pre_26112) and **reporting feedback to us**.

<p align="center">
  <img src="https://codingwonders.github.io/pictures/dt_relnotes/report_feedback.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://codingwonders.github.io/pictures/dt_relnotes/contrib_to_helpsys.png" />
</p>

We're also working on the next preview release of DISMTools, so expect more enhancements and goodies in around 2 weeks (November 22).