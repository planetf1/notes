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

## Questions

* What else is needed for production
* What is needed for demos
* What is needed for tutorials
