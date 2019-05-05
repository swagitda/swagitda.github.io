---
title: "Revisiting 2016 Security Predictions"
date: 2016-12-30T21:08:55-04:00
draft: false
toc: false
images:
tags:
  - InfoSec
  - Security Predictions
---

I totally get it — it’d be boring to say year after year, “Yep, phishing definitely still works,” so security vendors instead pour creative thinking and marketing pizzazz into their annual security predictions. Most seem to aim to match the majority of their predictions to other vendors’, with generally one or two unique predictions thrown in to show off their innovative thought leadering. Sometimes those unique ones are spot-on and glorify their authors, and other times we can look back a year later and share a good chuckle.

I chose 16 prediction reports for my analysis, published between September 2015 and February 2016 (later than that would give an unfair advantage), mostly by the larger security vendors and also Wired, since they’re one of the few publications who publishes their own predictions rather than crowdsourcing.

I'll delve into:

1. [What actually happened in 2016?](#what-happened)
2. [Which predictions were right? (naming names)](#correct-predictions)
3. [Which predictions were off? (not naming names)](#wrong-predictions)

***
![The fancy bear logo by Crowdstrike](/img/fancy-bear.jpg)
## <a name="what-happened"></a>What actually happened in 2016?
Looking back on infosec news in 2016, these seem to have been the biggest stories:

### Grizzly Steppe / Fancy Bear
Unless you’ve been living under a rock, Russia waged a (successful) campaign to stoke chaos and influence the U.S. election — hacking the DNC (and RNC), spreading fake news, etc. [FBI / DHS just released a joint report on the campaign](https://www.us-cert.gov/sites/default/files/publications/JAR_16-20296.pdf), deeming it “GRIZZLY STEPPE.” Crowdstrike named the group [“Fancy Bear,”](https://www.crowdstrike.com/blog/who-is-fancy-bear/) and has written about its intrusion into the DNC as well as its use of [Android malware to infiltrate Ukranian field artillery units](https://www.crowdstrike.com/wp-content/brochures/FancyBearTracksUkrainianArtillery.pdf) (which seemed to be a response to skeptics of attributing the DNC hack to Russia).

So how was this epic, history-shaping attack conducted? The initial delivery vector was spear-phishing…if it ain’t broke, don’t fix it. To be fair, this was “sophisticated” as far as spear-phishing goes — using legitimate domains and then spoofing a Google suspicious account activity email (not something obvious like malware.delivery.plzclick.ru), which ultimately tricked recipients into entering in their passwords through a fake webmail domain that appeared to be a password reset page. Then, the credentials were used to harvest the emails, exfiltrate them through encrypted communications and create the #Podesta debacle.

### Mirai Botnet (Dyn DDoS)
People panicked when Dyn, a DNS service provider, was getting DDoSed, breaking the internet even more than Kim Kardashian. Then, we found out that the nemesis was a botnet composed of [hundreds of thousands connected devices](http://www.theregister.co.uk/2016/10/21/dyn_dns_ddos_explained/), serving as a zombie army of “things” for their overlords. All Mirai did was log into devices by using the factory default passwords, which was successful enough to infect over 1 million devices.

The author of Mirai open sourced it, and given that the security of IoT devices hasn’t radically improved in the past few months, and consumers are generally allergic to security responsibility, [it’s easy to imagine massive IoT botnets happening again](https://www.wired.com/2016/12/botnet-broke-internet-isnt-going-away/).

### Crypto-ransomware boom
Most recently, San Francisco’s Municipal Transportation Agency [was infected by ransomware (specifically HDDCryptor)](http://arstechnica.com/security/2016/11/san-francisco-muni-hit-by-black-friday-ransomware-attack/), with the attackers demanding $73k in exchange for restoring the data. However, SFMTA decided instead to let riders ride for free for a bit, and then fixed the problem by using a backup to restore their systems. The initial access was gained by a vulnerability involving Oracle’s WebLogic server and the Apache Commons library (a deserialization vulnerability), and SFMTA only became a target because the attackers used a web scanner to find vulnerable servers.

[Hollywood Presbyterian Medical Center in Los Angeles was also held hostage](https://www.wired.com/2016/02/hack-brief-hackers-are-holding-an-la-hospitals-computers-hostage/) through the ransomware “Locky,” but ended up paying only $17k in BTC vs. the initial demand of $3.4 million. Locky ended up infecting a few other hospitals, as well, and is particularly nasty because it looks for and erases Volume Shadow Copy files, which means automatic backups are erased.

### SWIFT wire transfer hax
[Hackers stole $81 million from accounts at Bangladesh’s central bank](https://www.wired.com/2016/05/insane-81m-bangladesh-bank-heist-heres-know/) within a few hours, and that wasn’t the only bank they attacked. They achieved this by getting bank employees’ credentials to SWIFT, the network between banks that processes most of the world’s wire transfers. There’s nothing concrete on how they got the credentials, but we do know they used malware to subvert SWIFT’s software for recording money transfers — which is far from ideal. It resulted in SWIFT to push for 2FA, which should help in the future.

### Adult Friend Finder
This breach received perfect 10 on the [breach level index](http://breachlevelindex.com/top-data-breaches) — [over 400 million records were exposed](http://breachlevelindex.com/top-data-breaches). There isn’t much information on the breach yet, but it appears the passwords were kept in plaintext or used SHA1. The attackers allegedly exploited a [local file inclusion vulnerability](http://www.csoonline.com/article/3132533/security/researcher-says-adult-friend-finder-vulnerable-to-file-inclusion-vulnerabilities.html), meaning it’s yet another web app attack.

Honorable mention goes to two other hookup sites that were breached and stored their passwords in plaintext. Fling.com had credentials for [40 million of its users on sale for 0.8888BTC](http://www.ibtimes.co.uk/fling-com-breach-passwords-sexual-preferences-40-million-users-sale-dark-web-1558711) in May (~$400 at the time). Mate1.com had [over 27 million plaintext passwords for sale](https://motherboard.vice.com/read/hacker-claims-to-have-sold-27m-dating-site-passwords-mate1-com-hell-forum), but for 20BTC in February (~$8,700 at the time). For Mate1, the hacker said that they compromised the server and dumped the MySQL database, with no further details.

### Yahoo data breach
[It affected 1 billion user accounts](http://www.nytimes.com/2016/12/14/technology/yahoo-hack.html?_r=0)…which was surprising because most people never thought Yahoo had that many users. I won’t be counting this towards scoring the predictions, given the actual attack happened in 2013. But, there’s no denying it received substantial coverage, and will be an interesting case study going forward if it results in [Verizon successfully reducing the purchase price of the acquisition](https://techcrunch.com/2016/10/06/report-verizon-wants-1-billion-discount-after-yahoo-privacy-concerns/)…or not acquiring them at all.

***
![A crystal ball](/img/bad-cyberart-09.jpg)
## <a name="correct-predictions"></a>Which predictions were right? (naming names)
Spear phishing was mentioned 11 times total in all of the predictions — half of those were about mobile-specific spear phishing, and the rest mostly about the need to train employees on how to look out for it. Only McAfee and Sophos made any mention of hackers using “sophisticated” spear phishing more often, and even then it was a minor point in their larger reports. Election-themed phishing was predicted by Forcepoint, which I cover below, but no mention of spear phishing methods specifically. So, no one really wins on this one.

Kaspersky and Intel Security accurately predicted — although embedded rather than one of their primary predictions — that libraries used by servers (particularly open source libraries) would increasingly be targets, which was relevant in the SFMTA case. Otherwise, web app / server-side app attacks were virtually ignored — despite being a prevalent attack vector year after year. And exactly zero of the reports mentioned anything about SWIFT, or wire transfers more generally — the focus was primarily on credit card systems.

But other events fared better in their coverage:

### Influence operations & U.S. election-themed attacks
First up, ForcePoint (Raytheon) hit the nail directly on the head with their prediction on U.S. election-related influence operations. While a few others brought up electronic voting systems, ForcePoint specifically called out the fake news phenomenon (albeit missing involvement by nation-state threat actors):
>     Information on social media is often spread and accepted before fact can catch up with fiction, giving determined hacktivists an opening to misrepresent and/or misdirect the public’s perception of individuals and events… 
> …the other hand suggests there’s little to prevent incendiary, inaccurate information from virally spreading and being accepted by the public as factual. Even if such information is later corrected, this false information lives forever on the Internet, with the potential to inform opinions and as a result misinform — and potentially direct the actions of — the electorate.

They also correctly predicted the use of election-themed phishing campaigns, and even that candidates would be targeted:

> However, given the influence the choice of a U.S. President can have…it’s not hard to envision a circumstance where factions hoping to gain insight or advantage in an election or following it, might target a candidate or groups involved in promoting them for useful data in keeping ahead of or undermining the competition

So, congrats on them for being right, however unfortunate for the rest of us.

### IoT Botnets
The other big winner is Wired, who predicted the Mirai botnet, or what they called “the rise of the IoT Zombie Botnet.”

> One trend we’ve already spotted is the commandeering of IoT devices for botnets. Instead of hackers hijacking your laptop for their zombie army, they will commandeer large networks of IoT devices — like CCTV surveillance cameras, smart TVs, and home automation systems.

Anomali also gets some credit for this, too, although it was a minor point in their larger prediction about IoT exploitation.

### Ransomware…to a certain extent
This was easily one the safest predictions to make last year, which is probably why nearly all the vendors mentioned it. Some took a more hyperbolic approach and overshot its impact and potential damage. Others head-scratching-ly said that ransomware will “go corporate,” although there had already been plenty of documented cases of corporate ransomware before 2016. But technically they weren’t wrong about it hurting businesses more, so I’ll allow it.

Many warned about potential extortion, in which the attackers would threaten to go public with data in the hopes of receiving a higher ransom, but for obvious reasons we probably wouldn’t hear about those cases publicly, so the jury’s still out. I’d argue this fear was overblown, given we saw three major hookup site breaches, credentials for which were being sold on dark web forums (when they could’ve been used for extortion).

Predictions that ransomware would become cross-platform were also technically accurate, as there are now documented cases of ransomware for [Linux](http://www.computerworld.com/article/3113658/security/new-ransomware-threat-deletes-files-from-linux-web-servers.html) and [Mac](http://www.theregister.co.uk/2016/03/09/first_macosx_ransomware_actually_linux_port/) — although not many documented families of ransomware for these platforms as of yet. I’d personally say Linux ransomware could be a possibility for 2017 — after all, it’s what constitutes modern infrastructure for most enterprises.

### Attacks hidden in SSL vs cleartext
According to an [A10 Networks / Ponemon study](https://www.a10networks.com/news/cybersecurity-report-organizations-victimized-by-malware-hidden-in-encrypted-traffic) from this summer 41% of attacks used malware hidden in SSL traffic to evade detection. Appliances have a difficult time quickly inspecting SSL traffic to detect malware, making it a new headache for enterprises. And turns out A10 Networks was the only one to predict this trend.

***
![A digital thumbs down](/img/bad-cyberart-10.png)
## <a name="wrong-predictions"></a>Which predictions were off? (not naming names)

### IoT in theory, but not reality
> We won’t see widespread examples of attackers getting IoT devices to run arbitrary code any time soon.

Welp…see the aforementioned Mirai botnet.

### PKI ubiquity
> In 2016, we expect that PKI will become ubiquitous security technology within the IoT market.

A safe prediction for 2017 is that PKI will continue to be a mess, and so will IoT security.

### Drone hackpocalypse
> However, drones also present a wide range of risks, from privacy invasion to corporate espionage to terrorism.

Sure, but realistically it’s confined to nation-state level for now, so it’s dubious if it belongs in a predictions report aimed at corporate CISOs. Some [research](https://www.wired.com/2016/03/hacker-says-can-hijack-35k-police-drone-mile-away/) [was](https://hub.jhu.edu/2016/06/08/hacking-drones-security-flaws/) [published](http://arstechnica.com/security/2016/10/drone-hijacker-gives-hackers-complete-control-of-aircraft-in-midflight/) on how to hack drones, but there’s nothing confirmed in-the-wild. Amazon also just [published a patent](http://qz.com/873920/amazon-has-a-plan-to-defend-drones-from-hackers-and-bow-and-arrow-wielding-troublemakers/) for protecting its delivery drones against hacking…and against bows and arrows. My guess is this prediction is supposed to fall under the [Rule of Cool](http://qz.com/873920/amazon-has-a-plan-to-defend-drones-from-hackers-and-bow-and-arrow-wielding-troublemakers/) rather than having a logical basis for impact to enterprises.

### Terrorists pick up the (cyber)bomb
> In 2016, we will increasingly see the convergence of physical and cyber terrorism aimed at wreaking far-reaching havoc.

Terrorists did not become cyber ninjas blowing up power plants all over the place. The Grugq has [already written](https://medium.com/@thegrugq/isis-cyber-security-skills-suck-cc3466aa73f7#.jhezy91mj) [about this](https://medium.com/@thegrugq/just-the-facts-isis-encryption-c70f258c0f7#.e1ovjsbl8). [Squirrels are still the better conductors of cyber war ops](http://cybersquirrel1.com/) against our critical infrastructure.

### Post-quantum crypto
> “The cryptopocalypse is nigh.” (due to quantum computing)

Nope. Probably a prediction that can be safely shelved for a few years.

### Cyber. insurance. changes. everything.
> The cyber insurance market will dramatically disrupt businesses in the next 12 months.
> In 2016 many companies will turn to cyber insurance as another layer of protection, particularly as cyber attacks start mirroring physical world attacks.

Looks like most companies still think insurance is [inadequate risk mitigation](https://www.sans.org/reading-room/whitepapers/analyst/bridging-insurance-infosec-gap-2016-cyber-insurance-survey-37062). According to the [SANS survey](https://www.sans.org/reading-room/whitepapers/analyst/bridging-insurance-infosec-gap-2016-cyber-insurance-survey-37062), only 33.5% of companies have cyber insurance. What’s more, [83% of respondents to a PartnerRe survey](http://www.partnerre.com/assets/uploads/docs/PartnerRe_Cyber_Liability_Trends_Survey_2016.pdf) said that cyber insurance policies are only “sometimes” meeting the needs of insured companies. So, while it may be blossoming as a new “check the box” item, it’s nowhere near disrupting enterprise security strategies yet.

### Mobile app exploitation
> With the growing amount of malware and the vulnerabilities present in legitimate mobile apps, a major breach is bound to happen, potentially on a massive scale.

While many of the predictions highlighted mobile as an attack vector in general, where they specifically got it wrong is in thinking that vulnerabilities in mobile apps would be exploited. Why expend the effort when malicious apps still work just fine? See: [the poisoned app Fancy Bear used to hack Ukranian field artillery units](https://www.crowdstrike.com/blog/danger-close-fancy-bear-tracking-ukrainian-field-artillery-units/). There haven’t been any major corporate breaches directly tied to mobile malware, though I’ll concede it’s possible they just aren’t public. Mobile malware grew at a very healthy pace in 2016, however:

![Chart of new mobile malware by McAfee Labs](/img/new-mobile-malware-2016.png)

### Wearables as the new sexy attack vector
> Initially, we doubt that a smartphone will be completely compromised by an attack through a wearables device, but we expect to see the control apps for wearables compromised in the next 12 to 18 months in a way that will provide valuable data for spear-phishing attacks.

There’s been research on hacking them, but as far as I can find, no evidence that hacking wearables has ever been used as part of a corporate data breach. The only headlines in 2016 are variations of “Hackers targeting your wearables data?” or “Can Wearable Technology Threaten the Security of Your Biz?” so I’ll invoke [Betteridge’s law of headlines](https://en.wikipedia.org/wiki/Betteridge%27s_law_of_headlines) and say the answer is no.

### Remote-controlled cars
> Attacks on automobile systems will increase rapidly in 2016 due to the rapid increase in connected automobile hardware built without foundational security principles.

This didn’t happen. [Seriously cool research](https://www.wired.com/2016/08/jeep-hackers-return-high-speed-steering-acceleration-hacks/), but no reports in the wild — just because something can be hacked doesn’t mean it’s easily hacked.

<div class="center">
	<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Why is it that every headline is &#39;product X easily hacked&#39;. Hacking a car was hard. Hacking is hard. It is good that it is hard.</p>&mdash; Chris Valasek (@nudehaberdasher) <a href="https://twitter.com/nudehaberdasher/status/805419828756496384?ref_src=twsrc%5Etfw">December 4, 2016</a></blockquote>
	<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
</div>

### Password reuse attacks will decline
> Password reuse attacks will begin to decline… people are starting to adopt password managers… Advancements in biometrics are also helping the cause…most major Internet layers are also adding two-factor authentication as a standard option

All of those things might be true, but not enough to make a dent. These are entities publicly victims to password reuse attacks in this year alone: [Carbonite](https://www.carbonite.com/en/cloud-backup/business/resources/carbonite-blog/carbonite-password-attack/), [Citrix GoToMyPC](https://threatpost.com/gotomypc-suffers-major-password-reuse-attack/118781/), [Deliveroo](http://www.bbc.com/news/technology-38070985), [GitHub](https://techcrunch.com/2016/06/16/github-accounts-targeted-in-password-reuse-attack/), [Groupon](http://www.batblue.com/groupon-users-hit-password-reuse-attack/), [Mark Zuckerberg](http://www.vanityfair.com/news/2016/06/mark-zuckerberg-terrible-password-revealed-in-hack), [TeamViewer](http://arstechnica.com/security/2016/06/teamviewer-users-are-being-hacked-in-bulk-and-we-still-dont-know-how/), [U.K. National Lottery](https://www.itgovernance.co.uk/blog/uk-national-lottery-password-reuse-attacks-what-are-the-chances/). Further, Patrick Heim, Dropbox’s Head of Trust & Security said in September that [“99% of compromised user accounts come from password reuse.”](http://www.cso.com.au/article/606531/99-compromised-user-accounts-come-from-password-reuse-cso-heavy-hitters-reveal/) Seems more like wishful thinking / “it’s-2016-how-is-this-still-happening?!” than a prediction.

***

## Conclusion
I’ve already started reading some of the 2017 predictions — being diplomatic, I’ll say I’m looking forward to seeing how the next year unfolds. I saw one list described as not containing any “wows,” which I think accurately pinpoints the problem with these lists in general. 

It’s more an exercise in taking a provocative stance to raise attention and be able to tell customers how your product addresses this important upcoming issue, rather than a probability-weighted list of the actual threats enterprises will face in the upcoming year — users will keep clicking on things they shouldn’t, injection vulnerabilities are still in all the things, and not enough people use 2FA or encrypt their users’ credentials.

In conclusion, my ultimate 2017 prediction is that I’ll have plenty of content for an equivalent of this post next year.