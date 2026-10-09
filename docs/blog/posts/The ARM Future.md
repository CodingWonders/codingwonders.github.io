---
date: 2026-07-12
categories:
  - General
---



Recent announcements in the PC space have told us about the importance of ARM-based chips in devices that are not smartphones. In this post, I would like to talk about such news and where we're headed in the ARM world.

<!-- more -->

## The history of ARM's presence

I have thought that the ARM platform could start getting a foothold on desktop computers since the early 2020s. Now, ARM in computers and laptops has been a thing for much longer (ever since the 2010s), though it didn't attract as many people as it does nowadays.

While single-board computers such as the Raspberry Pi have embraced ARM-based chips in the 2010s, it wasn't until Apple released the M1 in 2020 that we started seeing a shift towards ARM by major computer companies.

The reason as to why they moved from Intel to their own silicon was the same as when they moved from PowerPC to Intel in 2006: performance per watt. In other words, getting more done with better efficiency. This resulted in their computers beating the competition, powered by x86. 6 years later, we saw the first version of their operating system that didn't support Intel platforms.

Enough Apple for today. What about Microsoft? They were already prepared with Windows on ARM, which began circa 2017 when they partnered with Qualcomm. They did have Windows RT, which debuted alongside Windows 8, but, unlike RT, Windows on ARM was exclusively a 64-bit system. With this project they addressed the major pitfall of Windows RT, its lack of application support, with translation layers, which are also used in projects such as Wine.

In 2019, Microsoft released the Surface Pro X: their first ARM-based device in 6 years. This device featured the Microsoft SQ1 chip, manufactured by Qualcomm. The SQ1 chip saw additional revisions leading to the SQ2 and SQ3. So, you could say Microsoft has also invested a lot in the success of ARM on Windows machines.

![Surface Pro X](https://cdn.mos.cms.futurecdn.net/3N7AheMH5ZhiQYzA82qsge.jpg)

*Source: Windows Central*

Fast forward to late 2022. On the Surface subreddit, I saw [a post asking people whether ARM had made progress](https://www.reddit.com/r/Surface/comments/yd9wlh/arm_vs_intel_do_you_think_arm_has_made_progress/) because the Surface Pro 9 shipped with both Intel and SQ3 options. Even though I don't own a Surface device (unless you count my brother's Surface Go 3), I still wanted to provide my opinions on the subject, stating that Windows on ARM would become more mainstream after, at least, 2-3 years.

Even though I didn't have a Surface, I still had an ARM-based device: a Raspberry Pi. Thanks to the Windows on R project, I could run full-blown Windows on it, and test the features of Windows on ARM. So, my prediction was going a bit on the right track. Eventually, however, it happened.

## Copilot+ PCs

As much as I hate some of their features, like Recall, I have to admit that, out of the 2 PC denominations Microsoft introduced in 2024 (AI PC and Copilot+ PC), the latter was announced around the time they had impressive improvements for Windows on ARM, the Prism compatibility layer being the big deal.

![Prism](https://cdn.mos.cms.futurecdn.net/Qeu88j9otoM8LZPdydfnCD.jpg)

*Source: Windows Central*

Previously, 64-bit applications that weren't native to the ARM platform were not fully optimized. Prism changed that by introducing several optimizations. Another change was that now there were 2 versions of ARM software targets: regular ARM64 and ARM64EC, which allowed developers to port existing x64 applications more easily.

Add to that the fact that the first waves of Copilot+ PCs were ARM-based and you'll see the increase in popularity.

Around the time that Copilot+ PCs were introduced, I received a reply to my comment from 2 years prior stating that I was right. My prediction was right. And it would be even more right the older it became.

Around a year later I reflected on my prediction and, for DISMTools, I wanted the experience to be better for ARM-based devices. Now, the main executable and libraries were already compatible with ARM64 (because of the Any CPU target for .NET applications), but I wanted to improve the experience with Windows PE tooling for ARM platforms.

Remember the Windows on R project? Well, it helped make the perfect test bed for ARM software: a Raspberry Pi 3B running Windows PE. This became what I call the O.A.T., or *Official ARM64 Tester*. To make the C++ components work in this new environment (the most important one being the Driver Installation Module), I had to adapt the projects to be compiled with Visual Studio 2022 and Microsoft Visual C++ 19.3. Then, I had to add the ARM64 target. Building it was effortless, and so was testing it. The Driver Installation Module just worked. DISMTools 0.6.2 introduced this ARM64 version, and, even to this day, with the move to Visual Studio 2026 and Visual C++ 19.5, it just works on ARM64.

When I had the ARM64 version working, I started thinking that ARM was the future. It appears as though that's the case, thanks to the green player. Here's an internal sheet I made specifically for this, back in 2025.

![](/pictures/Sheet_ARM64Compat.png)

*Back when the 0.6 series was still the latest and greatest.*

## NVIDIA enters the chat

Rumors about NVIDIA's N1X chip were surfacing since, at least, 2025. They answered in late May 2026, around Computex. Alongside MediaTek and Microsoft, they talked about the future of the PC.

At Computex, NVIDIA revealed the RTX Spark, with up to 128 GB of unified memory, up to 6144 CUDA cores in its GPU, and impressive AI capabilities (*not really interested in that*). While I'm not necessarily a fan of unifying a processor and memory, I was still impressed by their processor, from the events I saw (mainly Build 2026).

This year's Microsoft Build event featured 2 new Surface devices: the Surface Laptop Ultra and the Surface RTX Spark Dev Box. We'll see how they work out once they are available to the general public but, in my opinion, they are quite promising. The RTX Spark is an ARM-based chip, so it makes me think about what will happen in a couple of years.

## My prediction for ARM chips

With all the improvements we've seen for Windows on ARM, and the RTX Spark, what does the future entail?

Firstly, **NVIDIA will be a huge player in the ARM processor scene with their RTX Spark chips**. Not that they have already been a player with the Tegra chips ending in the Surface RT and Surface 2, but they will have a considerable market share when it comes to ARM-based devices.

Secondly, **Qualcomm will continue to be relevant in making chips for computers and laptops and will be a competitor to NVIDIA's offerings**. It's like the Intel vs AMD battle, only featuring NVIDIA and Qualcomm this time around.

Thirdly, **ARM devices will continue to become even more popular,** to the point of, potentially, surpassing Intel and AMD offerings in a couple of years. In other words, **the trend will continue**. Not just in the Windows side, but also on the Mac side with Apple Silicon and Linux improving support for Snapdragon X-series and, now, RTX Spark chips.

Finally, **Intel and AMD devices will continue to be competitive**, despite the increasing popularity of ARM. But, they will slowly fade away. I'm still passionate for what Intel and AMD offer though, so no hate towards them. But, I'm just pointing out the facts and trends.

## Image Sources

- [Surface Pro X](https://www.windowscentral.com/microsoft-surface-pro-x-vs-surface-go)
- [Prism](https://www.windowscentral.com/microsoft/windows-11/your-windows-11-on-arm-pc-can-now-run-even-more-x86-apps-and-games-thanks-to-microsofts-latest-prism-emulation-update)


*PS: this was entirely written on my new phone, featuring an ARM chip.*
