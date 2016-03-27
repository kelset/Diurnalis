# OrientDB The 2nd Generation of (multimodel) NOSQL

## Speaker: Roberto Franchini

## Date: 10-03-2016

## Conference event: CloudConf 2016

NoSQL claim was to use the right database model for the right domain. Bad news, in most cases a single database model is not enough! In last years NoSQL experienced a huge upward trend, offering new data models (Document, Graph, Key-Value...) to solve problems where old RDBMS failed. Now people who have chosen NoSQL as an architecture component, realize that a single data model (even when richer that relational), is not enough for average needs. In this lecture, we will discuss why graph databases are at the heart of the multi-model revolution  and why we're approaching the end of NoSQL's fragmented ecosystem where customers are forced to use multiple tools in their architectures.

Benefits and compromises of this approach along with real world use cases will also be shared.

### My Actual Notes

First conference in Turin for him, nice!

"Proud to be a developer"

Data is managed differently today: relational DB have been the standard for 45 years... but now, it can't stand the chance with the Big Data flooding.

He showed the map of data right now: <https://451research.com/451-research-data-platform-map>

It's totally different from the kind of data the relational DBs can handle.

_What's wrong with JOIN?_

It' works.

_Isn't enough?_

Not really. JOINs are HUGELY used in DBs: the bigger the DB, the worst are the performances.

_What about graph DBs?_

It is any storage system that provides _index-free adjacency_.

In a graph we have Vertices connected by Edges. We can have multiple Edges connecting two Vertices.

_...but how does a true graph db manage relationships?_

Each element in the graph has its _own immutable Record ID_.

Connections are stored has pointers.

-> So a graph DB creates the relationship _just once_ when the element is created.

In a Graph DB the traversiong time is not affected by the DB size!

This allows for easy management of Complex Relationships.

Soooo... waht's a Multi-Model DBMS?

_picture_

So, what's OrientDB? A Multi-Model DB which allows for polymorphic domain schema.

In a "magical DMBS quadrant", Multi model is where relation complexity and data complexity meet.

It's written in Java, and handles elements as JSON documents.

_demo time_

It is automatically able to scale up over multiple cores, and RAM usage too.

Multiple ways of deployment.

### The speaker bio

[Twitter](https://twitter.com/robfrankie)

Senior Software Engineer @ [OrientDB](http://orientdb.com/)

### The conference description

The big european event on cloud computing and scalability The CloudConf is coming back after the successful 2013, 2014 and 2015 editions. The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSearch...) The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!
