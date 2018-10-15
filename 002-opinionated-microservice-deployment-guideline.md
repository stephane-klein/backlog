# My opinionated microservice deployment guideline

## Context

Following this [Tweet](https://twitter.com/amicel/status/1009326802106552320):

> I’m wondering, if Kubernetes is the solution to the complexity we introduced
> by using microservices, then 1/ what is the solution to the complexity
> introduced by using Kubernetes? and 2/ why are we using microservices
> anyway?

This document complete my previous [« My opinionated project deployment guideline »](001-opinionated-project-deployment-guideline.md) document.

Note:

* between 2016 and 2018:
  * I have deployed and managed one On-premises Kubernetes cluster (on baremetal servers)
  * I have depolyed and managed one microservice app on this Kubernetes cluster
  * I have depolyed and managed several monolithic apps on this Kubernetes cluster

## Guideline

**First step**

* deploy your app with [docker-compose](https://docs.docker.com/compose/) (Follow [The Twelve-Factor App](https://12factor.net/) methodology)
* configure monitoring, instrumentation services:
  * [Prometheus](https://prometheus.io/)
  * [Sentry](https://sentry.io)
  * …

**Second step**

* Configure Automatically update running Docker containers with [watchtower](https://github.com/v2tec/watchtower).
* Configure your CI to automatically push your stable Docker Image to your private Docker Registry

Then when you merge to your Git stable branch your application will be automatically deployed.

**Third step**

Deploy your microservice app on [Kubernetes](https://kubernetes.io/) only if:

* you master the first and second steps
* and your app need scalability


**fourth step**

* Deploy [Envoy](https://www.envoyproxy.io/) / [Istio](https://istio.io/) on your Kubernetes Cluster

## My advice

Don't try to directly go to fourth step before masterize previous steps.
