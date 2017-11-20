---
id: 47
title: Koha 3 Development Updates
date: 2009-01-30T07:45:15+00:00
author: admin
layout: post
guid: http://kylehall.info/index.php/2003/01/02/koha-30-development-updates/
permalink: /2009/01/30/koha-30-development-updates/
categories:
  - Koha
tags:
  - clubs-and-services
  - fines
  - reserves
  - rotating-collections
---
It&#8217;s been awhile since I posted last so I thought I&#8217;d let everyone know what I&#8217;m doing development-wise involving Koha 3

We are about 5 weeks out from the point where we have to be ready to switch over from using the dev\_week development version of Koha to 3 which is based on dev\_week, but with many differences. To get ready, I&#8217;ve had to port a number of features from dev_week to Koha 3. These include:

  * Porting my Reserves System updates from dev_week to Koha 3
  * Porting my Rotating Collections system from dev_week to Koha 3
  * Adding the ability to pay fines by an amount paid, rather than paying individual fines one at a time.
  * Porting my &#8216;Fines On Return&#8217; system where actual fines are not generated until an item is checked in. I think it&#8217;s a great system and our librarians definitely prefer it to Koha&#8217;s standard fines system.
  * Porting my Clubs & Services feature from dev_week to Koha 3. This is the largest and complex addition to Koha I have made, and I&#8217;m done with the basic feature, but I haven&#8217;t sent a patch yet because I&#8217;d like to add some more bells & whisles to it first.

Hopefully I&#8217;ll have a public Git repository up soon so anyone can pull these updates from me instead of waiting for them to make it into Koha 3 proper.

In addition, I&#8217;ve set up a new website for KUDOS, the US based Koha Users & Developers Group. It&#8217;s located at <a title="KUDOS" href="http://kudos.koha.org" target="_blank">kudos.koha.org</a>.

Kyle