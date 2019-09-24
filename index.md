class: middle, blue

# How Cloud Run is the final destination in my Cloud Native journey

### Kevin Simper

---
class: middle

# disclaimer: I am not getting paid

### Please help 😆

---

# I like organizing meetups

## CopenhagenJS

## GDG Cloud Copenhagen

---
class: middle

# price conscious

# time efficient

---
class: middle

### or

# i am cheap

# and lazy

---
class: middle

# my goals

---

## I want to deploy:

## - everything<br>- really fast<br>- without locking myself in<br>- cheaply<br>

---
class: middle, black

# My life started simple..

---
class: middle

# php hosting

---
class: middle

# digital agency

# jails & freebsd

???

it was genius and complicated

wordpress hosting

newsletter brought down our servers

---
class: middle, blue

## Conclusion:

# scaling is difficult

---
class: middle

# vagrant setup

???

it was terrific and terrible

---
class: middle, red

## Nightmare!

# 3 GB blobs

---
class: middle, blue

## Conclusion:

# deploying is difficult

---
class: middle

# 2015

# 📣 docker meetup group

???

saw it and knew it would solve all my problems

miss the first one

January 2015 Mark Coleman

February 2015 about Docker hosting

---
class: middle

# 2015 docker startup

???

ycombinator interview

ideas to run on spot instances

quit our jobs

kubernetes & docker swarm


---
class: middle

<img src="./yc.jpg"/>

???

rejected, we could not explain our goal

---
class: middle

# docker swarm vs. kubernetes

### thought swarm would win 😅

---
class: middle, blue

## Conclusion:

# multitenantcy is difficult

---

class: middle

# hyper.sh

# chinese startup

???

mark coleman

implemented kubernetes with multi tenantcy - impressive

they implemented not kubernetes - but docker api

had no websocket api

closed down 2018

---
class: middle, blue

# hypervisor container

## now kata-containers

---
class: middle

# AWS serverless lambda

???

used it with this tool called up

AWS gateway & AWS Lambda
launched 2014

limits 50 megabytes compressed

could not teach it

---
class: middle, blue

## Conclusion:

# Proprietary

# Difficult to test

---
class: middle

# Kubernetes

???

connected cars

began teaching workshops 2016 feb

---
class: middle, blue


## Conclusion:

# Awesome!

# But not cheap!

---
class: middle

# Cloud functions

???

waited to launch in europe

2017 October copenhagenjs

---
class: middle, blue


## Conclusion:

# Can't control runtime!

---
class: middle

# KNative

### Open Source serverless framework ontop Istio

???

2018 November

gave a demo

---
class: middle

# We need:

## - quick to deploy

## - cheap

## - custom runtime


---
class: middle

### Enter

# Cloud Run

### Hosted KNative

???

December 2018

Martin Omander

---
class: middle

# What is Cloud Run exactly?

---

# - Takes a docker container

# - Listen on env PORT

# - Pay per request & gigabyte memory/sec

---
class: middle

# Free HTTPS

### via webmastertools

---
class: middle

# Stackdriver

## - Logs

## - Metrics

---
class: middle

## I moved

# everything to Cloud Run

---
class: middle

# Example:

---
class: middle

### $ gcloud beta run deploy \\<br/>cloud-run-continuous-deployment-example \\<br/>--image=gcr.io/cloud-run-cd-example cloud-run-continuous-deployment-example:$SHORT_SHA --region=europe-west1\\<br/>--platform=managed'

---

# Regions

```
* asia-northeast1
* europe-west1
* us-central1
* us-east1
```

---
class: middle

# Cloud SQL

???

proxy, not exposing databases to the network

----
class: middle

# Scaling

## Example:

---
class: middle

# Yes, YAML

### KNative YAML

???

proxy, not exposing databases to the network

---

```
apiVersion: serving.knative.dev/v1alpha1
kind: Service
spec:
  template:
    spec:
      containerConcurrency: 10
      containers:
      - image: gcr.io/cloud-native-aarhus-cloud-run/cloud-run-cloud-native-aarhus:845c6872
...
```
---

## $ gcloud alpha run services replace<br/>--platform managed <br/> --region=europe-west1<br/>example/service.yaml

---

```
Step #2: ERROR: (gcloud.beta.run.deploy) User
[806337517016@cloudbuild.gserviceaccount.com]
does not have permission to access project
[cloud-native-aarhus-cloud-run:testIamPermissions]
 (or it may not exist): Cloud Resource Manager API
has not been used in project 806337517016 before
 or it is disabled. Enable it by visiting
 https://console.cloud.google.com/apis/api/cloudresourcemanager.googleapis.com/overview?project=806337517016
  then retry. If you enabled this API recently,
  wait a few minutes for the action to propagate to our systems and retry.
Step #2: - '@type': type.googleapis.com/google.rpc.Help
```

---
class: middle, blue

# Conclusion

---
class: middle

# Loss leader 💸

### for google

## law of big numbers

???

it takes a lot of customers to earn money, average income

---
class: middle

# Serverless is focusing on shipping

### Don't fall for the Hacker News trolls

---
class: middle

# Do try it out

# Do configure CD

---
class: middle

# Tip: deploy on each commit!

---
class: middle, black

# Cloud Run is a new Era!

# You should join!

---
class: middle, black

# Thank you

## kevinsimper.dk
