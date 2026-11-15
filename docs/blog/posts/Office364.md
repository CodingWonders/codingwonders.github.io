--- 
date: 2026-11-15 
categories: 
  - General 
  - Cloud 
  - Sovereignty 
--- 
 
 
# What the Microsoft 365 outage teaches us 
 
![](/pictures/msoutage.jpg)
 
<!-- more --> 
 
On November 12 and across November 13, we saw how Microsoft 365 services didn't work as they were down globally. Now that we have recovered from this situation, I would like to share what we can learn from this outage.

## We depend on (unreliable) cloud infrastructures too much

This outage reminds me of how AWS went down just under a year ago, and how it affected many companies that depended on AWS. In that case, it was all down to a problem in DNS configuration. Later that year we had an Azure outage. And now we have what we had with this outage.

The thing in common with all of these outages is that they affected *cloud services*, such as Exchange Online or Intune. The problem, however, is not that we rely on cloud services, as they have been with us for a couple of decades without many significant issues. Instead, the problem is that cloud providers are no longer showing utmost care in service availability, and are letting these issues slide.

Case in point, look at us developers and the [many](https://www.githubstatus.com/incidents/0rn90wk115q9), [many](https://www.githubstatus.com/incidents/djlmxz2zd0j7), [**many**](https://www.githubstatus.com/incidents/zkxwbgr0cnmx) times GitHub let us down this year.

When developing an online service, a key metric is the **uptime**. The magical figure to target is "five nines", which means that the service is available 99.999% of the time, which, for you or the company you work at, results in clients being confident using your service. You can afford performing **scheduled maintenance** (maybe you want to update your servers or your software), but you can't have it go down for no known reason.

99.999% uptime is not even that hard to reach. Sure, you have to be *extra* sure that your service is not going to burn in flames, and that the dependencies and base systems you rely on are not going to fail; but, tell the cloud providers that. Historically, that has been the case, but now it seems that they are not as careful as they used to be. And this is a problem.

**Why is this happening, I hear you ask?** Well, I think it's because of 2 reasons:

1. **A series of bad decisions done in the past, which back then worked perfectly, but are now showing their age.** Maybe an engineer decided to take the short route to solve a problem and left an edge case unhandled. Maybe [a lava lamp exploded](https://blog.cloudflare.com/randomness-101-lavarand-in-production/). Who knows...
2. **Layoffs and AI.** Nowadays, Big Tech companies are laying off human engineers and replacing them with AI. While I am not against AI (as I have described many times in this blog), I think how companies are leveraging AI tools is not how it should be done. And, as such, you may have an agent tinkering *too* much on a network configuration or a setting in some component. And, you have screwed up the service in production

Now, these thoughts are **mine** and may not be entirely true. You may have guessed it: I want you to think. And no, I'm not talking about **outages related to security incidents;** that is another topic.

## Either they or we get involved

The future can be looked at in two ways, depending on what comes first (*I think you probably already know the answer*):

- **Companies commit to improving service dependability:** aside from all "commitment" statements that companies add to their incident reports, actual change is done to tone down AI usage, and to test what a change does more thoroughly
- **We begin embracing self-hosted solutions:** rather than relying on services, which are hosted by companies and you don't have control over, you rely on services you host yourself. While it is a hassle to set up these services at first, the work pays off once you finish, and you have something you can access through your local network and, with a VPN, you can access it from anywhere. For instance, I've had a self-hosted Immich instance on which I have my full photo backup for almost a year, and I've been very happy with it

## Go self-hosted where you can

Self-hosting is worth it when a service is critical and the cost of downtime is high. You regain control over updates, backups, and access, reducing dependence on third-party outages while keeping important tools available locally or through a VPN. It is not always simpler, but it is often more resilient and private.

So, what are you waiting for? Look at a service you may be using now and look for an alternative you can host, or build one if you want to.

On my end, I took advantage of this outage to install Microsoft Office on my system, for a feature you will see soon. Stay tuned!