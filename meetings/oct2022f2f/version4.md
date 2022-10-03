# Version 4

## Java Version

Java 11
Java 17

* Already build/run tests with Java 17 for egeria core. Most repos only use java 11 except for XTDB, IBM info server which adds Java 16
* Focus on gradle build?
* update language level for v4 
* Java 17 released Sep 2021

###  features

See also https://www.baeldung.com/java-17-new-features

* sealed classes 
* protection of jdk internal classes
* switch - inc. type checking on enumerations
* Records (see below)
* Text blocks
* instanceof (brevity/type check)

### deprecations

Many more deprecations are likely reported with Java 17. We need to sweep these up ready for the next round of Java updates in 2023 - and should start building with Java (current) now ie 19 as of 3 Oct.
* [5369](https://github.com/odpi/egeria-docs/issues/5369) - deprecation warnings


## Java Modularity

* Strict definitions of contract [2377](https://github.com/odpi/egeria/issues/2377
* https://www.baeldung.com/java-9-modularity

* Name – the name of our module
* Dependencies – a list of other modules that this module depends on
* Public Packages – a list of all packages we want accessible from outside the module
* Services Offered – we can provide service implementations that can be consumed by other modules
* Services Consumed – allows the current module to be a consumer of a service
* Reflection Permissions – explicitly allows other classes to use reflection to access the private members of a package
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

## Java records

Could new support for java records replace use of Lombok?
Limited: https://www.baeldung.com/java-record-vs-lombok
