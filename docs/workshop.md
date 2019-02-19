# 1. Omnia Radix Workshop 1

Purpose - a simple two module app. The public front-end (www) will respond to requests, request data from the non-public echo module - and echo the data back to the requestor. All magic!


* ```echo``` contains the echo module
* ```www``` contains the www front-end

![Conseptual diagram](../docs/smalldiagram.png)

<!-- /TOC -->
## 1.1. Part 1

### 1.1.1. Pre-requisites

- Added to radix user AD Group
    - currently: managed by us
    - in process: AccessIt
- Git installed and working locally against github.com
    - no other version control part of MVP
- Docker running locally
    - How many knows docker?
- Local dev. environment (IDE++) of your choice

### 1.1.2. Exploring the Echo app

1. Move into the [echo](../echo/) folder and explore how to develop the Echo app using ```Node.js``` as well as Dockerizing the application.

### 1.1.3. Exploring the WWW app

1. Move into the [www](../www/) folder and explore how to develop the WWW app using ```Node.js``` as well as Dockerizing the application. 

Remember that the Echo app needs to run somewhere to get proper response.

### 1.1.4. Preparing for Radix

* The Radix cluster we use for the workshop is available at https://console.radix.equinor.com/
* Radix "getting started++" is available at https://www.radix.equinor.com/

Important to know:

1. The difference between ```platform user``` and ```application user```
2. Important terminology: ```application```, ```environments```,```components```, and ```replicas```
3. ```raidxconfig.yaml``` - lives on the master branch and is your infrastrucure as code - drive your app in Radix.

### 1.1.5. Explore radixconfig.yaml

1. Reading the [docs](https://github.com/equinor/radix-operator/blob/master/docs/radixconfig.md)
2. Exploring the config file for the example app [./radixconfig.yaml](../radixconfig.yaml)

### 1.1.6. Creating the application on Radix

1. Update the name of ```your instance``` of the application in radixconfig.yaml
2. Follow the getting started guide (www.radix.equinor.com) or "just do it!"
3. Do a change to trigger the initial build (or use the "New job" feature in the jobs/environment section). Examine web-hooks and reponse in Radix
4. Verify that the app work on the public end-point it has been given.

### 1.1.7. Using multiple branches - multiple environments

Radix support connecting a branch to a specific environment. Let's explore this.

1. Update the radixconfig.yaml file, commit, push and explore what's happening in Radix. (Copy the file ./radixconfigs/radixconfig-feature1.yaml to ./radixconfig.yaml. Remember to update app name)
1. Check out the "new" branch (feature1)
2. Examine code - the new feature  (getting a new env variable from Echo)
4. Do a change, commit, push and explore what's happening in Radix.

### 1.1.8. Monitoring & Metrics

- To Be Decided

## 1.2. Part 2

### 1.2.1. Next steps

* Move your own apps into Radix


## 1.3. Typical questions

(Status as of January 2019)
* Storage - databases
* Authentication
* Logging
* Metrics - Monitoring
* Radix CLI (Api)
* Backup & Disaster recovery
* Own domain names / urls for apps

## 1.4. Where to get started, get help, log issues or feature requests

### 1.4.1. Getting help

* Slack (#omnia_radix, #omnia_radix_support)
* Radix Console -  https://console.radix.equinor.com/

### 1.4.2. Getting started

* Radix Getting Started - https://www.radix.equinor.com/

### 1.4.3. Log issues & feature requests

* https://github.com/equinor/radix-platform/issues

It makes sense to examing existing issues and perhaps discuss on Slack prior to logging a new one