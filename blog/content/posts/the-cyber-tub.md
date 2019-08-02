---
title: "The Cyber Tub: Communicating the Dynamics of Information Security Risk Management"
date: 2018-12-20T22:02:49-04:00
draft: false
toc: false
images: 
featured_image: "/blog/img/cyber-tub.png"
thumbnail: "/blog/img/cyber-tub.png"
tags:
  - InfoSec
  - Risk Management
---
![A tub covered in Matrix code](/blog/img/cyber-tub.png)*This is probably how a Cyber Tub looks, right?*

People struggle to understand how risk accumulates in complex systems, thereby also not understanding the extent to which risk must be reduced. This misapprehension can lead to “wait and see” decisions that cause a problem to snowball, or mitigations that don’t meaningfully reduce risk, creating the feeling of just barely treading water in your security program.

It is challenging for people to understand risk dynamics conceptually for two primary reasons. First, we are bad at tying inflows and outflows to the current level of risk in a system, as we tend to believe outputs are positively correlated with inputs. For example, from the climate change realm, 63% of MIT graduate students erroneously believed that if you stabilize emissions above the rate they’re being removed, atmospheric CO2 would stabilize.<a name="back-1"></a>[[1]](#cite-1) If emissions are still higher than reductions, there still will be net pollution — it will just be added at a more stable rate.

Second, we tend to ignore the accumulation of effects from inflows.<a name="back-2"></a>[[2]](#cite-2) For example, you may reduce the amount you overspend in a given year, but that doesn’t mean your personal debt is being reduced — you must earn a surplus over a period of time to pay down the debt you already accumulated. Ignoring accumulation leads us to underestimate the magnitude of mitigations required to stabilize risk — let alone make a dent in decreasing the risk level towards our goal.

What can we do about this lack of intuitive comprehension? A useful analogy to help people conceptually is a bathtub, with its straightforward inflows and outflows. When discussing information security risk, this analogy can help policy makers grasp the true implications of the decisions they’re making. Too often, mitigations are believed to “solve” the problem, while in reality, the inflows contributing to the problem are still outpacing the benefits from mitigations — but no further action is taken, resulting in continued accumulation of risk.

Thus, I’ve conceived the “Cyber Tub” as a way to better communicate information security risk and ensuring its dynamics — from accumulation to reduction — are well understood. Let’s delve into the analogy.

***

### The Spout
Let’s say you have a bathtub already full of water. The bathtub is actually a “Cyber Tub,” and the water already in it represents your risk level — it could include things like your legacy systems or even the risk of credential theft in modern systems. The spout is actively running, adding a steady, hot stream of complexity into the tub. You don’t want the tub to overflow, because in real life, that leads to a state where you want to tear your hair out from all the complexity you must manage, and probably something will go wrong. So what do you do?

### The Drain
First, you need to install a drain — the patch management drain, in fact — if you don’t have one already, which is going to be challenging given all the water already in the tub. If you do have a drain, it’s likely clogged with lots of gross hair from people using the tub, so you’re going to have to clean it out manually so it can drain — and you’ll have to do that each time manually when it gets clogged again.

But, of course, you’re very clever, so you decide to install a self-cleaning drain — an automated patch management solution. However, you already know it will take a lot of effort to implement, and it probably won’t work perfectly the first time (and probably not every time in the future, either). So, you perform some calculations to see which helps keep the tub from overflowing more effectively given how many manual uncloggers you have vs. how many auto-drain maintainers you have on your team.

### The Bucket
Regrettably, your drain solution only keeps the tub from filling up more rather than helping the water level go down. Clearly you need a bucket to remove a bunch of water all at once. But where do you get the bucket? Which type of bucket is right? How do you dunk in the bucket without splashing a bunch of water out? Where do you put the water in the bucket after? Do you need multiple buckets? There are lots of things to think about when transitioning to the bucket life.

Think of this like transitioning to a cloud or containerized world — the transition costs will be non-trivial and involve a lot of thinking over how to carefully lift the water without losing any.<a name="back-3"></a>[[3]](#cite-3) You can also only transition a certain amount of code at a time, so there needs to be a rollout plan as well. After all, even if you can buy a bunch of buckets at one time, it’s unlikely you can dump them all in at once to clear out the tub without something going wrong.

As you can see, there’s a lot of calculation here, including whether the bucket-based transition to cloud / containers can clear out the tub, since we already know the patch management drain will cancel out the complexity faucet, but nothing more. You also can’t forget that managing a bunch of little buckets is different from managing one tub, so you’ll need to consider the potential risks from that, too.

### Additional Examples

To solidify exactly what I mean through this analogy, let’s consider other examples from information security and how they can be viewed through the Cyber Tub lens:

1. A design review by the security team helps steady the water level as you release a new feature or product. By addressing security issues at the design phase, you tackle problems before they go into production and come out of the spout (you can use a threat model to prioritize). You could also require sign-off by the security team before release. Therefore, when a new feature or product is released, it won’t add as much water to the Cyber Tub.
2. Pentesting only tells you a very rough measure of your water level is — do limited findings mean your app is secure, or instead that your testing team is inadequate? Even if you remedy issues from the results of the pentest, it may only be counteracting the spout slightly more — you can think of a pentest like a leaky bucket that may or may not help. Adopting a continuous testing model instead can act as a healthy drain and hedge against ongoing risk that point-in-time assessments cannot catch.
3. If you are concerned about credential theft risk, think of it as the water in the bathtub. The drain could represent requirements for complex passwords —perhaps enough to counteract the additional risk of each new credential added. The bucket could be enforcing the use of SSO and a password manager, which will actually lower the level of the risk engendered by the existing pool of credentials.<a name="back-4"></a>[[4]](#cite-4)

***

## Conclusion
For any problem in the information security risk space, try to think of it in terms of this “Cyber Tub.” Consider these four key questions:

1. What are the inflows that add to the problem?
2. What can you do to reduce water coming in from the spout?
3. How can you keep the drain open and draining quickly?
4. What mitigations will actually make a dent in the problem? What are the best buckets available?<a name="back-5"></a>[[5]](#cite-5)

While the Cyber Tub may seem like an overly simplistic analogy, that is part of its beauty — nearly anyone can understand it, as long as they’re familiar with the basics of how a bathtub works. We can’t expect to present facts and figures to non-experts and have them perfectly grasp the dynamic processes around information security risk. Let’s give everyone a helping hand and start presenting information security risk in a way people can actually understand it — a way that leads to smarter decision making.

***

## References
<a name="cite-1"></a>[[1]](#back-1) Sterman, J. D., & Sweeney, L. B. (2007). [Understanding public complacency about climate change: Adults’ mental models of climate change violate conservation of matter.](http://web.mit.edu/jsterman/www/StermanSweeneyClimaticChangeFinal.pdf) *Climatic Change, 80*(3–4), 213–238. doi:10.1007/s10584–006–9107–5

<a name="cite-2"></a>[[2]](#back-2) Sterman, J. D. (2012). [Sustaining Sustainability: Creating a Systems Science in a Fragmented Academy and Polarized World.](http://jsterman.scripts.mit.edu/docs/Sterman%20Sustaining%20Sustainability%2010-2.pdf) *Sustainability Science*, 21–58. doi:10.1007/978–1–4614–3188–6_2

<a name="cite-3"></a>[[3]](#back-3) It’s surprisingly difficult to find a succinct explanation for how modern infrastructure can help with information security, outside of vendor drivel. For now, please check out [the fulltext of my keynote on resilience in infosec](/blog/posts/red-pill-of-resilience-infosec/), specifically the “adaptability” and “transformability” sections. You can also view [these resources by Leviathan](https://www.leviathansecurity.com/cloudsecurity), although they are a bit out of date (2015).

<a name="cite-4"></a>[[4]](#back-4) Thank you to [Julian Cohen](https://medium.com/@HockeyInJune/product-security-14127b5838ba) for this example.

<a name="cite-5"></a>[[5]](#back-5) You also have to consider the difficulty implementing these mitigations in the context of the stagnant bathwater — the problem — potentially obscuring your path to implementation (a topic for another time).

I also suggest reading: Åström, K.J. and Murray, R.M. [Feedback Systems: An Introduction for Scientists and Engineers](http://www.cds.caltech.edu/~murray/books/AM08/pdf/am07-complete_17Jul07.pdf).

*Thank you to Julian Cohen, Camille Fournier, and Alex Rasmussen.*