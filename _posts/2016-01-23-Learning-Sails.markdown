---
layout: post
title:  "Learning Sails"
date:   2016-01-23 21:14:30 -0500
categories: Javascript Sails
---
## Openshift boilerplate node application
Since I want to deploy this application online without spending money, Openshift is one of the good options out there.
Create an account if you don't have one and then create an open shift application.
Install rhc command line tools on your machine
clone the git repo from openshift using rhc tools "rhc clone.."

## Creating a new Sails application

## Deploying to OpenShift

## CI Using Travis

### Build

Enabled the project in Travis and created a minimal config file .travis.yaml

```
language: node_js
node_js:
- 0.1
```

### Deploy to openshift

Sample .travis.yaml

```
language: node_js
node_js:
- 0.1
deploy:
  provider: openshift
  user: amitrke
  password:
    secure: Wz4IPSIbyDOw2tlPwc.....................
  app: courtres
  domain: eduind
  on:
    repo: amitrke/courtres
after_success:
  - git config --global user.email "travis@localhost.localdomain"
  - git config --global user.name "Travis CI"
  - git add --all
  - git commit -am "Travis change"
```

It should work without the after_success block, but as travis was trying to deploy the code it would always complain that there was no code change.

```
after_success:
  - git config --global user.email "travis@localhost.localdomain"
  - git config --global user.name "Travis CI"
  - git add --all
  - git commit -am "Travis change"
```
