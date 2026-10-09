---
date: 2026-05-03
categories:
  - General
---


# My thoughts on "Windows K2" and how the overall PC industry should change

Recent news articles talked about leaked internal Microsoft plans to "revitalize Windows" with an initiative called "Windows K2" and how they could save the platform. People were also talking about said initiative and how it would make Windows better in the future. But, unlike many people, I think Microsoft, and the entire PC industry, needs to do more than just that. Here is what I think should happen for us to see noticeable changes for the better.

<!-- more -->

## On Microsoft's side

In the past I talked about my thoughts on the future of Windows after 40 years of it being around. During these last months, however, a couple of things became more apparent: the lack of quality control and the lack of focus.

On the one hand, updates have gone from things that would improve the user experience and provide meaningful fixes to Russian roulette. That can be said not just for Windows, but for other kinds of software (*in that case it's more because of supply chain attacks; look at what happened to Notepad++ and CPU-Z/HWMonitor*). But, let's focus on Windows.

Windows Updates, in recent months, while they have fixed many security vulnerabilities, have also introduced bugs for which Microsoft released out-of-band updates that have also had bugs. One thing is experiencing a bug in an OS because of specific configurations. For example, if you have this specific set of hardware and this specific set of software, then something could be causing conflicts and that's why you're facing such an issue. However, another thing is **bugs being more generalized**. For instance, let's look at the October update for 25H2, which caused 2 known issues:

- It infamously "broke localhost" due to some underlying issues with HTTP/2; fixed with a KIR (Known Issue Rollback)
- It broke keyboard and mouse input in the Recovery Environment; fixed with an out-of-band update

Another update from January 2026 caused some built-in Windows applications to stop working due to some server-side Store app licensing issues. That same month they released an out-of-band update that caused some systems to stop booting. And, another one in April broke domain controllers for a third year in a row, if they had Privileged Access Management enabled. Those were all known issues that Microsoft fixed after *some* coverage.

That's the key word right there: known issues. We've gone from highly specific issues to issues that are more known and more likely to happen.

On the other hand is the lack of focus. In the past year we've seen Microsoft screw it up trying to cram in AI features to everything they work on. We've seen Office being renamed yet again to *Microsoft 365 Copilot*, and we've seen things such as a prominent Copilot button on the ribbon and, in the case of Excel, a `COPILOT` function. They've also turned Visual Studio **CODE** into an AI code editor after vibe-coding exploded in popularity and derivatives such as Cursor or Google's Antigravity were made. And, more basic tools have also had AI features, such as Notepad, which has also received tons of unnecessary features, in my opinion, for a standard text editor. It now supports Markdown and lets you insert tables, do I have to say more?

In that case, one thing is adding such functionality while the other thing is the **execution and end-result** of said functionality, and it's safe to say that, while Microsoft sees AI as a profitable business (*which yes, in some cases it's both that and useful*), pretty much everyone, including me, thinks otherwise. And, instead of focusing on the feedback users have been sending for months or even years, they focus on a thing that will not take off without backlash.

But, in 2026, there is hope that things will change for the better. Pavan Davuluri talked about the Windows team's commitment to quality, which features 3 core pillars: performance, reliability, and craft. Stuff, such as actually letting people move the taskbar or relying on more native technologies for core components, is either already implemented or in the works. So, it seems as though they are already doing the work to improve the system's public perception.

## On manufacturers' side

It's clear that the problems with the current perception of the operating system are not just Microsoft's, but the PC manufacturers' too. For this, let's talk in depth about the other key pillars: performance and reliability. First, let's talk about performance.

2026 started out as a year of radical change for the PC industry, mainly due to RAM and storage price increases. Not only does it affect individual components, but it also affects their final form in pre-built machines. In general, pre-built machines have increased in price. But, I think the most impactful change was seen in the budget market, where budget computers with decent specs increased in value, whilst those that stayed in their previous price tags started packing worse features, such as 8 GB of memory and 128-512 GB of storage.

The thing is that, even though I was able to daily both Windows 10 and 11 on a laptop with 4 GB of RAM, Windows is unbearable to use with just 8 GB. 16 GB is starting to fall behind too, with Microsoft recommending at least 32 GB now. In my case, I no longer run into low memory issues because I have 64 GB. But what about other computers? For this we need to study how **and** why Windows is unbearable to use with low amounts of memory.

Picture this: we have a brand-new, budget HP laptop with 8 GB of memory and 256 GB of storage. The current memory recommendation for Windows 11 is 4 GB. Thanks to bloat and services from Microsoft we can safely say we're already using 4 of our 8 GB. Then, add in all the bloat and services from the manufacturer that include, for example, a third-party crappy antivirus and/or 50 other programs; and could well be using, at least, 2 GB. So, now we're looking at a memory usage of 6 GB, leaving us with only 2 GB free.

Then we add our favorite programs to the mix, which include additional services and programs, and we've just used all our RAM, and barely have memory for what we *actually* want to do.

In that case, the thing that can save the machine is uninstalling as much crap as possible. That way we can reduce RAM usage by a lot, maybe 2-3 GB. But, there's still not enough leg room if we want to do stuff *just a bit* more intensive, such as having 5 browser tabs while having a document and a spreadsheet open.

But, what if the laptop ships with known unreliable components? That's another thing that can hurt the experience, and the reason why **Reliability** goes hand in hand with performance.

I think that PC manufacturers in general should look at a specific product as a reference on how to build stuff right: the *MacBook Neo*. Even though I always talk smack about Apple. Even though I always say, and will continue saying, that macOS is the crappiest operating system ever. I think they did an amazing job with the MacBook Neo in telling the PC industry how to design an experience. Cramming an entire desktop operating system into a $600 laptop **with a phone chip** is surely a monumental task. But, if you know Apple, you probably know how they pulled this off. And it's because they control everything and, despite how limiting *and* limited it is, you get an optimized experience.

Let's talk about optimization and how it affects the user experience. For Apple, it's incredibly easy to deliver optimized experiences. They make the hardware. They only let the OS run on Macs, more so now with Apple Silicon. They deliver native applications first and **mandate** that application developers make native applications (*unlike in Windows where anyone can use any technology and we have web applications as a result*). Knowing that, you know the result.

Now let's talk about Windows. By default, a clean installation will feature the most basic set of devices. A basic graphics device. A basic audio device. Basic input devices. Basic storage and USB stacks. But, let's say that that does not offer the most complete experience and, for this, you need to add drivers. Assuming you have a 4090, you will need to download drivers from either NVIDIA or the graphics card subvendor, such as MSI. Also, your computer offers Dolby audio enhancements, for which you need to add APOs (audio processing objects). And, to top it all off, your computer features a smart card reader, for which you need to add another driver.

Let's assess the situation. Unlike macOS, where everything is tightly controlled and you are just relying on Apple to deliver on the optimized experience, on Windows, you have to rely on Microsoft **and** each and every hardware manufacturer involved in your computer to deliver on said optimized experience. **Am I saying that Windows should become macOS? Hell no**. Windows has way more advantages than macOS and I will always recommend Microsoft's OS over Apple's despite all its flaws. All I'm saying is that you have to rely on more factors on the Windows side.

When I get asked about OS optimization during conversations with friends, I always set the record straight. The more basic your hardware *and software* components are, the better, reliable, and more optimized your experience is. That's why my old laptop has seen no recurring crashes, and how my ThinkPad (my current laptop) hasn't either.

I also talk about software components because it's not just hardware and drivers that can deliver a poor experience. A badly-made piece of companion software can also mess up your day.

That's why I demand for more quality control when making any kind of hardware or software. One that involves more rigorous testing than just unit tests or an AI agent looking at the code and saying, *LGTM!*

## How the industry as a whole should change

I think that, in order to see a noticeable change, we have to merge all the work Microsoft seems to be doing with Windows K2 with changes I want to see in the PC industry.

First, stop making cheap, plastic crap and selling that with a high price tag. It's disgusting. Also, stop delivering under-powered products for cheap if you are going to shove all your bloatware on them. Don't make the RAM and storage situation worse than it is now with your software, so either don't ship your crap with it or don't ship the system or lineup.

Second, for stuff that is a bit more expensive, start delivering more reliable components. Not only deliver on defect-proof hardware, but also defect-proof software and drivers. For this statement I also include Microsoft, because I want them to start understanding the current situation with their operating system and delivering fixes. Come on, guys. I want to stop seeing generalized bugs for once.

Last, don't get in the way of the user. For this, both the industry and Microsoft are involved. If the user says no to an AI or some other unnecessary feature, respect their choice. Don't wake up to a user telling them to "finish setting up their computer" just because they declined the use of Microsoft 365, Xbox Game Pass, OneDrive, or some other technology. Apart from a software developer and a system administrator, I'm also a user, so this also annoys me.

Hopefully we can see stuff change if everyone follows these guidelines.