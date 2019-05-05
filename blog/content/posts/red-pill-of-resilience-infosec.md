---
title: "Red Pill of Resilience Infosec"
date: 2018-08-01T17:26:47-04:00
draft: true
toc: false
images:
tags:
  - InfoSec
  - Keynote
---

*What follows is the full text of my keynote, also available as [a video](https://www.youtube.com/watch?v=ux--pHFpeac) and [as slides](https://swagitda.com/speaking/Red-Pill-of-Resilience-Shortridge-Countermeasure-2017.pdf).*

***

There has been insufficient exploration of the first principles of resilience in the context of information security, despite the term being superficially peppered in our common discourse. Too often, resilience is conflated with robustness — to the detriment of us all.

To state more poetically, through the pen of the notable fantasy author Robert Jordan referencing one of Aesop’s fables, *“The oak fought the wind and was broken, the willow bent when it must and survived.”* To speak of protection without resilience is to believe you can always beat the wind. To speak of deterrence without resilience is to believe you can deter the wind from blowing at all.

There are times when attacks may be deterred or halted before damage is wrought, but one cannot always predict which way the wind will blow. We cannot predict the adversary we will face and the amount of resources they are willing to expend to compromise our systems.

Protection or deterrence can serve as a valuable tactic to grant some level of peace, but resilience — the ability to absorb change and survive — is the foundation on which survival rests. Again, far more poetically than I could ever say, Generalissimo [Chiang Kai-shek](https://en.wikipedia.org/wiki/Chiang_Kai-shek) of the Republic of China advised, *“The more you sweat in peace, the less you bleed in war.”* Attempt the peace, but assure you can still survive the war.

But the discourse about resilience in information security has, to date, been far from poetic. Rather, it’s been sprinkled as a buzzword, floating along at a shallow level primarily in discussions of cyber insurance and how companies can transfer risk by buying policies. I believe this is a waste of its potentially torrential conceptual power. Resilience is ultimately about accepting reality and building a defensive strategy around reality.

As in the Matrix, resilience serves as the red pill — once you accept the reality, it’s impossible to go back to a strategy that ignores it. My goal in this talk is to show you how digging into this heart of resilience can drive a paradigm shift in how we architect security strategy (and I don’t throw the term “paradigm shift” around lightly).

I’ll first explore why the time for the resilience paradigm is nigh, and how our grief as an industry has led us to this point. I’ll next briefly share the etymology of resilience. Its application to information security is one of the newest, and there exists a rich history of its use in other domains — a history worth exploring to see if there are principles and findings to be shared.

Information security is not the only complex system, and ecological systems dealing with climate change and urban areas dealing with natural disasters represent analogical systems in which dynamics are nearly impossible to predict, and the number of interrelating factors is prohibitive to enumerate.

This cross-domain research presents a concept of resilience based on robustness, adaptability, and transformability. I’ll cover these three concepts in detail so we can understand how they fit under the umbrella of resilience. I’ll expand on this cross-domain lens, and it will serve as the one through which I’ll examine what resilience means in information security.

I am humbly attempting to define and establish a notion around what resilience means for information security — both in an intellectual and practical sense. I would be shocked if all of my thinking is on the mark. More than anything, I desperately want to encourage a discussion of first principles around resilience, and to begin a fruitful conversation around how practical implementations of resilience ideology for defensive security should look. I believe we have a fighting chance.

***

## Stages of Grief in Information Security

But first, why is there rising talk about the term “resilience,” despite the industry not having solidly established what it means? I propose that it is the result of the final stage of grief — acceptance — of the fact that there is not, and likely will not ever be, such a thing as an un-hackable organization or system.

Over the past twenty years, the infosec industry has grieved the fact that companies are ever-vulnerable to attack. Very little can be done against the latest exploit or attack vector that is currently unpublished and unknown. The industry has not fully coped with this grief. Like most grief, it isn’t a linear process, and these cycles have ebbed and flowed at various times in the industry’s history.

The first stage of grief is **denial** — clinging to a false, preferable reality. This manifested as companies being hesitant to deploy security solutions at all, believing that they weren’t truly at risk.

**Anger** — recognizing the denial cannot continue, and becoming frustrated — seeing security as an unwanted necessity. This manifested in harsh penalties and legislation, prosecuting and punishing vulnerability researchers — even ones doing work for free or disclosing responsibly.

**Bargaining** — the hope that the cause of grief can be avoided — resulted in the explosion of new security tools in an attempt to stop the problem

**Depression** — despair at the recognition of the predicament — led to the refrain of more recent years in the vein of, “You’re going to get hacked, there’s nothing you can do about it.”

Finally, **acceptance** — the stage into which I believe we are now transitioning, understanding that there is an inevitability of successful attack, but recognition that there is an ability to prepare and that not all is hopeless.

Unfortunately, I fear the bargaining stage has set us up for a challenging road to implementing acceptance. The explosion of security tools in an attempt to avoid the problem has resulted in an untenable [market for lemons](https://en.wikipedia.org/wiki/The_Market_for_Lemons) in which tools and services are prescribed regardless of real need.

Fear, uncertainty, and doubt (FUD) specifically preys on this desperation to bargain, and its use by marketing departments is little different than selling hope of a cure to those who are chronically ill and in their own bargaining stage of grief through alternative, disproved methods. More simply put, the bargaining stage is the demand for which snake oil is the supply.

The resulting depression is unfortunately not the antidote for snake oil — security nihilism is an inaccurate conclusion and does little to incentivize practitioners to pursue more resilient strategies than unproven ones. Therefore, in this blossoming acceptance phase, it is important we have a conversation about what actually works — and to begin, I’d like to delve into what resilience has meant before we as an industry began to espouse it.

***

## Etymology of Resilience
Up until the early 19th century, the primary meaning of resilience was to “rebound.” Its first use in the context of engineering was in 1858, to imply strength and ductility, or a material’s ability to stretch under tensile stress.[1] The abstraction from this physical characteristic — the time it takes for a system to return to a pre-determined, single equilibrium — is the one which has persisted in the common understanding of resilience.

However, in the 1970s, resilience began being used in psychology — understood as a process of changing current behaviors to cope with an adverse condition, for reverting to a prior psychological state post-incident is unrealistic and can actually represent unhealthy coping strategies. The 1970s also saw the beginning of resilience’s use in ecology, but over time, the concept gradually expanded into use across the social sciences and with the two domains’ coupling, or socio-ecological systems.

Most recently, it began to be applied to climate change adaption in the early 2010s, including the natural disaster risk management space due to increases in natural disasters that by all evidence are caused by climate change.

### What does resilience mean for complex systems?
A complex system is one in which many of its underlying components interact with each other, and one in which it is very difficult to predict behavior. More simply put, it is a system with non-linear activity in the aggregate. Examples of complex systems in our daily lives include our universe, our planet’s climate, our cities, our brains, and even living cells.

Information security is also complex system. Defensively speaking, it is plagued by an inability to predict attacker actions, and it also consists of highly interconnected, dynamic relationships. Both sides of the security equation — defenders and attackers — are human. But there are additional relationships beyond the direct conflict, including users, governments, software vendors, service providers, and so forth. To unfurl these relationships and attempt to fit them into a predictive model is very simply prohibitive.

The first application of resilience through the lens of complex systems was by C.S. Holling in 1973, an ecologist who was one of the founders of ecological economics. Ecological resilience, he said, is measured by the amount of change that could be absorbed before the system’s underlying structure changes.[2] He asserted that an ecological system can be highly resilient, but also exhibit a high degree of instability — and, in fact, that the proper reaction of an ecological system was to continually adapt, rather than attempt to return to a static equilibrium.[1]
Heidelbach, W. (September 28, 2016). Chestnut.

For example, eastern North American forests were once full of chestnut trees until a chestnut blight in the first half of the 20th century wiped them out.[3] However, oak and hickory trees began spreading in its stead. The forests changed in appearance and composition, but still survived as forests.

Evolutionary resilience, borne from analyzing socio-ecological systems, operates under the assumption of complex systems that co-evolve, focusing on adaptation and transformation. Rejecting the idea of thresholds within which a system should fluctuate, it instead suggests multiple levels of controls and the ability to adapt the status quo by reorganizing or regenerating around the change, thereby creating a new status quo.

For example, communities can diversify their agricultural landscapes and production systems, designating some areas for soil conservation and organic agriculture while promoting multicropping in others. They can protect some forested areas while designating others for the community and focusing reforestation efforts there.

This notion of evolutionary resilience can be summarized as consisting of three central characteristics: robustness, adaptability, and transformability.[4] The core notion is that in order for a complex system to be resilient, it must be able to withstand a shock, adjust so as to incur less damage, and be open to challenging previous decisions and goals.

I will be keeping in mind these three core characteristics in the context of information security. With robustness, you must be able to withstand an attack; with adaptability, you must be able to adjust your environment so you incur less damage when attacked; with transformability, you challenge your existing assumptions and decisions, and potentially migrate from existing infrastructure as well as defensive strategies or current methods used in the way you model and understand your threats.
NASA/NOAA. (August 26, 2017). Hurricane Harvey’s Eye.

In most domains, robustness proved dominant in defensive strategy, and can be linked to the concept of engineering resilience — a mistake from the evolutionary resilience perspective. For example, barriers are a form of robustness, blocking storm surges. However, as seen recently with Hurricane Harvey, the primary source of damage was flooding from ongoing rain — highlighting the need for adaptability and transformability to incur less damage going forward and rethink your existing strategies.[5]

Instead, evolutionary resilience must also include adaptation and dynamic change towards the goal of preservation, with robustness as an ingredient rather than the sole objective.

Although the expression, “it’s not about the destination, it’s about the journey” is somewhat trite, it’s quite true for resilience. Resilience must be framed as a continuous, evolving, but sustainable process rather than a goal. As ecological economics scholar Peter Timmerman described, resilience is the building of “buffering capacity” into a system, to improve its ability to continually cope going forward.[6]

A focus only on robustness can also lead to a misleading presentation of the problem as one only based on reducing the risk itself. As in the previous example, the problem could be seen only as, “how can we withstand the hurricane?” instead of “we know the hurricane will hit us, how can we change so that it doesn’t damage our community as much?” This highlights the contrast between robustness and the adaptability and transformability characteristics, which accept that the risk will exist, and instead stress the need to reduce the potential damage from the risk and restructure around the risk.

Furthermore, the efforts around attack prediction represent yet another symptom of collective grief — it’s an endeavor to regain the illusion of control. I’ve given another related presentation at length about [why attack prediction should not be our goal](https://swagitda.com/speaking/Dangerous-Folly-Attack-Prediction-Shortridge-Art-into-Science-2018.pdf), so I will not elaborate further here. Suffice to say, prediction was attempted in other complex systems and not only failed miserably, but wasted precious time, money, and brainpower that could have been spent on a pragmatic aim: resilience — the need to design systems under the assumption the negative shock will not be predicted. As eloquently stated by Susan Elizabeth Hough,

> “A building doesn’t care if an earthquake or shaking was predicted or not; it will withstand the shaking, or it won’t.”[7]

While our industry has come to accept that there are many “unknown unknowns,” our strategy is still one based in hubris — that we can save ourselves in a breach with systems that can withstand unknown risks at unknown times with unknown faces. The evolutionary resilience approach embraces these unknowns, understanding that change is inevitable — ensuring the system survives by absorbing these unknown changes, naturally adapting and reorganizing around this unknown risk, keeping the option open of bearing its own new, unknown face.

***

## Robustness
Robustness involves withstanding and resisting a negative event. Engineering used the concept of resilience only in terms of robustness, measured by how long it takes a system to return to its equilibrium after a shock. However, experiencing an acute stress event implies the normal state was vulnerable to the stress, and that it is thus an “undesirable state to go back to because it would perpetuate this vulnerability.”[8]

In disaster recovery, it’s dangerous to present the problem of flooding, for example, as simply one about excess water. If it’s simply about a physical issue, then solutions are presented that are restricted to just the physical issue. In reality, flooding is a problem because of people, who understandably don’t want to lose their homes or drown. It is unnecessarily restrictive to only consider technical solutions to address the excess water, rather than broader solutions to address the problem in a societal context.[9]

When it is believed that a technical control will help prevent a shock, then it tends to lead to larger potential damage. This is called the safe development paradox.[10] The reason why it’s a paradox is that the stability and presumed safety gained by building a structural mitigation to the problem actually allows risk to accumulate over time due to the false sense of security, leading to a higher chance of catastrophic consequences.

The safe development paradox represents a maladaptive feedback loop — once a structural mitigation is in place, more development happens where it should not.[11] As the development becomes entrenched, the need for structural mitigations becomes even greater — and once the mitigation is in place, more development occurs.

When fires are suppressed in forests that are fire-adapted, fuel builds up in the form of trees or shrubs.[12] As more time passes without a fire, the probability of a ruinously-intense fire grows, posing more danger to nearby human settlements. This is exactly what happened in the mid-1990s in Florida as urban development expanded into fire-adapted pine forests and enjoyed trees and shrubs in their yards.[12] The result was fires during dry periods that resulted in higher damage than usual, destroying many homes in the process.

In security, implementing technical controls can lead to increased damage as well. Retroactively hardening or patching legacy systems in which vulnerabilities are frequently found, can lead to further development on top of these systems, and further entrenchment of those systems within the organization. Feeling like the threat is being prevented leads to development that relies on that assumption — and thus isn’t designed to absorb an attack.

In flood risk management, it’s known as the “levee paradox.”[13] Building a levee can lead to a sense of the problem being prevented, supporting further development and construction on the risky floodplain.[9] For example, less than 3% of people living in Illinois in floodplains with levees in place carry flood insurance.[13] The levee clearly lowers people’s awareness of the risk and ability to respond appropriately to it.[14]

When implementing a robustness control, it’s essential to ensure that it isn’t encouraging further development within a vulnerable system that leaves it open to cataclysmic risk when the control fails. Don’t focus just on resistance in your controls. Doing so will simply “treat the symptoms of bad planning with structures.”[11]

There’s also a lesson here for cyber insurance. Back to the levee paradox, oftentimes areas with levees in place aren’t categorized as official floodplains. This means that homes or offices in those areas don’t have flood-related insurance requirements. The clear lesson I see is: firms offering cyber insurance should consider very carefully whether they exempt companies from certain requirements based on technical controls being in place.

Related to the safe development paradox is the fact that preventing a system from negative exposure means that the system will only function in the artificially stable state. In the levee paradox, it actually creates an artificially stable system which can only survive in dry conditions.

Another example is with coral reefs. Marine reserves are maintained to protect coral from the damaging effects of climate change, such as ocean acidification and thermally-induced coral bleaching. However, unprotected coral actually proves more resilient to climate disturbance, since they’ve faced ongoing degradation due to exposure to the stressor and thus recomposed to have more disturbance-tolerant species.[15]

In information security, you must likewise expose your systems to stressors. Even if you’re building something to be internal-only, like APIs, you should design them with the same threat model as an externally-facing service — for instance, making sure you have data sanitization. Test your systems as if they were externally-exposed, to see if they are sufficiently resilient to global stressors. If it would take years to rebuild, reconsider what data you allow within the system.

The overwhelming focus to date in information security has been on robustness — how to withstand or resist an attack, before rebounding back to “normal.” The traditional components of security — firewalls, anti-virus, system hardening — are all components of a robustness strategy. Even when examining how startup security products are marketed, the words “stop,” or the more creative “thwart” are used, implying an improved ability to withstand an attack.

Remediation even plays into this singular focus on robustness. The goal of remediation within security is to most often fix any vulnerabilities, and, ideally, to return to “business as usual” by reversing damage from an attack. As we saw with the Equifax breach, there is absolutely no chance of “business as usual” when immutable data is compromised. Penetration tests often solely focus on vulnerabilities and what is needed to fix them, rather than proposing new technologies or architecture that would prove less vulnerable long-term.

Other domains have typically held this singular focus, as well. The engineering-led approaches sought to defy nature itself rather than allow the system to flux with nature. For example, the single equilibrium in flood risk management is to have dry conditions in floodplains so that people can continue living in them. Dikes, storm-surge barriers, and dams are all attempts to withstand a flood, and reflect engineering resilience approaches. Their goal is to keep the same artificial equilibrium, in spite of the water system’s natural behavior.[9]

An engineering-only focus leads to the current challenge of companies needing to constantly stay up to date on patches, but facing many hurdles in doing so — and having this be their primary line of defense. The model that must be embraced is one in which the system can survive even if patches aren’t immediately updated, or users still click on phishing links. Your systems must survive even if users download a pdf.zip.exe.

As we saw with coral, without palpable vulnerability through exposure to risk, it is unlikely that resilience will develop.[11] You need to assume that attackers will gain access to a system, and figure out how to reduce the impact. You need to actually practice and embrace disaster recovery, rather than just having a plan.

With all that said, robustness is absolutely important to resilience. But robustness needs to be performed correctly. Drawing from flood risk management, diversity is a cornerstone of robustness — there needs to be layers of controls and diversity of solutions.[9] For example, there are storm surge barriers, dikes, and dams for flood prevention.

New York City has published guidelines for climate change resiliency which also recommend a combination of controls. For example, for dealing with excess heat, they recommend backup generators to hybrid-power systems, using systems with higher heat tolerance, as well as passive cooling and ventilation through window shades or high-performance glazing.[16]

Diversity of controls helps provide redundancy in uncertain conditions. When complementing measures are in place, it’s less likely that there will be catastrophic damage through the failure of a singular control. But, the tradeoff is between efficiency and effectiveness. The easier route with lower upfront costs is to implement a single control. The effective route is to implement layered controls, which may cost more now, but will pay dividends in reduced consequences long-term.

I don’t believe this will be a new concept for many of you. For example, you could deploy a so-called APT-blocking appliance (aka the BlinkyBoxTM) on your network that purports to stop all attacks. However, what then happens when legitimate credentials are used to access a cloud-based service? Or, as we’ve seen recently with Kaspersky, what happens when the APT-blocking-box is hacked by the APT itself to gain access?

Diversity can also be seen through the lens of systems. While we think of fragmentation generally as poor to have, particularly in the context of asset management, there is an argument in its favor. Shared hosting providers can increase correlated risk. If there is a breach at one provider, or vulnerability in a key component or library used across all applications, then your risk exposure is far greater than it might have been otherwise.

The financial crisis in 2008 serves as a pertinent example of the dangers of ignoring correlated risk. There is something to be said for ensuring you have some level of diversity in your architecture. I am by no means the first to suggest that heterogeneity is important — Dan Geer was fired from @stake in 2003 for making that suggestion, specifically in regards to Microsoft’s hegemony.[17]

This sort of diversity also plays into the efficiency vs. effectiveness tradeoff. However, efficiency can actually lead to a more limited space in which you can operate. Being able to function using fragmented technologies and controls will ensure you can adapt much better to uncertainty. Systems diversity, through this lens, can provide the instability that can ensure survival. I posit that it is up for debate whether it is more optimal to have manageability through uniformity or limited impact of any one stressor through diversity.

Thinking in decision trees can help ensure robustness through proper diversity of controls. I’ve discussed decision trees towards information security strategy in prior talks, [most notably at Black Hat](https://swagitda.com/speaking/us-17-Shortridge-Big-Game-Theory-Hunting.pdf). Briefly, the goal should be to [walk through what steps](/posts/choice-architecture-infosec-blue-teams) an attacker would take to reach their goal in your organization. Naturally, there is not just one path an attacker will take; you have to consider what path they will take if they encounter a mitigation as well. From there, you can begin determining what cascading controls are necessary in order to raise the cost to the attacker as much as possible.

Raising the cost to the attacker serves as a bridge between robustness and adaptability. As frequently referenced, Dino Dai Zovi said, “Attackers will take the least cost path through an attack graph from their start node to their goal node.”[18] If you can raise attacker cost, you can begin deterring attackers. Attackers will need greater resources and a greater level of sophistication if you do so. One way to raise cost is through robustness with strong, diversified controls. Another way is through adaptability.

***

## Adaptability

Adaptability concerns reducing the costs of damage incurred and keeping your options open to support transformability. The evolutionary approach is one in which the assumption is that conditions will naturally change over time, and thus the system itself needs to incur long-term change. Reversion to the preexisting state is not necessarily — and often wholly — undesirable.

The Intergovernmental Panel on Climate Change (IPCC) highlights the need for realism and warns about the dangers of incremental changes under the guise of adaptation.[19] They specifically recommend questioning underlying assumptions and existing structures, acknowledging the inevitability of macro-level change, and making managed transformation the goal. Pretending you’re adapting while only undergoing incremental change creates a false sense of security — similar to the safe development paradox. You may alleviate symptoms in the short-term, but you can only cultivate resilience through meaningful change towards adapting to reality.

A macro-level example of adaptability is in the realm of climate change. While traditional protection strategies for wildlife at risk due to climate change have been focused on preserving their existing habitats, more recent research proposes alternative approaches. Protected areas are in static locations, and tend to become increasingly isolated, leaving nowhere to go. Preserving a species in such an isolated, at-risk area results in “genetic ghettos.”[20] The species becomes increasingly acclimated to this limited environment, which consequently staves off any potential for evolutionary adaptation.

Instead, wildlife naturally has shifted ranges in response to previous instances of climate change, in which preferable conditions are “tracked.” Recommendations now include helping connect disparate ecosystems together so that wildlife can more easily migrate. For example, in areas with urban environments, a narrow strip of land can be preserved, or another sort of route created, so that populations can connect to a different climactic area.

One can think of existing territories like legacy systems. We try to “preserve” these habitats through patching and retroactive hardening. The adaptive model from nature is to move to new territories that fit preferred conditions — ones in which the species can survive — which is similar, in effect, to moving to new infrastructure or a new mode of operation that is more resilient to the new threat.

As a highly tangible example, consider the case of database queries. The organization’s status quo might be that they use inline PHP code within the HTML of their web apps to perform database queries. If an injection vulnerability is discovered in an instance of this inline PHP code, they’ll fix that instance, but likely not conduct a full review across all of their inline PHP code. In this case, they’d be improving robustness by patching the code, but they’d be returning to their so-called “stable equilibrium.”

In contrast, embracing adaptability would mean the organization should instead remove inline queries, and use one class that accesses the database. This one class would be completely responsible for all sanitization. The result is not only that now you only have to fix issues in one place, but also that developer turnover can be managed — rather than writing their own new inline code, they can use the new library that you’ve built instead.

Preservation can also lead to misleading indicators of resilience. For example, static measurements such as high coral cover or fish abundance can be poor indicators of coral reef resilience.[21] These measures can just reflect favorable conditions in the past and not accurately reflect when resilience is being eroded.

Likewise, in information security, organizations using a library with no known vulnerabilities may currently treat their security model as complete and not perform continuous revisions. The issue is that the release of new vulnerabilities or attacker methods is not always well-publicized. Instead, organizations should frequently review their security posture to ensure threat models are not based on past favorable conditions, even if the product does not change. As a recent example, you likely had to update your threat models after the release of [EternalBlue](https://en.wikipedia.org/wiki/EternalBlue) — but it was still privately operational well before disclosure.

In the realm of climate change, moving members of a species that are used to warm areas to intermingle with its kind who live in colder locations can help the cold-adapted population actually survive long-term.[20] Applications built using legacy systems and libraries which have never been exposed to the outside world, which suddenly need exposure to external APIs, tend to fare extremely poorly in security terms.

As mentioned in the example of unprotected coral, the lack of the system’s exposure to the threat over their lifespan has led them to exist in a weakened, unpatched state. Security-wise, you should intermingle your internally-facing systems with your externally-facing systems to ensure they meet the standards of the evolving “global” threat model.

The goal for cities in the face of natural disasters is to maintain a flexible approach in order to properly adapt their response to the changing nature of their risks. If cities do not cultivate a process which assumes uncertainty and surprise in their model, then it’s safe to say they are being wholly unrealistic about the ways of the world.

As defenders, you should test attacker playbooks against yourself to determine how quickly you can adapt to attacker methods. I’m sure many of you wish you could have in-house red teams. For those who do have them, use them to your advantage in this way. I mentioned decision trees earlier as a way to determine which diverse set of controls to use — have your red teams map out the decision trees they created during their course of action to add realistic data into your own trees.

You also must test your ability to absorb the impact of an attack, and minimize the damage. One such test is through failure injection. [Chaos Monkey](https://github.com/Netflix/SimianArmy/wiki/Chaos-Monkey), part of Netflix’s suite of tools called the “Simian Army,” is a service which randomly kills instances in order to test their ability to withstand failure. In fact, Chaos Monkey is described as a resiliency tool.

While it was designed with a performance use case in mind, it can be repurposed for security. If your infrastructure is continually fluctuating, with instances killed at random, it makes it exceptionally difficult for attackers to persist. Attackers would have to conduct whatever they needed within an uncertain time frame. This is, of course, not impossible, but it absolutely raises the attacker’s cost and level of skill required.

Netflix’s goal with Chaos Monkey is to “design a cloud architecture where individual components can fail without affecting the availability of the entire system.”[22] Defenders should make it their goal to design a security architecture where individual controls can fail without affecting the security of the entire system. As I mentioned earlier, if your system becomes completely compromised because a user clicks on a malicious link, you must rethink your security architecture.

Rethinking security architecture is no easy feat. Defenders are considerably hindered in their ability to be adaptive and flexible. Most commonly, people think of organizational pressure as the key deterrent, but I would argue the infosec industry itself is the primary limiter. Defenders face an overwhelming level of complexity and uncertainty due to the sheer number of security vendors and the fragmentation of the solution space.

I believe some of the challenges can be solved by changing the types of infrastructure that are used to promote adaptability and support transformability. Deploying Chaos Monkey is one such example centered on adaptability, but a grander example that blends into transformability is using a container-based ecosystem.

Many of you have likely heard of the container revolution, though may not have used them yourselves. While I’m not a container expert, I’ll explain why containers are a natural fit for evolutionary resilience. Jess Frazelle — “the Keyser Söze of containers”— highlighted in her DevOpsDays talk that containers represent potential salvation from the tradeoff between usability and security.[23] I believe she’s absolutely correct.

As per Microsoft, containers are “a way to wrap up an application in its own isolated box” and are “an isolated, resource-controlled, and portable runtime environment.”[24] A container serves as a layer of abstraction between an application and the host server — which can be of any kind, whether virtualized or bare metal. Because of this, it allows for easier migration to and from underlying infrastructure without having to rebuild applications.

The most common buzzwords I hear for containers are flexibility, portability, and scalability, making them a natural fit for both the adaptability and transformability characteristics. Just as attackers need repeatability and scalability, so do defenders — as well as something that can adapt over time to changes in attacker methods. It cannot be overstated how much a container environment bolsters flexibility and flattens complexity.

When something goes wrong — whether security related or not — the legacy approach makes determining the root cause an effort in untangling and dependency management. With containers, verifiably working systems are available in one neat package, facilitating far less messy remediation. Even implementing them into existing legacy systems can help more easily manage dependencies and licenses.

In the vein of Chaos Monkey, if applications are attacked while running inside a container, all that must be done is kill the container and restart it. There is no need for vulnerability scanning, firewalls, anti-virus, and all the other fragments of the security solution space. You can instead isolate and shut down infected containers as it happens.

You have to ensure adaptability to manage resilience erosion as well. In the case of coral, there are “pulse-type stressors,” or acute stressors, which include tropical cyclones, coral bleaching events, and destructive fishing.[21] But there are also “press-type stressors,” which are stressors occurring over longer periods of time, such as pollution, sedimentation, overfishing, ocean warming, and acidification. With enough of the press-type stressors wearing it down, coral reef resilience is overwhelmed when a pulse-type stressor occurs.

Pulse-type stressors in information security can be thought of as new vulnerabilities or a new data breach. Press-type stressors can include large turnover of employees — particularly ones working on large projects — but I would say the most prevalent is complexity. As you add complexity to your applications and systems, it becomes more difficult to test every possible path to compromise, because the paths begin trending towards infinity. If you can no longer test every path because your system is too complex, you have eroded your resilience, a key part of which is flexibility — and will have neither adaptability or transformability.

***

## Transformability

Transformability can be thought of challenging your existing assumptions and reorganizing your system.

Returning to our previous example of an organization removing inline PHP database queries in favor of a single class, the latter approach also bolsters transformability. Because it is just one library, it allows for easier migration as-needed depending on how the company’s environment, or the threat environment, changes. You are not leaving your options open when your web app is riddled with inline code. You must be able to review and revise your previous choices — for example by moving to new tools or libraries.

Research from other domains has explored the policy implications of transformability, and how to implement the concept on a practical level. Disaster recovery in urban areas is one of the most well-researched domains in this regard. Given urban areas are dynamic systems, evolutionary resilience suggests that policy should encourage recovery efforts that prioritize re-building the urban area into an improved — or even better, optimized — system.[8] For example, in flood-prone areas, the policy should be to change the location and not build in those areas, while also implementing flood-proof construction for periphery areas.

As a tangible example of transformability, let’s explore Christchurch. In 2011, a devastating magnitude 6.3 earthquake hit Christchurch, the second most populous city in New Zealand at the time. It killed 185 people and damaged over 100,000 houses, with a financial cost to rebuild estimated at over $40 billion.

After the quake, the Canterbury Earthquake Recovery Authority (CERA) designated a new “red zone” throughout the area. This red zone includes damaged or vulnerable land where they believe rebuilding would be “prolonged and uneconomic.”[25] The assessment embraces transformability, rejecting the need to return to the status quo, and instead challenging the assumption that there should be buildings on the land at all.

As security professionals, you should work to identify what the red zones are within your IT systems. Organizations should identify which infrastructure or technologies present the most security challenges — whether through vulnerabilities or ongoing maintenance costs — and put them in the red zone for being phased out.

Defining the components of your own red zone calculation will be subjective, but I submit the following as potential criteria — systems that are directly exposed to external attacks, or entirely public facing, in particular:

* Those which expose complex or critical functionality and are accessible publicly
* Newly deployed systems or architectures, particularly those developed by inexperienced professionals
* Legacy systems using outdated libraries, software, or languages
* Systems with no backups, or which can’t easily be restored
* Any system with critical personally identifiable information (PII) or immutable data — such as in Equifax’s case
* Systems with privileged access to other systems or accounts
* Any system that has known or “accepted” risk associated with it
* Easily fingerprintable or overly verbose systems
* Anything that could be deemed a single point of failure for your organization
* Systems that are prohibitive to patch or update

Defining your security red zones isn’t about examining potential vulnerabilities or path to compromise in each of your systems. Instead, you want to identify any assets that fall under the red zone criteria, and attempt to move them out of the zone, into healthier systems.

For example, an organization might have an existing asset built using legacy technology, which now has to be exposed to public APIs. Furthermore, this asset consumes critical data and also has privileged access to backend APIs. This asset should likely be classified as being in the “red zone,” without actually assessing whether or not there are vulnerabilities. The goal is to move or rebuild the asset outside of the red zone and make it a safer system.

In this case, such measures could include:

* Locking down public exposure so that it’s only accessible via VPN
* Rebuilding the asset using newer, non-legacy technologies (such as containers)
* Avoiding storing critical data on this asset and proxy encrypted data further into the architecture’s core
* Introducing security logging and monitoring
* Locking down privileged access and enforcing the principle of least privilege

By implementing all, or at least some, of these, the system would no longer be in the red zone. This would be similar to moving a power plant out of a flood plain, and instead building it in an elevated area with fortified materials and an early warning system.

Using the example of levees, researchers have proposed having planned decommission of levees ahead of known maintenance hurdles. This way, levees can be used as a stop-gap as communities embrace transformability and relocate. It’s unrealistic to assume that a community could uproot overnight, but it’s important that it isn’t treated as a permanent Band-Aid.

In security, it’s similarly unrealistic to assume you can transform overnight — and your organization would probably not be pleased with you. But, you need to be able to migrate. Like levees, you could have planned decommission of retroactive hardening and patching before moving off of legacy systems. This ensures you don’t renew on software or hardware before it becomes too embedded in your organization or costly to maintain.

In general, you should have plans in place to decommission technologies that will eventually be obsolete or replaced, even down to libraries, hashes, and software versions. Continually consider how you can prepare in advance for migration.

Evolutionary resilience research has highlighted the need for more collaborative planning across stakeholders in a complex system. Rather than relying on inferred knowledge towards a pre-defined goal, local groups should work together and compile their own information towards optimizing relevant processes in their system.

Drawing from flood risk management, those in charge of risk management should be the ones to communicate what realistic level of protection each sort of approach provides.[9] Otherwise, it’s difficult for communities to cultivate knowledge on their own of what protection is in place and what limitations remain for risk reduction.

The security function within an organization is also not an isolated unit. Security should foster collaboration across the business towards optimizing security processes. You all should also be open in sharing knowledge of what protections are in place, what risks the protection realistically reduces, what risk remains, and any uncertainties around the approach.

The most obvious group with whom security should partner is engineering, which I discuss further in another keynote, [Security as Product](/posts/security-as-a-product). As is in the aforementioned case of containers, it’s possible that there are improvements engineering desires that might facilitate more adaptable security as well. The trend towards flexibility is perhaps the strongest in software development and engineering today, and security must embrace this trend as well. I highly recommend reading the recently released O’Reilly book on Agile Application Security for more in this vein.[26]

In this collaborative setting, the role of planners should be to manage transitions between states rather than create or mediate.[27] I don’t think security professionals can fully remove the need to create or implement solutions to some extent. Focusing on managing the transition from the current state to a more secure state can potentially reduce some labor burden, however.

For example, drawing again on the transition to containers, the engineering group will conduct the majority of the labor towards this endeavor. Security should manage the project to ensure necessary controls are in place, such as detection of container compromise.

As another example, security ideally should work with engineering to implement solutions like two-factor authentication. John “Four” Flynn at Facebook gave a great talk a few years ago about implementing 2FA at Facebook. Their goal was to put 2FA on SSH to make it hard for attackers to pivot into Facebook’s production environment.[28] During the process, they thought very carefully about the user experience, realizing they needed to support frequent use, allow for a flexible range of factors, and minimize help desk requests.

They decided to use DuoSecurity and YubiKey Nano — with the YubiKey, the developers only needed to touch the side of their laptop to SSH, and DuoSec’s cloud-based tokens ensured they’d still have access even if they lost the YubiKey. One of their key discoveries during this project was that:

> “You can actually implement security controls that affect every single thing people are doing and still make them love it in the process.”

I recognize that while “software is eating the world,” not every company is yet a technology company. Potentially, you will have a limited IT group with whom to collaborate on technical efforts. This doesn’t mean you can’t collaborate, however. It’s well recognized that there is division between even security and risk or fraud groups, let alone general counsel and financial functions. There is someone at your organization who wants their job to be easier. Your job then needs to be how security can make that happen, or at least fit into their existing workflows.

For this sort of transformability to happen, responsive governance systems are needed. Defenders must implement decision-making processes that are quick to identify and respond to emerging threats. Part of this in ensuring that your organization is learning from prior experiences — such as through the decision tree process I mentioned before, in which you can update your models after a breach.

However, your organization’s entire community must be involved in this learning process and be prepared to continually evaluate strategy. Implementing a security culture in your organization is perhaps the best chance of doing so.

***

## Conclusion

This is my humble attempt at a definition of resilience in information security:

> **Resilience in security means a flexible system that can absorb an attack and reorganize around the threat.**

The system, in this case, likely is your organization, although this can apply to its underlying systems as well. Crucially, resilience in security is not the ability to withstand or prevent an attack. That’s the blue pill.

The red pill is that the reality is that attacks will happen to you, and you must architect your security around this fact. I showed you how deep the rabbit hole goes on what security strategy fits this reality. Robustness, adaptability, and transformability are the keys to survival in Wonderland.

**Robustness**, while not the silver bullet, should be optimized through diversity of controls. **Adaptability** seeks to minimize the impact of an attack and keep your options open, and new types of infrastructure, such as containers, can enable it. **Transformability** demands you challenge your assumptions and reorganize your system around the reality — a reality that affects communities, which requires a collaborative effort.

My favorite fictional character growing up was Ian Malcolm, from Michael Crichton’s “Jurassic Park” novels. I believe the full quote of one of his most notable lines summarizes how you, as defenders, should think of your strategy:

> “Because the history of evolution is that life escapes all barriers. Life breaks free. Life expands to new territories. Painfully, perhaps even dangerously. But life finds a way.”[29]

Consider how you can escape barriers, consider how you can expand to new territories, consider how you can find a way to evolve — because attackers are doing all of these things. Doing so will likely be painful at first for your organization. Your job, as part of implementing transformability, is to manage these transitions and minimize the pain and danger. Much like with life, as per Malcolm’s quote, you can think of it as the survival of your organization’s data being at stake.

Attacks will happen. Attackers will continue to evolve their methods. We can evolve our methods, too. We face a choice, as an industry: we can either continue to indulge ourselves in anger, bargaining, and depression, or strive towards acceptance.

If we take this red pill of resilience, we can defend ourselves effectively and realistically. If we take the blue pill, we will keep attempting to rebound to an artificial equilibrium — relegating us to the role of a firefighting cat who is drunk on snake oil.

I am certain most of you are fed up with these dynamics. Instead of accepting snake oil, I encourage you to take the red pill of resilience instead.

***

## References

[1] Alexander, D. E. (2013). Resilience and disaster risk reduction: an etymological journey. Natural hazards and earth system sciences, 13(11), 2707–2716.

[2] Holling, C. S. (1996). Engineering resilience versus ecological resilience. Engineering within ecological constraints, 31(1996), 32.

[3] The American Chestnut Foundation. How Chestnut Blight Devastated the American Chestnut. Retrieved from https://www.acf.org/the-american-chestnut/ (accessed September 2017).

[4] Restemeyer, B., Woltjer, J., & van den Brink, M. (2015). A strategy-based framework for assessing the flood resilience of cities–A Hamburg case study. Planning Theory & Practice, 16(1), 45–62.

[5] Blake, E.S. & Zelinsky, D.A. (2018). National Hurricane Center Tropical Cyclone Report: Hurricane Harvey. National Oceanic and Atmospheric Administration.

[6] Timmermann, P. (1981). Vulnerability, resilience and the collapse of society. Environmental Monograph, 1, 1–42.

[7] Hough, S. E. (2016). Predicting the unpredictable: the tumultuous science of earthquake prediction. Princeton University Press.

[8] Sanchez, A. X., Osmond, P., & van der Heijden, J. (2017). Are some forms of resilience more sustainable than others?. Procedia engineering, 180, 881–889.

[9] Tempels, B. (2016). Flood resilience: a co-evolutionary approach. Residents, spatial developments and flood risk management in the Dender basin.

[10] Burby, R. J. (2006). Hurricane Katrina and the paradoxes of government disaster policy: bringing about wise governmental decisions for hazardous areas. The Annals of the American Academy of Political and Social Science, 604(1), 171–191.

[11] Wenger, C. (2017). The oak or the reed: how resilience theories are translated into disaster management policies. Ecology and Society 22(3):18.

[12] Gunderson, L. (2010). Ecological and Human Community Resilience in Response to Natural Disasters. Ecology and Society 15(2): 18.

[13] Martindale, B., & Osman P. (2007) Why the concerns with levees? They’re safe, right?. IASFM Fall 2007 Newsletter.

[14] Liao, K. H. (2012). A theory on urban resilience to floods — a basis for alternative planning practices. Ecology and Society 17(4): 48.

[15] Côté, I. M., & Darling, E. S. (2010). Rethinking ecosystem resilience in the face of climate change. PLoS biology, 8(7), e1000438.

[16] NYC Mayor’s Office of Recovery and Resiliency. (2018). Climate Resiliency Design Guidelines.

[17] Verton, D. (October 1, 2003). Former @stake CTO Dan Geer on Microsoft report, firing. Retrieved from https://www.computerworld.com/article/2572315/security0/former--stake-cto-dan-geer-on-microsoft-report--firing.html

[18] Dai Zovi, D. Attacker “Math” 101.

[19] Intergovernmental Panel on Climate Change. (2014). Climate Change 2014 Synthesis Report Summary for Policymakers.

[20] Sgro, C. M., Lowe, A. J., & Hoffmann, A. A. (2011). Building evolutionary resilience for conserving biodiversity under climate change. Evolutionary Applications, 4(2), 326–337.

[21] Anthony, K. R., Marshall, P. A., Abdulla, A., Beeden, R., Bergh, C., Black, R., … & Green, A. (2015). Operationalizing resilience for adaptive coral reef management under global environmental change. Global change biology, 21(1), 48–61.

[22] Izrailevsky, Y., & Tseitlin A. (July 18, 2011). The Netflix Simian Army. Retrieved from https://medium.com/netflix-techblog/the-netflix-simian-army-16e57fbab116.

[23] Frazelle, J. (July 27, 2017). A Rant on Usable Security. Retrieved from https://blog.jessfraz.com/post/a-rant-on-usable-security/

[24] Brown, T., et al. Windows Containers. Retrieved from https://docs.microsoft.com/en-us/virtualization/windowscontainers/about/ (accessed October 2017).

[25] Blundell, S. (April 19, 2016). Christchurch’s Game of Zones. Retrieved from https://www.noted.co.nz/currently/social-issues/christchurchs-game-of-zones/

[26] Bell, L., Bird, J., Brunton-Spall, M., Smith, R. (2017). Agile Application Security. O’Reilly Media.

[27] Batty, M. (2013). Complexity and Planning: Systems, Assemblages and Simulations, edited by Gert de Roo, Jean Hillier, and Joris van Wezemael. 2012. Farnham, UK and Burlington, Vermont: Ashgate Publishing. 443+ xviii. Journal of Regional Science, 53(4), 724–727.

[28] Flynn, J. (February 6, 2014). 2FAC: Facebook’s Internal Multi-factor Auth Platform — Security @ Scale 2014. Retrieved from https://www.youtube.com/watch?v=pY4FBGI7bHM

[29] Crichton, M. (1990). Jurassic Park. Random House.