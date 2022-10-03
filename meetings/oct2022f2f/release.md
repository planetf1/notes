# Release

We should review our release process and ensure the frequency is appropriate, and that we have enough shared responsibilities distributed knowledge.

## Release process

### Egeria

* Branch
* Push new release
* update versions on master
* update branch on main
* test
* create images
* test charts
* push to sonatype
* review scan
* create release notes
* posts announce

Execution not overly complicated, Currently takes 1-2 days elapsed if no significant issues come up

ESSENTIAL to get a backup for this to address
* workload/priorities
* unavailability

### UIs

Need to co-ordinate release of UI with core egeria -- a separate release lifecycle may make sense, but needs co-ordination, understanding of compatible versions, and understanding  integration testing, charts etc


### connectors

Highly variable, with differing levels of focus over time
How do we want to handle? release? testing?

### charts

There is no branch for the charts repo. versions are linearly incremented

### notebooks

Currently there is no versioning beyond git commits

### samples

These should be updated when a release comes out, we may not be doing this quick enough. How can we make more efficient?

## Dependency management

In addition to the release, every month:
* ~1st of every month PRs open with version updates
* Apply manually, test, integrate
* Usually quick, but sometimes find issues in test
* If issue cannot be fixed promptly, we open up an issue

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

## release notes

Need more detail?
simpler formatting?
Auto-generated PR list? Can use tags to separate?
easier to offer 'impact' with less frequent releases

Versioning of docs?

## Tracking candidate items
Use of 'projects' (across repos) or milestones?
For every issue, or just longer line items?
tagging of issues/PRs for consistency

## Issues
* [6332](https://github.com/odpi/egeria/issues/6332) - signing of artifacts by LF

## Other build issues
[5472](https://github.com/odpi/egeria/issues/5472) generation of openapi spec documents
[5463](https://github.com/odpi/egeria/issues/5463) Build logs - so much text
[5363](https://github.com/odpi/egeria/issues/5363) deprecation
[5290](https://github.com/odpi/egeria/issues/5290) publishing of artifacts to improve debug
[5089](https://github.com/odpi/egeria/issues/5089) - openAPI doc is poorly formatted
[4906](https://github.com/odpi/egeria/issues/4906) - publish test results & improve
[4662](https://github.com/odpi/egeria/issues/4662) - old code that doesn't work (glossary canonical model)
[3034](https://github.com/odpi/egeria/issues/3034) release outline
[2168](https://github.com/odpi/egeria/issues/2168) use of spring in non spring modules
[940](https://github.com/odpi/egeria/issues/940) metadata in jars
[931](https://github.com/odpi/egeria/issues/931) git version over API
