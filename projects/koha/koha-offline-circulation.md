---
id: 39
title: Koha Offline Circulation
date: 2008-03-05T09:02:28+00:00
author: admin
layout: page
guid: /projects/koha/offline/
---
# Koha Offline Circulation

  The Koha Offline Circulation program ( KOC for short ) was written to avoid requiring librarians to resort to using pen and paper to track circulation during events of downtime for a Koha server. It was first written for the Crawford County Library System of Pennsylvania, and it’s features were greatly extended due to funding provided by the Geauga County Library System of Ohio. The current iteration is a complete rewrite to improve stability and portability.

The client tracks issues and returns, and fines payments. In addition, the client has the ability to display data about the current patron, either by scanning the patron’s library card or using the built in search utility. This data is stored in a file that is created by Koha with the included script create\_koc\_db.pl

The client has been stream-lined so that use the mouse is rarely required. For example, when issuing an item, the borrowers card is scanned first, then the program jumps to the item barcode box. After all the barcodes have been scanned, the librarian can click a button to complete the transaction, or simple press the enter key on the keyboard instead. Switching between tabs can be accomplished with the keyboard shortcuts Alt+I, Alt+R, and Alt+H to change to the Issues, Returns and History tabs, respectively.

## Downloads

Koha Offline Circulation can be downloaded [here](https://github.com/bywatersolutions/koha-offline-circulation/releases).

## Source Code

Koha Offline Circulation is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

The source code is available for download via [GitHub](https://github.com/bywatersolutions/koha-offline-circulation).
