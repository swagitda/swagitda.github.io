---
title: "Analyzing the Black Hat USA 2018 Business Hall"
date: 2018-08-06T18:40:42-04:00
draft: false
toc: false
images:
featured_image: "/blog/img/bad-cyberart-17.jpg"
thumbnail: "/blog/img/bad-cyberart-17.jpg"
tags:
  - InfoSec
  - Market Analysis
---

## What type of vendors are showing themselves off in the Business Hall? Are they mostly startups?

<img style="display:block; margin-right:auto; margin-left:auto; max-width:80%;" src="/blog/img/bhusa2018/vendors-type.png" alt="Chart of number of vendors by funding type for the Black Hat USA 2018 Vendor Hall">

Not quite “mostly,” but 46% of vendors in the hall are indeed VC-backed companies at varying stages of maturity. Privately held companies are a non-trivial segment at 17%, and there are 30 Private Equity-owned companies making up 12% of the hall. There are also 12 companies who are acquisitions, primarily those who were acquired within the past year; booths require being booked far in advance, leaving insufficient time to be assimilated into their acquiror’s booth (if so desired).
<img style="float:right; max-width:50%; padding-left: 10px" src="/blog/img/bhusa2018/vc-by-age.png" alt="Chart of number of VC-backed companies by age of last raise">

Nearly half (44%) of VC-backed companies were funded within the past year, shooting up to 82% within the past two years and 92% in the past three. Only 10 companies have not been funded in the past three years, and one could hypothesize that they are considered long in the tooth by their VCs.


***
## How many VCs are dedicated to investing in infosec?
<img style="float:right; max-width:50%; padding-left: 10px" src="/blog/img/bhusa2018/fund-numbers.png" alt="Chart of the number of VC funds by companies invested">
The overwhelming majority (69%) of Venture Capital firms are investors in only one company exhibiting in the BH USA 2018 Business Hall. Out of 350 total investors in 118 VC-backed companies, 46% [led](https://avc.com/2013/09/leading-vs-following/) at least one deal — and of those 46%, 71% only led one deal.

I’ve long held a hypothesis that the list of “dedicated” investors in infosec is actually quite small, and that the incredible amount of deal volume we presently see is driven by one-off investors who want to dip their toe in the infosec waters, having seen blazing, FUD-ridden headlines declaring its relevance. The data seem to support this hypothesis.

There are 21 VC firms who participated in four deals or more (i.e. invested in four or more companies exhibiting). Thus, I consider them the most “dedicated.” Data Collective, while following in four deals, did not lead any deals, meaning they just miss the cut to be part of the “Top 20 VCs”:
<script src="https://gist.github.com/swagitda/c27200dedbac7090090d7a0a2fe98ba1.js"></script>

You can explore all of the Venture Capital firms, ordered by number of companies in the Business Hall in which they’ve invested by [visiting the GitHub repo](https://github.com/swagitda/bhusa2018-bizhall/blob/master/vc-analysis/vc-fund-count-with-names.png), or scrolling to the very bottom of this post.

***

## What venture stage are vendors & how much capital are they raising?
<img style="float:right; max-width:50%; padding-left: 10px" src="/blog/img/bhusa2018/vc-by-round.png" alt="Chart of the number of VC-backed vendors, by latest round">
As you might suspect given the steep price for Black Hat booths, there are few seed-stage companies present. The VC-backed vendors are highly concentrated between Series A and Series C (68% of all VC-backed vendors), which reflects general infosec funding trends, as few companies get funded to the late stage, either being acquired or quietly starved for capital.

Note, “Venture Round” is a nebulous term and can mean basically anything — from earlier stage to later stage — so it should not be interpreted in the same timeline as the Series rounds.

The size of the funding round naturally grows the later stage the company reaches. Note that there are few data points for Series E and Series F rounds, so don’t read too much into the decline in size at Series F (a hypothesis might be that reaching such an exceedingly late stage means investors’ patience has worn thin).

<img style="display:block; margin-right:auto; margin-left:auto; max-width:80%" src="/blog/img/bhusa2018/vc-dollars-by-round.png" alt="Chart of the average size of funding rounds, by stage">

***
## How many Private Equity firms are backing companies on the floor?

There are 30 companies backed by 27 total Private Equity firms in the Business Hall this year. While the majority (81%) are mostly one-off investors (though some are also participants in late-stage VC rounds), there are five PE firms that back two or more companies presenting on the floor:
<script src="https://gist.github.com/swagitda/5115bd90d76dfe7b67029dc3f665c90d.js"></script>

***
## How fresh is the Innovation City?
<img style="float:right; max-width:50%; padding-left: 10px" src="/blog/img/bhusa2018/innovation-city.png" alt="Chart of Innovation City 'residents,' by type">
Innovation City, with 41 “residents,” has a higher concentration of VC-backed companies than the total population (59% vs. 46%), as well as of privately-held companies (34% vs. 17%). What might be surprising is that there are still two acquired companies and one PE-backed company presenting in Innovation City.

True to its marketing pitch of being a designated area for early-stage companies, the average amount of the latest raise by Innovation City residents who are VC-backed is $11.4mm, in contrast to the overall average of $27.2mm. 58% of residents most recently raised a Series A or Series B, while only 4% most recently raised a Series C or later (vs. 34% in the general VC-backed Business Hall population). Nearly double (25% vs. 14% in the general VC-backed population) raised a “Venture Round,” which again, being a nebulous term, is troublesome to place in the VC funding timeline.

***

## How U.S.-centric are the vendors at Black Hat, anyway?
<img style="float:right; max-width:60%; padding-left: 10px" src="/blog/img/bhusa2018/geo-all.png" alt="Chart of all companies, by geography">
The answer is pretty U.S.-centric, at 83% of all vendors in the Business Hall (and 86% of all VC-backed vendors). While I know Brexit hasn’t happened yet, I do consider the UK infosec market somewhat distinct from the EU, as there’s a decently active infosec startup scene there and an emergent VC ecosystem, too. There are 13 (5%) EU-based vendors, but less than half of those (6) are VC-backed. The UK is slightly more VC-weighted, with 6 VC-backed companies out of 10 companies total (4% of all companies).

<img style="float:right; max-width:40%; padding-left: 10px" src="/blog/img/bhusa2018/geo-vc.png" alt="Chart of VC-backed companies, by geography">
Although funding activity is exceptionally strong for Israel-based security startups, there are only 7 Israeli vendors (3%) in the hall this year, 3 of which are VC-backed startups. Given the stark contrast with the funding volume into Silicon Wadi I’ve personally witnessed this year, I suspect it’s either that the companies are too young to have reserved a booth in time for 2018, or that quite a few are playing the classic game of listing HQ in the U.S. so as not to deter customers or investors.

Within the U.S., California makes up nearly half (47%) of all U.S.-based vendors presenting, and over half (52%) of VC-backed startups in the Business Hall. After California, the usual suspects of Massachusetts, New York, and the D.C. area (Virginia/Maryland) round out the bulk of companies, along with growing areas of VC interest like Colorado and Texas.

<img style="display:block; margin-right:auto; margin-left:auto; max-width:80%" src="/blog/img/bhusa2018/state-all.png" alt="Chart of all U.S. companies, by state">

***
## How many companies have some form of name collision?

We’re all familiar with the infosec startup tropes, so I decided to see whether the data support it. Unsurprisingly, many companies (13%!) have some form of “Security” or “Secure” in their name. Net (which can include Networks), and Cy (which can include Cyber) present a solid showing as well. More recent tropes, such as “Dark” or “Deep” are less prevalent than I assumed — in fact, Deep only lurks in two vendors’ names.

<img style="display:block; margin-right:auto; margin-left:auto; max-width:80%" src="/blog/img/bhusa2018/name-trope.png" alt="Chart of the number of companies, by trope in name">

***

## A few notes on the data
Vendors were retrieved from the [Black Hat 2018 Business Hall Floorplan](http://www.expocad.com/host/fx/ubm/18blckh/exfx.html#exhibitors), and exclude any federal agencies, educational organizations, or nonprofits. I also excluded any companies in the Career Zone, as they are aiming to recruit security talent rather than sell products or services — for example, I presume Major League Baseball is not selling the latest Threat Intelligence Automation on the Blockchain.

***

Care to explore the data yourself? [The raw table is available on GitHub](https://github.com/swagitda/bhusa2018-bizhall/blob/master/data-table/bhusa18-bizhall-list.md), as is the [general project repo](https://github.com/swagitda/bhusa2018-bizhall) (potentially more to come later!).

***

## Appendix

### Exactly which VCs funded exactly how many companies exhibiting in the Black Hat USA Business Hall this year?
<img style="display:block; margin-right:auto; margin-left:auto" src="/blog/img/bhusa2018/fund-names-tall.png" alt="List of VCs, sorted by number of business hall vendors funded">
