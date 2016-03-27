# Building Event-Driven Serverless Applications

## Speaker: Danilo Poccia

## Date: 10-03-2016

## Conference event: CloudConf 2016

We built event-driven user interfaces for decades. What about bringing the same approach to mobile, web, and IoT backend applications? You have to understand how data flows and what is the propagation of changes, using reactive programming techniques. You can focus on the core functionalities to build and the relationships among the resources you use. Your application behaves similarly to a "spreadsheet", where depending resources are updated automatically when something "happens", and is decomposed into scalable microservices without having to manage the infrastructure, The resulting architecture is efficient and cost effective to run on AWS and managing availability, scalability and security becomes part of the implementation itself.

### My Actual Notes

From the first edition of CloudConf 4 years ago a lot changed: they are currently able to build single Functions in the Cloud.

"Event-Driven" is nothing new, all the Front-End stuff is already event driven.

But what about the Backend? Can we use this approach in it?

Having Back End Logic can let multiple kind of devices connected to the server (Browsers, Mobile, IoT, etc).  And most of these interactions will be via API call.

What if Functions are our only API? --> AWS Lambda! It can be done via Synchronous Invocations.

Functions can _Modify Resources_ ! And even the Resources can be attached to Functions (and so Event Driven).

This can be quite useful when working with media files: 3 levels:

_picture_

How do you call Functions from the client? (Since he stated that Functions could be our API) Via the AWS api, or even your own (using classic HTTP verbs).

And, of course, we are (are we?) working on Distributed solutions, so we need to React to the Changes in the Architecture. It is actually possible to preserve Functions Independency from architecture.

_(actual demo!)_

He uses Atom. _Y U NOT SUBLIME BRO?_

You can even select the Environment for the Deployment for a Function as API. That's cool boys. SDK Generators! (mobile)

OH GOSH HE'S USING OPENCV in a Function. That's huge!

### The speaker bio

[Twitter](https://twitter.com/danilop)

Technical Evangelist @ [Amazon Web Services](https://aws.amazon.com/it/)

### The conference description

The big european event on cloud computing and scalability The CloudConf is coming back after the successful 2013, 2014 and 2015 editions. The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSearch...) The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!
