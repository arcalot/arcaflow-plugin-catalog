# Arcaflow Plugin Catalog

> [!WARNING]
> This catalog is currently manually maintained and is not expected to be up-to-date.

Arcaflow plugins that are officially maintained by the community are in individual
repositories in the Arcalot GitHub organization. The plugin repository names should
always begin with the prefix *arcaflow-plugin-*, so the current list of plugins is
generally searchable in the repos list with [*in:name
arcaflow-plugin-*](https://github.com/orgs/arcalot/repositories?q=in%3Aname+arcaflow-plugin-).

> [!NOTE]
> There are a few supporting repositories that also begin with the *arcaflow-plugin-*
> prefix that are **not** plugins, such as [this
> repository](https://github.com/arcalot/arcaflow-plugin-catalog) and
> [arcaflow-plugin-sdk-python](https://github.com/arcalot/arcaflow-plugin-sdk-python).

## Plugin Containers

The [Arcaflow Container Toolkit
(ACT)](https://github.com/arcalot/arcaflow-container-toolkit) is used in GitHub CI
automations to auto-build multi-architecture plugin containers and upload them to the
public [Quay cotainer repository](https://quay.io/organization/arcalot). In general, the
`:latest` tag should point to the latest released version of the plugin container, and
the `:main_latest` tag should point to the latest container build from the main branch
of the plugin. Development builds are also auto-created by ACT, with tags that include
the development branch name and commit hash, such as `:simplify-schema_be4f338`.

## Catalog

### Maintained and Supported Plugins

These plugins are considered actively-maintained and have full CI automation to build
containers and push them to the Quay image repository. Issue reports are monitored, and
plugins are maintained for compatibility and updates of dependencies.

| Plugin | Description | Support Status | Latest Version | Container Path |
| :----- | :---------- | :------------: | :------------: | :------------- |
| [arcaflow-plugin-coremark-pro](https://github.com/arcalot/arcaflow-plugin-coremark-pro) | Runs the CoreMark®-PRO certify-all workloads and returns the results in a machine-readable format | active | 0.1.3 | [quay.io/arcalot/arcaflow-plugin-coremark-pro:0.1.3](quay.io/arcalot/arcaflow-plugin-coremark-pro:0.1.3) |
| [arcaflow-plugin-example](https://github.com/arcalot/arcaflow-plugin-example) | Says hello :) | active | 0.5.1 | [quay.io/arcalot/arcaflow-plugin-example:0.5.1](quay.io/arcalot/arcaflow-plugin-elasticsearcho:0.5.1) |
| [arcaflow-plugin-fio](https://github.com/arcalot/arcaflow-plugin-fio) | Executes the fio workload with a given input schema defined in a yaml file | active | 0.4.0 | [quay.io/arcalot/arcaflow-plugin-fio:0.4.0](quay.io/arcalot/arcaflow-plugin-fio:0.4.0) |
| [arcaflow-plugin-horreum-client](https://github.com/arcalot/arcaflow-plugin-horreum-client) | Uploads a structured payload to a Horreum server | active | 0.2.0 | [quay.io/arcalot/arcaflow-plugin-horreum-client:0.2.0](quay.io/arcalot/arcaflow-plugin-horreum-client:0.2.0) |
| [arcaflow-plugin-kubeconfig](https://github.com/arcalot/arcaflow-plugin-kubeconfig) | used to input a kubernetes or openshift kubeconfig file and parse and extract components of the kubeconfig file such as cluster name, user, server url, client certificate, client token etc. | active | 0.3.2 | [quay.io/arcalot/arcaflow-plugin-kubeconfig:0.3.2](quay.io/arcalot/arcaflow-plugin-kubeconfig:0.3.2) |
| [arcaflow-plugin-metadata](https://github.com/arcalot/arcaflow-plugin-metadata) | Collects all data from ansible-facts and outputs it | active | 0.5.1 | [quay.io/arcalot/arcaflow-plugin-metadata:0.5.1](quay.io/arcalot/arcaflow-plugin-metadata:0.5.1) |
| [arcaflow-plugin-opensearch](https://github.com/arcalot/arcaflow-plugin-opensearch) | Load data into an OpenSearch-compatible instance | active | 0.3.0 | [quay.io/arcalot/arcaflow-plugin-opensearch:0.3.0](quay.io/arcalot/arcaflow-plugin-opensearch:0.3.0) |
| [arcaflow-plugin-pcp](https://github.com/arcalot/arcaflow-plugin-pcp) | Runs PCP pmlogger, collects data until cancelled, and then generates a structured output of the results | active | 0.10.1 | [quay.io/arcalot/arcaflow-plugin-pcp:0.10.1](quay.io/arcalot/arcaflow-plugin-pcp:0.10.1) |
| [arcaflow-plugin-rtla](https://github.com/arcalot/arcaflow-plugin-rtla) | Runs the rtla timerlat hist tool to collect CPU latency data from the target system and then generates a structured output of the results | active | 0.1.0 | [quay.io/arcalot/arcaflow-plugin-rtla:0.1.0](quay.io/arcalot/arcaflow-plugin-rtla:0.1.0) |
| [arcaflow-plugin-stressng](https://github.com/arcalot/arcaflow-plugin-stressng) | Provides the functionality of stress-ng with various stressors | active | 0.8.1 | [quay.io/arcalot/arcaflow-plugin-stressng:0.8.1](quay.io/arcalot/arcaflow-plugin-stressng:0.8.1) |
| [arcaflow-plugin-sysbench](https://github.com/arcalot/arcaflow-plugin-sysbench) | Workload plugin of the sysbench benchmark tool | active | 0.7.1 | [quay.io/arcalot/arcaflow-plugin-sysbench:0.7.1](quay.io/arcalot/arcaflow-plugin-sysbench:0.7.1) |
| [arcaflow-plugin-template-python](https://github.com/arcalot/arcaflow-plugin-template-python) | Serves as a template from which new plugins can be built | active | 0.4.0 | [quay.io/arcalot/arcaflow-plugin-template-python:0.4.0](quay.io/arcalot/arcaflow-plugin-template-python:0.4.0) |
| [arcaflow-plugin-uperf](https://github.com/arcalot/arcaflow-plugin-uperf) | Handles all components of uperf to run the given benchmark profile | active | 0.5.0 | [quay.io/arcalot/arcaflow-plugin-uperf:0.5.0](quay.io/arcalot/arcaflow-plugin-uperf:0.5.0) |
| [arcaflow-plugin-utilities](https://github.com/arcalot/arcaflow-plugin-utilities) | Used to store common utility functions used by various plugins/workflows. Where each step of the plugin corresponds to a different utility functionality. Refer to individual step functions in arcaflow_plugin_utilities.py to see what input is expected for each step. | active | 0.7.0 | [quay.io/arcalot/arcaflow-plugin-utilities:0.7.0](quay.io/arcalot/arcaflow-plugin-utilities:0.7.0) |

### In-Development Plugins

These plugins may be in various states of development, with or without CI automation in
place. Please see the individual plugin repos for details.

| Plugin | Description | Support Status | Latest Version | Container Path |
| :----- | :---------- | :------------: | :------------: | :------------- |
| None | ||||
### Archived Plugins

These plugins have been archived, and as a result are effectively frozen at their last
development and release state at the time of archive. The plugins are not maintained,
but the released container builds should remain avalable in the Quay image repository.

> [!WARNING]
> It is not recommended to use these plugins. They remain available for reference and to
> ensure existing workflows are not broken. If you would like to see an archived plugin
> moved back into a maintained state, please open an issue on the plugin or reach out to
> the Arcalot community.

| Plugin | Description | Support Status | Latest Version | Container Path |
| :----- | :---------- | :------------: | :------------: | :------------- |
| [arcaflow-plugin-elasticsearch](https://github.com/arcalot/arcaflow-plugin-elasticsearch) | A plugin for loading data into an Elasticsearch instance | archived | 0.1.0 | [quay.io/arcalot/arcaflow-plugin-elasticsearch:0.1.0](quay.io/arcalot/arcaflow-plugin-elasticsearch:0.1.0) |
| [arcaflow-plugin-instructlab](https://github.com/arcalot/arcaflow-plugin-instructlab) |  Run instructlab standalone, or as a part of a workflow | archived | N/A | N/A |
| [arcaflow-plugin-iperf3](https://github.com/arcalot/arcaflow-plugin-iperf3) | iperf3 server and client plugin | archived | 0.3.0 | [quay.io/arcalot/arcaflow-plugin-iperf3:0.3.0](quay.io/arcalot/arcaflow-plugin-iperf3:0.3.0) |
| [arcaflow-plugin-minio](https://github.com/arcalot/arcaflow-plugin-minio) | Creates an ephemeral object store that can be used during the operation of a workflow. A single arca-bucket storage bucket is created, and the plugin returns in its output object the required credentials for accessing the bucket. | archived | 0.2.0 | [quay.io/arcalot/arcaflow-plugin-minio:0.2.0](quay.io/arcalot/arcaflow-plugin-minio:0.2.0) |
| [arcaflow-plugin-service](https://github.com/arcalot/arcaflow-plugin-service) | creates a Kubernetes service for the given specification | archived | 0.2.1 | [quay.io/arcalot/arcaflow-plugin-service:0.2.1](quay.io/arcalot/arcaflow-plugin-service:0.2.1) |
| [arcaflow-plugin-smallfile](https://github.com/arcalot/arcaflow-plugin-smallfile) | A workload plugin of the smallfile benchmark tool | archived | 0.2.0 | [quay.io/arcalot/arcaflow-plugin-smallfile:0.2.0](quay.io/arcalot/arcaflow-plugin-smallfile:0.2.0) |
| [arcaflow-plugin-wait](https://github.com/arcalot/arcaflow-plugin-wait) | Introduces a pause during workflow execution *(Use the `wait` step of [arcaflow-plugin-utilities](https://github.com/arcalot/arcaflow-plugin-utilities) instead)* | archived | 0.2.0 | [quay.io/arcalot/arcaflow-plugin-wait:0.2.0](quay.io/arcalot/arcaflow-plugin-wait:0.2.0) |
| [arcaflow-plugin-aws-ec2-control](https://github.com/arcalot/arcaflow-plugin-aws-ec2-control) | Runs AWS EC2 actions | archived | N/A | [quay.io/arcalot/arcaflow-plugin-aws-ec2-control:latest](quay.io/arcalot/arcaflow-plugin-aws-ec2-control:latest) |
