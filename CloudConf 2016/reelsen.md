#Awesome Logging Infrastructure using the Elastic Stack
###Speaker: Alexander Reelsen 
###Date: 10-03-2016
###Conference event: CloudConf 2016

The Elastic stack consisting of Elasticsearch, Logstash, Kibana and Beats offers easy-to-use components to ingest, parse, analyze and visualize your data.

In this talk we will focus on the aspect of log files, and in addition to the already known capabilities of the ELK stack new features in Elasticsearch simplifying your logging life and the relatively new Beats and their respective implementations will be covered as well.

######My Actual Notes

We are going to talk about Logging!
Elastic have a bunch of products = ElasticSearch, X-Pack, Kibana, etcetc

Why do we log?
Well, because we must.

BUT *LOGGING IS HARD*.
-> It requires expertise.
-> Access Rights (not everyone may have access to all logs)
-> Unstructured logging (worst nightmare)
-> Semi-Structure Logging (ex. syslog) (still not proper usage)
-> Structured logging (but it's hard to find a common structure and you to know the format of your data)
-> Timestamps (HORRIBLESSSS)
-> Enrichment (and Parsing)
-> Centralization
-> Shipping (how do I get logs from A to B)
-> Visualization (if you can't visualize them properly, you should not log at all)
-> Alerting 
-> Outages (how to handle it?) (you need to test it befor you go live)
-> Peaks (how to sustain them)

Those are "usual" problems... how about we get worse?

MICROSERVICES. Yup, that's it. 
And serverless stuff too.
Really hard to work with those: you are working in the cloud, where do the logs go?

Let's get even worse: short lived services. Ugh.

Lifecycle of a log:
1 creation
2 sthip
3 centralize
4 enrich
5 store
6 analyze
7 visualize
8 archive

for the steps 1-7 the execution times *must* be low.

From an architecture POV, we need some elements:
- shipper (gets data from A to B) (Beats from Elastic Search)

those beats (written on google Go) will go on

- logstach (analyze and visualize) (doesn't store data)
- elastic search 

After which there is Kibana.

(see picture)

And obviously we need to consider Authentication and Encryption, and maybe have some sort of "xternal tool layer" between Beats and Elastic Search to have some sort assurance over outrages.

In the next version of Kibana an "ingest pipeline" feature will be added which will allow to do document enrichement before processing.

So it will be easier than ever to use Apache Logs in Kibana :D

A final summary: they want to have things:
- Ease to use
- Minimal dependencies
- Extensibility
- Flexibility (just pick the products you need)

He suggested a book for ElasticSearch (you can read it online for free)

-- Q&A --

Best practise for auth layer: they have a commercial extension. Or another extension linked in the slides. 

######The speaker bio

(Twitter)[https://twitter.com/spinscale]
Software Engineer @ (Elastic)[https://www.elastic.co/]

######The conference description

The big european event on cloud computing and scalability
The Cloud Conf is coming back after the successful 2013, 2014 and 2015 editions.
The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSEarch...)
The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!