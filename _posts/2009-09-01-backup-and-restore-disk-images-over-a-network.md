---
id: 106
title: Backup and Restore Disk Images Over A Network
date: 2009-09-01T07:30:56+00:00
author: admin
layout: post
guid: http://kylehall.info/?p=106
permalink: /2009/09/01/backup-and-restore-disk-images-over-a-network/
aktt_notify_twitter:
  - 'yes'
categories:
  - General
---
Here is a quick and easy way to save and restore hard disk images using dd, netcat and gzip.

To Save An Image:
  
On the server: nc -l 7000 | dd of=Output.img.gz
  
On the client: dd if=/dev/sdb | gzip -9 | nc 12.34.56.78 7000

To Restore:
  
On the client: nc -l -p 7000 | gzip -dc | dd of=/dev/sda
  
On the server: dd if=Output.img.gz | nc 12.34.56.78 7000

I just boot the client using an Ubuntu live-cd, all the neccessary tools are already installed. I store my images gzipped to save space, I just copied a 40 GB disk and the image file compressed down to 4.4 GB!