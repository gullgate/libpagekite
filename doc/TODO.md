# PageKite in C #

These are Things TO DO for libpagekite.


## Known Bugs ##

   * pkproto.c: Fix parser to fragment chunks that are too big to fit in the
                available buffer space.
   * SSL certificates are not verified


## Milestones ##

### Reached ###

   * pkproto.c: parse pagekite proto, emitting a callback for each chunk
   * pkproto.c: serialize the pagekite protocol to buffer or file descriptor
   * httpkite.c: Implement a very basic back-end (hello world)
   * pagekite.c: libev based single-kite pagekite proxy (blocking)
   * pagekite.c: multiple-kite pagekite proxy (blocking, BE use only)
   * pkmanager.c: reconnect automatically
   * pagekite-jni.c: Bare-bones android wrapper for libpagekite
   * pkproto.c: Use session IDs for replacing old/dead connections.
   * pkmanager.c: added flow control for individual streams
   * pkmanager.c: added flow control for tunnels
   * pkblocker.c: choose best front-end automatically.
   * pkblocker.c: Update DNS records
   * libpagekite: create simple fork/thread/anonymous-pipe based API for
                  easily adding PageKite support to existing TCP/IP servers.
   * Windows compatibility and build rules
   * pkmanager.c: add listeners, for built in web UI and relays
   * pkmanager.c: make update/reconnect schedule tweakable
   * bindings: auto-generate JNI bindings and API documentation

### Ahead / In progress ###

   * pkmanager.c: add callbacks for watching/influencing data flow
   * pkproto.c: add SSL support - finish cert checking code

   * pklua.c: make libpagekite extensible with lua code
   * pkwebui.c: built-in web server (lua?)
   * pkconfig.c: parse pagekite.py-style config files

   * pkproto.c: add ZChunk support
   * pkmanager.c: SOCKS and HTTP proxy support for outgoing connections
   * pagekitec.c: truly non-blocking pagekite proxy, suitable for front-end
   * Python wrapper (libpagekite.py)

### External ###

   * pagekite.py: only very rarely, if ever, pings mobile devices.
   * pagekite.py: block certain requests server side to save traffic.
   * Maybe: pagekite.py, queue incoming requests in case of reconnect?

