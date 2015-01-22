---
layout: post
title: "Tips & Tricks: The SSH config file"
category: blog
---

A reasonably secured SSH setup (with non-standard ports, key-based
authentication, etc.) requires a lot of typing to work with. This is especially
annoying when you have access to more than one of these installations, as it
requires you to explicitely state the private key to be used on each login. All
of this can be easily avoided by using a SSH configuration file.

Said file has to be placed in the directory where you would store your keys (On 
most systems, this is `~/.ssh`) and is simply called `config`. In this file, you
can basically create aliases for SSH commands (not unlike aliases you define in
your Shell configuration). Below is a simple example:

```
Host example
	HostName example.com
	Port 1337
	IdentityFile ~/.ssh/example.com.key
```

This file would allow you to shorten the command
`ssh example.com -p 1337 -i ~/.ssh/example.com.key` to `ssh example`.

Of course you can create as many of these as you want, and since you can
actually configure nearly everything you can pass as an argument to SSH, these
file can be a huge time-saver.
