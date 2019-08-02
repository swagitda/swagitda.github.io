---
title: "Choice Architecture for InfoSec Blue Teams"
date: 2017-02-08T16:17:34-04:00
draft: false
toc: false
images:
featured_image: "blog/img/frederic-audet-161331.jpg"
thumbnail: "blog/img/frederic-audet-161331.jpg"
tags:
  - InfoSec
  - Behavioral InfoSec
---
![Image of Darth Jar Jar](/blog/img/frederic-audet-161331.jpg)

I recently spoke at Art into Science: A Conference for Defense, which was an intellectually-stimulating (and delightfully quirky) conference focused on moving towards a professional discipline for defensive infosec. Sadly, I had to rush through the last part of my presentation, so I wanted to do it justice by fleshing out my thoughts here. I’m going to skip through the first two sections of my talk— an introduction to cognitive biases and how they manifest in infosec, then challenges that arise due to the group nature of blue teams — but feel free to [check out the slides here](https://swagitda.com/speaking/Know-Thyself-Kelly-Shortridge-ACoD-2017.pdf).

The last part of the presentation focused on the “what to do about it” — I developed a choice architecture for blue teams in information security. Choice architecture is a term coined by Richard Thaler and Cass Sunstein in their famous book “Nudge,” and means the design of how choices can be presented to people. 

The implication is that it can be designed in a way that impacts decision making, and more specifically in a way that minimizes errors due to cognitive biases. It’s basically a “how do we fix it?” response to the flaws in thinking that behavioral economics exposes (see [my post on Prospect Theory & Information Security](/blog/posts/behavioral-models-infosec-prospect-theory/) for a primer on some of these flaws as they appear in infosec).

I’ll walk you through my proposed choice architecture for how blue teams can develop a decision-making process that is resilient to cognitive biases, or you can just skip to the conclusion for the 6-step guide.

1. [Belief Prompting](#belief-prompting)
2. [Decision Trees](#decision-trees)
3. [Social Tactics](#social-tactics)
4. [Conclusion](#conclusion)


***

## <a name="belief-prompting"></a>Belief Prompting
![Gif of Cher from Clueless thinking](/blog/img/thinking-clueless.gif)*Get your thinky thinky face on*

People have beliefs about their opponents in any confrontation. People also tend to believe their opponents are less rational than they actually are — and often make imprudent decisions as if their opponent is randomly choosing their decisions. A counter to this blunder is asking players for their explicit beliefs about what their opponents will do, known as [**belief prompting**](https://books.google.com/books?id=bMWHDAAAQBAJ&pg=PA132&lpg=PA132&dq=%22belief-prompting%22&source=bl&ots=QsfBOYXBlM&sig=EDB2DND3JdfbnXJG7CJycLQOMjk&hl=en&sa=X&ved=0ahUKEwjlupiu7fTRAhXq5YMKHfzxClgQ6AEIKjAD). Think of it as increasing one’s thinking by an additional step — how will your opponent respond to your move?

What beliefs about adversaries need to be evaluated in information security? I believe the answer is capital, time, equipment and risk aversion. You can also use the kill chain as a guide for the timeline of moves you need to consider. It’s critical to keep in mind that attackers aren’t profligate; as Dino Dai Zovi said, “attackers will take the least cost path through an attack graph from their start node to their goal node.” 

Thus, theorizing probabilities of each type of move is necessary in order to consider weighted risk — for example, your adversary using iOS 0day on one of your employees may have a 1% chance (probably even less) of successfully occurring, so it most likely shouldn’t be the top influence in your decision making.

Some example questions to ask yourself, or when discussing with team members, are:

* Which of our assets will attackers want?
* How does our adversary choose and craft their delivery method?
* What countermeasures does our adversary anticipate?
* How would an attacker bypass our [insert security product / solution / strategy here]?
* How would an attacker respond to our [insert security product / solution / strategy here]?
* What are the cost / resources required for an attacker to make [insert type of offensive move]?
* What is the probability that an attacker will conduct [insert type of offensive move here]?

As an example of where these questions might lead you, here’s a belief prompting process for exfiltration, with defensive moves in blue and offensive moves in orange:

![An example of belief prompting for information security, by Kelly Shortridge](/blog/img/belief-prompting-example.png)

***

## <a name="decision-trees"></a>Decision Trees
![Jared from the show Silicon Valley presenting a SWOT analysis](/blog/img/jared-swot.gif)*I’m basically Jared for the infosec industry*

Creating a decision tree allows for a feedback loop that is invaluable in aiding the decision-making process, particularly in prioritizing strategies. I believe a decision tree model is the most efficient means of solving a few challenges in decision-making, as it:

1. Forces you to belief-prompt and increase your thinking by many additional steps
2. Provides an auditable risk model so you can identify where your assumptions broke down (and thus mitigate the “doubling down” effect and self-justification) in event of a breach — an attempt to remove politics out of security strategy (e.g. favoring a product because you implemented it)
3. Allows for easy refinement as data is generated from incidents
4. Lets you see commonalities between attack trees where certain solutions might counter multiple moves
5. Helps you visualize the hardest path for attackers so you can tune your strategy to force them down that path

In creating the decision tree, you need to map out how attackers will respond to each of your countermeasures and to assign probabilities to the likelihood that they will pursue a certain option, as well as what options defenders have and the probability that these countermeasures will successfully prevent the offensive move.

The decision tree below from my presentation is for illustrative purposes— it covers a criminal group gaining access to a company’s server. It’s based on a Defender-Attacker-Defender model (see [my upcoming talk at Troopers](https://swagitda.com/speaking/Volatile-Memory-Kelly-Shortridge-Troopers-2017.pdf) to go deeper!), with potential countermeasures by defense in blue and potential moves by attackers in gold. 

The left branches in each set of moves represent the lower-cost moves, while the right branches represent the more expensive moves (cost here meaning monetary, human and time capital). For example, “#YOLO” means doing absolutely nothing, while “Privilege Separation” requires doing more than nothing, thus making it the more expensive option.

![An example of a decision tree for information security, by Kelly Shortridge](/blog/img/decision-tree-example.png)

For those who need a walkthrough — if you start with the “Criminal Group” adversary that has just arrived on one of your servers, you can consider a preemptive defensive move being either: implementing privilege separation, which has an guesstimated 60% chance of deterring or thwarting the attacker; or “implementing” the #YOLO strategy of doing nothing, which has a 0% chance of deterring the attacker.

If you decide to implement Privilege Separation, the attacker’s response will either be the lower cost option — to scan for reachable data from their lower-privilege vantage with a guesstimated 50% likelihood of leading the attacker to a valuable box — or they could pursue the more resource-intensive option of throwing a known exploit, which has a guesstimated 50% chance of successfully working.

Following the “hard path,” whereby the attacker chooses using the known known exploit, the defender then contemplates what countermeasures they can put in place to challenge the attacker further. For example, they could implement seccomp, which filters sys calls and has a guesstimated rate of thwarting the known exploits 50% of the time, or they could implement GRSec, which bears the higher cost of being barely usable but blocks basically all known exploits.

If you go down the GRSec path, the attacker’s only option becomes “elite” 0day (meaning 0day that requires certain level of finesse and reliability), which takes significantly more time to craft — and the probability of it being deployed successfully is very low.

I know how y’all can be, so let me emphasize: **the goal is not to quibble over exact probabilities until you can prove who is the better pedant**. It’s meant to be a framework to aid in decision-making by visualizing your belief-prompting and is a starting point from which you can tweak your assumptions as you ingest real-world data.

***

## Social Tactics
![A gif of kittens having a "meeting"](/blog/img/kittens-meeting.gif)*omg it's kittens having a meeting*

I won’t cover the social dynamics of teams here ([check out the presentation](https://swagitda.com/speaking/Know-Thyself-Kelly-Shortridge-ACoD-2017.pdf) to read about it if interested), but belief-prompting vis a vis probability-labeled decision-trees ameliorates team-based biases as well. However, blue team leaders need to consider a few additional tactics to round out their decision-making model — most of which are in the vein of framing, i.e. how choices are presented (see [framing effects](https://en.wikipedia.org/wiki/Framing_effect_%28psychology%29) for more).

First and foremost, leaders shouldn’t state their own views before soliciting feedback, lest it anchor the rest of the team’s opinions. It could lead to the team then guessing, “Ok, what do I think the boss believes?” but hopefully there’s a sufficient culture of respect that there isn’t that sort of paranoia. In that vein, using a decision tree can also serve as a starting point to solicit dissenting feedback — it can be easier to disagree with a probability or label on a tree rather than words coming out of someone’s mouth.

A key challenge for blue teams is how to deter short-termism and overly risky decisions. The nebulousness of costs and benefits of certain strategies or implementing solutions results in uncertainty of blue team members in regards to how their performance is evaluated. Soliciting longer-term views on these decisions, clearly articulating what constitutes success and failure for them, and agreeing on these figures with whomever is the “doer” for the project would alleviate much of this uncertainty. 

The goal is to not pressure team members into agreeing to something just to show off their skill level, or because they fear they will look incompetent if they refuse, but to foster a sense of buy-in to the plan and maintain explicit expectations.

Finally, blue teams can leverage the decision trees when weighing different types of strategies or solution options, by estimating how much of a difference it would make in decreasing the probability of an attack succeeding vs. its cost — including monetary cost as well as personnel cost (having to hire a new person just to manage a product would require a hefty reduction in risk to justify).

***

## Conclusion
Ultimately, the ideal bias-resilient decision making process for blue teams in information security looks something like:

1. State beliefs about your adversaries
2. Model decision trees
3. Create a spectrum of success / failure for each decision
4. Develop a probability / payoff matrix for different decision options (leveraging the decision tree)
5. Prioritize rationality and overall benefit over risk-taking
6. Revisit and refine your decision trees after each incident

I don’t claim to have all the answers, and welcome any and all feedback on how to refine this model of a decision-making model. In the spirit of the Art into Science con, we need to collaborate in order to move the ball forward meaningfully in the philosophy of defense and ultimately give defenders a more auspicious foundation upon which to architect their security strategy.

***
Many thanks to [snare](https://twitter.com/snare?lang=en) for reviewing.