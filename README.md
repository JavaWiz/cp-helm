### Installing helm chart
```
helm repo add javawizinc https://github.com/JavaWiz/cp-helm-charts/   #<1>
helm repo update    #<2>
helm install cm-helm/cp-helm-charts --name cp --version 0.0.1    #<3>
```
1. Add `javawizinc` helm charts repo
2. Update repo information 
3. Install Confluent Platform with release name `cp` and version `0.0.1` 

### Documentation

[https://helm.sh/](Helm) is an open-source packaging tool that helps you install applications and services on Kubernetes.
Helm uses a packaging format called charts.
Charts are a collection of YAML templates that describe a related set of Kubernetes resources.

This repository provides Helm charts for the following Confluent
Platform services:

* ZooKeeper
* Kafka brokers
* Kafka Connect
* Confluent Schema Registry
* Confluent REST Proxy
* ksqlDB
* Confluent Control Center

### Environment Preparation

We must have a Kubernetes cluster that has Helm configured.

### Install Helm on Kubernetes

Follow the directions to [https://helm.sh/docs/intro/](install and deploy Helm) to the Kubernetes cluster.

View a list of all deployed releases in the local installation.
```
helm init
helm repo update
helm list
```