# Infrastructure Management via ACM

This repository includes an *init* objects required to implement an Openshift multi-cluster and multi-environment configuration approach based on Red Hat Advantage Cluster Management (ACM).

In terms of the repo organization, the following list includes the most important information about the different folders:

* chart -> This folder includes an Helm Chart required to configure the Hub instance in order to deploy the respective ArgoCD ApplicationSets and ACM Placements for setting up the Openshift clusters in des, pre and pro environments (Create quotas, network policies, etc)
* init-acm.yaml -> This file includes an ArgoCD Application that configures the Hub instance linking the previous chart

## Prerequisites

It is necessary to keep into account the following prerequisites:

- Openshift 4.18+
- Red Hat Red Hat Advantage Cluster Management (ACM) Installed
- Red Hat GitOps Operator Installed in the Hub and managed clusters

## Setting Up

In order to start working with ACM and define the required minimum ArgoCD applications, execute the following command:

```$bash
oc apply -f init-acm.yaml
```

## Author

Asier Cidon @RedHat