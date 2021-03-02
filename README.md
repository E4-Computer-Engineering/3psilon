# 3psilon
[Polymorphic|Minimalistic|Transactional] Operating System


## Idea
Epsilon (3psilon, or 3os for shorts) want to be an idem-potent container based agnostig GNU/Linux distro and a transactional/immutable platform for large scale clusters, IoT, or embedded devices.


## What's the problem
Different GNU/Linux distributions implement different approaches to solve same problems. Migration between different distro always involve OS reinstall and often is not transparent from cluster management point of view.

Immutable and/or minimalistic operating system flavors from different distros are not interoperable and not interchangable. It is not possible to create a mixed cluster based on [Fedora CoreOS](https://getfedora.org/en/coreos?stream=stable), [openSUSE MicroOS](https://microos.opensuse.org), and [Ubuntu Core](https://ubuntu.com/core) (to name a few in alphabetical order); at the same time, it is not feasible to migrate from CoreOS to MicroOS without interrupting the cluster service.

Distribution, or specific version, end-of-life could cause the needs to re-engineer the entire production solution (e.g. CentOS 8 path change).

Containers are the building block to address the idempotency capability, but not the only part needed to obtain distro agnostic cluster implementations. Lifecycle management of the nodes are a critical part of any cluster implementation.


## How to solve
1) Normalize
2) Standardize
3) Modularize

### Normalize
[Diskimage-builder](https://docs.openstack.org/diskimage-builder/latest/), a tool for automatically building customized operating-system images, can handle the job to create a GNU/Linux image with the exact same characteristics regardless of the distribution they came from.
Embedded approach followed by [NanoBSD](https://docs.freebsd.org/en_US.ISO8859-1/articles/nanobsd/article.html)

### Standardize
All the builed GNU/Linux image will have same basic features:
1) Same partitioning and file system strategies
2) Same container functionalities
3) Same kernel capabilities
4) Same service management

### Modularize

## Disclaimer
...


## 10,000 feet view
...


## Settings
...


## Building
...


## Running
...


## Feedback / Input / Collaboration
...
