# Repositories

We have many repositories. We should review what we have, consider what repos we need, and how to manage them

## Challenges

* Tracking work - Issues
* Consistency
* Ownership
* Do we need a repo for cross-egeria tracking?

## Inclusive language

We should not use non-inclusive terms. Part of this relates to the naming of the default branch in a repository

See [6907](https://github.com/odpi/egeria/issues/6907)

* Branch rename supported by git
* Updates all PRs
* UI informs end user of few commands to correct local clone

## Issue auto closing

* too annoying?
* So often we end up removing the tag, perhaps manual review better

## templates

* only on egeria, do we need elsewhere
* [6849](https://github.com/odpi/egeria/issues/6849) remove checkboxes from bug/enhancement

## migrations
* open lineage connector
* some issues including [6602](https://github.com/odpi/egeria/issues/6602) dependency issue
* [6299](https://github.com/odpi/egeria/issues/6299) graph repository
* [4096](https://github.com/odpi/egeria/issues/4096) cassandra metadata connector
* Should OMASs be moved?
* Anything else?

## repos
* various repos need cataloguing properly, and some remaining actions from new repo template need completing inc. #6541 (UI)
* [4667](https://github.com/odpi/egeria/issues/4667) mega distribution & streamlining

## General
* Do we need consistency for templates, tages, build -- or just work local?
* See also security scans - [codescans](codescans.md)
* Ensure latest versions of Java being used
* Ensure artifacts are being published correctly
* subgroup for all repository owners?

### Repo list

Are the details below correct?
What needs to change?

|Name|Owner|Artifacts|Release|Build|
|--|--|--|--|--|
|egeria-connector-sas-viya|Chris (SAS)|MC|Y|G|
|egeria-connector-hivemetastore|David|A|N|G|
|egeria-database-connectors|?|MCA|y|G|
|egeria|Mandy/Nigel|MCA|Y|MG|
|egeria-docs|Mandy|Web|N|mkdocs|
|egeria-connector-integration-topic-strimzi|David/Nigel|ACm|N|G|
|egeria-samples-api|Mandy|A|N|G|
|egeria-dev-projects|Mandy||||
|egeria-connector-hadoop-ecosystem|Nigel|MA|y|M|
|egeria-connector-repository-file-sample|David|Am|N|G|
|egeria-connector-xtdb|Chris G|MA|Y|M|
|egeria-connector-ibm-information-server|Ljupcho|MA|y|M|
|egeria-charts|Nigel|charts|Y*|action|
|egeria-jupyter-notebooks|Mandy/Nigel|(git clone)|N||
|egeria-ui|Cezar|A|Y*|npm|
|egeria-ui-components|Cezar||||
|egeria-react-ui|David|AC|Y|npm|
|egeria-ui-core|Cezar||||
|egeria-js-commons|Cezar||||
|happi-graph|Cezar||||
|egeria-samples|Mandy||||
|egeria-connector-integration-event-schema|David/Nigel|ACm|N|G|
|egeria-api-mocks|Cezar||||
|egeria-template-newrepo|Nigel|am|n|G|
|egeria-palisade|?||||
|egeria-k8s-operator|Nigel||N|script|
|data-governance|Mandy||||

Key:
* Artifacts *C*ontainer  *A*ttachment
* Build - *G*radle *M*aven

### Non Egeria repos

We do not touch these repositories - they are used by other teams 

|repo|
|bi-ai|
|OpenDS4All|
|OBAIC|
