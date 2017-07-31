---
layout: post
title:  "Amazon web services"
date:   2017-07-30 21:14:30 -0500
categories: Cloud
---
## AWS

I want to deploy a small Node/Angular webapplication to AWS, as I try to explore the options here is what I learnt


## Where do I run the server side NodeJS code
Amazon has few options grouped together under the section "Compute"

#### Amazon S2 - Beanstalk - Can host node js code, be careful about pricing.
S2 is perfect from a perspective that I can create a docker image and host it, however looking at the pricing I think I don't want to pay more than $10 a month, which could be a problem after the free first year.

#### Lambda (Serverless) - Host a function
I like the pricing on this one, it is based on how many calls to a function, and if the calls are under a certian number it could be free after the first free year too.
The downside is that it is not a like having an express application, but I think I can live with functions at this point.

## How to I create web accessable URL for Lambda functions
#### API Gateway
AWS API Gateway can create web URLs for the Lambda functions

## How do I host the static content
#### Amazon S3 - Can host static site, free for one year
I can use S3 to store and serve static content, HTML/CSS/JS (Angular code)
