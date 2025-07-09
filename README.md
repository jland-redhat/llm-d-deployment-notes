# Deploying LLM-D

Writing notes for deploying LLM-D on a fresh ROSA cluster

## Cluster Info

Openshift Version: 4.18

## Setup ROSA cluster

### Setting up the Machine Set

Need to create a GPU machinepools using L40S GPU. This can be done through the ROSA UI.

### Setting up Operators

> [!TIP]
> Referencing this doc https://github.com/rh-aiservices-bu/ocp-gpu-setup

Install the Kustomize operators inside of the cluster-operators folder.
 
Can be installed using the following command:

```bash
oc apply -k cluster-operators
```

Or using gitops which is what I recommend:

```bash
oc apply -f cluster-operators/application.yaml
```

### Install LLM-D

> [!TIP]
> Referencing this doc https://github.com/llm-d/llm-d-deployer/tree/main/quickstart

#### Required Tools 

- yq (mikefarah) – installation
- jq – download & install guide
- git – installation guide
- Helm – quick-start install
- Kustomize – official install docs
- kubectl – Installed and logged in

#### Installing

There is a lot going on here with the install. I want to make a kustomize/helm chart to make this more gitops friendly (and I will) but lets just stick to the quickstart script for now:

https://github.com/llm-d/llm-d-deployer/tree/main/quickstart
