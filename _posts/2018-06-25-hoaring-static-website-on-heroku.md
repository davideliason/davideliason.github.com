---
layout: single
title: Hosting Static Site on Heroku
date:   2018-06-25 17:03:27 -0700
categories: heroku

---

Just as soon I'll have to slave over my lawnmower to cut down the evergrowing grass and weeds, it was time to weed out the repos in my Github portfolio. Out went the repos that, well, just needed to go. But what about that odd piece that was front-end only? How should that be posted?

Following some online advice, I found that there's a pretty easy solution, which is to host it on Heroku. Here's the steps that I took to do so with a browser-based Babel and React simple application:

1. In the root directory, where your index.html resides, create a composer.json file:
````
$ touch composer.json
````
2. Add an empty object within that file 
````
{}
````
3. Add a index.php file
````
$ touch index.php
````
4. Add a single line within that file:
````
<?php include_once("index.html"); ?>
````
5, create a heroku repo for your code to go into:
````
$ heroku create <your app name>
````
6. Push your code into that repo
````
$ git push heroku master
````
7. open it up
````
$ heroku open
````

And that was it - my vanilla html file rendering a React application worked just fine. You can take a look at it here:
[Browser React App](https://browser-react-todolist.herokuapp.com/)
