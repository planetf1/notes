# Version 4

## Java Version

Java 11
Java 17

* Already build/run tests with Java 17
* Focus on gradle build?
* update language level for v4 

### work items to look at
* records - may replace some lombok use?
* deprecations

## Java Modularity

Strict definitions of contract

## Gradle

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
