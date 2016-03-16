#Connecting the Unconnected: IoT made simple
###Speaker: Max Amordeluso
###Date: 10-03-2016
###Conference event: CloudConf 2016

Connecting physical devices to the cloud can enhance the user experience. AWS IoT is a new managed service that enables Internet-connected things (sensors, actuators, devices, and applications) to easily and securely interact with each other and the cloud.
In this session, we will discuss how constrained devices can send data to the cloud and receive commands back to the device. Devices can securely connect using MQTT, HTTP, Websockets protocols  and developers can leverage several features of AWS IoT such as the Rules Engine and Thing Shadows to quickly and easily build a real connected product.

######My Actual Notes

"Madrid Room"
Amazon AWS IoT: how to get started in the new trend around, Internet of Things.

It is cool again to play with hardware.

Why is there so much interest in IoT? Because Smarter Products gets better over time. An example? Sonos.

(picture of improvement over time of IoT)

How did Sonos got the way? SPotify wasn't on the map when they started. Their smart hardware was sending feedback to them!
And that way they knew how to predict where the product would have to go.

But having data to analyze means understanding them, and use the Agile methodology to products.

And this brings in also having a closer relationship with your customer.

Another great example of IoT is the Philips Health Suite which lets patients to live in their houses instead of staying in hospitals.

(picture of AWS architecture)

Basically, there is a gateway at the patient's house which communicate with every other sensor in the house.

_*The product is now the interface.*_

One example of this is Amazon Echo, where communication happens *naturally*. (you speak with it, no need to touch)
People actually thank the device. (and btw it's only a good speaker, everything else is in the Cloud)

The Echo works on a AVS (Alexa Voice Service) on which we can develop via its SDK (there's a contest for whole March!).

But still, we have issues...
- Devices are Hard to Connect, Manage
- Things do not interoperates out of the box
- Low signal to noise Ratio in collected data
- Applications and THings do NOT always match (in the way they speak) -> M2M (machine to machinee, telemetry) // Applications (Web and RESTful)


Veniam (a company) is trying to bring the cloud into moving objects.

--> How to overcome these issues?
We focus on two things: Security and Scalability.

AWS IoT is a service which focus on these.
It provides MQTT + Mutual Auth TLS as a new security protocol.

It keeps a registry of all the devices conncted and allows filtering on the ones you want to work to (via SQL).
Moreover IoT keeps the last known state of the device as a "Device Shadow".

It has an SDK physically implanted in some devices, and we are able to put it in others. (if it runs linux, you should be fine)

This AWS IoT is by default "secure":
- Multi-protocol message fateway
- Elastic Pub/Sub Broker
- Secure by default

Remeber: any advice can be connected to something else.

-- Q&A --

Best IoT: connected Floor.

######The speaker bio

(Twitter)[https://twitter.com/maxamorde]
Head of Solution Architecture (EU) @ (Amazon Web Services)[https://aws.amazon.com/it/]

######The conference description

The big european event on cloud computing and scalability
The Cloud Conf is coming back after the successful 2013, 2014 and 2015 editions.
The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSEarch...)
The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!