# Version 4

## Java Version

Java 11
Java 17

* Already build/run tests with Java 17 for egeria core. Most repos only use java 11 except for XTDB, IBM info server which adds Java 16
* Focus on gradle build?
* update language level for v4 

### work items to look at
* records - may replace some lombok use?
* deprecations

## Java Modularity

Strict definitions of contract [2377](https://github.com/odpi/egeria/issues/2377

## Gradle

* [6854](https://github.com/odpi/egeria/issues/6854) maven vs gradle - how dependencies managed
* [6609](https://github.com/odpi/egeria/issues/6609) gradle catalogues
* [6111](https://github.com/odpi/egeria/issues/6111) multiple slf4j bindings
* [4442](https://github.com/odpi/egeria/issues/4442) publish build artifacts
* [3370](https://github.com/odpi/egeria/issues/3370) overall gradle

Will close remaining maven issues

### Benefits
* faster incremental compilation, caching (seconds vs 10s minutes)
* more precise over dependencies (scope, transitivity, resolution)
* more configurable (ie hive hms work, more assembly work)
* better IDE integration
* ongoing development and support vs maven 

### status
* gradle build already compiles all code & runs FVTs
* definitions need adding to publish artifacts (we already do this for postgres etc)
* refactoring may help simplify build scripts
* need to verify end result is same
* 
## Security

* remove all certs from the source tree
* Everyone will need to take an action to use/gen certs (another full topic)

## Spring

* May fix logback issue [6884](https://github.com/odpi/egeria/issues/6884)
* WebSecurityConfigureAdapter [6848](https://github.com/odpi/egeria/issues/6848) - deprecation
