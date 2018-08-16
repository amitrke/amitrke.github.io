---
layout: post
title:  "Learning Python"
date:   2018-08-16 21:14:30 -0500
categories: Technology
---

# Sample programs

Send a post JSON request

```
import requests

url = 'http://localhost:8080/api/articles/'
data = {"userId":1,"status":"Active","title":"Test Title","imageURL":"/abc/def/a.jpg","description":"Test Description","fullText":"Test Full Text","priority":1}

response = requests.post(url, json=data)

if (response.status_code != 200):
    print(response.status_code)
else:
    print(response.json())
```