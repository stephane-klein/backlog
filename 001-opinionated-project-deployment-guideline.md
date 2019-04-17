# My opinionated project deployment guideline

Status: Draft / Work in progress

This is my opinionated guideline to deploy one application:

* Follow [The Twelve-Factor App](https://12factor.net/) methodology
* Your applications:
  * [Store your app configuration in the environment variable](https://12factor.net/config)
  * [Write log messages to stdout](https://12factor.net/logs)
  * If you can don't save data directly on file system but use [Object storage system](https://en.wikipedia.org/wiki/Object_storage) like [Minio](https://www.minio.io/) ❤️, [S3](https://en.wikipedia.org/wiki/Amazon_S3)...
  * Provide database upgrade and downgrade migration script, use tools like [migrate](https://github.com/golang-migrate/migrate) ❤️ or [alembic](http://alembic.zzzcomputing.com/en/latest/)
  * Provide demo test data (for development environment)
  * Provide script to anonymize customer private data, like this tool [mysql-anonymize](https://github.com/davedash/mysql-anonymous)
* Use Docker container everywhere
* Strictly separate container build (use CI to build your application Docker images) and container run stages
* Use [Infrastructure as Code](https://en.wikipedia.org/wiki/Infrastructure_as_Code) tools (installation/configuration with Web Console, Ssh… is denied):
  * Try to use [Infrastructure as a service platform](https://en.wikipedia.org/wiki/Infrastructure_as_a_service) like [Scaleway](http://scaleway.com/) ❤️, [DigitalOcean](http://digitalocean.com/), [Vultr](http://vultr.com/), [AWS](https://en.wikipedia.org/wiki/Amazon_Web_Services), [Google Cloud Platform](https://en.wikipedia.org/wiki/Google_Cloud_Platform)
  * Use [Terraform](http://terraform.io/) ❤️ (you can also use [Ansible](https://en.wikipedia.org/wiki/Ansible_(software)), [Puppet](https://en.wikipedia.org/wiki/Puppet_(software))…) to manage your infrastructure
  * Maybe use [Packer](https://www.packer.io/) to directly install pre configured OS (with Docker, [Node exporter](https://github.com/prometheus/node_exporter)…)
  * Use [Ansible](https://en.wikipedia.org/wiki/Ansible_(software)) ❤️, [Puppet](https://en.wikipedia.org/wiki/Puppet_(software)), [Salt](https://en.wikipedia.org/wiki/Salt_(software)), or [Chef](https://en.wikipedia.org/wiki/Chef_(software)) configuration management tool to install and configure your application on your infrastructure
  * Use [DnsControl](https://stackexchange.github.io/dnscontrol/), [Terraform Provider](https://www.terraform.io/docs/providers/index.html) or [Ansible Cloud Modules](http://docs.ansible.com/ansible/latest/list_of_cloud_modules.html) to manage your DNS Configuration
  * Don't store uncrypted secrets in Git, use [GnuPG](https://en.wikipedia.org/wiki/GNU_Privacy_Guard), [git-crypt](https://www.agwa.name/projects/git-crypt/) or better, install and use [HashiCorp Vault](https://www.vaultproject.io/)
* Backup your application data:
  * If your application use PostgreSQL database, configure [Continuous Archiving system for Postgres](https://github.com/wal-e/wal-e)
  * If your application store data on filesystem, you can use [BorgBackup](https://github.com/borgbackup/borg/) to backup your files.
  If you can refactor your application, I suggest you to don't save data directly on file system but use [Object storage system](https://en.wikipedia.org/wiki/Object_storage) like [Minio](https://www.minio.io/), [S3](https://en.wikipedia.org/wiki/Amazon_S3)...
* [Sentry](https://docs.sentry.io/) up with your application to track errors
* Docker log to centralized logging system. I suggest [Fluentd](http://fluentd.org/)/[Fluentbit](http://fluentbit.io/documentation/current/) ❤️ + [Elasticsearch](https://en.wikipedia.org/wiki/Elasticsearch) ❤️ + [Kibana](https://en.wikipedia.org/wiki/Kibana) ❤️ + [Curator](https://github.com/elastic/curator)
* Monitor your servers, I suggest this stack [Prometheus](https://prometheus.io/) ❤️ + [Node exporter](https://github.com/prometheus/node_exporter) ❤️ + [Grafana](https://grafana.com/) ❤️ + [alertmanager](https://prometheus.io/docs/alerting/alertmanager/) ❤️
* Export your app monitoring data to [Prometheus](https://prometheus.io/)
* [Do things that don't scale](http://paulgraham.com/ds.html)
  * First install your application on one server or one server by service. Use simply [docker-compose](https://docs.docker.com/compose/) with [watchtower](https://github.com/v2tec/watchtower) ❤️ (You can read also my document named [« My opinionated microservice deployment guideline »](002-opinionated-microservice-deployment-guideline.md))
  * Next, when you need to scale your service, simply migrate your Docker-compose configuration to [Kubernetes](https://en.wikipedia.org/wiki/Kubernetes) cluster
* Provide script to execute load testing
* [Deploy several environments](https://en.wikipedia.org/wiki/Deployment_environment):
  * Production environment
  * Staging environment
  * Test environemnt
  * If possible, one environement by branch
* Install [Continuous delivery](https://en.wikipedia.org/wiki/Continuous_delivery) system

Ressources:

- [Google Cloud Production Guideline](https://medium.com/google-cloud/production-guideline-9d5d10c8f1e)
