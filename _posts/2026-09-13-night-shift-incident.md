---
title: "The Night Shift Incident"
description: "Alerts at 2 AM hit different when Kayne is on call."
tags: [incident-response, on-call]
categories: [stories]
---

## The page

2:14 AM. Alert fires. Weird outbound traffic from a lab box.

Most people wake up confused and grumpy.

## The response

Kayne wakes up and opens a terminal.

```console
$ ss -tunap | grep ESTAB
tcp  ESTAB  10.0.0.23:51122  203.0.113.7:443  users:(("totally_legit",pid=1337))
```

He isolates the box, grabs memory, starts a timeline, and drops a calm update in the team channel. Then he goes back to sleep.

## The next morning

There's a full writeup waiting for everyone. Clean timeline. Root cause. Action items.

It was a student's forgotten test script, not an attacker. But he handled it like it could have been real, which is exactly how you're supposed to handle it.

## The lesson

Night or day, the response is the same: stay calm, make a list, start at the top.
