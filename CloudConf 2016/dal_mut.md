# The Road to the Cloud: Continuous Delivery and Deployment

## Speaker: Walter del Mut

## Date: 10-03-2016

## Conference event: CloudConf 2016

The final rush to the perfect development. Connect your local development to cloud services  with continuous delivery services and techniques in order to reduce time to market and engage application availability. Tools and strategies over different cloud providers and pay as you go models.

### My Actual Notes

Last pitch of the event!

Starting with the Rocco's quote is the best opening ever.

He started working with "the Cloud" in 2009.

Focal points for a cloud:

- Pay only for what you use
- Everything is addressable with an API

With Cloud Computing, with the pay for what you use paradigm, a lost of Startups were able to sustain costs.

Serverless is a new step in this direction, making us pay _exactly_ for what we use.

The experience he made with autoscaling showed a **NEW issue**: how to manage/deploy these instanced?

They switched to continuous development: they decided to use Fabric to deploy application artifacts.

At this point, they were able to:

- Deploy one instance at a time
- Deploy concurrently to all of them

**NEW issue**: how to deploy the current running version to new instances?

But the deploy wasn't yet simple.

So they moved to Jenkins to continuous deploy; its delivery flow was quite automagical. (the build was triggered on a git push, Jenkins is responsible to run the test suite, etc etc)

Now Jenkins also works with Docker, and also with CircleCI, CodeShip, etc etc

AWS CodeDeploy is truly interesting, thanks to the concept of deployment groups. (it uses an agent to orchestrate the deploy)

_demo code of how to implement it_

The most interesting part of CodeDeploy are the hooks, which are basically triggers to which methods can be linked. (ex. the application stops)

Jenkins can also be integrated into the AWS CodePipeline. (for more complex cases)

### The speaker bio

walter.dalmut@corley.it  

[Twitter](https://twitter.com/walterdalmut)

Solution Architect @ [Corley Cloud](https://www.corleycloud.com/)

### The conference description

The big european event on cloud computing and scalability The CloudConf is coming back after the successful 2013, 2014 and 2015 editions. The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSearch...) The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!
