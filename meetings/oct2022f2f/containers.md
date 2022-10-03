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

Recent additions include
* Ensuring connector jars can be downloaded
* improved security (containers, passwords etc
* Separating out the jupyter notebooks into their own github repo

#### lab
* recently changed to jupyter charts downloaded on demand. Master only - sufficient?
* [odpi/egeria-charts#191](https://github.com/odpi/egeria-charts/issues/191) Jupyter self-cert [see here](certificates.md)
* [odpi/egeria-charts#195](https://github.com/odpi/egeria-charts/issues/195) New UI v4
* [odpi/egeria-charts#179](https://github.com/odpi/egeria-charts/issues/179) continual resetting of auto gen password in Jupyter
* [odpi/egeria-charts#126](https://github.com/odpi/egeria-charts/issues/126) ssh between containers (ie copying files, demos)
* What needs adding?

#### base
* [odpi/egeria-charts#195](https://github.com/odpi/egeria-charts/issues/195) Business UI?
* [odpi/egeria-charts#182](https://github.com/odpi/egeria-charts/issues/182) content packs
* [odpi/egeria-charts#133](https://github.com/odpi/egeria-charts/issues/133) Atruvia/IBM suggests to use in real scenario


* fixed configuration
* Some improvements have been submitted to add flexibility

#### cts
* [odpi/egeria#197](https://github.com/odpi/egeria-charts/issues/197) issue getting cts results

#### pts
* not regularly run

#### Note on XTDB
* [odpi/egeria-charts#125](https://github.com/odpi/egeria-charts/issues/125) XTDB in base/lab charts - work with chris

#### Additional helm charts
* Scenario to include postgres or database connector?
* Open lineage
* Apache Atlas (see [here](connectors.md)

#### All charts
* [odpi/egeria-charts#5](https://github.com/odpi/egeria-charts/issues/5) certificate/CA configuration
* [odpi/egeria-charts#166](https://github.com/odpi/egeria-charts/issues/166) Open kafka configuration (ie for event streams)
* [odpi/egeria-charts#166](https://github.com/odpi/egeria-charts/issues/166) Open kafka configuration (ie for event streams)
* [odpi/egeria-charts#104](https://github.com/odpi/egeria-charts/issues/104) health checks 
.. some other minor issues see https://github.com/odpi/egeria-charts/issues?page=1&q=is%3Aissue+is%3Aopen
* [odpi/egeria-docs#392](https://github.com/odpi/egeria-docs/issues/293) - docs on persistence in charts


### Operator
* Go based
* can be built and deployed via CLI
* not in catalog
* Deploys config as-is to server (so endpoints must be correct)
* At point of testing replication/with Crux - helps to validate other production-oriented scenarios
* no specific consumer identified & needs review
* [egeria-k8s-operator#12](https://github.com/odpi/egeria-k8s-operator/issues/12) - publish to marketplace
* [egeria-k8s-operator#18](https://github.com/odpi/egeria-k8s-operator/issues/18) - automated testing




## Issues 

These issues are broader than k8s and apply to other deployment environments, but k8s work tends to draw attention to them, plus provide a useful approach to reproducing, or sharing good/bad patterns

### Scalability/Management
* [6813](https://github.com/odpi/egeria/issues/6813) - kafka - unavailability?
* [5471](https://github.com/odpi/egeria/issues/5471) checking connector status
* [6809](https://github.com/odpi/egeria/issues/6809) review jvm mem
* [6804](https://github.com/odpi/egeria/issues/6804) smaller footprint containers
* [6732](https://github.com/odpi/egeria/issues/6732) image support for more architectures (s390?)
* [6728](https://github.com/odpi/egeria/issues/6728) shutdown hook

* [5918](https://github.com/odpi/egeria/issues/5918) container environment for ui server chassis
* [5912](https://github.com/odpi/egeria/issues/5912) UBI8 image for configure container
* [1070](https://github.com/odpi/egeria/issues/1070) mixed cohort testing
* [229](https://github.com/odpi/egeria/issues/229) out of reach repos
* [egeria-charts#17](https://github.com/odpi/egeria-charts/issues/17) - prometheus
* [egeria-charts#180](https://github.com/odpi/egeria-charts/issues/180) - java heap dump


### Security
* [6005](https://github.com/odpi/egeria/issues/6005) omvs log incomplete
* [5956](https://github.com/odpi/egeria/issues/5956) configure image error checking
* [5955](https://github.com/odpi/egeria/issues/5955) docker tag for latest release
* [5944](https://github.com/odpi/egeria/issues/5944) container metadata

### Development, distribution & tidying up
* [5514](https://github.com/odpi/egeria/issues/5514) performance - use slf4jh message formatter
* [6702](https://github.com/odpi/egeria/issues/6702) egeria parms passed to kafka
* [1734](https://github.com/odpi/egeria/issues/1734) PR build of docker container for testing
* [6340](https://github.com/odpi/egeria/issues/6340) cross egeria container image <- proposal for uber image

## Questions

* What else is needed for production
* What is needed for demos
* What is needed for tutorials
