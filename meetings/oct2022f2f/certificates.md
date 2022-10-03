# Certificates

Currently Egeria has self-signed certificates held within the source tree. These are self-signed, and result in validation errors via API or browsers

## Current approach to certificates

* I developed [scripts](https://github.com/odpi/egeria/tree/master/open-metadata-resources/open-metadata-deployment/certificates) that use open source tools to generate
  - root certificate authority
  - intermediate certificate authority
  - certs for each component/layer (ie server chassis, clients, UI etc)

Since the root certificate authority is not trusted (ie default), certificate validation will fail unless root certificate authority is specified by [java parameters](https://egeria-project.org/guides/admin/omag-server-platform-transport-level-security/?h=tls#certificates-for-the-omag-server-platform), or 'installed' as default onto hosting system

Certificates also need to include the HOSTNAME - which is not known until deployment time (other than localhost!)

## Generating certificates automatically

### Kubernetes cert-manager
* Docs [here](https://cert-manager.io/docs/)
* Can be used in manual k8s deployment, via helm charts, or operator environment
* supports integration with many services like letsencrypt,encrypt, hashicorp vault, venafi
* deploys & updates certificates

### LetsEncrypt
* Docs [here](https://letsencrypt.org/docs/)
* Free!
* Supports cert-manager - example tutorial [here](https://www.thinktecture.com/en/kubernetes/ssl-certificates-with-cert-manager-in-kubernetes/)
* 90 day validity
* Must have real hostnames/network routing (problematic for demo/test/dev)

## Issues

* [6807](https://github.com/odpi/egeria/issues/6807) perm format for truststore (jupyter)
* [6351](https://github.com/odpi/egeria/issues/6351) certs for ui chassis
* [6326](https://github.com/odpi/egeria/issues/6326) self signed certs expired
* [odpi/egeria-charts#171](https://github.com/odpi/egeria-charts/issues/171) Automatically generate certs in charts

## Questions

* How do we handle the developer use case? -> Setup script (gradle task)?
* How do we handle demos with unknown environment -> cert-manager?
* Do we need to one one step further for other production options, or just concentrate on k8s + documentation ?

## Todos
* Ensure user can easily replace certs (docs, configuration) - reviews needed
* add mechanism to dynamically generate certs
* remove all certs from source trees - scripts move to samples/dedicated repo for certificates
* ensure certificate validation is enabled even in notebooks & demos

