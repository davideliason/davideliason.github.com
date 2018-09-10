---
layout: single
title: Deploy React + Node/Express to AWS part 2
date:   2018-09-10 12:03:27 -0700
categories: express
author_profile: true

---

Okay, the first post was getting too long so had to break it up! :)

So, I left off with having got nginx botted up and with everything being run off port 80. Now we are wanting to move away from the hard-coded simple Express server that I orginally build using vim on the EC2 instance, to being able to pull backend code using git to that instance.

To do that, I instantiated a repo for the backend code. 