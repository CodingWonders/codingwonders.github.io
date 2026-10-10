---
date: 2026-06-21
categories:
  - General
---


# The Recycle Bin issue

This post is not what you would see from this subreddit, but I thought about making it more of a Windows-related subreddit. You will still see DISMTools release notes once new versions come out.

<!-- more -->

After installing the June 2026 cumulative update for Windows 11, you will see this lovely file name when trying to permanently delete a file in the Recycle Bin:

![](https://codingwonders.github.io/pictures/Delete File_b1.png)

An uninitiated user may probably think that the file is corrupted in some way. Microsoft has declared this a known issue and they state that this shows the internal name in the recycle bin. However, they don't go into much detail. That's why I decided to discuss this rather hilarious issue.

### How the Recycle Bin has worked

I would like to talk about how the Recycle Bin has worked over the years, because it is important to understand this in order to understand the source of the issue.

The Recycle Bin was introduced in Windows 95. Ever since its introduction, it's always been a folder in the root of volumes. In the Windows 9x family of operating systems, this folder is called `Recycled`. But, you don't see this folder as Recycled. You see it as the Recycle Bin:

![](https://codingwonders.github.io/pictures/vmware_4qTF5CKS5U.png)

You have to show all files in the folder options dialog to view the folder itself. However, if you access this folder by double-clicking it, you will see the same results.

![](https://codingwonders.github.io/pictures/vmware_3pRrMQ81CJ.png)

This is because inside this folder there is a `desktop.ini` file that dictates how to render this folder. Normally, this is done with associations to a CLSID. We'll discuss that later. Now, how do we view the internal names? With a command prompt, of course

Load `command` and go to this folder. Then, list the contents. Et voilà !

![](https://codingwonders.github.io/pictures/vmware_R71tsuODTC.png)

Back in 9x versions of Windows, this was the typical file structure:

- `DCn.ext` were the files themselves
- `INFO` (Windows 95/NT 4.0), `INFO2` (Windows 98+/Windows 2000+) contained information about the deleted files, including their original locations and the date they were deleted. We'll look at INFO2

INFO2 is a binary file. If we load it in a hex editor, we can see that information:

![](https://codingwonders.github.io/pictures/vmware_0zBMdo60KG.png)

While we're at it, let's view our desktop.ini file:

![](https://codingwonders.github.io/pictures/vmware_fMgv8yirfC.png)

If we check this CLSID with the list of CLSIDs in `HKEY_CLASSES_ROOT\CLSID`, we can see that it indeed is the class ID for the recycle bin:

![](https://codingwonders.github.io/pictures/vmware_wYzUYe1ExB.png)

Windows NT inherited this system with version 4.0 (using `INFO` instead of `INFO2` and a root folder name of `RECYCLER`) but, with NT being a proper multi-user system, there is a recycle bin for each user. The recycle bin folders are distinguished by user Security Identifiers (SIDs). This separation can also be seen on more recent versions of Windows.

![](https://codingwonders.github.io/pictures/vmware_NAxla1P9Jr.png)

![](https://codingwonders.github.io/pictures/vmware_eDz7U3gxJK.png)

### Windows Vista and later

Windows Vista changed how the Recycle Bin works. The root folder is now called `$Recycle.Bin`. While user-based separation is still a thing, the files inside the recycle bin are now laid out differently.

Rather than having a single file with all the metadata, there are now metadata files for each file in the recycle bin. When you delete a file in the Recycle Bin, 2 files are stored:

- `$Innnnnn.ext`: the metadata file
- `$Rnnnnnn.ext`: the deleted file

`nnnnnn` is a random set of characters. Like in older versions of Windows, the metadata file contains the original file location and the deletion date.

![](https://codingwonders.github.io/pictures/CWindowssystem32cmd.exe 1_b1.png)

You may notice that folders also follow this structure. However, items inside these folders are not renamed.

Anyway, here's the metadata file for one of the files in the recycle bin:

![](https://codingwonders.github.io/pictures/notepad++_hAr7g6Ymf1.png)

So, what's happening is that Windows is not reading this metadata file when showing the confirmation, despite showing the file correctly in the recycle bin.

### What to do

Well, you have to wait until Microsoft fixes this. In the meantime, don't freak out. If someone you know stumbles upon this bug, tell them not to freak out.