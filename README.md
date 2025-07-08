# Deploying LLM-D

Writing notes for deploying LLM-D on a fresh ROSA cluster

## Cluster Info

Openshift Version: 4.18

## Setup ROSA cluster

### Setting up the Machine Set

Need to create a GPU machinepools using L40S GPU. This can be done through the ROSA UI.

### Setting up Operators

Install the Kustomize operators inside of the cluster-operators folder.

Can be installed using the following command:

```bash
oc apply -k cluster-operators
```

Or using gitops which is what I recommend.

