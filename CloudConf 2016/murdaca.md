# Docker: Advanced Features

## Speaker: Antonio Murdaca

## Date: 10-03-2016

## Conference event: CloudConf 2016

Behind docker run, we'll go through Docker's advanced features such as user namespaces, plugins, logging drivers, security profiles and networking.

### My Actual Notes

_Some more Docker sweetness for ME :D_

He's not going to talk about 'docker run' and 'container orchestration'.

He'll dive deep into Docker:

- User Namespaces

A kernel feature, which will be out _tomorrow_. Basically, it want to avoid that processes inside a container as root (since mostly it goes like that). Daemon option: --users-remap=default, and it is possible to remap the UID of ROOT in order to avoid that, when something goes wrong and a process escapes its docker, the UID outside is not root. But it's not that good since there are some issues (ex. no containers with --privileged, not per container, lack of filesystem support)

- Plugins

A generic plugin API, regarding Volumes, Network, Authorization, Authentication. Link: <https://github.com/docker/go-plugins-helpers>

- Logging Drivers

Journald should be the best one to use, which allows container's logging directly into the journal.

- Security Profiles

Seccomp (filter every system call happening, and using policies to decide which ones to allow -- apparently by passing a .json) AppArmor () There are a lot os syscalls in linux so this is one way to make Docker more secure.

- SeLinux

He's assuring that it will work properly; it's one of the best security features in Linux. And he's asking not to disable it. Can't be used with the User Namespaces feature, one or the other.

### The speaker bio

runcom@redhat.com

[Twitter](https://twitter.com/runc0m)

Associate Software Engineer @ [RedHat](http://www.redhat.com/en) (Docker Core maintainer)

### The conference description

The big european event on cloud computing and scalability The CloudConf is coming back after the successful 2013, 2014 and 2015 editions. The goal is always the same: make a great day full of networking and technical speeches about cloud computing, involving (as in the past) great companies and speakers (in the previous editions: AWS, Zend Technologies, OpenStack, OrientDB, Redis, Cloud9 IDE, Spotify, ElasticSearch...) The CloudConf is suited for developers, devOps, startups e IT managers, and it will be hosted in Turin, a fantastic and dynamic italian city. Don't miss it!
