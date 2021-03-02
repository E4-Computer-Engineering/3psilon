# 3psilon
[Polymorphic|Minimalistic|Transactional] Operating System (3os)


## Idea
Epsilon (3psilon, or 3os for shorts) want to be an idem-potent container based agnostig GNU/Linux distro and a transactional/immutable platform for large scale clusters, IoT, or generic embedded devices.


## What's the problem
Different GNU/Linux distributions implement different approaches to solve same problems. Migration between different distro always involve OS reinstallation and often is not transparent from cluster management point of view.

Immutable and/or minimalistic oriented operating system flavors from different distros are not interoperable and not interchangable. It is not possible to create a mixed cluster based on [Fedora CoreOS](https://getfedora.org/en/coreos?stream=stable), [openSUSE MicroOS](https://microos.opensuse.org), and [Ubuntu Core](https://ubuntu.com/core) (to name a few in alphabetical order); at the same time, it is not feasible to migrate from CoreOS to MicroOS without interrupting the cluster service.

Distribution (or even a specific version) end-of-life could cause the needs to re-engineer the entire production solution (e.g. CentOS 8 path change).

Even if containers can be identified as the building block to address the idempotency capabilities across GNU/Linux distros, it is not enough to achieve agnostic cluster implementations due to the lifecycle management of the nodes as a critical part of the cluster implementation itself.


## How to solve
An over-structure outside distro drivers (and strategies) is mandatory to avoid lock-in. 3psilon achieeve this goal by following three principles:
1) Normalize
2) Standardize
3) Modularize

### Normalize
Equality release opportunities. [Diskimage-builder](https://docs.openstack.org/diskimage-builder/latest/), a tool for automatically building customized operating-system images, can handle the job to create GNU/Linux images with the exact same characteristics regardless of the distribution they came from.

### Standardize
Rules are the key for interoperability. All the builed GNU/Linux images will have same basic features:
1. Same partitioning and file system strategies
2. Same container functionalities
3. Same kernel capabilities
4. Same service management

### Modularize
Freedom is the foundation of democracy. Multiple choice for every "standard" feature can be selected from a pool of promoted list.

Given a fixed matrix of features can produce multiple GNU/Linux images, based on different distros, but with equal capabilities and functionalities.


## Basic feaures:
1. Dual read-only root for Blue/Green upgrade & rollback
2. Fixed disk layout partitioning
3. Dynamic data handled by LVM at the end of the disk (/etc, /var, /home, etc.)
4. Scripting to handle in-memory and persistent configuration

## Optional features:
* Container engine: Docker, CRI-O, containerd
* Hypervisor: KVM, Xen

## Frequently Asked Questions
**Q:** Why not creating a new distro from a specific one
>The independency from a specific distro fate is one of our mandatory goal. Secondly, what would be the best GNU/Linux distribution?
We want to give the freedom of choice, as well as the ability to change your mind.
