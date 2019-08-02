---
title: "WTFunding: Industrial / Manufacturing Analytics"
date: 2015-10-13T17:24:07-04:00
draft: false
toc: false
featured_image: "/blog/img/sparks.jpg"
thumbnail: "/blog/img/sparks.jpg"
tags:
  - WTFunding
---

![Image of Sparks](/blog/img/sparks.jpg)

*WTFunding is one of my “spare time” projects to delve into tech sectors attracting VC funding that pique my curiosity. I like connecting dots between disparate things, it’s also pretty useful.*

### Table of Contents:
1. [So what is "industrial / manufacturing analytics"?](#so-what-is)
2. [What are the applications?](#applications)
3. [What's hindering adoption?](#adoption)
4. [Who cares?](#who-cares)
5. [What are the risks?](#risks)
6. [What's the current scene?](#current-scene)
7. [Final thoughts](#conclusion)

***

## <a name="so-what-is"></a>So what is “industrial / manufacturing analytics”?
There doesn’t seem to be a great catch-all term for it yet, but there are a few different terms for and related to the sector I’m discussing: smart manufacturing, infrastructure analytics, manufacturing analytics, industrial analytics and, though it’s a broader term, IoT analytics.

My preference is towards “infrastructure analytics,” but when I use those terms interchangeably throughout, know I mean the same thing (and it’s also helpful to keep an eye out for that range of terms in your own reading). The one sub-sector I’ve seen broken out the most is predictive maintenance, but otherwise startups in this space use some selection of the terms above when self-describing.

Gartner’s definition says, “providers that help manufacturers support variable product content through the manufacturing process and improve the visibility and analysis of manufacturing performance.” Other research creates some beautiful imagery like, “removing the barrier between physical and information flows,” and, “translating the physical world into a model accessible by IT.” Or that, you know, this is all about “IoT orchestration” and “big-data-driven manufacturing.”

My [ELI5](https://www.urbandictionary.com/define.php?term=ELI5) definition, that makes me want to stab my eyes out less, is, “providers that help manufacturers manufacture better, and for less money, using data from machines.” They listen to all the stuff the manufacturers’ machines have to say, figure out what part of the stuff shows that things are going wrong or things could be done better, and show the manufacturers pretty pictures and clear advice on how to fix machines or make the machines do things better.

Industry people refer to this data as generated “on the edge,” which just means at the sensor or machine level. As I’ll talk about farther down, there are lots of machines that provide data for solutions to leverage. To visualize the different types of machines, here are some pictures along with what they are:

|![machine vision systems](/blog/img/industrial-01.png) | ![RFID/barcode scanners](/blog/img/industrial-02.png) | ![welding machines](/blog/img/industrial-03.png)|
|:-----------------------------------------------:|:-----------------------------------------------:|:-----------------------------------------------:|
|Machine vision systems     | RFID/barcode scanners     | Welding machines |

*

|![PLCs](/blog/img/industrial-04.jpeg) | ![Robots](/blog/img/industrial-05.jpeg) | ![Plasma cutters](/blog/img/industrial-06.jpg)|
|:------------------------------:|:------------------------------:|:------------------------------:|
|PLCs     | Robots     | Plasma cutters|


Oh, and don’t forget “factory-floor software” like MES (manufacturing execution system) and ERP (enterprise resource planning).

Let’s walk through an example manufacturing process to get a sense of what data is generated; for example, putting together the chassis (the car’s frame) on an automobile.


<img style="float: right; max-width:50%; padding: 5px" src="/blog/img/industrial-07.png">

Robots will put together the chassis by welding different parts together. Then, the robots will typically put in the engine, transmission and suspension. Building the rest of the body operates in much the same way — putting in parts and welding them together (some human interaction is still involved).

Tracking temperature abnormalities can help cut down on defects and, once enough data is analyzed, potentially speed up production time as well. But, what is arguably even more valuable is tracking the robots themselves. The data generated from their operations allows better forecasting of production time, maximizing uptime, performing predictive maintenance, spotting quality issues and generating insights into how processes might be improved.

So, this software mines information across the manufacturing floor from all those machines, sensors, devices, etc. But how is that done?

The data is typically either collected via a gateway device that’s located on the factory floor or via a local node that transfers the collected data to a central gateway device. Then, the data needs to be made usable, or “transformed” (as is true for traditional data analytics), so there needs to be cleansing, normalizing and organizing.

This transformed data is then analyzed, either on-prem or cloud-based, using industry-specific data models. These include those tailored towards discrete, batch and process manufacturing. Since VC’s ❤ KPI’s, some of the common ones from these analytics are performance, uptime, quality, cycle time, OEE (overall equipment effectiveness), along with reasons for defects and downtimes.

The results of this analysis and the KPI’s are then shown to the customer that is (ideally) highly understandable and conducive to informing decision-making and action. Which brings us to what sorts of decisions and actions can be informed by this analysis.

***

## <a name="applications"></a>What are the applications?
I’m not the first to suggest that there’s a big resource allocation problem across a number of industries due to prioritization of “collect all the things” (the NSA approach) rather than finding the “why” first and narrowing down what needs to be collected from there. Perhaps as a result of the jubilant headlines on how revolutionary big data is, it often seems that data collection serves primarily as a signal for organizations to show that they’re doing something about big data.

It’s a similar conundrum to my company’s industry, information security, in which most organizations care foremost about showing they care about security, and vendors are happy to be providing something that sounds really cool but doesn’t solve anything real. But companies showing that they care about security ends up being expensive not just financially, but also time, resource and user experience-wise (something my company is attempting to change) — and the same is largely true for companies attempting to “do something” with the big data they’ve now spent a lot of money to collect and store.

Going into researching this smart manufacturing area, I assumed there would exist roughly the same narrative. Tons of data is given off by sensors, which is being collected and now companies are searching for applications to show that their investments into collecting and storing all this data have not been fruitless.

However, to a large extent this is not the case. As I’ll get to in the next section, a big problem is actually in the data collection itself. And companies have some pretty crystalline use-cases in mind that would materially — perhaps even disruptively — enhance their operations, and the challenge is how to get the right data to do so in a non-cost-prohibitive manner.

At the highest level, the primary application is “optimizing operations.” For a tech startup, that can mean reducing downtime, maximizing processing speed, and so forth. For a manufacturing floor, the implications are enormous. I had the pleasure of seeing a manufacturing floor up-close when I was very young, and it’s one of the clearest of my early memories. But for those who may not have before, here are a few pictures as a guide (in addition to all the lovely machines from earlier):

|![PLCs](/blog/img/industrial-08.png) | ![Robots](/blog/img/industrial-09.png) | ![Plasma cutters](/blog/img/industrial-10.png)|
|:------------------------------:|:------------------------------:|:------------------------------:|


As you can see, there are lots of machines, and different types of them. This means that there’s a lot of opportunity for malfunctioning, misbehaving, slowing down, speeding up and so forth. Identifying and fixing these issues costs money, and before they’re fixed, there are also potential losses from downtime and quality issues as well.

As a result, there is, in fact, a long list of potential applications of being able to analyze data from these machines, including, but not limited to (and with some overlap):

* Improving quality
* Identifying issues in real-time
* Minimizing operational variability
* Reducing waste of raw materials
* Reducing unplanned downtime
* Reducing scrap rates
* Identifying opportunities for process improvements
* Increasing production speed
* Predicting supply needs
* Synthesizing visibility of operations across plants
* Reducing compliance costs
* Improving auditability

The impact of these applications is huge in an industry with slim margins. Being able to better predict, streamline and “smooth out” operations results in significant savings at scale.

*** 

## <a name="adoption"></a>What's hindering adoption?
![Image of a man watching a car fly through a screen](/blog/img/industrial-11.jpeg)*Maybe one day humans can just think of a bunch of dots and have it turn into a sportscar that shoots out of random screens, disrupting manufacturing entirely.*

As foreshadowed above, one of the largest barriers to adoption of these technologies is in data collection. Though it can be treated as a distinct part of the big data chain, the “data cleanup” aspect is extremely challenging, as it is difficult to combine and centralize sensor data emanating from disparate machines and devices.

And, that’s not to mention the sheer amount of data causes some hefty storage requirements, and the pace at which data is generated means that solutions have to be able to keep up. There are also challenges like needing to make sure sensors and communications hardware can survive potentially rough environments, but it seems like people know more or less how to accomplish that.

The most-repeated challenge in realizing the “Fourth Industrial Revolution” is that there needs to be a standard data architecture across vendors. Lacking a global government to decree all vendors must adhere to a certain data architecture or perish, most of the people who cite this challenge have suggestions to ameliorate it along the lines of ¯\\\_(ツ)_/¯.

As a result, current capabilities are pretty okay at helping solve basic problems but not great at solving tricky, complex and big problems. Most of the time, being able to solve those hard problems comes with a big price tag and requires a lot of human input.

When you visualize the manufacturing floor, it becomes super easy to understand why this is the state of the world. Ignoring the fact that there are lots of different kinds of machines involved in any particular manufacturing process, individual machines themselves will have different types of sensors recording tons of data points on different things involved in its operation. Considering then that an individual machine will have thousands of data points in a single operation, an entire manufacturing floor will have millions — so just imagine the sheer scale of how much data is generated from ongoing operations.

<p align="center"><img src="/blog/img/industrial-12.jpg"/ alt="Spock sobbing mathematically"></p>


It’s a frustrating realization, and if you’re like me, then your mind begins to furtively think of how to fix it. Starting at a small scale, theoretically vendors could ensure that all sensor data generated from a single machine adhered to the same data architecture. Let’s be bold and optimistic and even say that a vendor could ensure that all their different machines adhered to the same data architecture, so if you had a floor with only their equipment, you could collect and combine all this juicy data with ease.

But in the real world, making sure all the sensor data has the same architecture is decidedly not trivial. What incentives does the vendor have to implement this extra process when designing their products? Do customers really care so much about the data that they’re willing to pay a premium for machines with a common data architecture?

This results in first-mover disadvantages both on the vendor and customer side. For vendors, they don’t want to be the dopes that were first to put all this effort into having this gorgeous, seamlessly combinable spring of sensor data from their machines that customers end up not buying because it’s more expensive than that of their Tower of Babel-esque competitors. For customers, they don’t want to be the dopes that were first to pay a premium for this theoretically awesome tech that turns out not to generate such actionable insights after all, or worse, isn’t as easily collected and synthesized as promised. Not to mention the customers will still need to buy or develop the analytics that leverage this data.

It’s going to take a risky bet on one side or the other. My personal bet is on the customer side, which will (hopefully) put pressure on vendors. Why? Because the customers (the manufacturers) may be able to sell some of the insights they gain to their own customers as part of a value-added offering. For example, they can differentiate from their competition by suggesting data-supported ways for their customers to improve the quality of their products or speed at which their products can get to market. While helping bottom-line by reducing their downtime, use of raw materials, etc. is all well and good, there’s nothing like a boost to the top-line to really cultivate interest.

This still doesn’t solve the problem of how standardization will actually be accomplished. It doesn’t do a ton of good if each vendor standardizes within itself but makes it even harder for manufacturers to combine data from machines across different vendors. Very few vendors will make all of the machines and devices manufacturers need to run their operations, so it is realistic to assume that broader standardization is essential.

There is some evidence of the government looking to help facilitate standardization, but I, for one, have little faith in how quickly any initiative might be accomplished in that manner. Realistically, the GE’s and other titan industrial firms will throw a lot of money at figuring this out and monetize it as something like IoTAaaS, but those will likely be in areas away from the manufacturing part of “industrial” and instead in use-cases where their machine or part can serve as a strong sole-source of data (e.g. sensors on jet engines to help optimize fuel efficiency).

What I’d love to see is an approach similar to what the founders of Flatiron Health performed in its earliest days. The lore is they traveled around the country speaking with cancer specialists and treatment centers to better understand the challenges they faced, what sort of data was relevant, how it was currently being shared, etc. From gathering those insights first-hand, they developed a solution that has been very sincerely described as “fighting cancer with big data.” There are meaty enough sub-sectors within the industrial space that I strongly believe something similar could be accomplished and help leap over the standardization hurdle to the phase where meaningful insights can be generated with ease.

But, I’m only half joking when I think that maybe this whole problem will be solved if Google open sources whatever software it develops as it builds its self-driving cars and/or AI-driven robot and drone army, *ahem*, logistics network, then executes its Order 66 to have the global leaders it’s funded and seeded mandate Google’s way as the standard.

***

## <a name="who-cares"></a>Who cares?

Luckily from a “who cares” perspective, the field of potential customers is actually enormous. Manufacturing spans behemoth industries, including pharmaceuticals, transportation, aerospace and defense, oil and gas, electronics and chemicals. And within each industry is a chunky supply chain full of many vendors, from raw materials to packaging. Being the go-to operational analytics solution provider for any one of these industries alone would very likely result in a hefty amount of revenue.

From the VC perspective, it’s pretty obvious why there’d be interest in investing in this area, particularly if you’re an investor for a corporate VC arm who happens to be a part of the manufacturing or industrial supply chain. It also heavily touches on IoT, which is an area still attracting a considerable amount of interest, but has crossover appeal to enterprise software investors who are familiar with more general analytics and business intelligence companies.

***

## <a name="risks"></a>What are the risks?
![more sparks](/blog/img/more-sparks.jpg)*Our lizard brains are programmed to like pictures of sparks.*

Being early to the party is no fun, and even though the “Fourth Industrial Revolution” has had its cue music on for a while, it’s still extremely early and somewhat speculative. Nanotechnology is an example industry that’s had an excessively long drumroll, to the point that now legitimately exciting advances are met by many with indifference. And many of the early “plays” in it never took off or lived up to the hype.

To generalize, VC’s like taking “safe risks.” What this means is that they typically like to fund new companies in markets somewhere between totally unproven and super saturated. So where does the infrastructure analytics market fall?

On the one hand, it’s sort of a “no duh” that companies want this operational intelligence, for all the potential applications described earlier. On the other, will these companies buy these sorts of from startups? And can these startups prove that their solutions provide disruptive-level value early enough? Those are questions that are true for a lot of enterprise solution providers, but I feel are magnified given the higher-stakes of the physical realm.

There’s also the uncertainty of standardization. Can companies actually extract the value they promise in a world with that many disparate types of data? There’s potentially the question of whether their value is eroded a bit if standardization happens, and thus it becomes substantially easier to use existing data science methods to garner operational intelligence, but I personally think that’s a lesser risk (and definitely cart before horse).

As in my Flatiron Health analogy earlier, a startup that cataloged all the different machines and things involved in the processes of a specific sub-sector in industrial analytics might have the potential to do exceptionally well. That level of granularity may be necessary to truly crack the code on how to most efficiently and meaningfully collect, combine and analyze this data. But it would involve a longer time horizon and doing Paul Graham’s “things that don’t scale,” both which add execution risk that might be insurmountable in an investors’ eyes.

***

## <a name="current-scene"></a>What's the current scene?
There are a handful of startups that are already operating in this arena (and I have no doubt I’m missing some and quite a few are in stealth). They self-describe in roughly four buckets:

* **Manufacturing Analytics/Intelligence** — Hai, Northwest Analytics, OFS Systems, Optimal+, SightMachine
* **Predictive Maintenance** — Augury, DecisionIQ, Maintenel, Predikto
* **Industrial Analytics** — Seeq
* **IoT Analytics** — Decisyon, mnubo

Some of the more notable VC funds that have invested in these companies include:

* First Round
* Formation 8
* IA Ventures
* Lerer Hippeau
* Madrona Venture Group
* O’Reilly Alpha Tech
* Orfin Ventures
* …and KKR

There are a number of industrial conglomerates that have created data science wings, realizing the potential of the space, such as the list below. They tend to self describe as “industrial analytics” or “process analytics.”

* ABB
* Dionex
* GE (Predix)
* Genpact
* Honeywell
* Siemens

Along with analytics and consulting incumbents spreading out into industry-specific solutions, including the list below. In contrast to the industrial conglomerates above, they come up if you search for “manufacturing analytics.”

* Ayasdi
* CSC
* Datawatch
* Deloitte
* Oracle
* ParStream
* Predixion
* Tableau
* TIBCO
* Wipro

***

## <a name="conclusion"></a>Final Thoughts
I think the issue with the industrial analytics sector isn’t level of VC interest, but instead that the pipeline of companies is really small; so even if investors wanted to take a gamble, there hasn’t been much opportunity to do so. After all, the “right” founders will have come from working in the industrial sector, and if they have the level of data science expertise required to create a novel startup in this space, I’d suspect they’re really well paid (especially if in oil and gas). More typical SV data science founder-types may be apprehensive of tackling this problem space as well given the domain expertise required, which seems to be tricky to acquire without access to industrial equipment.

My prediction is we’ll see some of the incumbent analytics players creating industry-specific modules at first along with the big industrial companies creating analytics solutions. And from there, I hope (and I suspect VC’s hope as well) there are defectors that take the risk to create a pure-play company that takes the big leap forward rather than incremental shuffles.