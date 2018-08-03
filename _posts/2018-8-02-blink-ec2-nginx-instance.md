---
layout: single
title: AWS EC2 instance using SSH Blink and nginx reverse proxy server
date:   2018-08-02 17:03:27 -0700
categories: aws
author_profile: true

---

![Intro]({{ https://davideliason.github.io/ }}/assets/images/aws/8-2-18-Posst2/8218-VPC-EC2-Post.png)

There's my fance splash page! I wanted to share the steps I took to get some experience doing a few things: first, creating an EC2 instance within a VPC, then spinning up a simple express app on top of node, spitting out response to port 3000 but allowing our reverse proxy nginx server to channel that to route 80.


![Steps]({{ https://davideliason.github.io/ }}/assets/images/aws/8-2-18-Posst2/Exercise-Steps.png)