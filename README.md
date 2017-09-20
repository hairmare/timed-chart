# Timed Application

## Introduction

This chart bootstraps a Timed application deployment on a [Kubernetes](https://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Prerequisites

- Kubernetes 1.7+ with Beta APIs enabled
- PV provisioner support in the underlying infrastructure

## Installing the Chart

To install the chart with the release name `my-release` git clone repository and run
following command:

```bash
$ helm install --set ingress.hosts={"test-timed.k8s-dev.sycloud.ch"} --set service.databaseUrl="psql://user:password@host:5432/database"
```

The command deploys Timed on the Kubernetes cluster in the default configuration whereas host is set to ingress.hosts and database is running on databaseUrl.

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```bash
$ helm delete my-release
```

## TODOs

* Integrate Timed Frontend
* Deploy postgres as well
* Migration of database
* creation of default user
* Documentation of configuration options
