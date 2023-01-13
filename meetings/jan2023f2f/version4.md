# Version 4

## Overview

Version 4 could include
* Java 17 
* Gradle as default
* Java modules

We may also wish to consider [certs](certmgmt.md)

See [project](https://github.com/orgs/odpi/projects/5)

## Decisions to be made
* Approx timescale for release
* Expectations from overall dev team
* Use of Java Modules
* Tracking

For more detail see below

## Java 17

* Needed due to
 - other dependencies starting to require, such as Spring 6
 - LTS/maint dates
 - improved performance/footprint
 - newer language features
* Available Sep 2021
* Current LTS [dates](https://www.oracle.com/java/technologies/java-se-support-roadmap.html)
* Next LTS version is Java 21 in Sep 2023
* Current build strategy has been to build at future java versions up to the next LTS - so Java 17 issues have already been fixed
* Once we switch we should add a new build for Java 19 (now), 20 (march), 21 (sep)
* Builds already available (see below)
* Deprecations should be reviewed
* Should be able to coexist with code using Java 8/11 language, or written for older JVMs
* container runtime moves to Java 17

### Java 17 changes

* [Java 17 features](https://www.baeldung.com/java-17-new-features)
* [Java 17 deprecations](https://www.baeldung.com/java-17-deprecations)


## Gradle

* gradle becomes the default (for core egeria)
  - but already been running and using gradle builds
* maven build is removed (for core egeria) - don't want to parallel maintain
  - maven only specific build issues are closed
  - makes dependency updates easier - halves the commits
* Will do this across all repos as much as possible except where difficult
  - timelines don't have to match exactly
  - difficult example: egeria-k8s-operator java operator code - requires maven plugins for operator-sdk
* Need to get ALL code owners to validate their components contents & behaviour
* interstitial components are removed - ie where the maven module was only present due to directory structure
  - these can be added if needed, suggest on a case by case basis
* Final cross-check of dependency versions will be done
* Building of light chassis needs checking (PR open)

### IntelliJ note
Disable Dependency checker plugin
see https://youtrack.jetbrains.com/issue/IDEA-304093/IntelliJ-EAP-New-UI-leaks-CPU-in-gradle-task-com.android.tools.idea.gradle.dsl.parser.elements

### Lightweight chassis
-PPadminChassisOnly to build the 'thin' server chassis

## Version 4 build (gradle + java 17)

* [egeria-release-4.0pre](https://github.com/odpi/egeria/tree/egeria-release-4.0pre)
* 22 additional commits (so far)
* regularly rebased on main (not PR/merge until ready to work with dev)
* Containers & maven artifacts being published as '4.0-SNAPSHOT'
  - other projects can test/validate NOW
* New pipelines for v4 (will remove old ones when closer to release)

## Java Modules

Java Modules (JPMS) has been available since Java 9
Modules provide better isolation by requiring more explicit contracts
can form basis of cut down distributions with only required classes 

* [Java 9 modules introduction](https://www.baeldung.com/java-9-modularity)

Consumers do not have to use modules, but we provide info in our java packages to allow them to do so. Most current libraries have at leas some module support.

### Egeria JPMS prototype

* Used intelliJ for initial creation of module definitions
* Manual corrections to module definitions and dependencies
* Had to resolve issues where packages appeared in multiple artifacts (not allowed)
* Needed to inject additional module metadata into our use of some third party libraries
* Not yet addressed test code

#### Module options:
* Declares a NAME
* requires
* requires transitive ((ie our dependents are exposed to consumers))
* exports - makes all public available to anyone
* exports to - restricts access only to the named modules
* uses - declares a service consumer
* provides with - offers an implementation of a service
* open, opens, opens (to) - allows reflection ie access to all public at runtime

#### Services
* [Service example](https://www.infoq.com/articles/java11-aware-service-module/)
* [another one](https://www.oreilly.com/library/view/java-9-modularity/9781491954157/ch04.html)

#### Example build

https://github.com/planetf1/egeria/tree/egeria-release-4.0pre-modules 

- not ready for inclusion
 - refactoring of unique packages
 - need to understand / work with the service/provider definitions and appropriate reflection ie for spring dynamic loading

## Summary
* when to switch/commit to v4
* whether/when to go with modules
* what testing/other considerations





