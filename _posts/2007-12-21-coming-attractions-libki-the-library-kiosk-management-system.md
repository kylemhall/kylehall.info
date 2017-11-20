---
id: 28
title: 'Coming Attractions: LibKi &#8211; The Library Kiosk Management System'
date: 2007-12-21T08:23:01+00:00
author: admin
layout: post
guid: http://kylehall.info/index.php/2007/12/21/coming-attractions-libki-the-library-kiosk-management-system/
permalink: /2007/12/21/coming-attractions-libki-the-library-kiosk-management-system/
categories:
  - Libki
tags:
  - LibKi
---
I&#8217;ve nearly completed a new project for our library system. I have named it LibKi, short for Library Kiosk, though I wish I had gone with KiLock, for the humor.

LibKi was written to take some of the load of handling the public computer systems off our librarians. The libraries currently use sign in sheets and have to keep track of who is on which computer. LibKi allows a patron to login, and a timer keeps track of how much time they have left. I&#8217;ve written a script to import our patron data from Koha each night, and to reset every patrons allotment to 30 minutes a day.

The entire system is written in PHP. The daemon is cli-only PHP. The web interface is built on CakePHP and allows librarians to alter a patron&#8217;s minutes, log them out, disable their account and send the user a message. The kiosk client is written in PHP/Gtk+ and should run on any OS with Gtk support. I&#8217;ve tested it in KDE and XFCE, and it work&#8217;s great.

I&#8217;ll be putting up a new section for LibKi on this site soon. But for now you can peruse the code at sourceforge here: <a href="http://http://sourceforge.net/projects/libki" target="_blank">http://sourceforge.net/projects/libki</a>

Happy Holidays.