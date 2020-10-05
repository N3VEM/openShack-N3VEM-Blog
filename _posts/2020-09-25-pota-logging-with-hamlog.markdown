---
layout: post
title:  POTA logging with Hamlog
redirect_from: /wwff-logging-more-with-hamlog/
date:   2020-09-25 19:29:59 +0000
image:  hamlogicon.jpg
tags:   reprint POTA logging portable
---
Welcome to this first post in my "reprint" series!  As a kick off to the newly updated blog, I wanted to start by republishing some of my most visted posts, but with updated material.  So, without further ado, here is the reprint.

#### POTA LOGGING & MORE WITH HAMLOG

<small>First Published 7/28/2017</small>

There are quite a few ham radio apps out there, but if you are an iOS user, you can probably download this one app and be done.  This is because there is not much you could ever want a ham radio app to do, that isn't included in this one.  Look at the insanely low price along with everything this app does, and you'd have to be a crazy person to not download it.  I'm going to be up front with you and let you know that this app does SO MUCH that this is a loooong post.  

[![Hamlog Icon]({{site.baseurl}}/img/hamlogicon.jpg)](https://itunes.apple.com/us/app/hamlog/id308437400?mt=8&at=1000lvce)

You can skip to the end of this article for a list of all of the amazing things that this app will do, and I won't be offended, because most of this post will focus on the feature that I just "found" in the app that has helped me immensely with one of the things I love doing in ham radio - portable operating for the Parks on the Air program.

##### LOGGING

A topic that comes up regularly for these types of programs is logging while operating portable.  When portable, one of the biggest concerns is power, so while logging on a laptop might be nice, it is often times power prohibitive.  Many people choose to log on paper and then transcribe their contacts into a program when they return home.  If you're like me, free time is at a premium, so an option that lets you get the contacts logged in the proper format as you make them is always preferable.  Since many of us now carry around a portable device that operates for a number of hours on relatively low power, using it for ham radio logging is an obvious choice.

What makes Hamlog so great for logging?  It has a "hidden" feature called "Create A Log" that lets you build a log sheet with exactly the fields you need, no more, no less.  For POTA this is awesome, because there are a couple of fields in the ADIF format that the POTA database uses, that are not included in the "standard" layout of most (any?) iOS based logging apps.  Hamlog lets you create logs with exactly the data you need.  This makes it easy for you, but also for the program administrators when they upload your logs (they'll thank you for it!)  

What ADIF data fields does POTA need, and how are they used?  Here they are, with a brief description of each - but don't be intimidated!  I'll explain how hamlog makes this very easy later in this article.

<medium>STATION_CALLSIGN</medium>
​This field is used for the call sign that is getting "credit" for the activation.  Usually, we are activating by ourselves, so it is just our own call-sign.  There might be times however, where you are activating with a club or something similar.  In this case the club callsign would be the one you enter here.

<medium>OPERATOR</medium>
​This is the filed where the person making the contacts puts their callsign.  When we are operating by ourselves, it is usually just our own callsign a second time.  It may be different then the "station_callsign" however, if you are activating with a club or with someone else.  This is also a place to put the callsign of a guest operator if another ham happens to stumble by, and you put them on the air.

<medium>MY_SIG</medium>
​This is one of the fields that databases use, that might not seem to make sense based on the name of the field, until you relaize that SIG is not signal - it's short for "Special Interest Group."  You can think of it like being a field to put the name of the program into (i.e. POTA, SOTA, IOTA, etc.)  Every contact in your log should have the same value here.

<medium>MY_SIG_INFO</medium>
​Once you understand MY_SIG, it's easy to think of MY-SIG_INFO as being the details - i.e the park number.  Programs maintain a list of their park numbers and designations, so just be certain to use the right park number!  (Luckily, most programs are flexible, so if you activate a location that qualifies under multiple things - i.e. you activate a SOTA peak, that is on an IOTA Island, that is in a park, you can usually indicate when submitting logs where you were, making you able to submit the same logs to multiple groups (an example of the above is Cadillac Mountain on Mount Desert Island in the Acadia National Park.)

<medium>CALL</medium>
​This is the field where you type the callsign of the person that contacted you.  That's pretty straightforward!

<medium>QSO_DATE</medium>
​This is the field that contains the date the contact was made (if you're logging as you go, its just today's date, in UTC)

<medium>TIME_ON</medium>
​This is the field that contains the time the contact started, in UTC.

<medium>BAND</medium>
​This field contains the band of operation.  Different log uploading tools seem to handle this differently, but for award purposes, pretty much universally, you don't need the exact frequency, just the band.  What we need here is simply the band, followed by the letter "m".  As an example, if I made the contact on 20 meters, I would be entering "20m" in this field.  The "m" is important (learned the hard way with the help of Jeff Dahn!) because this is what lets logging databases know that you have entered a band and not a specific frequency.  Don't forget the "m"!

<medium>MODE</medium>
​This is where you enter the mode of the contact.  Pretty much all of the standard abbreviations (SSB, CW, DIG, RTTY, etc.) are accepted.

<medium>SIG</medium>
​Special Interest Group of the person you are contacting. for POTA, we use this field to indicate the "program" that the person chasing you is participating in.  Normally it will be blank, but if they also happen to be in a park doing an activation (known as a park-to-park contact) this is where you put the letters "POTA" to indicate that this chaser is also doing a park activation.

<medium>SIG_INFO</medium>
​The final Special Interest Group field. This field is complimentary to the one above.  If this is a Park-to-Park contact as indicated above, this is where you put the designation of the park that the other person is in. 
​
<medium>NOTES</medium>
​No logging databases that I know of actually need anything in this field, but since we often like to type little tidbits about our contacts, it gets included in nearly every logging package as a "catch-all" field.
You may notice that their are some fields not included, that we commonly exchange, like signal reports.  Here's a little secret - very few logging databases care whether or not you use signal reports.  When portable, the name of the game is to do only what you need to do, no more.  So yes, while I may give signal reports as a courtesy while I am activating, I don't actually put them in my log.

Luckily for us, since my origional post, the creator of hamlog has added a POTA template right in the app for us, so to start your log, from the main part of the app go to:

Tools -> Create a Log

At the bottom, you'll find "web templates."  If that section is blank, click "refresh templates" and you should see POTA pop up in the list.  

Each time you choose this you'll create a "new" log.  I generally do new log for each activation and give it a name like *park_name_K-0000_20200925*.  

![Hamlog Screenshot]({{site.baseurl}}/img/hamlogscreenshot.png)

Once you're ready to submit your log, click the "ADIF" button in the lower right to export your log, type in the email address for where you'd like to send it, and you're done!

*ed. my orgional post had a much longer section detailing all the other features in hamlog - let's just suffice it to say that there are* ***ALOT*** *of features.*
