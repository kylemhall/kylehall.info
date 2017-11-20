---
id: 115
title: Convert a 2D Associative Array To CSV using PHP
date: 2009-10-19T08:32:19+00:00
author: admin
excerpt: 'Here is a bit of code to convert an array of associative arrays into a CSV file. The first line will be a header line of the key values:'
layout: post
guid: http://kylehall.info/?p=115
permalink: /2009/10/19/convert-a-2d-associative-array-to-csv-using-php/
categories:
  - General
---
Here is a bit of code to convert an array of associative arrays into a CSV file. The first line will be a header line of the key values:<!--more-->

<pre>function to_csv( $array ) {
 $csv;

 ## Grab the first element to build the header
 $arr = array_pop( $array );
 $temp = array();
 foreach( $arr as $key =&gt; $data ) {
   $temp[] = $key;
 }
 $csv = implode( ',', $temp ) . "n";

 ## Add the data from the first element
 $csv .= to_csv_line( $arr );

 ## Add the data for the rest
 foreach( $array as $arr ) {   
   $csv .= to_csv_line( $arr );
 }

 return $csv;
}

function to_csv_line( $array ) {
 $temp = array();
 foreach( $array as $elt ) {
   $temp[] = '"' . addslashes( $elt ) . '"';
 }

 $string = implode( ',', $temp ) . "n";

 return $string;
}</pre>