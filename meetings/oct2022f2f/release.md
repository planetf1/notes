# Release


## Release process

### Egeria

Branch
Push new release
update versions on master
update branch on main
test
create images
test charts
push to sonatype
review scan
create release notes
posts announce

Execution not overly complicated

Look for backup to also be able to work through this, and potentially mostly take over the monthly task?
### UIs

project only mostly manage
.. still need to consider integration testing, charts etc

### connectors

Highly variable, with differing levels of focus over time

How do we want to handle?

### charts

### notebooks

### samples

## Dependency management

~1st of every month PRs open with version updates
Apply manually, test, integrate
Usually quick, but sometimes find issues in test

## signing

LF have mechanism to sign artifacts (currently I sign them) which we should move to
this is also a precursor for creating & publishing SBOMs

## Frequency

Every month

Less Often?
* more issues can build up
* more chance of service being needed on prior release
* dependencies getting more out of date - esp security
* But more to talk about

Every 2, 3 months?

Align subcomponents so we can talk about all together?

How to handle release notes

Versioning?
