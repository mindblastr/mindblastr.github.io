---
layout: post
title: How to check Kerberos Ticket Cache Programatically
subtitle: Code Snippets to check the Kerberos Ticket Cache for a valid Ticket with Python and Bash
category: snippets
tags: [kerberos, python, bash]
image: /images/logos/kerberos.jpg
image_alt: /images/logos/kerberos.jpg
menubar: true
time_to_read: true
hero_image: /images/code2.jpg
---
 

If you have scripts that depend on authenticating with Kerberos and on the ticket cache, you either always get a ticket before executing the script, or you never check for it before executing whatever command requires authentication.

The best practice on this scenario would be to validate that at least you have a valid ticket before executing the rest of your script. 

The most common languages I use for scripting are Bash and Python, and I mostly work around CentOS and RHEL, so in that sense I'll share bellow 2 pieces of code that verify that you have a valid ticket in the ticket cache in these languages, with the specific Kerberos implementations available for linux. 


## Python Code

<script src="https://gist.github.com/mindblastr/fad200538b626bdb66e8b0a9a53e496a.js"></script>

This way you can check the ticket cache only using the Python Standard Library (and calling command)


## Bash Code

<script src="https://gist.github.com/mindblastr/94bb30e9241ce4dea94ce9365281a21c.js"></script>


There's also the question of maybe reading which principals are available in the ticket cache, but I'll maybe explore that in another article, if I come across a use case for it.

## References

- [klist(1): cached Kerberos tickets - Linux man page](https://linux.die.net/man/1/klist)
