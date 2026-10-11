--- 
date: 2026-10-11 
categories: 
  - General 
  - Scripts 
--- 
 
 
# Removing JScript support for answer files 
 
A relic from the past of WSH is now gone. Am I worried about it? **Not at its slightest.**
 
<!-- more --> 

Before we discuss the removal of JScript support, we have to talk about Microsoft's *scripting* capability history, which basically goes back to the 80s with MS-DOS.

**MS-DOS** was one of their first products. I'm not counting their actual first product, a BASIC interpreter, as that is more for making *programs*, not scripts (you could think differently about this, but let's not get bogged down with that). MS-DOS itself also has an interesting story, with origins on QDOS, but that's another topic.

MS-DOS introduced **batch** scripts. Basically, this would allow anyone to perform a *batch* of commands automatically, cutting down time to perform an action significantly, just like with any scripting technology. One of the most common batch scripts at the time was `AUTOEXEC.BAT`, which would launch at the beginning of the command interpreter, `COMMAND.COM`. Other script extensions associated to batch scripts were eventually added, such as `.CMD`. Batch scripts are still being used **and written** to this day, and has proven to be one of the easiest ways to perform tasks automatically.

In the late 90s, Microsoft introduced the Windows Scripting Host as a way to make scripting even more powerful not just at a computer level, but online too, accompanied by ActiveX. This resulted in the introduction of 2 scripting languages: VBScript and JScript (not to be confused with *JavaScript*), with VBS and JS extensions. Even though they were very popular back then (*and even more popular to write malware*), its use has diminished over the years. Nonetheless, more people wrote VBScript code than JScript code.

The problems with VBScript and JScript, however, were their barrier for entry.

- Batch had the upside of being easy to work with, but felt lacking in other areas. Microsoft significantly improved CMD's internal commands with Windows 2000, but it still feels lacking in some areas to this day
- VBScript/JScript had the upside of being more powerful, and more integrated (as Microsoft added WSH capabilities to their products); but felt quite cumbersome

In the 2000s, Jeffrey Snover proposed *Monad* as a way to bridge the gap between simplicity and power. This eventually became the **PowerShell** we know today. PowerShell has the advantage of leveraging the .NET framework, which allows script makers to do crazy things with it (for example, adding C# types that call Windows APIs via P/Invoke or creating windows with WinForms and WPF), and outputting most of its results in object form, which allows for easier data retrieval and manipulation.

Based on this, we have 4 good scripting languages with which you can make scripts for unattended answer files:

- Batch
- PowerShell
- VBScript
- JScript

## So, why is JScript support being dropped?

*UnattendGen*, the component responsible for making answer files from DISMTools, uses [Christoph Schneegans' answer generator library](https://github.com/cschneegans/unattend-generator). It has removed JScript support for no (apparent) reason. This dictates all of the answer file components, so they were updated to reflect this change.

You could probably see why JScript support was removed. I think it was dropped because of lack of popularity. As such, UnattendGen, the unattended answer file creation wizard, and the Starter Script Editor have been updated to drop JScript support and you will begin to see this change with DISMTools **0.8.2 Preview 4**.

## So, what do I do if I have and/or rely on JScript files?

Well, at this point, I recommend that you spend some time rewriting your existing JScript files in PowerShell.
