---
layout: post
title: "Gitlab for a local Github alternative"
date: 2012-06-13 21:04
comments: true
categories: 
---
[Git](http://git-scm.com/) as everyone may already know is a really great tool for version control. I have started using it for all of my day to day coding. It is by far the best off site git tool, but there are instances where you may not want to have your code hosted there or you may just want to host your code in multiple places (which is a smart thing to do). I use [Github](https://github.com/) for almost all my repositories, as well as [Bitbucket](https://bitbucket.org/) but if you are looking for an alternative to both and don't wish to pay for the enterprise version of [Github](https://github.com/) then you have a few open source choices. Ranging from [Gitorious](http://gitorious.org/) to [Gitlab](http://gitlabhq.com/). There are many other alternative projects out there that work really well, but I'm using an amazon micro instance which can't take too much stress and quickly runs out of memory with all the other crap that I have running on it as well. I therefore settled with [Gitlab](http://gitlabhq.com/) which is a nice open source project written on ruby on rails.

Installing [Gitlab](http://gitlabhq.com/) is pretty straight forward, they have a [tutorial](https://github.com/gitlabhq/gitlabhq/blob/stable/doc/installation.md) on their [Github Page](https://github.com/gitlabhq/gitlabhq) on how to install it on Ubuntu but you can easily take that and use it to install on your favorite linux distro. It does require that you install [Redis](http://redis.io/), and [Resque](https://github.com/blog/542-introducing-resque), but again the process is pretty straightforward and simple.

Gitlab is a good simple solution if you are looking to hosting a few repositories with a small group of people. It works well for my needs though I will say it is pretty plain and simple, it doesn't have all the bells and whistles github offers. As an additional remote backup location this is a great little rails app.

I also wrote a small ruby script that can be run automatically through a cronjob that helps with backing up all the repos hosted by your [Gitlab](http://gitlabhq.com/) installation and uploading the compressed back up to an Amazon S3 bucket. It's a simple script that can be used as a template for a more sophisticated back up script.

{% gist 2928017 %}