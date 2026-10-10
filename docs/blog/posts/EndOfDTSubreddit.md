---
date: 2026-10-10
categories:
  - General
---


# Revamping the news source

You may have heard the news about Reddit shutting down its RSS service in mid-November 2026. If not, here I am to tell you that. According to the platform, RSS is a "common surface for large-scale scraping and automated abuse", which is *obviously true* (pick the sarcasm). This affects DISMTools in a large way. In this post I'll explain more about this shutdown.

<!-- more -->

## So what is going on?

As stated before, the end of the RSS service affects DISMTools. The home screen is comprised of 2 areas: the project list, and a Start page (similar to how Visual Studio works). In the latter view, one half is comprised of news designed to inform you about the latest in DISMTools. 

<p align="center">
    <img src="https://codingwonders.github.io/pictures/dIDNvDY6b7.png">
</p>

This entirely relies on the RSS service (which you *could* trigger on any subreddit by appending `.rss`). For example:

- `https://reddit.com/r/DISMTools.rss`
- `https://reddit.com/r/Windows.rss`

I say *could* because you may be reading this after the shutdown of the RSS service, planned to happen on November 13. After the shutdown, **all DISMTools versions up to 0.8.2 Preview 3 will not be able to pull news from the RSS source**, meaning everything down to version 0.4. They were also affected by Reddit's rate limits.

This is a worrying topic that needed to be solved quickly. And, it has been solved.

## The new news source for all news CodingWonders Software

I am thrilled to announce the new [CodingWonders Software website](https://codingwonders.github.io), the new source for everything I make. This is powered by GitHub Pages.

I decided to use GitHub Pages as it was the easiest to integrate my existing repositories with, and works with the static site generator I use, MkDocs. Plus, it gives me a free SSL certificate. I know GitHub is an unstable platform that has been in various outages in 2026, so you can consider this a bet. We'll see how it goes in the long run. Who knows what might happen in the future...

Anyway. On to the website. It uses the same style of the DISMTools Help Documentation, as I have enjoyed Material for MkDocs and its built-in blog capabilities. All posts since March 28 have been posted here, and this site will be where new blog entries will be posted.

<p align="center">
    <img src="https://codingwonders.github.io/pictures/firefox_SpS86q5stl.png">
</p>
<p align="center">
    <img src="https://codingwonders.github.io/pictures/firefox_7hHzTt1vH6.png">
</p>

MkDocs also offers RSS capabilities (via plugins), meaning that I am now in control of the RSS service (to an extent; we'll evaluate the reliability of GitHub). Integrating this new RSS service into DISMTools has been a very simple task, and the service issue has been resolved in 0.8.2 Preview 4 (in the works as of writing this) and any future versions of DISMTools.

## It will no longer be just DISMTools

The new website allows me to blog about more than just DISMTools; it also allows me to talk about what I find most fascinating: *technology*. So, expect me to talk about my other projects too. I plan on bringing [utterances](https://utteranc.es) support in the future so we can talk more about posts in the comments.

The cool thing about all of this is that the website is open-source and anyone can contribute to it. So, go ahead and enjoy the new site!