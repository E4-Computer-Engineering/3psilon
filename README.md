# 3psilon
[Polymorphic|Minimalistic|Transactional] Operating System


## Idea

Epsilon (3psilon, or 3os for shorts) want to be an idem-potent container based agnostig GNU/Linux distro and a transactional/immutable platform for large scale clusters, IoT, or embedded devices.


## What problem 3psilon wants to solve

Different GNU/Linux distribution implement different approaches to solve same problems. Migration between different distro always involve OS reinstall and often is not transparent from cluster management.

Immutable and/or minimalistic operating system flavors from different distros are not interoperable and not interchangable. It is not possible to create a mized cluster based on Fedora CoreOS, Ubuntu Core, and SUSE MicroOS (to name a few); at the same time, it is not feasible to migrate from CoreOS to MicroOS without interrupting the cluster service.

Distribution, or specific version, end-of-life could cause the needs to re-engineer the entire production solution (e.g. CentOS 8 path change).

Containers are the building block to address the idempotency capability, but not the only part needed to obtain distro agnostic cluster implementations.


## Architecture

Embedded approach followed by [NanoBSD](https://docs.freebsd.org/en_US.ISO8859-1/articles/nanobsd/index.html)


## Disclaimer
...


## 10,000 feet view
...


## Settings
...


## Building
...


## Running
The code supports multiple mode of operation:


## Feedback / Input / Collaboration
...
