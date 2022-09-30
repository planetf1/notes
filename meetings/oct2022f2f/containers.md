# Containers & Kubernetes 

## Containers

* Egeria
* Jupyter - had hoped to remove, but some issues with permissions in loading from github has left us with an image
* configure - should replace with generic image
* UIs - should be to UBI8 for security
* Postgres, SAS connectors - include connector with Egeria - not needed?

## Kubernetes

### Helm Charts

### Current
#### lab
* recently changed to jupyter charts downloaded on demand
* using self-cert - issues with UI?
* What needs adding?
#### base
* does not include business UI
* fixed configuration
* Some improvements have been submitted to add flexibility
#### cts
* issue getting cts results
#### pts
* not regularly run

#### Note on XTDB
* will work with Chris to use in lab/base

### Operator
* Go based
* can be built and deployed via CLI
* not in catalog
* Deploys config as-is to server (so endpoints must be correct)
* At point of testing replication/with Crux

## Scalability/Management
* #6813 - kafka - unavailability?
* #5471 checking connector status
* #6809 review jvm mem
* #6804 smaller footprint containers
* #6732 image support for more architectures
* #6728 shutdown hook
* #6702 egeria parms passed to kafka
* #6340 cross egeria container image <- proposal for uber image
* #6005 omvs log incomplete
* #5956 configure image error checking
* #5955 docker tag for latest release
* #5944 container metadata
* #5918 container environment for ui server chassis
* #5912 UBI8 image for configure container
* #5514 performance - use slf4jh message formatter #5514
* #1734 PR build of docker container for testing
* #1070 mixed cohort testing
* #229 out of reach repos
## Questions

* What else is needed for production
* What is needed for demos
* What is needed for tutorials
