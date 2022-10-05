# Codescans

We have multiple codescans, applied inconsistency across repositories

* CodeQL
* NexusIQ
* Sonatype Lift
* SonarCloud
* Linux foundation lfxsecurity

We also have features which can/could be run in the build

* Compiler flags - warnings
* SonarLint
* pmd
* owasp (cve)
* errorprone (google)

Tools vary in their capabilities including language

## Objectives

* Understand our dependencies
* Evaluate code coverage
* Produce an SBOM (ultimately)
* Static code analysis to look for bugs/issues

## Tools

### CodeQL

* Supported/owned by github
* static code analysis with PR injection
* 2 levels - error/warnings, info
* 1000s of issues on core egeria

### NexusIQ

* Dependency analysis
* dated

### Sonatype Lift

* Triggered by/injects into PRs
* static analysis & dependency analysis
* enforced as part of publishing maven artifacts
* Very good support / integration
* Some work needed to refine rules & validate results, especially for non-java code

### Sonarcloud

* [ODPI](https://sonarcloud.io/organizations/odpi/projects) & [LFAI](https://sonarcloud.io/organizations/odpi-github/projects)
* No (working) PR injection
* Good for backlog
* accompanied by IDE plugin for intelliJ
* main egeria repo only
* Very opinionated 'code smells'
* rules can be customized
* There are additional projects configured, but they are not defined correctly nor triggered by PRs - so results are not worthwhile

### LFX Security

* Uses Snyk scanning engine
* no PR injection
* common reporting across many LF products
* Configured at [PCC](https://projectadmin.lfx.linuxfoundation.org) under tools/security
* [Public charts](https://security.lfx.linuxfoundation.org/#/a0941000012Y73ZAAS/foundation-details?projectId=a092M00001IV4JtQAL&search=Egeria) showing we have 56.5K open vulnarabilities !
* Also reports on non-inclusive language - see [6907](https://github.com/odpi/egeria/issues/6907)

### Dependabot
* frequency varies by repo, but monthly is max period

### Compiler warnings
* Still compiler warnings ignored

## SBOMs

* SBOMS for egeria [6621](https://github.com/odpi/egeria/issues/6621)

## CII badge/openssf

* [6423](https://github.com/odpi/egeria/issues/6423) silver/gold badge

## Issues

In addition, codeQL & openssf explicitly add observations into the 'security'/issues section on github


* [6803](https://github.com/odpi/egeria/issues/6803) openssf scorecard
* [5329](https://github.com/odpi/egeria/issues/5329) printStackTrace
* [5340](https://github.com/odpi/egeria/issues/4340) passwords in code
* [3969](https://github.com/odpi/egeria/issues/3969) code coverage
* [3414](https://github.com/odpi/egeria/issues/3414) FVTs checking for exceptions
* [1610](https://github.com/odpi/egeria/issues/1610) license list
* [odpi/egeria-docs#394](https://github.com/odpi/egeria-docs/issues/394) - doc LFXSecurity scans



## Challenges

* Agree how to use, which, tools
* getting tool use into the process
* what to we need to do for licensing
* tracking progress
* code coverage?

## Repo list

|Name|SonarCloud|NexusIQ|CodeQL|Sonatype lift|Dependabot|LFXSecurity|
|--|--|--|--|--|--|--|^
|egeria-connector-sas-viya|N|N|Y|Y|Y|Y|
|egeria-connector-hivemetastore|N|N|Y|Y|Y|Y|
|egeria-database-connectors|N|N|Y|Y|Y|Y|
|egeria|Y|Y|Y|Y|Y|Y|
|egeria-docs|N|N|N|N|N|Y|
|egeria-connector-integration-topic-strimzi|N|N|Y|Y|Y|Y|
|egeria-samples-api|N|N|Y|Y|Y|Y|
|egeria-dev-projects|N|N|Y|Y|Y|Y|
|egeria-connector-hadoop-ecosystem|N|N|Y|Y|Y|Y|
|egeria-connector-repository-file-sample|N|N|Y|Y|Y|Y|
|egeria-connector-xtdb|N|N|Y|Y|Y|Y|
|egeria-connector-ibm-information-server|?|?|Y|Y|Y|Y|
|egeria-charts|N|N|N|Y|N|Y|
|egeria-jupyter-notebooks|N|N|N|Y|N|Y|
|egeria-ui|N|N|Y|Y|Y|Y|
|egeria-ui-components|N|N|Y|Y|Y|Y|
|egeria-react-ui|N|N|Y|Y|Y|Y|
|egeria-ui-core|N|N|Y|Y|Y|Y|
|egeria-js-commons|N|N|N|Y|N|Y|
|happi-graph|N|N|N|Y|N|Y|
|egeria-samples|N|N|N|Y|N|Y|
|egeria-connector-integration-event-schema|N|N|Y|Y|N|Y|
|egeria-api-mocks|N|N|N|Y|N|Y|
|egeria-template-newrepo|N|N|Y|Y|Y|Y|
|egeria-palisade|N|N|N|N|N|Y|
|egeria-k8s-operator|N|N|N|Y|Y|Y|
|data-governance|N|N|N|N|N|Y|

Note: this summary should be added to [odpi/egeria-docs#442](* [egeria-docs#169](https://github.com/odpi/egeria-docs/issues/42)
