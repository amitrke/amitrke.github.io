---
layout: post
title:  "Learning Sails"
date:   2016-01-23 21:14:30 -0500
categories: Javascript Sails
---

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
    secure: Wz4IPSIbyDOw2tlPwcGZdR7SgoDIg0YlZtfNC71YG/O1qa9c41g59cC889MFD872dexmrh210vQNNO9iwv7W4EdIa4qKUPcCtB9VWKyRTC2j/q5WDAAqYlujsFPQfyr66XKATabrfygoq1bzHs1tgRZEjDGCQo4CoGJnAefbLY5dNQVX7E3Wf3jWjlynF7F9QGmqeOloJ8Hsxq7e6VfIGh9IX/Lwmq+QAnlB/vUObRnuHMiC+8DtL3Lpe0y1BeLdwGB96YmdPY4pjxxPCcYbL1Rh50p+zXRVcrUQ1q2mTaLgDJwasGUwGU+ob31boPXa559cyw5uF5zFCn44TDPNhzNAnjmozhYiKdb/yTNrxEIqxcVFNaZL+wse4cZfnEi2Z3EeVdVIVstyucFZlao9/lZWvaacy7x4EMW/KsB+LXLWV/0Lpjxe+RJ/Z8tToh5m+giauEyczHG+9hQccBDDMX4+FSt49RxCh2MxcpND+ei6YdCOhxt36vcC8LNpiiWo+yCUCkFOijj7l//6DcNDAUT3zYuiV2suB7bMs9BQOlWYwyXKOIf/WM82cnfzdPTiV0/0o4ysdfbINB+7KXKILH9zHUHeq85sLkQVq8GheFq9jxW0TJf3N4grWBk8hUqf3OZcd5QByyMpPFkvxz6r+34bDQ58lXu6nRJGa7zKc7M=
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
