#Evolution of Network Security Monitoring and How to Stay Ahead of the Hacker’s game
###Speaker: Almerindo Graziano (UK)
###Date: 05-03-2015
###Conference event: GrappaHat 2016

The Network Security monitoring (NSM) model was first introduced by Bamm Visscher & Richard Bejtlich in 2002. Nearly 15 years later, NSM has become even more important for organizations while it has evolved to include many more security technologies. In this presentation the author draws on his experience in developing effecting security monitoring controls and processes that have helped organizations to keep up with the hackers’ game and to quickly identify attacks and react to intrusions. This talk highlights the technical complexities and the “fun” in defending and monitoring corporate systems and infrastructures along with practical lessons learned that will help you raise the bar hackers have to pass.

######My Actual Notes

Here we go!
They do Security Awareness (comic).
He'll focus on defense; right now it is mostly reactive (monitoring and then do something).
Monitoring is basically "ok, let's get all these data and collect them into groups (alert, statistical, session, full content)".
But this monitoring starts by an analyst looking at a screen! This can't be a good way to handle security: this way the person will focus on a single alert, restrincting the scope of the investigation to *that* one alert.
This could be risky, I could not see the full picture of the attack I'm facing.

Over the last 2 years there has been an evolution: we moved to a 4 step scenery with Prediction -> Protection -> Detection -> Reaction.
Meaning, in pure Lao Tsu way, we start to study our enemies, and know how and what they are going to attack.
Even if we have a dedicated staff for defensive security, we need to recognize that each member need to *achieve maturiy*: we tend to panic when facing a new thread.
We have to consider the behevioral part of the people involved.

The paradigm seems to be: the best security is given but a large amount of skilled and experienced DIVERSIFIED staff, which use advanced/enterprise level tools.

In military doctrine we can identify two defenses:
* Active Defense
-> limited offensive action... but in cybersecurity it is illegal to fight back, so we identify in this category the tools techniques and processes to affect the interntion, execution and the outcome of a cyber attack.
And being able to identify WHO attacked us.
4 main approaches:
_Deception_ = give a "false" image of the target. (ex. playing with DNS servers adding fake IPs pointing to honeypots)

Honeypots = not much to say about them. We need some work here, since these solutions only works on statistical analysis of attacks.
So it's very easy to detect one and the attacker will simply move on. Moreover each honeypot has its own configuration and alerting... and logging is actually HUGE, and we need to take care of that.

_Annoyance_ = making the attacker work harder to get to me. Example of tool for that: weblabyrinth. We basically detect a scan, and generate a hugh number of fake pages to make a labyrinth and generate noise!
Or having a recursive file system "trap", in order to prevent those sort of scans by killing them right away.

_Baiting and Trapping_ = really helpful to identify the attacker. We know the shit is going to hit the fan, let's be prepared for it.
Some good places for baits: shared folders, email inbox, HTML comments, etc etc. 
We can also use fake credentials! Ex. in Windows there is a command "runas" which generates a fake set of credentials, and make the attacker use those (which exist only in memory) and catch them!
THere are also some tools (Canary) which have triggers on defined actions and send alerts each time those are done. 
This sort of things can be also done to prevent fishing over illegal copies of my website.

_Attribution_ = Usually these attacks are passed over Tor (bad news) but we can still try to get them by exploiting misconfiguration and arrogance.
We can handle this by honeytokens OR social engineering.
Both have pros and cons... but the tools are hit/miss situations since those are not always up-to-date.
For social engineering, Honey Badger is the tool to go. Another one is decloack.

A small trick to go around the legal part of attacking back an attacker, is by using banners! (the one about cookies)
When accepted those install a small applet.

-> T-POT good solution for honeypots, work with docker.
-> Another one MHN (Modern Honey Network) - more research-based. 

Still, we already said that honeypots are not that good.
We ned a NEW/BETTER model, which yes has honeypots BUT also integrates some active defense techniques, and have sooo many less logs.

At Silencsec they are wokring on this (see picture). -> they will release it on github!

ELK stack = Elasticsearch+LogStash+Kibana the triad for log management.

* Passive Defense

######The speaker bio

Almerindo Graziano is the CEO of Silensec, a management consulting, technology services and training company, specialized in information security. Almerindo holds an MSc in Electronic Engineering and a PhD in mobile computer security, both from the University of Naples, Italy. For five years he was also the founder and course Leader for the MSc in Information Systems Security at Sheffield Hallam University, in collaboration with the British Standard Institution (BSI). He has personally authored and delivered a number of training courses from ethical hacking to intrusion detection, along with the first ever ISO27001 Lead Implementer certification course offered by the British Standards Institution worldwide. His areas of expertise include information security standards compliance, IT infrastructure protection, design of SIEM and Log Management systems and development of security monitoring processes for effective and efficient incident response. He also collaborates with the International Telecommunication Union (ITU) for the development of cyberdrill scenarios for national CIRTs in areas such as threat intelligence, hacking techniques and log analysis. He has consulted in formation security for private and government organizations across Europe, Africa and Middle East. As a passionate biker, he is currently planning a motorbike trip around East Africa.

######The conference description

The [Grappa Hat](https://grappahat.net) is a part of the «itinerary gourmand» set of conferences:
Italy, UK, Africa … and more to come!