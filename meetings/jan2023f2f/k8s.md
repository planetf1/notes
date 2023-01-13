# Kubernetes

Kubernetes 'todos', ideas, bugs etc are documented in the project board at https://github.com/orgs/odpi/projects/8 . Review/sort

Other things to consider:

## Quarkus

* [Quarkus](https://quarkus.io) - Kubernetes/cloud native java
* Dynamic test environment - running in container
* quicker container startup time - ie for microservices
* option to compile to native (has caveats, may not be quicker)
* Many examples use maven, but [gradle is now supported](https://quarkus.io/guides/gradle-tooling)
* using this in operator experiments

## Operator
* Needs to become more dynamic
* Needs test framework
* needs to be easier to develop
* needs to use APIs
* based on skills in team

### Java operators
- investigating Java based operator using [java operator sdk](https://javaoperatorsdk.io) . Supported by Red Hat.
- Uses [fabric8](https://fabric8.io) for kubernetes client

### Operator functionality

* Model servers (including special governance etc)
* Need to discuss roles - admin (k8s) vs data professional
  * Capabilities?
