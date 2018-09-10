---
layout: single
title: Deploy React + Node/Express to AWS part 1
date:   2018-09-1017:03:27 -0700
categories: express
author_profile: true

---

My goal is to deploy a react app using CRA on the client-side using s3, and using an EC2 instance for instantiating an express server running on node.js for an API server. 

Instead of building a montolithic MERN app served by a server, which does server-side rendering for example, I've decided to separate the business logic of the API from the front-end design. There are a lot of advantages to such a microservices approach, including separation of deployment allows for speedier file access and lower latency, faster iteration, and simpler product logic. 

S3 holds files, and so is great for file storage or for hosting a static website; For this project, I'll be using s3 for the view provided by React. The advantage to using S3 is scalability, reliability, and speed. Having the CDN in front of the S3 will offer faster delivery for the users and cheaper costs.

The EC2 instance will be serving API server via node.js and express. This will be the Node API. This could have been handled by Elastic Beanstalk, but as I'm wanting to get my hands dirty with each of the MERN components, I'll be building out the EC2 instance and then connecting the db manually. Then of course there is the option of going serverless using Lambda functions and the API Gateway, which is definitely a great option, but I really want to build that solid foundation using the MERN stack before taking advantage of more speciality tools available. If that makes sense :)

As noted in [this blog](https://stackoverflow.com/questions/41250087/how-to-deploy-a-react-nodejs-express-application-to-aws), it's advantageous to put a CDN via Cloudfront in front of the s3 for a variety of reasons. 

Anywho, using CRA to create /client sub-folder within main app. Now, how to upload to s3 bucket? Simple, just use:
```
aws s3 cp build/ s3://<bucket name/> --recursive
```
That command will use the AWS CLI to upload the production build files from your local computer to the bucket. Just remember to set the bucket permissions to public accessible :)