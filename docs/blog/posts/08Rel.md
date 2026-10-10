---
date: 2026-06-27
categories:
  - release
---
# DISMTools 0.8 - Now available

![](/pictures/DT08_Release.png)

DISMTools 0.8 is now available as a stable release, and comes with new features and enhancements.

<!-- more -->

[Download this release](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_stable)

### What's new?

- The Sysprep Preparation Tool has seen support for `CopyProfile` and can now remove AppX packages from the reference system
- Guards have been added to prevent running the PE Helper on a PXE environment, and to warn when running the PXE Helpers on a non-PXE environment
- The autorun menu now has options to browse disc contents and copy the boot image to a WDS server
- The DISMTools Preinstallation Environment can now be configured via policies
- You can now view images and groups in a WDS server graphically
- When launching the Driver Installation Module, the Preinstallation Environment can now tell you the hardware IDs of unknown devices
- HotInstall can now export SCSI adapters to install them in the DTPE image
- If a non-sysprepped volume is selected in the image capture script, it will now warn you. *Ignore the warning if you are capturing a volume containing a just-deployed Windows installation
- A new task has been added to copy installation images to a Windows Deployment Services (WDS) server
- From the Autorun application you can now specify the WDS image group to upload the image to
- The Autorun application and HotInstall have seen HiDPI improvements
- Partition table overrides can now be used when deploying images with the WDS Helper
- PXE Helper Servers can now be started using a different port by holding down SHIFT and performing an action in the following places:
	- From the Autorun application
	- From the Tools > Start PXE Helper Server for... menu in the main program
- The architecture for the WDS boot image is now picked graphically
- The default set of DISMTools Preinstallation Environment backgrounds has been overhauled
- The WDS Helper Client now detects the assigned volume letter for the image share more reliably
- ISO file creation results are now displayed in a notification
- You can now configure the keyboard layout in the Preinstallation Environment graphically
- If the Sysprep Preparation Tool was invoked before capturing the image, temporary files and boot entries are now removed if the capture succeeds. The resulting Windows image will still not contain any of those items
- The version reporter watermark in the DISMTools Preinstallation Environment can now detect when the environment has booted via a network
- The PE Helper can now include your target system's essential drivers (storage controllers and network adapters) in the DISMTools Preinstallation Environment
- The ISO creation wizard will let you specify a save location if you clicked OK without having specified one
- You can now specify scripts written in VBScript and JScript
- The following starter scripts are affected by this version:

| Starter Script                                                                 | Stage                                   |    State    | Changes (if modified)  |
| :----------------------------------------------------------------------------- | :-------------------------------------- | :---------: | :--------------------- |
| **Enable Batch script file locks**                                             | During System Configuration             |   **New**   |                        |
| **Remove MAX_PATH length limit**                                               | During System Configuration             |   **New**   |                        |
| **Show and Hide System Desktop icons**                                         | When the first user logs on             |   **New**   |                        |
| **Set File Explorer Launch Folder**                                            | When users log on for the first time    |   **New**   |                        |
| **Disable Windows Admin Center/Azure Arc banner** (*Windows Server EXCLUSIVE*) | During System Configuration             |   **New**   |                        |
| **Disable Shutdown Event Tracker** (*Windows Server EXCLUSIVE*)                | During System Configuration             |   **New**   |                        |
| **Refresh Windows Explorer**                                                   | When the first user logs on<sup>1</sup> |   **New**   |                        |
| **Configure Start Menu Appearance**                                            | When the first user logs on             |   **New**   |                        |
| **Disable warnings for unsigned RDP files**                                    | During System Configuration             |   **New**   |                        |
| **Configure PowerShell execution policy**                                      | During System Configuration             |   **New**   |                        |
| **Configure Power Plan Values**                                                | During System Configuration             |   **New**   |                        |
| **Invoke Windows Utility Configuration**                                       | When the first user logs on             | **Updated** | Invoke command updated |
| **Restore classic context menu in Windows 11**                                 | When users log on for the first time    |   **New**   |                        |

<sup>1</sup> Use this script as many times as you want in any stage to allow changes to be noticeable without having to restart Windows Explorer. This is not a substitute of the "Restart Windows Explorer" option, however, and you should continue using it if the script does not make your changes noticeable

- The Starter Script Editor has seen several improvements:
  - The Starter Script Editor has received dark mode support
  - The Starter Script Editor now detects read-only starter scripts and removes such attribute when saving them
  - Spacing in script code can now be normalized
- Organizational units and users in OUs are now sorted alphabetically in the ADDS domain join wizard
- The ADDS domain join wizard will now let you continue if you had selected an account that does not require a password (contains *PASSWD_NOTREQD* in its `userAccountControl` attribute)
- A task has been added to copy a pre-configured answer file to an image so that it boots to Audit mode automatically
- The ADDS domain join wizard has seen a couple of improvements:
	- The wizard will no longer let you continue when you specify a domain account that does not exist
	- You can now test domain name resolution by invoking `nslookup`
	- You can now pick account objects from anywhere in your domain
	- You can now choose a domain suffix from available DNS zones
- When applying answer files you can now choose whether to copy them to the target image's Sysprep folder
- You can now enlarge the preview area for starter script code
- You can now configure account *display names* independently from account names
- Post-installation scripts can now be reordered
- Batch scripts with NT extensions are no longer supported
- Service information can now be saved to a report, whether you manage a Windows image or an installation
- Services can now be removed
- The image information saver is now run asynchronously
- When information about a package file can't be obtained, DISMTools will now continue processing the rest of the queue
- Filter assistants have been added to the feature, capability, and driver information dialogs to allow you to build queries more easily
- A new automatic image reload service is now included, to let you have all your images reloaded on system startup
- You can now export drivers by class name
- Image capture tasks will now warn you when source installations have not been prepared with Sysprep
- A new task has been added to optimize Windows images
- Support for Full Flash Utility (FFU) has been introduced. Variations of the image application, capture, split, and optimization have been introduced with FFU support
- From the project view you can now perform commit operations to FFU files using a workaround
- You can now get installed driver information from Windows 7 images
- Projects and installation management modes now load and unload much faster
- Removing provisioned AppX packages from the online installation management mode is much more reliable now
- You can now access WIM and FFU variants of the image capture and application tasks much more easily
- After extracting images from ISO files, the program will now let you select the most suitable installation image from it
- You can now view information specific to FFU files when viewing mounted image properties
- When downloading packages from App Installer files you can now copy the URLs to the main application package
- When exporting drivers by class name or when filtering installed drivers by class name, you can now choose from third-party classes provided by third-party drivers in your Windows image or installation
- You can now export drivers from Windows 7 images and installations
- Saving service changes is much faster now
- Questions asked by the image information saver are no longer asked in the background
- FFU file commit operations are now carried out when saving changes to mounted FFU files after performing image tasks such as adding packages or enabling features
- An option has been added to prevent the machine from sleeping while performing image operations
- Help documentation has seen a major visual refresh
- File associations are now set for the Starter Script Editor
- The home panel has seen a visual overhaul
- 7-Zip has been updated to version 26.01
- **CODE:** setting load and save functionality has been revamped
- The Starter Script Editor and the theme designer can now be invoked from the Tools menu
- In portable installations, file associations can now be toggled for the Starter Script Editor
- The DynaLog log viewer has received support for event log filters
- Date properties can now be displayed in a Windows-native format
- The following libraries and components have been updated:

| Component | Version in 0.7.3 | New version |
|:--:|:--:|:--:|
| [Markdig](https://github.com/xoofx/Markdig) | `0.45.0` | `1.3.1` |
| [Scintilla.NET](https://github.com/desjarlais/Scintilla.NET) | `6.1.1` | `6.1.2` |
| [Managed DISM API](https://github.com/jeffkl/ManagedDism) | `4.0.7` | `6.0.0` |
| [Windows API Code Pack](https://github.com/PWagner1/Windows-API-CodePack-NET) | `8.0.14` | `8.0.15.2` |

### What's fixed?

*This will show the bugfixes in all the preview releases.*

- Fixed an issue where removed features would appear in the wrong place
- Fixed a minor UI issue where the proper user principal name (UPN) would not be shown when selecting a user in the ADDS domain join wizard
- Fixed a minor UI issue where the NT logon path of a domain user would not be shown when launching the ADDS domain join wizard for the first time
- Fixed some HiDPI issues
- Fixed an issue where, when managing the active installation, the version's revision number would sometimes not coincide with the actual revision number
- Fixed an issue where information about a Windows image would be cleared after adding or removing packages
- Fixed an issue where the program would throw an exception if it couldn't create the logs directory (#344)
- Fixed an issue where GraphoView would not display information about a selected Windows image if the WDS group it belongs to only has 1 image
- Fixed an issue where capture compression type options were not being used when performing FFU captures
- Fixed an issue where the program would throw an exception when performing multiple driver exports by class name
- Fixed an exception (#350)
- Registry hives that were unloaded externally no longer cause errors when unloading them from the image registry control panel
- Non-PowerShell-based endpoints no longer throw CORS issues when calling WDS Helper Server APIs
- Fixed an issue where App Installer download errors would not appear in the foreground
- Fixed an issue where tutorial videos would not be playable
- The WDS Helper client message for downloading unattended answer files no longer shows at all times
- Fixed an issue where the program would throw an exception when saving Windows PE configuration of an offline Windows PE installation
- Fixed an issue where the full date string was not displaying correctly when accessing image properties with Windows representations of dates turned off
- When adding a boot image to the WDS server, the service start is now requested only when it is not running
- Fixed an exception that would happen when adding certain AppX packages (#365, #366)

### What's removed?

- The WDS preparation script has been removed in favor of the WDS Helper

### What changed since last preview release?

- Fixed accuracy issues when performing Windows UEFI CA 2023 readiness checks on systems that were deployed using updated boot loaders
- Fixed an issue where background processes would fail with "The parameter is incorrect" in some cases (#362)
- UnattendGen has been updated to the latest version, now requiring .NET 10
- The news feed previewer has seen several improvements
- The Preinstallation Environment Helper now detects answer files created by Rufus, and lets you act on answer file conflicts

### How do I get started?

As always, you can begin contributing to the project by [**downloading this version today**](https://github.com/CodingWonders/DISMTools/releases/tag/v0.8_stable) and **reporting feedback to us**.

<p align="center">
  <img src="https://codingwonders.github.io/pictures/dt_relnotes/report_feedback.png">
</p>

Feedback is very crucial for the success of this project.

If you want to help us with something else (like documentation or artwork), we also welcome your suggestions. The help documentation content pages are available on [GitHub](https://github.com/CodingWonders/dt_help) and we encourage you to **contribute to them** so that we can make DISMTools easier to use.

<p align="center">
    <img src="https://codingwonders.github.io/pictures/dt_relnotes/contrib_to_helpsys.png" />
</p>

### Looking into the future

We're already working on the next version of DISMTools, **0.8.1**. If you want to take a closer look at this release, be sure to check out the latest preview releases, starting around July 5.

Again, this version is expected to be released in about 2 months.