---
title: "Darth Jar Jar: a Model for Infosec Innovation"
date: 2019-05-05T08:30:09-04:00
draft: false
toc: false
featured_image: "/blog/img/darth-jar-jar.jpg"
image: "/blog/img/darth-jar-jar.jpg"
thumbnail: "/blog/img/darth-jar-jar.jpg"
tags:
  - InfoSec
---


![Image of Darth Jar Jar](/blog/img/darth-jar-jar.jpg)

Despite its seeming absurdity and superficiality, the theory of Darth Jar Jar can serve as a poignant parable for security innovation. For those unfamiliar, the notion of a Darth Jar Jar springs from a [meticulously researched fan theory](https://www.reddit.com/r/StarWars/comments/3qvj6w/theory_jar_jar_binks_was_a_trained_force_user/) from the Star Wars subreddit. While I do not wish to spoil the breathtaking beauty of the fleshed-out theory, the underlying legend is one of an ostensibly bumbling fool who, in reality, is an insidious puppet master full of cunning and strength.

What lessons from Darth Jar Jar can we glean and apply to information security? I argue there are a few innovative strategies one can postulate on both the offense and defense sides, which I will explore within this post.

***
## Darth Jar Jar for Offense
For an attacker to fully become one with Darth Jar Jar, they must be content playing a fool. Just as Darth Jar Jar appeared to be clumsy to lead to his underestimation, attackers should likewise appear to be sloppy to lead to their underestimation by defenders. By conducting purposefully noisy and messy operations in one part of a system, attackers can direct defenders’ attention away from the attack that is truly transpiring right under their cocksure noses.

There already exist public examples of attackers embracing the spirit of Darth Jar Jar. One of my favorites is the misdirection employed by [attackers back in 2013](https://krebsonsecurity.com/2013/02/ddos-attack-on-bank-hid-900000-cyberheist/), in which they conducted a DDoS to cover their tracks when exfiltrating funds out of corporate accounts. A further three banks were hit by [the same approach later that year](https://www.cnet.com/news/cybercrooks-use-ddos-attacks-to-mask-theft-of-banks-millions/) – a low-powered DDoS attack that captured defenders’ attention, while fraudulent money transfers happened concurrently.

Additionally, the Nigerian prince scam is arguably a long-term ploy very much in the vein of Darth Jar Jar. Scammers specifically use poor spelling and grammatical errors to weed out victims who would be less trusting. Those who are not deterred by lacking language are more likely to believe in the tale the scammer is spinning – and thus more willingly depart with their money. The clumsiness is intentional to lure precisely the right victims into the attacker’s maw.

I collected and brainstormed a few additional offense strategies for attackers who seek to replicate the brilliance of Darth Jar Jar:

### Meesa so noisy!
One option is to flood EDR systems with noise so that alert fatigue sets in on the part of the defender, letting subtler attacks slip through. The goal is to create noise for events that will receive a higher priority flag within the tool, such as purposefully clumsy kernel exploits – no team with a hundred critical-priority alerts (often called "P0s," for priority-zero) would clear them in time to catch your sneakier attack. 

Even cleverer would be to throw sloppy attacks over a period of time, while inserting the exact same quieter traffic that you plan to leverage in your real attack, so that the machine learning systems begin baselining it in. After all, Darth Jar Jar maintained his foolish façade for more than just one day!

### EICAR-CAR Binks
A common strategy in security detection is the notion of “alert on the first bad thing, then stop processing” so that there is not a flood of alerts. Thusly, an attacker could send EICAR in the same data stream or file as a real attack so that defenders see the EICAR alert and dismiss it. Then, the darker, sneakier underlying attack will go unnoticed – just as Darth Jar Jar used rambling babbling during the entirety of *The Phantom Menace* to obscure his devious speech that directly led to the dissolution of democracy.

### Ex-squeeze the data outta the network
During the rescue of Queen Amidala, Darth Jar Jar proved to be a master of diverting the attention of his enemies to take them by surprise. In the realm of critical infrastructure, an attacker could send a large volume of fake location update requests from SIMs, which would certainly attract the attention of defenders at any telecom provider. 

While defenders remain distracted and scrambling, the attacker could then infiltrate the internal telecom network by plugging into [an eNodeB](https://en.wikipedia.org/wiki/ENodeB) and moving horizontally to compromise elements such as [the MME](https://en.wikipedia.org/wiki/System_Architecture_Evolution#MME_(Mobility_Management_Entity)) or even [the HSS](https://medium.com/@AlepoTech/home-subscriber-server-hss-82470d3f332) (think: the master user database). Darth Jar Jar would absolutely approve of deflecting defender attention to outside of their own network to conceal the true threat from within.

***
## Darth Jar Jar for Defense
Just as attackers must play the fool to follow the wisdom of Darth Jar Jar, so must defenders. Luckily, many defenders are accidentally foolish, making purposeful foolishness all the more likely to lead attackers to underestimate defenders. While I usually strongly advise against #yolosec strategies, pretending to deploy a #yolosec strategy can perfectly replicate the sinister subterfuge of Darth Jar Jar.

There are fewer public examples in the realm of defense that highlight the gloriousness of a Darth Jar Jar approach. The closest might be the use of honeypots or canarytokens, such as a webserver that appears to be configured in a thoroughly #yolosec manner, creating irresistible temptation for attackers to explore them – and thus alert defenders to the fact that someone is very intrigued by their data.

In ths vein, there are a few Darth Jar Jar-esque defense strategies I collected and brainstormed:

### Oh, no! Yousa connection is slow
Once you detect attackers within your network, begin throttling their connections to satellite-link speeds at random. The goal is to make it seem like an unstable system to test how the attacker reacts and alters their strategy – just as Darth Jar Jar “clumsily” handled a booma during the Battle of Grassy Plains to take down an armored assault tank.

### Where wesa executing?
Darth Jar Jar never revealed to his Jedi companions that they were succumbing to his duplicity. Likewise, defenders can avoid revealing that they have not only caught attackers, but are bamboozling them. 

For instance, when defenders catch an attacker attempting to pwn a production instance, they can migrate that instance out of production, setting up all the same network connectivity so no change is perceived by the attacker. Then, defenders can begin logging and monitoring everything for later learning (and to inform broader investigation) while spinning up a replacement instance in production to avoid downtime.

### Mmm, dissen loverly data
Just as Darth Jar Jar tricked the Jedi into travelling through the core of a planet to make himself indispensable, defenders can trick attackers into going down a heavily monitored path to make it inevitable that they will be caught. For example, defenders can sprinkle cleartext AWS credentials in places that lead to alert traps. Or, defenders can “accidentally” reveal credentials attackers would need to access a seemingly sensitive system – when in reality, there is no valuable data residing in the system, just deep monitoring present.

***
Ultimately, no matter which side of the infosec game on which you fight, I hope that you will adopt the following mantra to let the dark side flow through you, elevating your #basic strategy to one of subtle manipulation and insidious deception – “What would Darth Jar Jar do?”

![Gif of Darth Jar Jar peeking through Vader's helmet](/blog/img/darth-jar-jar.gif)