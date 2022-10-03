# Version 4

## Objective

To define the timescale and potential candidate items for Egeria Release 4

The top items include
* Java
* Gradle
* Certificates

## Java Version

Switching to the current level of Java 
 - maintains currency
 - enables use of new Spring version
 - offers performance and language improvements

### Java 11
* Current LTS
* Used by default for all our java repositories

### Java 17

* Already build/run tests with Java 17 for egeria core. 
* Most other repos only use java 11 except for XTDB, IBM info server which adds Java 16
* Java 17 released Sep 2021

### Features of Java 17

See also https://www.baeldung.com/java-17-new-features

updated language level for v4:
* sealed classes 
* protection of jdk internal classes
* switch - inc. type checking on enumerations
* Records (see below)
* Text blocks
* instanceof (brevity/type check)

### deprecations in Java 17

Many more deprecations are likely reported with Java 17. We need to sweep these up ready for the next round of Java updates in 2023 - and should start building with Java (current) now ie 19 as of 3 Oct.
* [5369](https://github.com/odpi/egeria-docs/issues/5369) - deprecation warnings

###  Java records

Could new support for java records replace use of Lombok?
Limited: https://www.baeldung.com/java-record-vs-lombok

### Building with current Java
* Egeria builds up to & including Java 18
* Currently fails at java 19

## Java Modularity

* Added in Java 9 - so in 11 LTS, but not currently used - does not require 17
* Strict definitions of contract [2377](https://github.com/odpi/egeria/issues/2377
* https://www.baeldung.com/java-9-modularity
* Name – the name of our module
* Dependencies – a list of other modules that this module depends on
* Public Packages – a list of all packages we want accessible from outside the module
* Services Offered – we can provide service implementations that can be consumed by other modules
* Services Consumed – allows the current module to be a consumer of a service
* Reflection Permissions – explicitly allows other classes to use reflection to access the private members of a package

## Gradle

Gradle offers immensely quicker incremental building, and is also more actively developed with more flexible capabilities. It is already in use within many Egeria repositories

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

### Issues

* [6854](https://github.com/odpi/egeria/issues/6854) maven vs gradle - how dependencies managed
* [6609](https://github.com/odpi/egeria/issues/6609) gradle catalogues
* [6111](https://github.com/odpi/egeria/issues/6111) multiple slf4j bindings
* [4442](https://github.com/odpi/egeria/issues/4442) publish build artifacts
* [3370](https://github.com/odpi/egeria/issues/3370) overall gradle

Would close remaining maven issues

## Security

We should simplify our approach to certificates. These are required at deploy time and we need to both document & make it easy to get the right certificates in place. Any constructs we provide such as demos, tutorials should show best practice.

See also [certificates](certificates.md))
* remove all certs from the source tree
* Everyone will need to take an action to use/gen certs (another full topic)

## Spring

Move to spring version 6

* Overview https://www.baeldung.com/spring-boot-3-spring-6-new
* May fix logback issue [6884](https://github.com/odpi/egeria/issues/6884)
* WebSecurityConfigureAdapter [6848](https://github.com/odpi/egeria/issues/6848) - deprecation

## Slimline chassis

* Chassis can be build 'slimline' by default
* Add more docs on this
* deploy slim by default
* adapt charts etc to use slim version
