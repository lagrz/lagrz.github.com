---
layout: post
title: "Backup box.com"
date: 2012-07-26 20:43
comments: true
categories: 
---
# Box.com Download #

Taken from the [Readme File](https://github.com/lagrz/BoxDownload)

This script will download all files recursively from your [Box.com](http://www.box.com) account.

You will need to modify the `box.yml` file with your api key. You can get an api key [here](https://www.box.com/developers/services/edit/). You will need to create a Box.com app in order to get an api key. The `auth_token` attribute in the box.yml will be automatically saved after you authenticate with your api key, modify it if you already have one premade or leave the value 0 as the script will try to get one for you.

    box.yml
    --- 
    api_key: API_KEY
    auth_token: 0

## Getting an auth_token ##

Make sure you have already modified the `box.yml` file and added your `api_key`. 

First run:

    bundle install
    bundle exec ruby box.rb

The script will use launchy to run your default browser to the box site. Enter your site credentials and authorize your app. Once you have done so go back to your terminal window and type `y` or `yes`.
   
    ready to continue?
    yes

The script will then save the token information onto the `box.yml` file for future use, and proceed to download the files stored on your box account.

---
NOTES: 

- The auth_token may expire (I'm not sure how long they are good for)
- There may or may not be a bandwidth limit as to how much you can download from a free account.