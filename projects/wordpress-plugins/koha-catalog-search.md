---
id: 88
title: Koha Catalog Search
date: 2009-02-02T18:53:31+00:00
author: admin
layout: page
guid: http://kylehall.info/?page_id=88
---
## Koha Catalog Search

This WordPress plugin allows one to insert a small search form into a WordPress site that searches a given Koha catalog.

[Download KohaCatalogSeach 0.1](/files/KohaCatalogSearch-0.1.zip)

## Installation:

  1. Enable the plugin
  2. Go to Options->KohaCatalogSearch, fill in the neccessary data
  3. Paste this code where you want the search form to appear:

> <?php
  
> if (function\_exists(&#8216;kcs\_display\_search\_form&#8217;)) {
  
> kcs\_display\_search_form();
  
> }
  
> ?>