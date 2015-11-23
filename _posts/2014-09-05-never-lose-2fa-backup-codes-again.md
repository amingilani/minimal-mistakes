---
layout: post
title: "Never Lose 2FA Backup Codes Again"
modified:
categories:
- Geeking-Out
excerpt: After being locked out of my account a bunch of times, I worked out a way to never let that happen again.
tags:
- Two Factor Authentication
- Backup
image:
  feature:
date: 2014-09-05T04:00:56+05:00
comments: true
---

Sometimes don't print my Two-Factor Authentication backup codes all the time. I'm either not near a printer, or I'm just being lazy. Although, finally, after being locked out of my account a bunch of times, I worked out a way to never let that happen again. Here's what you need:

+ A Gmail account
+ A PGP Key --- extra laziness points if it's published on a keyserver

Got those? Perfect. Do this:

1. Open [https://encrypt.to](https://encrypt.to) and type in your key id, or email address.
2. Paste in the codes
3. To: `youremailaddress+2FA$service@gmail.com` where $service is your 2FA provider.
    example: `me+2FAgithub@gmail.com`
4. Send!
5. That's it!

Now if you never need your codes, just search for `to:me+2FAgithub@gmail.com` in your gmail and voila. The lazy man's secure backup. **Remember, this is a backup of your codes,** not the primary method to be storing your codes. This is no replacement for a good old fashioned printout! What do you think you'll do if you lose access to your Gmail?

This works because Gmail ignores anything after the `+` sign after your username. You can send an email to `you+anything@gmail.com` and the email will always show up in your inbox.

*Freebie: When signing up for dodgy websites, use `you+dodgysite@gmail.com` as your email address. That way if they leak your email address to spammers, you can simply set a filter to direct all mail to that email address into your Spam.*