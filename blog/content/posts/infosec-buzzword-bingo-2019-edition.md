---
title: "InfoSec Startup Buzzword Bingo: 2019 Edition"
date: 2019-02-27T16:57:23-04:00
draft: false
toc: false
images:
featured_image: "/blog/img/infosec-startup-bingo-2019.png"
thumbnail: "/blog/img/infosec-startup-bingo-2019.png"
tags:
  - InfoSec
  - Market Analysis
---

This is the [third](https://twitter.com/swagitda_/status/912494974779973632) [edition](https://twitter.com/swagitda_/status/967566556262694912) of my Infosec Buzzword Bingo, just in time for 2019’s RSA Conference (RSAC). Rather than relying on my keenly tuned snake oil spidey senses to generate the words populating the bingo card, I took a more data-driven approach this year.

I surveyed 100 companies’ websites<a name="back-1"></a>[[1]](#cite-1), the vast majority of which are exhibiting at RSAC and possess VC funding. I did not include any of the large security vendors<a name="back-2"></a>[[2]](#cite-2), who probably could populate their own bingo cards across their mastodonian websites.

The idea is to take this with you to RSAC or any other vendor halls at information security conferences this year to see how many times you can win bingo at a single vendor booth! For more fun, [try out my Cyber Tagline Generator script](https://github.com/swagitda/infosec-buzzword-bingo/blob/master/cyber-taglines.py) to create your own maniacally terrible buzzword salad ([then @ it to me on Twitter](https://twitter.com/swagitda_/)).

Without further introduction, here’s the bingo card in all its glory — read on if you want more analysis on the stats:
![Infosec Startup Buzzword Bingo card for 2019](/blog/img/infosec-startup-bingo-2019.png)

The top word by far this year was ***automated*** and its variants — nearly three quarters of all companies used it on their sites in one way or another (e.g. ***automatically***, ***automation***, ***automates***, etc.). There were a few repeats from prior bingo cards, perhaps proving my natural acuity for sensing the buzziest buzzwords. The [following table](https://github.com/swagitda/infosec-buzzword-bingo/blob/master/buzzword-bingo.md) of the top 25 buzzwords (the ones on the bingo card) includes the number of companies who cited the buzzword, along with whether the buzzword was on prior bingo cards:
<script src="https://gist.github.com/swagitda/7a55615c8b7889b92a3edaae7e8462e2.js"></script>


## Which buzzwords are on the rise?
Let’s start with the words on the bingo card itself. You can’t just enable security people anymore, you must ***empower*** them. Seemingly a reaction to CISOs through SecOps analysts complaining about the complexity of security tools, ***simple***, ***simplifies***, and ***simplified*** are being used to (proactively ;) assuage concerns.

Allegedly, security professionals now want to ***discover*** things, and I suppose with most data lakes being more akin to data swamps, the predilection for adventure that ***discovery*** implies is required. And, taking a page from the DevOps world, ***orchestration*** is peppered around enough now to create a veritable symphony of infosec startups ***orchestrating*** away.

Not quite making it to the bingo card, but still heating up, is ***collaborate*** and ***collaboration***. Who knew that infosec teams wanted to work together? And if your security product isn’t ***optimized***, what are you even doing? Note that you do not have to say for what your product is ***optimizing***, just that it is, in fact, ***optimized***.

Finally, solutions for ***runtime*** security are growing, which basically is just saying it doesn’t break the computer as it is computing. The fact that this assurance must be stated at all says more about the infosec vendor situation than perhaps [even a long thought piece](https://techcrunch.com/2019/02/13/the-infosec-reckoning-has-arrived/) can.


## Which buzzwords are starting to fall?
***Hunting*** / ***hunt***, most frequently used with “threat” before it, just barely missed making the Infosec Buzzword Bingo card again this year. I anticipate that it’ll fall even further by next year as the category morphs into SIEM 2.0. While ***behavioral*** is still holding strong, ***anomalies*** is beginning to wane — it’s much sexier to say you have ***behavior-based machine learning*** or ***AI*** instead.

As far as threats, they are notably less ***sophisticated***, and less found on the ***dark*** web or in ***IoT*** devices. You def don’t want to talk about your product as a ***single-pane-of-glass*** anymore (try ***intuitive*** instead, which is on the rise). And, ***cloud-based*** is becoming less relevant as most security solutions move to a SaaSy model. If anything, companies should now specify when they *aren’t* cloud-based.


## Which buzzwords are the weirdest?
Most of the weirdo-words are only used in a handful of companies’ marketing spiels, thankfully. But, a full seven companies used ***real-world***, which, I mean — as far as I know, we aren’t trying to secure hypothetical worlds? I’m being purposefully obtuse (in the Dostoevskyan-fool spirit), since I do understand that too many solutions catch bad stuff only in theory without rigorously testing against what attackers will actually do (or without even really considering this during the product’s conception). But, its usage still makes me sad.

Another odd buzzword was ***holistic***, also cited by seven companies, which is perhaps the most credible buzzword due to its close association with essential “healing” oils. However, the one I hate the most by far is ***quantum-resistant***. For my sanity’s sake, I am grateful only one company chose to use that term.

***

<a name="cite-1"></a>[[1]](#back-1) I scoped it to the websites’ landing and product/platform pages (e.g. no blog content).

<a name="cite-2"></a>[[2]](#back-2) When I say “large” security vendors, think those who are publicly traded, are more than ten years old, or who have entire product “suites.”