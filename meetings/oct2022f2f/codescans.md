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

### Sonarcloud
* No (working) PR injection
* Good for backlog
* accompanied by IDE plugin for intelliJ
* main egeria repo only 
* Very opinionated 'code smells'
* rules can be customized

### LFX Security
* Uses Snyk scanning engine
* no PR injection
* common reporting across many LF products

## Challenges

* Agree how to use, which, tools
* getting tool use into the process
* tracking progress
