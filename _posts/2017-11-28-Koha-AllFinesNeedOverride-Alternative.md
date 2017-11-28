---
title: Koha - An alternative to AllFinesNeedOverride
date: 2017-11-28
author: Kyle M Hall
layout: post
categories:
  - Kohe
---
## Koha - An alternative to AllFinesNeedOverride

Do you use SIP2 selfchecks and AllFinesNeedOverride? If so, you've probably noticed that any patrons with fines cannot do self-checkout! Here is an alternative to AllFinesNeedOverride using custom JavaScript so you can disable AllFinesNeedOverride!

```javascript
$(document).ready(function() {
  if ($("a[href^='/cgi-bin/koha/members/pay.pl?borrowernumber=']")) {
    $('#circ_circulation_issue input').attr('disabled', 'disabled');
    $('#circ_circulation_issue button').hide();
    $("<button id='allow-circulation' class='btn btn-danger'>Patron owes fees</button>").insertAfter('#circ_circulation_issue button');

    $('#allow-circulation').on('click', function(e) {
      e.preventDefault();
      $('#circ_circulation_issue input').removeAttr('disabled');
      $('#circ_circulation_issue button').show();
      $('#allow-circulation').hide();
    });
  }
});
```

Just place that in your IntranetUserJS system preference and you'll be good to go! This code would also be modified as an alternative for other uses, such as confirming checkouts for patrons with overdues for example.
