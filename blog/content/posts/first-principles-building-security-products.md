---
title: "First Principles of Building Security Products"
date: 2017-06-12T16:32:41-04:00
draft: false
toc: false
images:
featured_image: "/blog/img/by-wlodek-428549_1920.jpg"
thumbnail: "/blog/img/by-wlodek-428549_1920.jpg"
tags:
  - InfoSec
---

*Using Shamir’s 10 Commandments of Commercial Security to build better security products*

A printout of Adi Shamir’s [10 Commandments of Commercial Security](http://www.ieee-security.org/Cipher/ConfReports/conf-rep-Crypto95.html) has been my #1 office essential since I first stumbled upon them, and I argue it should be yours, too. Shamir outlined these commandments in his talk at the Crypto ‘95 conference (yes, way back in 1995), and they not only spell out the first principles of enterprise security, but serve as a poignant reminder that although it feels as if the industry is evolving around us at a feverish pace, the fundamentals of building security products are true even two decades later.

Despite these tenets being evergreen, I rarely see them referenced — hence, I want to re-post and draw attention to them, and discuss why they’re still pertinent even today. While it’s absolutely beneficial reading for blue teams, the examination after the list is specifically about their importance from the perspective of people building commercial information security products.

***
## 10 Commandments of Commercial Security
Directly quoted from [Adi Shamir, Crypto ‘95](http://www.ieee-security.org/Cipher/ConfReports/conf-rep-Crypto95.html)

> **1\. Don’t aim for perfect security**
> So, be realistic, and do the best you can within your limits. Roughly, you should double security expenditure to halve risk.

> **2\. Don’t solve the wrong problem**
> For example, note that US banks lose 10 billion dollars a year in check fraud but only 5 million in online fraud. [naturally, these are 1995 figures and no longer accurate]

> **3\. Don’t sell security bottom-up**
> (in terms of the personnel hierarchy).

> **4\. Don’t use cryptographic overkill**
> Even bad crypto is usually the strong part of the system.

> **5\. Don’t make it complicated**
> This yields more places to attack the system, and it encourages users to find ways to bypass security.

> **6\. Don’t make it expensive**

> **7\. Don’t use a single line of defense**
> Have several layers so security can be maintained without expensive replacement of the primary line.

> **8\. Don’t forget the “mystery attack”**
> Be able to regenerate security even when you have no idea what’s going wrong. For example, smart cards are attackable but are great for quick cheap recovery.

> **9\. Don’t trust systems**

> **10\. Don’t trust people**	

***
## How can these commandments help us build better security products?

Let’s review these commandments from the product perspective one by one.

**1. Don’t aim for perfect security**

No matter what sort of security product you’re building, you must be realistic that you will never block, detect, monitor, “thwart,” mitigate, or remediate all attacks. While for blue teams the rule of thumb is you should double your security budget to halve risk, for product teams, it should be that you should double your R&D budget to halve your customer’s risk. Don’t invest too much time or money on addressing niche threats just because doing so sounds sexy — and don’t just consider what would meaningfully decrease your customer’s risk today, but also 1–2 years from today. Nor should you prioritize trendy attacks that will be passé to attackers next year.

**2. Don’t solve the wrong problem**

I believe this is the primary failing of most security product teams. The problem is never about stopping X attack. Let’s explore this with the “5 Whys” method (in which you may not need all 5 whys). Why does the customer need to stop X attack? X attack can cause a data breach, which blue teams want to prevent. Why? Data breaches lead to regulatory fines, reputational impact, etc. that blue teams want to prevent. Why? Damage to the organization makes the blue team look incompetent, which blue teams don’t want. Why? Blue teams looking incompetent can lead to them losing their jobs. 

Ultimately, if your product is not helping blue teams look competent — meeting compliance, demonstrating mastery of your organization’s security posture to executives, being able to demonstrate why a breach was not the result of negligence — then you aren’t solving the right problem. This is why dashboards, reporting, visualizations, scoring, compliance modules, and all the other “boring” things matter.

**3. Don’t sell security bottom-up**

This is why buyer vs. user personas matter. This is also why including the aforementioned “boring” things like dashboards, reporting, and other high-level elements matter. You must be able to demonstrate value to CISOs, SOC directors, AppSec managers, and any other relevant team leads. This doesn’t mean your UX should be geared towards the buyer — your PoC/PoV will fall flat if so. It means you should consider the value to the buyer, and how you can articulate and demonstrate that in your product. Design UX for drill-downs, but market with dashboards.

**4. Don’t use cryptographic overkill**

The classic advice is “don’t roll your own crypto,” but what this really means is don’t rely on crypto to check the box for deeming your product “secure.” While Shamir may not have envisioned a future so dismal that [AV products don’t even deliver updates over SSL](https://www.av-test.org/en/news/news-single-view/32-products-put-to-the-test-how-good-is-antivirus-software-at-protecting-itself/), the point stands that with shameful frequency, security product vendors don’t rigorously audit their own product’s security.

**5. Don’t make it complicated**

One of my paramount frustrations with the infosec industry is the earnest shock and sneering contempt infosec professionals seem to have regarding the fact that users often bypass security protections. While a good handful of the booths at RSA this year finally demonstrated apt attention towards UX, too often UX is ignored in security product design — and specifically, UX to end users. 

Yes, infosec is hard, but design is hard as well, and security product builders should respect it far more. Mediocre security that users love — or even simply tolerate in their workflows — will always be superior to fine security that users will spend vast amounts of effort looking to circumvent. And guess which will win in the market, too? 

The other point here is that introducing complexity — more features, more parsers, more attempts at “all in one” security — degrades the security of the systems the product is meant to protect. Complexity means more limited ability for vendors to verify security, and even now, big vendors often get away with providing assurances of security standards without actually meeting them.

**6. Don’t make it expensive**

Security vendors violate this all the time, catering to only the largest of enterprises, while the medium enterprise market remains one of the juiciest yet most neglected. For example, Okta, who had an incredibly successful IPO and is adored by the public market, explicitly developed their product in a mid-size enterprise-friendly manner, but one from which large enterprises could still benefit. Their pricing is transparent with a menu of potential products, but as a reference, their bread and butter SSO offering would run an organization of 1,000 employees about $24,000 per year. 

Compare this to a solution like the original FireEye box priced at $250,000 per year. In fact, FireEye has somewhat turned their previously lagging fortunes around in large part by releasing FireEye Helix, a far simpler — and far less expensive — platform available in an as-a-service subscription model. Selling to the large banks or generating massive services fees may allow for some initial success, but will set security products up for failure in the broader market.

**7. Don’t use a single line of defense**

For product builders, this commandment means you should assume that your product will not serve as your customer’s single line of defense. Do not try to make your product the solution to all problems. This doesn’t mean you can’t offer multiple products under one “platform,” because, frankly, most of the time what people mean by platform is just that all the vendor’s products have API rails to talk to each other, and that there may be a central console from which you can click buttons to access each of the products. 

This does mean that each product should aim to tackle one particular challenge, and tackle it well. To quote the illustrious Ron Swanson, [“don’t half-ass two things, whole ass one thing.”](https://www.youtube.com/watch?v=zl-HalherjQ)

**8. Don’t forget the “mystery attack”**

Consider how your product helps your customers deal with unknown unknowns. This can take many forms, such as presenting valuable context or creating resilient environments. As a simple example, offering detection only with signatures creates a binary of “bad” and “not bad,” while looking for behaviors can allow for risk scores whose traits can be used to help narrow down attacker activity when a breach is discovered. Or, by exposing context around events to security analysts, you can present relevant information to assist in threat hunting and incident response, rather than only showing the direct cause of an alert. 

Further, with the rise of VMs and containers, it’s become easier to tear infrastructure up and down should compromise occur. For example, Slack rebuilt each component of their cloud infrastructure from scratch after a major breach in March 2015. Infosec vendors should consider leveraging these technologies and strategies in their own products and systems, too.

**9. Don't trust systems**

Design your product in a way that assumes the customer’s estate is compromised and that your product can be compromised. The former should absolutely be taken into consideration for any machine learning or baselining approach, but it also means that compromised customers can lead to attackers learning how your product works — and thus developing countermeasures. The latter assumption is related to #4 and #5, in that you should consider how to minimize impact to your customer should an attacker exploit your product. 

This naturally includes being careful about the third parties on which you rely, such as by auditing any proprietary or open source libraries you incorporate in your product — but also ensuring that your product minimizes privileges and permissions. This is, in part, why customers are wary of adopting host agents, as evidenced by the fact that Tavis Ormandy has found [many highly embarrassing bugs](https://www.wired.com/2016/06/symantecs-woes-expose-antivirus-software-security-gaps/) due to endpoint protection products running at a high level of privileges.

**10. Don't trust people**

Don’t assume end users will operate like *Homo securitas*, perfectly adhering to proper security hygiene and willing to bear some inconvenience by understanding that security is so important. For whatever reason, it doesn’t seem like the industry accepts yet that users will click things they shouldn’t, bypass things that get in the way of their work, and not understand things that you think are obvious. From the customer angle, although it’s more of a basic principle of UX, assume that your customers will also often use your product in a way that you didn’t intend — whether benign or malicious. 

Consider a particularly iniquitous example: if you’ve built a user monitoring product for finding insider threats, bear in mind that it could be used as a tool for [LOVEINT](https://en.m.wikipedia.org/wiki/LOVEINT) and harassment depending on how it’s designed, allowing someone to effectively spy on the activity of another employee. 

Or, DLP solutions that give granular visibility into documents going in and out of the organization’s estate could expose potentially revealing titles — like M&A-Agreement-With-Acquiror.pdf or Reputationally-Sensitive-Deal-Draft.docx— that could violate confidentiality agreements or cause other damage should an employee of either the customer or the vendor see — or worse, leak — this information.

***
## Conclusion
I hope I’ve adequately convinced you of these commandments’ relevancy today (and going forward), and that they can serve as a constructive framework for building security products. For product managers, challenge your roadmap against these commandments. For engineers, consider if your plan for how to architect product features and underlying systems adheres to these tenets. For marketers, leverage these principles in messaging value to the customer and demonstrating alignment with their priorities.

The reality of the infosec industry is that few products adhere to these commandments, which means this framework offers opportunities for differentiation. [Keep it simple, stupid](https://en.wikipedia.org/wiki/KISS_principle), and design your product to help customers return to these first principles, even if they don’t know yet that they need them — build the car, not faster horses.

***
Many thanks to [Leigh Honeywell](https://twitter.com/snare?lang=en) for reviewing.