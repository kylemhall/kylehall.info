---
id: 95
title: Libki Updates
date: 2009-02-11T09:43:14+00:00
author: admin
layout: post
guid: http://kylehall.info/?p=95
permalink: /2009/02/11/libki-updates/
categories:
  - Libki
---
Hey All,

I&#8217;ve been hard at work getting Libki into a form that is more suitable for the general public to use. First, I&#8217;ve moved the code from SourceForge&#8217;s subversion repo to GitHub, at least for now.

I&#8217;ve finished porting the code from using PostgreSQL to MySQL. In addition I&#8217;ve been working on the startup scripts that disable hotkeys that could be used to bypass LibKi on Windows clients. These scripts were made with <a href="http://www.autohotkey.com/" target="_blank">AutoHotKey</a>, a wonderful piece of FOSS that was designed for creating Windows shortcuts, but has grown so fast it&#8217;s possible to write complete graphical programs using only an AutoHotKey script. These scripts are located in the libki/client/src/windows directory, as they only function on Windows. There are four, each one is slightly different to better suit individual needs.

<ul style="text-align: left;">
  <li>
    libki-keylock &#8211; Disables alt-tab, ctrl-alt-del, and many other commands that can be used to gain unauthorised access. With this version the key combo ctrl-alt-shift-L will pop up a password dialog that can disable the script. The password is contained in the file /etc/libki/keylock
  </li>
  <li>
    libki-keylock-nopwd &#8211; The same script without the password unlock feature.
  </li>
  <li>
    libki-keylock-startbutton &#8211; The same as libki-keylock, but this version also disables the start button, so only shortcuts on the desktop can be used to launch programs.
  </li>
  <li>
    libki-keylock-startbutton-nopwd &#8211; The same as above, but without the password unlock feature.
  </li>
</ul>

For each of these scripts, there is an executable, and a corrospondingÂ _.ahk_ file which contains the original AutoHotKey script code in case someone would wish to modify the scripts further.

That&#8217;s all for now. More updates will be coming soon.