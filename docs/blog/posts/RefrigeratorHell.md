---
date: 2026-11-08 
categories: 
  - General
  - Cybersecurity
---


# My views on the refrigerator situation 

Lately I've seen the news on television about refrigerators across supermarkets in Europe being hacked, effectively spoiling food inside. Some news outlets attribute this to hybrid warfare without getting into the nitty-gritty of the situation. In this post, I would like to talk about what I think about this situation and how we can learn from this sort of thing.

<!-- more -->

The first time I heard about refrigerators being hacked was from [a Louis Rossmann video](https://www.youtube.com/watch?v=yR8H9hnRJkY), and this formed the basis of what I will explain in the post. I could not believe it at first, but after news outlets started covering the story, I realized that this was serious.

The problem is not really a potential hybrid warfare attack, but rather a major flaw in how modern technology works.

## We should blame Internet of Things

The title of this section may seem clickbaity, so I will explain. IoT started to become mainstream in the early 2010s with a great value proposition. From anywhere in your home, you could now control the temperature of your air conditioner, turn on the lights in your house, and even program your vacuum cleaner to clean your house while you are away.

The problem is that manufacturers mostly focus on convenience. Here is a quote you must not forget in your life:

> Security is a journey, not a destination.

Way back before IoT became mainstream, security was already a concern. Before IoT, the only devices that could connect to the internet were computers, tablets, and smartphones. On computers alone, we began to see that we were not safe online from cyberattacks (*not that we are fully safe today either*). With IoT devices, you now have common electrical appliances, such as your washing machine, connecting to the internet, therefore adding more attack vectors. I have seen many instances of stuff exposed to the internet being hacked, and networks that would have become botnets had they not had a firewall.

Back to the refrigerator situation. The provider of most of these refrigerators is [Danfoss](https://www.danfoss.com/en/), a Danish company that makes refrigeration and air conditioning systems. Most of the refrigerators in the affected supermarkets were old refrigerators for which Danfoss no longer provided support.

One of the selling features of these refrigerators was that they allowed remote management. This was a huge convenience for supermarket owners, as this kept them from going to the refrigerators themselves to do things like, for example, controlling the temperature. The problem, however, was how it was set up.

The refrigerators exposed a web server to the *public* internet, and most supermarket chains kept using the default credentials, which people easily found out were `admin` and [the current date as the password](https://cyberplace.social/@GossiTheDog/117429502412235079). Let's remember that Danfoss stopped supporting the affected models of refrigerators.

So, not only were supermarket chains using "unsupported" refrigerators, but they were also exposing themselves by using the management interfaces of those refrigerators. The perfect recipe for disaster. And it happened on France, Germany, the UK, and other countries in Europe. It also happened to three blood banks in France.

A security-conscious person, or someone who doesn't understand the craze of IoT, would have probably asked *why the refrigerator became unsupported by its manufacturer*, or *why the refrigerator is exposing a web server to the public internet*. Surely, the manufacturer could have instructed supermarket chains to properly set up the refrigerators on the network, right?

It appears not, as this vulnerability was also discovered in other countries, **including Spain**. Yikes.

With this, we have seen one of the many problems of this Internet of Things world. Apart from the fact that manufacturers can render devices non-functional by turning off the servers they connect to, among other things.

## Future prevention is only happening now

Only now are regulatory authorities starting to instruct supermarket chains to properly secure their devices. Their instructions are to either disconnect the refrigerators from the internet, or to leave them isolated in a VPN. In my opinion, this is a good move, but it came in too late.

This should have been done many, *many* years ago, from when the refrigerators were first deployed. For major supermarkets, that could have been done in a jiffy by hiring IT technicians. For smaller markets, this could have been done by contacting a friend or a local IT company. Or, companies could have done the more sensible thing and not connected these things to the Internet.

*Anyways. Rant over. Hold on to your food if you bought it from a chain that was affected by this. I will see you soon.*