# Testing at Scale with Docker

## Speaker: Emil Stolarsky

## Date: 10-03-2016

## Conference event: CloudConf 2016

It's impossible to iterate quickly on a product without a reliable, responsive CI system. At a certain point, traditional CI providers don't cut it. Last summer, Shopify outgrew its CI solution and was plagued by 20 minute build times, flakiness, and waning trust from developers in CI statuses. Now our new CI builds Shopify in under 5 minutes, 700 times a day, spinning up 30,000 docker containers in the process. This talk will cover the architectural decisions we made and the hard lessons we learned so you can design a similar build system to solve your own needs.

### My Actual Notes

Shopify = ecommerce platform. When he thinks CI he thinks:

- Scheduler
- Compute

In a managed provider you are fully hosted, but you have to share resources with other clients - on the other hand the custom provider which gives the complete customization.

Last year Shopify was using an Hosted provider, but:

- Build times were slow (20+ minutes)
- Flankiness (underprovisioned resources)
- Expensive (pay per month)
- Closed System (couldn't improve build times)

So they wanted to move to something better (ex. build time under 5 min).

99% of scheduling use the same components!  So they found Buildkyt, where instances were:

- AWS Hosted
- Managed with Chef
- Memory bound
- IO Optimizations (RamFS to handle I/O)

So they built their own EC2 autoscaler (Scrooge) (A simple Rails app which polls Buildkyte and understand how much it need to scale).

When Scrooge builds a new instance, it is let run for one full hour, in order to understand the actual usage.

They use Docker in their CI system; one of the best features is the boot up time. Docker allows them to do all the standard stuff ONCE, and then each instance is already cached so the boot up time is way faster.

It also gives them:

- Test isolation
- Distribution
- Canary for Production: Allowing to identify bugs in new Docker versions before rolling them out to production.

They build containers with Locutus (Implements custom docker build API, ran on a single machine in EC2 with standby)

Ruby tests and broswer tests are run on separate containers soooo that's kinda of an issue sometimes. Because it inflates your build time.

BUT Docker apparently created a lot of issues: shipping second provider brought confusion among devs, Docker failures were crippling the success rate.

Soooo they had to find a strategy to react to these behaviours.

They tried two ways, to treat the Infrastructure like a Pet, or like a Cattle.

If you don't build your own CI, you'll find some tradeoff to work with, like build times and such.

Lesson learned: treat your nodes as cattle, commit everything. (and a third one i wasn't able to write down in time)

### The speaker bio

(Twitter)[<https://twitter.com/emilstolarsky>] Production Engineer @ (Shopify)[<https://www.shopify.com/>]

### The conference description

The big european event on cloud computing and scalability The CloudConf is coming back after the successful 2013, 2014 and 2015 editions. The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSearch...) The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!
