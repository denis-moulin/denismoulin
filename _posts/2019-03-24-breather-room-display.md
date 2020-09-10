---
layout: post
title: Breather Room Display
date: 2019-03-24 09:15:16
description: Breather is a service offering meeting rooms to book from an hour
  up to several consecutive days. Bookings can be completed via the website or
  the mobile app. In 2018, we've internally prototype a better way to access our
  spaces.
categories:
  - read
  - featured
link: https://breather.com
matters: Product Design
header: /assets/images/posts/bud-post.png
preview: true
banner: false
featured: false
is_post: true
banners: none
---
Breather is a service offering meeting rooms to book from an hour up to several consecutive days. Bookings can be completed via the website or the mobile app. Once a booking is completed, and on the day of the booking, the customer is offered an access code to open the door of his meeting rooms.

Whether it’s the first time to unlocking your Breather space or while in your booking you’re coming back from the bathroom, a unique to your booking 6 to 10 digits code is required to open the door again. My colleague and iOS developer at that time Joel and I paired to come up with an access solution to reduce friction and customer input.

### Some technical workarounds

No interface is the ultimate friction-less experience, and we aimed for it knowing it might cost us extra work and cost. In 2018 it was fair to assume that most of our users had an iOS or Android OS device, platforms on which both Breather app are running.

Ideally, as a customer, the door would be unlocked as you approach it. The only conditions would be that you need an upcoming or ongoing reservation. Since most of our customers weren’t memorizing the digits but instead look up the code on their reservation tab in the app, the phone was naturally brought up as the “key” needed to unlock the doors.

![Technical Flow](/assets/images/posts/brc_bud-internal-mvp-1-.png "Technical flow for our prototype")

The first issue to be solved was to make sure we could somehow “read” if a phone holds through the breather app a reservation matching our rules. Beacons were the ideal solution. The way I remember it is that a beacon could establish Bluetooth communication with a phone and ask for specific data from an app without waking the screen of the phone. I would even work if the app isn’t running (both actively and in the background).

One downside, although Beacons are relatively cost-effective devices, while dormant they require an external signal to start the action. The second piece of the puzzle, we needed action from customers.

![](/assets/images/posts/b-01-no_rez.png)
![](/assets/images/posts/B--03--ongoing_rez.png)
![](/assets/images/posts/C--01--proximity--search.png)
![](/assets/images/posts/D--01--key_pad-default.png)
![](/assets/images/posts/C--02--proximity--check_in--valid.png)
![](/assets/images/posts/C--04--proximity--error_general.png)

So our no interface unlocking experience wasn’t happening but could we get as frictionless as possible and could we turn that downside positive. We paired the beacons with tablets. Not only it fixed the issue about waking up the beacons. It helped us with unsolved questions about fall-back solutions(what if you don’t have the app?) and visibility issues we were having at the time. Branding outside of our spaces was restricted (by landlords) to our name on the door; we could advertise Breather spaces to potential customer working on our same floors/building where we rented spaces.

![](/assets/images/posts/E--01--space_around-displayed.png)

### Post-prototype (afterward)

Implementation on most of our markets spaces is still in discussion. Installation of such a system requires talks with every landlord or building owner, which add a bit of complexity. It’s a variable we were well aware of when thinking of such solution, most of what’s inside the space are of our control, anything outside the space (door, walls, windows) is relatively limited. In addition to that we have to take into consideration the cost of security, implementation, and promotion in a user flow, and many other aspects I’m not allowed to share here. It’s also not all or nothing implementation as I would make more sense in a dense network such as New York where the advertising part of the project would make sense.

![Picture of prototype attached to a door](/assets/images/posts/img_0339.jpeg "Our prototype in situ")

Internally part of our learning process was to use the solution our self to book some meeting room (not a stretch of use when you think of office setup and meeting rooms, service we are starting to offer). Although the intention is loyal, I’m doubtful in the quality of feedback we would get.

However, it gets implemented this functioning prototype a critical piece of the ecosystem we’re selling as a company.