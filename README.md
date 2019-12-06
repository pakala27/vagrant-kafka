# Introduction

Ansible provides a simple way to deploy, manage, and configure the Confluent Platform services. This repository provides playbooks and templates to easily spin up a Confluent Platform installation. Specifically this repository:

* Installs Confluent Platform packages
* Starts services using systemd scripts
* Provides configuration options for plaintext, SSL, and SASL_SSL communication amongst the services

The services that can be installed from this repository are:

* ZooKeeper
* Kafka
* Schema Registry
* REST Proxy
* Confluent Control Center
* Kafka Connect (distributed mode)

# Documentation

You can find the documentation for running this playbook at https://docs.confluent.io/current/tutorials/cp-ansible/docs/index.html.


# vagrant

Vagrant facilitates to create, configure and destroy virtual machines on developer laptops. Vagrant cloud contains variety of vboxes and they can be downloaded and used as per the developer requirements.

Git Repository : vagrant-kafka

We can provision the four virtual machines and install the Confluent Kafka and then monitor the cluster using Prometheus.

Provision the Virtauls machines using vagrantfile:

Prerequisite : Vagrant and virtaulbox
#cd vagrant
#vagrant status
#vagrant up


Install and configure Confluent kafka:

Run the below command from another server where ansible is installed and configured password less authentication between Ansible node and Kafka nodes.

#ansible-playbook -i plaintext_hosts.yml plaintext_all.yml




