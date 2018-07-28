---
layout: single
title: Node/Express User Authentication Using Passport Locally
date:   2018-07-12 17:03:27 -0700
categories: node.js
author_profile: true

---
I thought I'd share some of the things that I learned in building my first user authentication approach for a node/express application. I used a bunch of resources which I've listed at the bottom of this post.

There were a couple learning steps with getting going with user authentication within my app. First up was brushing up on cookies, which was instantiated using the cookie-parser module. After setting that module's code to the variable cookieParser, I then nested that within the other middleware by calling it as a method with the argument value. Now, cookies used to have



## Resources
* 'Learning Node.js: A Hands-On Guide To Building Web Applications in Javascript' by Marc Wandschneider
*