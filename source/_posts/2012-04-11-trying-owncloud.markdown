---
layout: post
title: "Trying Owncloud"
date: 2012-04-11 21:32
comments: false
categories: linux
---
I have a ton of files scattered around the web and various backup external drives as well as usb drives. It's a pain keeping track of where any given file is at. I need a central place to keep all my files and be able to access them mostly from all my computers at home, as well as use it sort of like a dropbox replacement. I have an extra box running on an Intel Atom processor, so I therefore installed Linux on it, a webserver and slapped [Owncloud](http://owncloud.org/) on it.

The installation is pretty simple and straightforward specially if you have installed a php application on a vps before. The website has pretty clear installation [instructions](http://owncloud.org/support/setup-and-installation/linux-server/).

After the initial install I would highly recommend mounting the webdav locally and then plug in your external devices and perform an `rsync` or `cp -R` into it. 

Install davfs2 package first if you don't already have it installed.

	sudo apt-get install davfs2

Create the folder it will be mounted on.

	sudo mkdir /mnt/DavDropbox

Mount the webdav folder of course replace the content inside the single quotes with the path to your webdav.php (you can use localhost here).

	sudo mount.davfs 'http://127.0.0.1/owncloud/files/webdav.php' /mnt/DavDropbox

You are now ready to start copying files into that folder.

Now the only issue is organizing files and what not. Also remember you can make this accessible outside of your LAN by forwarding port 80 from your router to your linux box and setting up some kind of dynamic dns service like [Dyn](http://dyn.com), or [no-ip](http://www.no-ip.com), a simple web search will get you more alternatives.

