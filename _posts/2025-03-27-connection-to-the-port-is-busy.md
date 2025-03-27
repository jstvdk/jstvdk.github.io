---
title: "Connection to the port is busy…"
excerpt: "Finding the port on which I am working"
---

If your address is in use because you're rapidly developing and not properly closing connections, you're not alone.

My first post here inevitably supposed to be about the issue I encountered the most while "developing" this website. The process (as usual in such situations) consisted mainly of adding a feature and restarting everything. During this constant back-and-forth, I frequently encountered the following error:
```
Error: Address already in use - bind(2) for 127.0.0.1:4000
```
It happened so often that I decided to document the solution here, so I never forget it again.

You can resolve this issue by first finding the process ID (PID) that is occupying the port:

```bash
lsof -i :4000
```

It will give you output something like:

```bash
COMMAND   PID USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
ruby    58101  vdk    9u  IPv4 0x4032def487f7a1bf      0t0  TCP localhost:terabase (LISTEN)
```

After this you can get rid off the nasty process!

```bash
kill -9 58101
```

And continue to create new bugs.