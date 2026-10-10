---
date: 2026-07-04
categories:
  - General
---


# Upload your Starter Scripts to the Library!

DISMTools 0.8.1 Preview 1 introduces a new way of sharing starter scripts with the world with the *Starter Script Library*. Because sharing knowledge (and stories about why printers aren't working) unites IT admins, sharing starter scripts can help you, as well as everyone, get what you want out of your Windows image.

<!-- more -->

### Count with my Starter Script!

To share your starter script with the community, you need a few things:

- Version 0.8.1 of the Starter Script Editor, available in DISMTools 0.8.1 Preview 1 and later,
- A GitHub account (*[create one](https://github.com/signup) if you don't have it*), and
- A GitHub API key

The API key is needed in order for the Starter Script Editor to automate as many things as possible when uploading your script to the Library. Anyway, let's begin.

With your Starter Script ready, click "Upload Script" on the toolbar. A window will appear telling you more about the process and what you need to do:

<p align="center">
    <img src="https://codingwonders.github.io/pictures/StarterScriptEditor_0k78e5LXks.png">
</p>

<p align="center">
    <img src="https://codingwonders.github.io/pictures/StarterScriptEditor_GiuoTYRokG.png">
</p>

You will need to provide a GitHub API key. Any type of API key can work, whether it's a classic or a fine-grained token. You can create API keys regardless of your GitHub account's age. Click *How do I get an API key?* for a detailed, step-by-step guide on how to do this. Additional notes are provided later in this post, so **KEEP READING**.

Before uploading your starter script, it is a good idea to check if it contains information that can be used to identify people or network resources, as well as service tokens. To perform an automated inspection of your code, click *Inspect my code*. The code will be inspected using 100 rules covering most security violation patterns (API keys, hard-coded credentials...). If results show up, you will see an inspection results screen that you can pin to one of the corners of your primary monitor.

Even with automated inspection, it's advised to review script code manually for any security violations that might slip through.

Finally, accept the acknowledgements and click *Upload to the Library*. Wait a couple of moments, and you should see a pull request URL, as well as the pull request itself. Your script will be reviewed and, if valid, will be merged into the Library.

### Viewing my creation

Use the unattended answer file creation wizard in DISMTools to view starter scripts from the Library.

When browsing starter scripts, expand the script type drop-down menu and select *Scripts uploaded to the Library*:

<p align="center">
    <img src="https://codingwonders.github.io/pictures/DISMTools_KMDKTpmyc4.png">
</p>

Then, select your script and click OK.

### Notes regarding API keys

You don't need to create an API key every time you launch the Starter Script. Simply make a note of the API key that you had reserved for the Starter Script Editor and use it in subsequent runs until the API key expires.

When your API key expires, you will need to create a new one to be able to upload more scripts to the Library.