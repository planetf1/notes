# Certificates

Currently Egeria has self-signed certificates held within the source tree. These are self-signed, and result in validation errors via API or browsers

## Current certificates

* I developed scripts that use open source tools to generate
  - root certificate authority
  - intermediate certificate authority
- certs for each component/layer (ie server chassis, clients, UI etc)

Since the root certificate authority is not trusted (ie default), cert validation will fail unless root cert auth is specified by java parms, or 'installed' as default onto hosting system

Certificates also need to include the HOSTNAME - which is not known until deployment time (other than localhost!)

## Todos
* Ensure user can easily replace certs (docs, configuration)
* add mechanism to dynamically generate certs
* remove all certs from source trees
* ensure cert validation is enabled

