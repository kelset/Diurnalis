# Rise of the machine: automate your development

## Speaker: Sven Peters

## Date: 10-03-2016

## Conference event: CloudConf 2016

When we talk about automation in software development, we immediately think of automated builds and deployments.  We may also be using scripts to help make our daily work easier. But this is really just the beginning of the rise of the machines. I show you how leading developers in our industry are using open source and commercial tools for automating  much more: "robots" for monitoring production servers, updating issues, supporting customers, reviewing code, setting up laptops...

### My Actual Notes

_(first an introduction from one of the organizers)_

_Slide and videos will be sent a few days after the event, via email._

Continuous integration and development are a reality today. And he won't talk about these topics.

This talk is about giving us ideas through examples.

Some examples of the rise of the machine are Nest, Roomba, Google's automate car. But we shouldn't trust bots _too much_.

The first bot he found was Agent Charlie. It's a little bot which helps you install and configure a new machine.

5 categories of bots:

```
- Coding Bots
```

Because coding ISN'T just coding.  We should keep the team updated!  The best way to do issue tracking is _smart_commits_, which doesn't rely on a precise tool (so no tool switching). But this robot still needs commands, so at Atlassian they worked on something more.

A big issue is when a branch is created on a failing build - bots can avoid this sort of behavior. To handle it they made a small plugin for BitBucket which suggests reviews when you create a branch to fix an issue. And it also sets a minimum number of approvals before merging.

```
- Test Bots
```

To do smart tests... because over time your code quality gets worse. It's caused by the fact that developers are trying to solve problems.

A bot to avoid this is using Dr. Code. And when you get caught by Dr.Code are entered in the Hall of Shame! **MWHAAHHAHAHAHAH**

Moreover, right now developing is not about code but there are also images etc etc, so we need to be able to also compare those when we get through tests.

Hallelujah is another functional based test, and it manages to detect flanky tests. Once it found it the test code gets moved into quarantine, where devs can go and check.

```
- Ops Bots
```

We are not throwing stuff to the ops guys and not caring about it anymore. They made a feedback bot to accelerate the feedback loop.

This bot goes to identify the deployment configuration and send it to the team: this way we can write our own code. Meaning that the loop is complete!

Moreover, when we are ready for production we need to write Release Notes. And the only way to do it is to go read all the commits! Soooo let's create a bot that reads everything and post them into the Release Nots. Which basically means that we are using Issue Description as Release Notes. This way, there are no surprises and those notes are Human readable.

```
- Service Bot
```

Usually support works by asking for the log file, and scanning it. Having the system knowledge we can identify the problem and fix it. But this stops the dev from his true work.

So let's use a bot: Hercules! It is basically a reader that can suggest fixes. "Well, Fuck, the ROBOT was right!".

```
- Report bots
```

Because reports suck. Let's automate the stand ups: this sort of meeting is inefficient, people tend to talk too long, and you need to setup the meeting and everything.

So they created an actual bot which basically is a timer which buzz when time is over. And another which is a reminder, it plays music.

To fix the location issue of a stand up a bot can be developed to be the interactor of the speaker: the person writes to the bot, then it delivers to them the message.

To avoid reinventing the wheel (and not get trapped into unmaintained GitHub projects) they are currently using the 10% of sprint time to maintain those.

And _PLEASE_ treat your bots well! Keep them clean and updated, and have deployment scripts.

('cause we know someday Skynet will take over)

--Q&A time--

If your team is at least 5-6 people you should start to consider automatic stuff.

### The speaker bio

[Twitter](https://twitter.com/svenpet) Evangelist @ [Atlassian](https://www.atlassian.com/)

### The conference description

The big european event on cloud computing and scalability The CloudConf is coming back after the successful 2013, 2014 and 2015 editions. The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSearch...) The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!
