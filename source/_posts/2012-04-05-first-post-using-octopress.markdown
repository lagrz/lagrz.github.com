---
layout: post
title: "First post using octopress"
date: 2012-04-05 21:44
comments: false
categories: 
---
Installing [Octopress](http://octopress.org/) on OSX Lion required a small extra step. RVM required me to install [osx-gcc-installer](https://github.com/kennethreitz/osx-gcc-installer) because it does not work with the current version of XCode which kind of bummed me out a bit because I had to download an extra 200 somewhat megabyte file, and install it. From there things were a bit easier using RVM to install 1.9.2 was pretty easy, as well as doing the initial setup of [Octopress](http://octopress.org/). The only thing that I need to figure out is why instead of just using `rake` I have to use `bundler exec rake`. Not a big issue but just a bit annoying, and I'm sure I'll find a way around it eventually. First order of business is tweak the layout around, hopefully I'll get a chance soon.
