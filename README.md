# blackknight
Unmanned setup for deploy of k8s through minikube/minishift

## Introduction
The project came to light through the need to prepare hosts for testing
[ripsaw](https://raw.githubusercontent.com/cloud-bulldozer/ripsaw).

blackknight holds a set of ansible playbooks that can be used to setup a fedora
baremetal host to run minikube/minishift.

## Setup a host
To setup a host for running minikube or minishift

### Requirements
* Please make sure that the target hosts have fedora installed, preferably 29.
* Ensure that root access is provided
* python is installed on the hosts

### Instructions
* Update the inventory file to reflect the hosts
* Update the [vars](group_vars/all.yml) file
* For minikube setup, please use the `setup_minikube.yml`
* For minishift setup, please use the `setup_minishift.yml`

## Start the k8s cluster
To start the cluster through minikube or minishift

### Requirements
* Please make sure that the target hosts have been setup to run minikube/minishift
* Ensure that root access is provided

### Instructions
* Update the inventory file to reflect the hosts
* Update the [vars](group_vars/all.yml) file
* For minikube setup, please use the `start_minikube.yml`
* For minishift setup, please use the `start_minishift.yml`

## Issues
If you face any issues with using the playbooks please create an issue.
